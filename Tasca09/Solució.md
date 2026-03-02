# T09: Seguretat: les vulnerabilitats dels sistemes
## Abdeslam Khfif Koubee
---

![imatge](IMG/1.png)

Primer de tot el que haurem de fer sera entrar a la maquina de metasploitable 

---

![imatge](IMG/2.png)

Aqui farem un ip a per veure la nostre ip 

---

![imatge](IMG/3.png)

Ara entrem a la maquina de OPENVAS i ficarem de usuari admin i de contrasenya admin 

---

![imatge](IMG/4.png)

Aqui ens portara a un menu despres de ficar el nostre usuari i la nostre contrasenya 

---

![imatge](IMG/5.png)

Ens sortira aquest menu amb tres opcions "yes", "no", "cancel". i li donarem al yes

---

![imatge](IMG/6.png)

Ens sortira un altre menu amb dues opcions "yes" i "no" i nosaltres li donarem a yes 

---

![imatge](IMG/7.png)

Ara ens demanara fer un nou admin i ficarem de nom de compte usuari i el nostre numero de llista en el meu cas es "usuari13" i de contrasenya usuari

---

![imatge](IMG/8.png)

Despres de ficar-ho tot li donarem a ok per avanzar a la seguent opció

---

![imatge](IMG/9.png)

I aqui ens avisara de que el usuari ja se ha creat correctament

---

![imatge](IMG/10.png)

Aqui ens demanara una clau de subscripció i nosaltres li donarem a skip perque no hen tenim cap


---

![imatge](IMG/11.png)

Aqui no tocarem res i li donarem a "OK" per a continuar 

---

![imatge](IMG/12.png)

Ara ens surten 4 opcions pero nosaltres entrarem a la primera que diu setup

---

![imatge](IMG/13.png)

Al entrar al menu de setup ens sortiran unes altres 6 opcions i entrarem a la segona opcio que diu "network"

---

![imatge](IMG/14.png)

Despres de entrar al network sortiran 6 opcions mes pero nosaltres entrarem a "interfaces"

---

![imatge](IMG/15.png)

Ara configurarem la interface eth0

---

![imatge](IMG/16.png)

Per configurar-ho correctament ficarem en enabled el IPv4 i el DHCP i sortirem 

---

![imatge](IMG/17.png)

Ara despres de configurar el eth0 configurarem el eth1

---

![imatge](IMG/18.png)

Veiem que tot esta en disabled

---

![imatge](IMG/19.png)

Però nosaltres tindrem que ficar en enabled el IPv4 i el DHCP i sortirem 

---

![imatge](IMG/20.png)

Ara tornarem a aquest menu que ara tindrem que entrar a la opció que diu "IP"

---

![imatge](IMG/21.png)

I despres de ficar en enabled el eth0 i el eth1 i veurem les nostres ip's 

---

![imatge](IMG/22.png)

Despres de fer tot ja tancarem la sesió ja que tot esta fet correcte 

---

![imatge](IMG/23.png)

Ara anirem a google i al buscador buscarem https://192.168.56.103 que es la ip que ens han donat anteriorment i iniciarem sesió 

---

![imatge](IMG/24.png)

Un cop dins anirem a la opció de "assets" i dins i ha una opció que es la de hosts i anirem a aquella opció

---

![imatge](IMG/25.png)

Al entrar a hosts farem una nova host i ficarem la ip que ens han donat a la maquina virtual anteriror la de metasploitable

---

![imatge](IMG/26.png)

Ara farem una nova target i de nom li ficarem un nom en el meu cas li he ficat vulnerable linux i guardarem 

---

![imatge](IMG/27.png)

Aqui ficarem la primera opció que diu "use scan config default" i a on fica SMB ficarem "mfsadmin" i guardarem 

---

![imatge](IMG/28.png)

Ara farem una nova tasca ficarem un nom el que vulguis en el meu cas Vulnerable linux i on fica "scan targets" triarem la target creada anteriorment

---

![imatge](IMG/29.png)

Aqui veiem que la tasca ja esta en proces

---


![imatge](IMG/30.png)

Ara veiem que la tasca ja ha acabat


---

![imatge](IMG/31.png)

Aqui veiem els resultats de la tasca 

---


![imatge](IMG/32.png)

I aqui veiem tots els ports de la nostre tasca 

---


