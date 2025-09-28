**Definición técnica:**  
Un **broadcast domain** es el conjunto de dispositivos de red que reciben un mensaje de difusión (broadcast) enviado por cualquier dispositivo dentro de ese dominio.

**Definición simplificada:**  
Es el “área de cobertura” donde un anuncio es escuchado por todos los dispositivos conectados.

**Analogía:**  
Imagina un altavoz en un vecindario: todos los vecinos oyen el anuncio.

**Aplicación en Cloud Computing:**  
En la nube, los **broadcast domains** se aíslan mediante **VPCs y subnets**, evitando que un broadcast se propague a toda la infraestructura global.

**Ejemplo en programación (broadcasting):**
```python
devices = ["PC1", "PC2", "PC3"]

def broadcast(sender, message):
    print(f"{sender} sends broadcast: {message}")
    for device in devices:
        if device != sender:
            print(f"{device} received the broadcast")

broadcast("PC1", "Hello everyone!")
```

