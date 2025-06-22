AWS Snowmobile es un servicio de transporte físico de datos a escala exabyte, diseñado para migraciones masivas hacia AWS. A continuación te explico con enfoque técnico y casos de uso reales:

🔍 **¿Qué es AWS Snowmobile?**
AWS Snowmobile es literalmente un camión blindado que transporta un contenedor de 45 pies (como los de carga marítima) equipado con almacenamiento seguro de hasta 100 petabytes por unidad. El objetivo es transferir enormes cantidades de datos (del orden de petabytes a exabytes) desde data centers on-premise hacia Amazon S3 u otros servicios en la nube de AWS.

🧠 **¿Por qué usar Snowmobile?**
Cuando mover datos por la red sería demasiado lento o inviable. Por ejemplo:

Si tienes 10 PB de datos y una conexión dedicada de 10 Gbps, tomaría más de 3 años transferir todo.

En cambio, con Snowmobile podrías hacerlo en semanas.

🧰 **¿Cómo funciona técnicamente?**
Evaluación previa: AWS te asigna un equipo de seguridad y logística. Evalúan red, capacidad eléctrica y seguridad física.

Entrega del Snowmobile: Se traslada físicamente a tu sitio, junto con personal especializado.

Conexión: Se conecta mediante red de alta velocidad (por ejemplo, 40 Gbps Ethernet) al data center.

Transferencia: Usas herramientas como Snowball Edge client, AWS OpsHub o scripts personalizados para mover los datos.

Encriptación: Todos los datos son cifrados con claves de 256 bits gestionadas por AWS KMS.

Transporte: Se lleva el camión de vuelta a un centro de datos de AWS, donde se hace el ingest a S3 u otro destino.

🔐 Seguridad
Todos los datos están cifrados en tránsito y en reposo.

El vehículo está blindado, con GPS, videovigilancia 24/7, acceso restringido y escoltas de seguridad.

Solo un número muy limitado de clientes puede usar Snowmobile, con aprobación directa de AWS.

🎯 Casos de uso típicos
Migraciones de data centers heredados (legacy) a AWS.

Archivos multimedia de alto volumen (empresas de cine, estudios científicos, etc).

Backups históricos o recuperación tras desastres de escala masiva.

Gobiernos o empresas con datos regulatorios que requieren migración segura y auditable.

❓Dato interesante
AWS Snowmobile no es un servicio de autoservicio ni disponible bajo demanda. Es altamente especializado y se coordina directamente con el equipo de AWS.

