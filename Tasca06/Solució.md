# Guia de desplegament del domini - Tasca 06

---

## 1. Preparació de les eines d’administració

![Eines administratives](/Tasca06/IMG/1.png)

Aquesta captura mostra el menú d’eines del Windows Server. Seleccionem **Active Directory Users and Computers** (i també el Centre d’administració) per crear usuaris, grups i unitats organitzatives.

![Active Directory Administrative Center](/Tasca06/IMG/2.png)

Des d’ací podem veure l’estructura inicial del domini (contenidors per defecte com Builtin, Computers, `Domain Controllers, etc.). Més endavant afegirem les nostres pròpies unitats organitzatives.

---

## 2. Creació de l’estructura d’unitats organitzatives (OU)

Per organitzar millor els usuaris i equips, crearem unes OUs pròpies. La tasca demana una estructura coherent; jo he optat per separar els usuaris per departaments i els equips en una OU a part.

![Creació de l'OU Magatzem](/Tasca06/IMG/5.png)

Aqui estem creant una OU anomenada **Magatzem** directament a l’arrel del domini. 

També hem creat les OUs **Gestio** i **Gerencia** (no es veuen a la captura, però seguint el mateix procediment). Després, dins d’una OU pare anomenada **Usuaris**, hi hem ficat aquestes tres OUs departamentals. Així queda més net:

- translogic13.test
  - Usuaris (OU)
    - Gestio (OU)
    - Magatzem (OU)
    - Gerencia (OU)
  - Equips (OU) – encara no creada però la farem servir per PC-1.

![Camí cap a un usuari dins d'una OU](/Tasca06/IMG/16.png)

A la creació de la plantilla _plantilla-gestio veiem que la ruta és …/Usuaris/Gestio. Això confirma que l’estructura d’OUs està funcionant.

---

## 3. Creació dels grups de seguretat

Els grups que ens demanen són: **gestio**, **magatzem**, **gerencia** i **personal**. El grup personal ha de contenir els altres tres.

![Creació del grup Grup_Global](/Tasca06/IMG/6.png)

Primer creem un grup anomenat Grup_Global

![Llista de grups creats](/Tasca06/IMG/7.png)

Ací veiem tots els grups demanats: gestio, magatzem, gerencia i personal. A més apareix Grup_Global que potser és un grup addicional per a una altra pràctica.

![Membres del grup personal](/Tasca06/IMG/8.png)

En obrir les propietats del grup personal, a la pestanya **Members** hi afegim els grups gerencia, gestio i magatzem. D’aquesta manera, qualsevol usuari que sigui membre d’algun d’aquests tres departaments també serà membre indirecte de personal (herència de grups).

---

## 4. Configuració de la carpeta compartida i permisos

L’enunciat diu que cada usuari ha de tenir una carpeta personal. Crearem una carpeta personal al segon disc dur (E:) i la compartirem.

![Carpeta personal al disc E:](/Tasca06/IMG/9.png)

A E:\ hi creem la carpeta personal. Dins d’ella hi haurà subcarpetes per cada departament i per cada usuari.

![Permisos NTFS avançats de personal](/Tasca06/IMG/10.png)

En els permisos NTFS de E:\personal veiem que l’heretatge està actiu. Però després el desactivem per controlar millor qui pot fer què.

![Bloqueig d'heretatge](/Tasca06/IMG/11.png)

Quan bloquegem l’heretatge, triem **Convertir els permisos heredats en explícits** per no perdre els permisos bàsics del sistema.

![Permís especial per a Users](/Tasca06/IMG/12.png)

Modifiquem l’entrada del grup **Users** perquè només pugui **Llegir** i **Crear carpetes** (però no crear fitxers directament a l’arrel de personal). Aplicarem aquests permisos només a “Aquesta carpeta”.

![Compartició de la carpeta personal](/Tasca06/IMG/13.png)

A la finestra de **Compartició** donem permisos de **Lectura** al grup Domain Users. Així tothom pot veure la carpeta, però els permisos NTFS ja restringiran més endavant.


---

## 5. Creació de plantilles d’usuari

Les plantilles ens estalvien temps: definim una vegada els grups i la carpeta personal, i després en copiem per crear usuaris reals.

![Creació de la plantilla de gestió](/Tasca06/IMG/16.png)

Creem un usuari amb nom _plantilla-gestio. El nom comença per _ per distingir fàcilment que és una plantilla. El situem dins l’OU Gestio.

![Pertinença a grups de la plantilla](/Tasca06/IMG/17.png)

A la pestanya **Member Of** afegim el grup gestio. Com que gestio ja és membre de personal, aquesta plantilla hereta l’accés a recursos comuns.

![Carpeta personal de la plantilla](/Tasca06/IMG/18.png)

A la pestanya **Profile** indiquem la unitat Z: que connectarà a \\DC13\personal\gesti. Aquesta ruta apunta a una subcarpeta dins del compartit personal. Quan copiem la plantilla per a un usuari real, canviarem el nom de la subcarpeta.

Repetim el mateix procediment per a les plantilles _plantilla-magatzem i _plantilla-gerencia, cadascuna al seu grup corresponent.


---

## 6. Creació d’usuaris de prova a partir de les plantilles

Ara generem un usuari real per a cada departament copiant les plantilles.

![Copiant la plantilla de gestió](/Tasca06/IMG/19.png)

Fent clic dret sobre _plantilla-gestio → **Copiar**, creem un nou usuari. Li posem nom test gestio i logon t.gestio.

![Establir contrasenya](/Tasca06/IMG/20.png)

Assignem una contrasenya temporal i marquem “L’usuari ha de canviar la contrasenya la propera vegada que iniciï sessió”. Així compleix amb polítiques de seguretat bàsiques.

Repetim per a magatzem (usuari t.magatzem) i gerencia (usuari t.gerencia).

![Carpetes personals creades automàticament](/Tasca06/IMG/21.png)

Quan l’usuari inicia sessió per primera vegada, el sistema crea la seva carpeta personal dins E:\personal\gestio (o magatzem, gerencia). Aquí ja veiem les carpetes t.gestio, t.magatzem, t.gerencia i també les de departament.



---

## 7. Preaprovisionament de l’equip PC-1

Abans que el client es connecti, hem de donar d’alta l’objecte de l’equip al domini.

![Creació de l’objecte PC-1](/Tasca06/IMG/22.png)

Dins del contenidor Computers (o millor dins la OU Equips que hauríem creat per organitzar), creem un nou equip amb nom PC-1. El camp “El següent usuari o grup pot unir aquest equip al domini” per defecte és Domain Admins, que és correcte.


---

## 8. Configuració de la màquina virtual client

Creem una VM amb Windows 11, 4 GB de RAM i xarxa NAT. L’enllaçem al domini seguint aquests passos:

### Comprovem que el DNS sap on és el domini

![nslookup del domini](/Tasca06/IMG/23.png)

Des del client executem nslookup translogic13.test i obtenim l’adreça 10.0.2.15`. Aquest és el controlador de domini (DC).

### Configurem la IP i el DNS del client

![Configuració TCP/IP](/Tasca06/IMG/24.png)

Posem el servidor DNS preferit a 10.0.2.15 (el DC). Així el client pot resoldre el nom del domini i trobar els controladors.

### Canviem el nom i unim l’equip al domini

![Canvi de nom i domini](/Tasca06/IMG/25.png)

A Propietats del sistema, canviem el nom a PC-1 i seleccionem **Domini** posant translogic13.test.

![Credencials per unir-se](/Tasca06/IMG/26.png)

Introduïm l’usuari Administrator i la seua contrasenya del domini.

![Unió correcta](/Tasca06/IMG/27.png)

Missatge d’èxit. Reiniciem l’equip.

### Verifiquem que està unit

![Propietats de PC-1 al servidor](/Tasca06/IMG/28.png)

Al servidor, dins l’objecte PC-1, veiem que el sistema operatiu és Windows 11 Enterprise Evaluation.

---

## 9. Prova d’accés amb els usuaris de prova

Finalment, comprovem que podem iniciar sessió al client amb els tres usuaris creats.

### Pantalla d’inici de sessió

![Inici de sessió amb altre usuari](/Tasca06/IMG/29.png)

Fem clic a “Otro usuario” i introduïm les credencials en format t.gestio@translogic13.test o TRANSLOGIC13\t.gestio.

### Sessió iniciada correctament

![Escriptori de test gestio](/Tasca06/IMG/30.png)

L’usuari test gestio ha pogut entrar. Si obrim “Este equipo”, veurem la unitat Z: que apunta a la seua carpeta personal. Repetim la prova amb t.magatzem i t.gerencia i tots funcionen.



