🧩 Control de versions: treball local + GitHub

Fins ara hem gestionat el control de versions utilitzant directament el repositori des de la web de GitHub. Tot i que ens ha permès resoldre diversos problemes, aquesta metodologia presenta limitacions importants.

⚠️ Limitacions de treballar només des de GitHub Web

Lentitud a l’hora d’editar
L’editor web no és tan versàtil ni eficient com un editor local de codi com Visual Studio Code o un editor específic de Markdown com Ghostwriter.

Gestió del repositori poc eficient
Afegir arxius, crear carpetes o reorganitzar el projecte pot resultar feixuc i requereix passos innecessaris.

🚀 Nou enfocament: treball professional amb Git i GitHub

Per aquests motius, començarem a treballar com es fa en el món real, combinant:

Git → control de versions local

GitHub → repositori remot

Tot i que GitHub no és l’única opció (existeixen alternatives com GitLab o Bitbucket), en el nostre cas serà la plataforma utilitzada.

🧠 Context: què és Git?

Git és un sistema de control de versions descentralitzat, creat per Linus Torvalds, el creador de Linux.
Va aparèixer abans que GitHub i va suposar una revolució respecte als sistemes centralitzats que s’utilitzaven anteriorment.

🔁 Flux de treball que seguirem
1️⃣ Repositori remot

Partim sempre d’un repositori existent a GitHub.

2️⃣ Còpia local

Creem una còpia sincronitzada del repositori al nostre ordinador (PC de casa o de l’escola).

3️⃣ Treball en local

Tots els canvis es fan en local, utilitzant editors adequats.

El flux de treball és:

git add
git commit

4️⃣ Puja de canvis

Quan acabem una sessió de treball:

git push

5️⃣ Sincronització

Quan reprenem la feina o canviem d’ordinador:

git pull


Això garanteix que el repositori local estigui sempre actualitzat amb els últims canvis del repositori remot.

✅ Beneficis d’aquest sistema

Edició més ràpida i potent

Millor organització del projecte

Flux de treball realista i professional

Facilitat per treballar des de diferents ordinadors

Preparació per entorns reals de desenvolupament
