# 🖥️ P02: Llicenciament Windows Server 2025

## 📖 Breu descripció

Mentre inicieu la vostra aventura emprenedora, cal continuar assumint despeses i gestionant nous projectes. Gràcies a la bona feina realitzada a **EverPia**, la consultora ha decidit confiar en vosaltres i derivar-vos alguns encàrrecs de clients que actualment no poden assumir.

---

# 🚚 Introducció al client

L'empresa **TransLògic S.A.**, especialitzada en logística regional, vol modernitzar la seva infraestructura tecnològica mitjançant la migració a **Windows Server 2025**.

Actualment disposen d'un servidor físic antic que ha quedat obsolet i necessiten una solució més moderna basada en la **virtualització**, amb l'objectiu de:

* ⚡ Millorar el rendiment.
* 🔒 Incrementar la seguretat.
* 📈 Facilitar l'escalabilitat futura.
* 🛠️ Simplificar la gestió dels serveis.

---

# 🏗️ Infraestructura actual

## 💻 Servidor físic (Host)

* 1 servidor físic.
* 2 processadors (CPU).
* 12 nuclis físics per processador.

### Total de nuclis:

**24 cores físics**

---

## 🖥️ Màquines virtuals (VMs)

La infraestructura virtual estarà formada per:

| Servei                                           | Quantitat  |
| ------------------------------------------------ | ---------- |
| Active Directory (Controlador de Domini)         | 1          |
| Servidor de Fitxers                              | 1          |
| Servidor d'Impressores i Gestió Documental       | 1          |
| SQL Server (ERP)                                 | 1          |
| Aplicacions de logística i terminals de magatzem | 8          |
| **Total**                                        | **12 VMs** |

---

## 👥 Usuaris i dispositius

### Personal de l'empresa

* 45 empleats en total.

### Distribució

#### 🏢 Treballadors d'oficina

* 30 empleats.
* Cada treballador disposa de:

  * 1 PC.
  * 1 portàtil.

**Total dispositius oficina: 60**

#### 📦 Mossos de magatzem

* 15 empleats.
* Comparteixen 5 tauletes robustes.
* Funcionament en 3 torns.

**Total dispositius magatzem: 5**

### Total dispositius

**65 dispositius**

---

# 🔍 Anàlisi del model de llicenciament

Microsoft utilitza un sistema de llicenciament basat en:

* 🧩 Nombre de nuclis físics (cores).
* 👤 CALs d'usuari (User CAL).
* 💻 CALs de dispositiu (Device CAL).

El servidor disposa de:

**24 cores físics**

Microsoft exigeix llicenciar tots els nuclis del servidor.

---

# 💰 Opció 1: Windows Server 2025 Standard

### Característiques

* Inclou dret d'execució de fins a **2 màquines virtuals** per cada servidor completament llicenciat.
* Es poden acumular ("stacking") llicències per obtenir més drets de virtualització.

### Necessitats del client

* 12 màquines virtuals.
* Cada paquet complet de llicències permet 2 VMs.

Càlcul:

12 VMs ÷ 2 = **6 llicències Standard completes**

### Cost aproximat

Preu Microsoft Standard (16 cores):

**1.176 $**

Adaptació a 24 cores:

* 1 paquet de 16 cores.
* 4 paquets addicionals de 2 cores.

Cost aproximat per servidor complet:

≈ 1.764 $

Com que necessitem 6 drets de virtualització:

**1.764 $ × 6 = 10.584 $**

---

# 💰 Opció 2: Windows Server 2025 Datacenter

### Característiques

* Virtualització il·limitada.
* Storage Spaces Direct.
* Software Defined Networking (SDN).
* Containers il·limitats.
* Preparat per a entorns híbrids i cloud.

### Cost aproximat

Preu Microsoft Datacenter (16 cores):

**6.771 $**

Adaptació a 24 cores:

Cost estimat:

≈ **10.156 $**

---

# 👤 User CAL o 💻 Device CAL?

## Opció User CAL

Es llicencia cada treballador.

* 45 empleats
* 45 User CALs

### Avantatges

✅ Cada usuari pot accedir des de diversos dispositius.

✅ Ideal per als treballadors d'oficina amb PC i portàtil.

---

## Opció Device CAL

Es llicencia cada dispositiu.

Dispositius totals:

* 60 dispositius oficina
* 5 tauletes

Total:

**65 Device CALs**

---

## Comparativa

| Tipus      | Quantitat |
| ---------- | --------- |
| User CAL   | 45        |
| Device CAL | 65        |

### Solució més econòmica

🏆 **User CAL**

Es necessiten 20 llicències menys.

---

# 📊 Comparació final

| Característica        | Standard            | Datacenter  |
| --------------------- | ------------------- | ----------- |
| Cost aproximat        | 10.584 $            | 10.156 $    |
| Virtualització        | 12 VMs amb stacking | Il·limitada |
| Escalabilitat         | Mitjana             | Molt alta   |
| Storage Spaces Direct | ❌                   | ✅           |
| SDN                   | ❌                   | ✅           |
| Containers avançats   | Limitats            | Il·limitats |
| Futur creixement      | Limitat             | Excel·lent  |

---

# ✅ Recomanació final

Després d'analitzar els costos i les necessitats de TransLògic S.A., la millor opció és:

## 🏆 Windows Server 2025 Datacenter + User CALs

### Motius

* 💰 Cost similar o fins i tot inferior a Standard.
* 🚀 Virtualització il·limitada.
* 📈 Preparat per al creixement futur.
* 🔒 Major disponibilitat i flexibilitat.
* ☁️ Integració amb entorns híbrids i cloud.
* 🛠️ Accés a funcionalitats avançades exclusives.

Aquesta solució garanteix que l'empresa pugui ampliar serveis i desplegar noves màquines virtuals sense haver de comprar noves llicències de servidor.

---

# 🎤 Proposta de presentació al client (5-10 minuts)

### Diapositiva 1

🏢 Presentació de TransLògic i objectius del projecte.

### Diapositiva 2

🖥️ Infraestructura actual.

### Diapositiva 3

☁️ Beneficis de la virtualització.

### Diapositiva 4

⚖️ Comparativa Standard vs Datacenter.

### Diapositiva 5

💰 Comparativa de costos.

### Diapositiva 6

👤 User CAL vs Device CAL.

### Diapositiva 7

🏆 Solució recomanada.

### Diapositiva 8

❓ Torn de preguntes.

---

# 📚 Materials i enllaços de suport

* 📘 UD6.AA1. Introducció a Windows Server (Moodle 0224 SOX)
* 📗 Microsoft Windows Server 2025 Licensing & Pricing

Documentació oficial:

[Microsoft Windows Server Licensing & Pricing](https://www.microsoft.com/en-us/windows-server/pricing?msockid=2e31bcad10cd665c1743aa2b11b36772&utm_source=chatgpt.com)

