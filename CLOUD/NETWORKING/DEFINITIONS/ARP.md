> **Address Resolution Protocol**

## 1. **Definición técnica y simplificada**

- **Definición técnica:**  
    El **Address Resolution Protocol (ARP)** es un protocolo de la capa de red (entre la capa 2 y 3 del modelo OSI) que permite mapear una **dirección IP** (lógica) a una **dirección MAC** (física) en una red local.
- **Definición simplificada:**  
    Es como una guía que traduce la dirección de una casa virtual (**IP**) a la dirección física exacta (**MAC**) para que los datos lleguen al dispositivo correcto.
    
## 2. **Analogía o ejemplo de la vida real**

Imagina que quieres enviarle una carta a “Juan Pérez” (IP), pero necesitas su dirección exacta de casa (MAC) para que el cartero pueda entregarla. Llamas a todos los vecinos (broadcast) preguntando:  

👉 “¿Quién es Juan Pérez?”  
Cuando Juan responde, ya guardas su dirección para futuros envíos.


## 3. **Aplicación en Cloud Computing**

En **Cloud Computing** (AWS, Azure, GCP), los dispositivos virtuales (VMs o instancias EC2) también necesitan resolver IPs a MACs dentro de la red virtual.

- En AWS, cada **Elastic Network Interface (ENI)** tiene una MAC y una IP privada.
- El **ARP virtual** lo maneja el **hypervisor** (no los usuarios), garantizando que cada instancia encuentre a su vecino dentro de la misma **subnet**.
- Esto también asegura el **aislamiento entre VPCs**, porque un ARP de una VPC no puede resolver direcciones MAC de otra.

## 4. **Ejemplo de código o aplicación en programación**
Ejemplo en **Python** usando la librería `scapy` para enviar una petición ARP:

```python
from scapy.all import ARP, Ether, srp

# Enviar ARP request para descubrir la MAC de una IP en la red
target_ip = "192.168.1.1"
arp_request = ARP(pdst=target_ip)
ether = Ether(dst="ff:ff:ff:ff:ff:ff")  # Broadcast
packet = ether/arp_request

result = srp(packet, timeout=2, verbose=False)[0]

for sent, received in result:
    print(f"IP: {received.psrc}, MAC: {received.hwsrc}")

```

Este script pregunta en la red:  
👉 “¿Quién tiene la IP 192.168.1.1?”  
y obtiene la **MAC address** correspondiente.