
> Virtual Private Cloud

### Amazon Virtual Private Cloud (Amazon VPC)

An Amazon VPC lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define.

### Subnet

Subnets are used to organize your resources and can be made publicly or privately accessible. A private subnet is commonly used to contain resources like a database storing customer or transactional information. A public subnet is commonly used for resources like a customer-facing website.


## AWS Cloud, Regions, Amazon VPC, and AZs

The **AWS Cloud** is the outermost box in most diagrams.

**Region** is the next box. AWS Regions are separate geographic areas. You choose your Region based on your users' geographic location for lower latency, compliance and data residency requirements, available services, and cost.

**Amazon VPC** is a solid box, and it represents your isolated, logically segmented network within AWS. A VPC helps you to control your network resources and security.

**Availability Zones** are shown as separate boxes across a region. AZs consist of one or more discrete data centers, each with redundant power, networking, and connectivity, and housed in separate facilities. Using multiple AZs can protect your applications from the failure of a single location in the Region.

**Subnets** are essentially segments of your VPC, allowing you to divide your VPC into smaller, manageable sections. A subnet is a range of IP addresses in your VPC.

**Private subnets** are designed to isolate resources that shouldn't be directly exposed to the public internet. In diagrams, they are illustrated with solid boxes.

# Spanish -- 

Una **VPC** (_Virtual Private Cloud_) en AWS es **una red virtual privada** donde defines cómo se comunican tus recursos en la nube.

La puedes imaginar como **tu propio centro de datos dentro de AWS**, completamente aislado de otras redes, pero con la flexibilidad de conectarte a Internet o a redes corporativas según lo necesites.

En AWS, **cada cuenta** puede tener varias VPCs, y cada VPC es **lógicamente independiente**.

---

##  Elementos principales dentro de una VPC

1. **CIDR Block**
    - Es el rango de direcciones IP privadas que tendrá tu red. Ejemplo: `10.0.0.0/16`.
        
2. **Subnets**
    - Divisiones de la VPC.
        - **Públicas** → con acceso a Internet (vía Internet Gateway).
        - **Privadas** → sin acceso directo a Internet (usadas para bases de datos, backend, etc.).
            
3. **Route Tables**
    - Tablas que definen hacia dónde va el tráfico desde una subred.
        
4. **Internet Gateway (IGW)**
    - Permite que las subnets públicas tengan acceso a Internet.
        
5. **NAT Gateway**
    - Permite que las subnets privadas salgan a Internet (por ejemplo, para actualizaciones), sin que se pueda iniciar una conexión desde fuera hacia ellas.
        
6. **Security Groups** y **Network ACLs**
    - Firewalls que controlan el tráfico a nivel de instancia (Security Groups) o a nivel de subnet (NACLs).
        

---

## ¿Para qué sirve una VPC?

- **Aislar y segmentar recursos** (por ejemplo, tener la base de datos en una subnet privada).
- **Controlar el flujo de red** con reglas y rutas.
- **Conectarte de forma segura** a tu empresa mediante VPN o AWS Direct Connect.
- **Cumplir requisitos de seguridad y normativas** al tener control total del direccionamiento IP y firewalls.
    

---

## ✅ Ventajas

|Ventaja|Descripción|
|---|---|
|🔒 Seguridad|Control total sobre el tráfico entrante y saliente.|
|📐 Flexibilidad|Puedes definir tu propio esquema de IPs y subredes.|
|🌎 Conectividad híbrida|Integración con tu red on-premise vía VPN o Direct Connect.|
|♻️ Escalabilidad|Puedes agregar más subnets, gateways o peering a otras VPCs.|
|💰 Costos controlados|No pagas por crear la VPC en sí, solo por los recursos que usas.|

---

##  Ejemplo práctico de uso

Imagina que vas a desplegar una aplicación web en AWS:

1. **Subnet pública**:
    - EC2 con tu servidor web.
    - Un Load Balancer público.
        
2. **Subnet privada**:
    - RDS para la base de datos.
    - EC2 backend sin acceso directo desde Internet.
        
3. **Internet Gateway**:
    - Para que el tráfico web llegue al Load Balancer.
        
4. **NAT Gateway**:
    - Para que el backend pueda actualizarse desde Internet sin exponerse.
        

---

## Building an Amazon VPC in the AWS Cloud

**Core components covered in this demonstration**

It's helpful to understand how resources are created using the AWS Management Console. The following is a high-level overview of the resources and core components created in the preceding demonstration.


### Create the Amazon VPC

Before you can create resources in the AWS Cloud, the first step is to create your own Amazon VPC.  You will also specify the Region best located for your resources.

![[Pasted image 20250811211232.png]]
### Create the subnets

You will create two public and private subnets across two availability zones. This is a best practice to achieve high availability.
![[Pasted image 20250811211304.png]]
### Create an internet gateway and route traffic

Without an internet gateway, your users can't get to your resources. First, you create the internet gateway. Then, you create route tables to route traffic to allow internet traffic in and local traffic out.
![[Pasted image 20250811211333.png]]
You are well on your way to creating your resources in your Amazon VPC. At this point, you would consider what type of security you need and filter the traffic coming in and out. Remember security groups and network ACLs? That's where they come in handy! And finally, you'd be ready to add your resources like EC2 instances or databases in your subnets.