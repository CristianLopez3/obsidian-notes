
**`Open Systems Interconnection`**
* OSI model by AWS [LINK](https://aws.amazon.com/what-is/osi-model/)
* 

![OSI MODEL](/assets/img/OSI-MODEL.png)

Propósito del modelo OSI

- **Interoperabilidad:** Permite que dispositivos y software de diferentes fabricantes se comuniquen entre sí, fomentando un mercado abierto.
- **Enseñanza y aprendizaje:** Al separar las funciones de red, facilita la comprensión y el estudio de los procesos de comunicación.
- **Desarrollo de tecnologías:** Los ingenieros pueden desarrollar nuevos sistemas de red conociendo la capa en la que trabajan, basándose en procesos y protocolos repetibles.
- **Diagnóstico de problemas:** Ayuda a los profesionales de redes a identificar la capa donde se encuentra un fallo para resolverlo de manera más eficiente. 

Las siete capas del modelo OSI

Las capas se organizan de manera jerárquica. Durante la transmisión, los datos se originan en la capa 7 del dispositivo emisor y bajan hasta la capa 1. En el dispositivo receptor, los datos suben de la capa 1 a la capa 7. 

Capas de host (capas superiores)

Están más cerca del usuario final e interactúan directamente con el software. 

- **Capa 7: Aplicación:** Permite a las aplicaciones de software acceder a la red. Es la capa con la que interactúan los usuarios directamente (por ejemplo, navegadores web, clientes de correo electrónico). Los protocolos comunes incluyen HTTP, FTP, SMTP y DNS.
- **Capa 6: Presentación:** Traduce, cifra y comprime los datos para que sean entendibles por la capa de aplicación. Garantiza que los datos de un sistema sean legibles por el otro, manejando la sintaxis y el formato.
- **Capa 5: Sesión:** Establece, gestiona y finaliza las conexiones (sesiones) entre las aplicaciones. Sincroniza el intercambio de datos y gestiona los diálogos entre las aplicaciones. 

Capas de medios (capas inferiores)

Gestionan la comunicación física y la transmisión de datos a través de la red. 

- **Capa 4: Transporte:** Garantiza la entrega de datos fiable y ordenada entre los procesos de la aplicación en los sistemas host. Los protocolos más conocidos son TCP (orientado a la conexión) y UDP (sin conexión), que gestionan la verificación de errores y el control de flujo.
- **Capa 3: Red:** Se encarga del direccionamiento lógico (direcciones IP) y el enrutamiento de paquetes de datos a través de diferentes redes. Utiliza el Protocolo de Internet (IP) para encaminar los datos a su destino.
- **Capa 2: Enlace de datos:** Proporciona un tránsito de datos fiable a través del enlace físico. Detecta y, en algunos casos, corrige errores en la capa física. Se divide en dos subcapas: Control de Enlace Lógico (LLC) y Control de Acceso a Medios (MAC).
- **Capa 1: Física:** Transmite y recibe el flujo de bits sin procesar a través del medio físico, como un cable de red, fibra óptica u ondas de radio. Se encarga de las especificaciones eléctricas y mecánicas de la interfaz. 

Diferencia con el modelo TCP/IP

El modelo TCP/IP, que es el protocolo utilizado en internet, a menudo se compara con el OSI. Aunque ambos son modelos de capas, tienen diferencias clave en su estructura: 

- **Número de capas:** El modelo OSI tiene siete capas, mientras que el TCP/IP tiene cinco (o a veces cuatro, dependiendo de la interpretación), agrupando varias de las funciones del OSI en capas más amplias.
- **Detalle:** El modelo OSI es más detallado y teórico, lo que lo hace una excelente herramienta de enseñanza. El TCP/IP es más práctico y se centra en los protocolos que realmente se utilizan para la comunicación en la red.