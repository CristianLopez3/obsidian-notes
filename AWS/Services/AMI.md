### 🧱 ¿Qué es una AMI (Amazon Machine Image)?

Una **AMI** (_Amazon Machine Image_) es una **plantilla inmutable** que contiene toda la configuración necesaria para lanzar una instancia EC2. En términos simples, es una "imagen base" con:

- Un **sistema operativo** (Linux, Windows, etc.)
- **Configuración preinstalada** (drivers, configuraciones de red, etc.)
- Software adicional o paquetes que elijas
- Scripts de arranque o configuraciones customizadas
    
Cuando lanzas una instancia EC2, estás seleccionando una AMI que define el estado inicial de esa máquina virtual.

---

### 🎯 ¿Para qué sirve?

Las AMIs sirven para:

1. **Lanzar instancias EC2 rápidamente y de forma consistente**.
2. **Automatizar despliegues**, replicando entornos sin errores manuales.
3. **Guardar snapshots de sistemas operativos o aplicaciones listas para usar**.
4. **Implementar infraestructura como código** con consistencia (por ejemplo, con Terraform o CloudFormation).
5. **Escalar horizontalmente** más rápido (autogenerando instancias idénticas desde la misma AMI en un Auto Scaling Group).
    
---
### ✅ Ventajas clave

|Ventaja|Descripción|
|---|---|
|🔄 Reutilización|Puedes reutilizar la misma AMI para lanzar múltiples instancias consistentes.|
|🚀 Rápido arranque|El tiempo de boot es menor que configurar desde cero cada vez.|
|📦 Customización|Puedes crear AMIs propias con tus apps, librerías, configuraciones y actualizaciones preinstaladas.|
|🔐 Seguridad|Puedes mantener control sobre lo que hay dentro (SO, puertos, configuraciones, etc.).|
|♻️ Versionamiento|Permite mantener imágenes versionadas por ambiente o ciclo de vida (dev, staging, prod).|
|☁️ Integración|Funciona perfectamente con otros servicios como **Auto Scaling**, **Launch Templates**, y **Elastic Beanstalk**.|

---

### 🧪 Ejemplo práctico

Supón que configuraste una instancia EC2 con:

- Ubuntu 22.04
- Node.js + nginx
- Un archivo `.env` de variables
    
En lugar de repetir ese setup manualmente cada vez, puedes crear una **AMI personalizada** y luego lanzar instancias desde ella con todo ya configurado.

### 🛠️ Tipos de AMIs

1. **AMIs públicas** (disponibles en el marketplace de AWS)
2. **AMIs privadas** (creadas por ti o por tu organización)
3. **AMIs compartidas** (de terceros, certificadas o validadas por AWS Partners)
    
---

### 🔒 ¿Qué no es una AMI?

- No es una instancia: es solo una plantilla.
- No es un contenedor Docker: no es portátil fuera de EC2.
- No es mutable: no puedes modificar una AMI directamente; debes crear una nueva basada en otra.


### AMI components

An AMI includes the operating system, storage setup, architecture type, permissions for launching, and any extra software that is already installed. You can use one AMI to launch several EC2 instances that all have the same setup.


### AMI repeatability

AMIs provide repeatability through a consistent environment for every new instance. Because configurations are identical and deployments automated, development and testing environments are consistent. This helps when scaling, reduces errors, and streamlines managing large-scale environments.