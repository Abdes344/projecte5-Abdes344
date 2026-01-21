# Despliegue de Active Directory – Prueba de Concepto (PoC) 🏢

## 1. Introducción

Como continuación de la tarea anterior, se procede al **despliegue de Active Directory** sobre la máquina virtual previamente instalada con **Windows Server 2025**.  
Este procedimiento tiene como objetivo:

- Practicar el despliegue del servicio.
- Validar el diseño como **Prueba de Concepto (PoC)**.
- Presentar el resultado a los responsables de **TransLògic** para ajustar la configuración a las necesidades reales del cliente.

---

## 2. Instalación de los roles necesarios

Para poder crear un dominio, es necesario instalar los siguientes roles:

- **Active Directory Domain Services (AD DS)**
- **DNS Server**

### Procedimiento
1. Abrir **Server Manager**.
2. Seleccionar **Add roles and features**.
3. Instalación basada en roles o características.
4. Seleccionar el servidor local.
5. Marcar:
   - Active Directory Domain Services
   - DNS Server
6. Completar el asistente y reiniciar si es necesario.

📸 *Captura: selección de roles AD DS y DNS.*

---

## 3. Creación de un nuevo dominio en un nuevo bosque

- Nombre del dominio:  
  **translogicXX.test**  
  *(XX corresponde al número de lista del alumno)*

### Configuración principal
- Tipo de despliegue: **Nuevo bosque**
- Nombre del dominio raíz: `translogicXX.test`

📸 *Captura: configuración del nuevo bosque.*

---

## 4. Nivel funcional del dominio y del bosque

- **Nivel funcional del bosque:** Windows Server 2025  
- **Nivel funcional del dominio:** Windows Server 2025  

🚀 *Esto permite utilizar todas las funcionalidades modernas de Active Directory.*

---

## 5. Promoción del servidor a Controlador de Dominio

Durante el asistente de promoción:

- Se configura el servidor como **Controlador de Dominio**.
- Se instala automáticamente el servicio DNS.
- Se establece la contraseña de **DSRM**.

### Pantalla resumen (IMPORTANTE)
Antes de finalizar, el asistente muestra una **pantalla resumen** con toda la configuración:
- Nombre del dominio
- Nivel funcional
- Roles instalados
- Opciones de DNS

📸 *Captura obligatoria: pantalla resumen de la promoción.*

El servidor se reinicia automáticamente tras completar el proceso 🔄.

---
