
> Connect us to the internet, it acts like a gateway to connect our router to the internet, acting like a first line of defense basing on the rules we can set up on it, with firewalls, white ips, etc.


**ISP**: internet service provider
**Bandwidth**: how much traffic can this connection handle? 25mb, 1GB
**Speed**: How much latency do our connections have?

### **Definición técnica:**

Un **Border Router** es un router ubicado en el límite entre **dos dominios de red distintos**, normalmente entre una red interna (LAN, campus, datacenter o VPC) y una red externa (Internet, otra WAN, otra VPC).  
Opera en **capa 3** y maneja protocolos de enrutamiento externos como **BGP**.

### **Definición simplificada:**

Es el **router que está en la frontera** de una red, encargado de comunicarse con redes externas y controlar qué tráfico entra o sale.


**Aplicación en Cloud Computing**

En la nube, el concepto de border router se implementa como componentes virtuales que conectan la red privada con redes externas:

### **AWS**

- **Virtual Private Gateway (VGW)** → conexión a redes on-premises vía VPN.
- **Internet Gateway (IGW)** → conexión a Internet.
- **Transit Gateway (TGW)** → conecta múltiples VPCs y WANs.  
    Todos estos actúan como _border routers_ virtuales.
    

### **Azure**
- **VPN Gateway** y **ExpressRoute Gateway**.
- **Azure Firewall** y **Virtual WAN Hub**, cuando enrutan tráfico externo.
    
### **GCP**

- **Cloud VPN** y **Cloud Router** (BGP dinámico).
- **Interconnect** y **NAT Gateway** para tráfico externo.

En todos los casos, estos gateways administran **rutas hacia redes externas**, tal como lo hace un border router físico.