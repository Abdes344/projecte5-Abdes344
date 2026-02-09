Aquí ho tens passat a Markdown, clar, ordenat i llest per documentar la pràctica:

📘 Introducció

Un cop tenim creat el domini, el següent pas és desplegar-lo, és a dir, crear i organitzar els diferents objectes que el formen:

Usuaris

Grups

Equips

En aquesta pràctica veurem la importància d’organitzar aquests objectes mitjançant Unitats Organitzatives (OU), per facilitar l’administració, l’escalabilitat i l’aplicació de polítiques.

🛠️ Procediment pràctic
1️⃣ Estructura d’unitats organitzatives (OU)

Crear una estructura d’OU coherent per a l’organització.

Justificar la decisió de disseny (criteri funcional i administratiu).

2️⃣ Creació de grups

Definir la següent estructura de grups de seguretat:

gestio

magatzem

gerencia

personal

📌 Nota:
Els grups gestio, magatzem i gerencia han de ser membres del grup personal.

3️⃣ Plantilles d’usuari

Crear una plantilla d’usuari per a cadascun dels grups següents:

Gestió

Magatzem

Gerència

Cada plantilla ha de tenir:

Pertinença automàtica al grup corresponent

Creació de la carpeta personal de l’usuari

4️⃣ Usuaris de prova

Crear un usuari de prova per a cadascuna de les plantilles definides.

Verificar que:

Pertanyen al grup correcte

Tenen la seva carpeta personal creada correctament

5️⃣ Aprovisionament d’equip client

Crear una OU anomenada equips

Aprovisionar un equip amb el nom:

PC1

6️⃣ Màquina virtual client

Crear una VM amb Windows 11 amb les següents característiques:

💾 RAM: 4 GB

💽 Disc: suficient per al sistema

🌐 Xarxa: NAT

Un cop creada la VM:

Afegir l’equip al domini

7️⃣ Verificació del funcionament

Comprovar el correcte funcionament del domini:

Iniciar sessió a PC1 amb:

Usuari de Gestió

Usuari de Magatzem

Usuari de Gerència

Verificar:

Autenticació correcta

Aplicació de la plantilla d’usuari

Accés a la carpeta personal
