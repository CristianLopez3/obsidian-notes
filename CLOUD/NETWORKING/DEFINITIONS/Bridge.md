**Definición técnica:**  
Un **bridge** es un dispositivo de red que conecta y filtra tráfico entre dos segmentos de red en la capa 2 (enlace de datos), reduciendo colisiones.

**Definición simplificada:**  
Es como un "puente inteligente" que conecta dos redes pequeñas y decide qué tráfico debe pasar.

**Analogía:**  
Piensa en un portero que deja pasar solo a las personas que realmente tienen que cruzar de una sala a otra, evitando congestión.

**Aplicación en Cloud Computing:**  
Los **bridges virtuales** se implementan dentro de hipervisores (como en AWS EC2 con Xen/KVM) para conectar interfaces de máquinas virtuales con redes virtuales.

**Ejemplo en programación (pseudocódigo):**

```python
class Bridge:
    def __init__(self):
        self.mac_table = {}

    def forward(self, src, dst):
        self.mac_table[src] = True
        if dst in self.mac_table:
            print(f"Forwarding frame from {src} to {dst}")
        else:
            print("Frame dropped: destination unknown")

bridge = Bridge()
bridge.forward("PC1", "PC2")

```


### Ejemplo Grafico

![Example](/assets/img/bridge-example.png)
