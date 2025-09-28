**Definición técnica:**  
Un **switch** es un dispositivo de red que opera en la capa 2, segmenta el tráfico en múltiples **collision domains** (uno por puerto), y envía datos solo al destino correcto usando direcciones MAC.

**Definición simplificada:**  
Es como un “director de orquesta” que asegura que cada mensaje llegue a la persona correcta sin interrumpir a los demás.

**Analogía:**  
En una oficina, en vez de que todos griten para hablar, el recepcionista (switch) escucha y envía el mensaje solo a la persona indicada.

**Aplicación en Cloud Computing:**  
En AWS, un **switch virtual** está representado por los **subnets en una VPC**, donde el tráfico se envía de forma selectiva a instancias, evitando colisiones.

**Ejemplo en programación (tabla MAC):**

```python
class Switch:
    def __init__(self):
        self.mac_table = {}

    def send(self, src, dst):
        self.mac_table[src] = True
        if dst in self.mac_table:
            print(f"Switch sends frame directly from {src} to {dst}")
        else:
            print(f"Flooding: {src} -> ALL ports")

sw = Switch()
sw.send("PC1", "PC2")
sw.send("PC2", "PC1")

```