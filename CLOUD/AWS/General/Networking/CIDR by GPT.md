un **CIDR** (Classless Inter-Domain Routing) es un formato para **especificar rangos de direcciones IP** junto con su máscara de red, usado tanto en **networking tradicional** como en **cloud computing** (AWS, Azure, GCP, etc.) para definir subredes y controlar el alcance de las comunicaciones.

## 📍 Concepto básico

En lugar de usar las antiguas clases de red (Clase A, B, C), CIDR utiliza un **prefijo** que indica cuántos bits de la dirección IP forman la parte de la red.  
Se expresa como:

CopyEdit

`DirecciónIP/Prefijo`

Ejemplos:

- `192.168.1.0/24` → 24 bits para la parte de red, 8 bits para hosts.
- `10.0.0.0/16` → 16 bits para red, 16 bits para hosts.

## 🔹 En **networking tradicional**

- Sirve para **definir subredes** y optimizar el uso de direcciones IP.
- Se utiliza en routing para **agrupar redes** y reducir tablas de enrutamiento.
- Ejemplo: Un router puede anunciar `172.16.0.0/12` en lugar de muchas redes pequeñas.

## 🔹 En **cloud computing**

- Es clave al **crear una VPC** (en AWS, GCP, Azure), porque define el **espacio de direcciones IP privado** que podrá usar la red.
    
- Se usa para **subnetting** (dividir la VPC en subredes más pequeñas).
    
- Ayuda a controlar:
    
    - **Rangos de direcciones internas** (no se pueden cambiar después de creada la VPC en muchos casos).
    - **Reglas de seguridad** (Security Groups, Firewalls).
    - **Conectividad entre redes** (peering, VPN, Direct Connect).
        

**Ejemplo en AWS**  
Si creas una VPC con:

```makefile
CIDR: 10.0.0.0/16
```

- Rango total: 65,536 direcciones.
    
- Puedes dividir en subredes como:
    
    - `10.0.0.0/24` (256 direcciones)
    - `10.0.1.0/24`
    - etc.
        

---

## 🧮 Tabla rápida de tamaños CIDR (IPv4)

|CIDR|Nº de hosts utilizables*|Ejemplo de rango|
|---|---|---|
|/32|1|192.168.1.5/32|
|/30|4 (2 utilizables)|192.168.1.0 – 192.168.1.3|
|/24|256 (254 utilizables)|192.168.1.0 – 192.168.1.255|
|/16|65,536 (65,534)|10.0.0.0 – 10.0.255.255|
|/12|1,048,576 (1,048,574)|172.16.0.0 – 172.31.255.255|

> *Los utilizables excluyen dirección de red y broadcast en subredes tradicionales.

---
💡 **Tip Cloud**: En AWS, las subredes siempre reservan 5 direcciones IP por cada rango, incluso en privadas, para uso interno del servicio.