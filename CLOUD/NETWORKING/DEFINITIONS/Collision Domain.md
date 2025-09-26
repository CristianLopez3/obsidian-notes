**Definición técnica:**  
Un **collision domain** es un segmento de red donde los dispositivos comparten el mismo medio físico y, si dos dispositivos transmiten datos al mismo tiempo, ocurre una colisión.

**Definición simplificada:**  
Es el "espacio" de la red donde los mensajes pueden chocar si dos dispositivos hablan a la vez.

**Analogía:**  
Imagina un grupo de personas en una misma sala pequeña. Si dos hablan al mismo tiempo, nadie entiende nada → ocurre una “colisión”.

**Aplicación en Cloud Computing:**  
En la nube, las colisiones prácticamente no ocurren porque los **switches virtuales** y la infraestructura de los proveedores (AWS VPC, Azure VNet, GCP VPC) usan conmutación a nivel de capa 2 y evitan este problema.

**Ejemplo en programación (simulación con Python):**

```python
devices = ["PC1", "PC2", "PC3"]

def send_message(sender, message):
    print(f"{sender} is sending: {message}")
    for device in devices:
        if device != sender:
            print(f"Collision detected at {device}!")

send_message("PC1", "Hello")
send_message("PC2", "Hi")

```

