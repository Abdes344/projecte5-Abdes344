# Guía de instalación – Windows Server 2025  
**Proyecto:** Despliegue de servidores – TransLògic S.A. 🚀  

---

## 1. Introducción al caso

Tras el asesoramiento previo, **TransLògic S.A.** encarga el despliegue de sus servidores basados en **Windows Server 2025**.  
Con el objetivo de seguir buenas prácticas y optimizar el proceso, se realiza una **instalación de prueba** que servirá como base para:

- Aprender los procedimientos de despliegue.
- Elaborar una **guía de instalación** reutilizable.
- Documentar la futura implantación en los sistemas del cliente.

---

## 2. Configuración de la máquina virtual

La máquina virtual se ha configurado con las siguientes características:

| Recurso              | Configuración |
|----------------------|---------------|
| Memoria RAM          | 8 GB |
| CPU                  | 2 procesadores |
| Disco principal      | 32 GB (SO) |
| Disco secundario     | 10 GB |
| Interfaz de red 1    | NAT |
| Interfaz de red 2    | Host-Only |

🖥️ *Esta configuración permite simular un entorno realista de servidor corporativo.*

---

## 3. Comparación con los requisitos de Microsoft

### Requisitos mínimos de Windows Server 2025 (según Microsoft):

| Recurso         | Mínimo requerido | Configuración VM |
|-----------------|------------------|------------------|
| CPU             | 1.4 GHz, 64-bit  | ✔ 2 CPU |
| RAM             | 2 GB (GUI)      | ✔ 8 GB |
| Almacenamiento  | 32 GB           | ✔ 32 GB + 10 GB |
| Red             | 1 adaptador     | ✔ 2 adaptadores |

### Conclusión

✅ **La configuración es coherente y supera ampliamente los requisitos mínimos**, lo que garantiza un funcionamiento fluido y margen para futuras ampliaciones.

---

## 4. Procedimiento de instalación

### 4.1 Creación de la máquina virtual
- Se crea una nueva VM en el hipervisor.
- Se asignan los recursos definidos en el apartado 2.
- Se monta la ISO de **Windows Server 2025**.

📸 *Captura: configuración de hardware de la VM.*

---

### 4.2 Instalación del sistema operativo
- Se inicia la VM desde la ISO.
- Idioma de instalación: **English (US)**.
- Formato regional y teclado: **Español**.
- Se selecciona **Windows Server 2025 – Desktop Experience (GUI)**.
- Instalación en el disco principal de 32 GB.

📸 *Captura: selección de idioma y edición.*

---

### 4.3 Configuración inicial
- Se establece la contraseña del usuario `Administrator`.
- Se accede al escritorio del servidor.

📸 *Captura: primer inicio de sesión.*

---

### 4.4 Cambio de nombre del equipo
- Desde **Server Manager → Local Server**.
- Se cambia el nombre del equipo a:  
  **DCxx** (siendo `xx` el número de lista correspondiente).
- Se reinicia el sistema.

📸 *Captura: cambio de nombre del equipo.*

---

### 4.5 Actualización del sistema
- Se ejecuta **Windows Update** hasta completar todas las actualizaciones disponibles.
- Una vez finalizado, se **pausan las actualizaciones** el máximo tiempo permitido.

⚙️ *Esto evita cambios inesperados durante fases posteriores del despliegue.*

📸 *Captura: configuración de Windows Update.*

---

## 5. Observaciones finales

- La instalación en modo GUI facilita la administración inicial.
- El uso de dos interfaces de red permite separar tráfico interno y externo.
- La documentación en **Markdown** garantiza portabilidad y facilidad de mantenimiento 📘.

---

## 6. Próximos pasos

- Promoción del servidor a **Controlador de Dominio**.
- Configuración de roles y servicios adicionales.
- Replicación del procedimiento en el entorno productivo.

---

