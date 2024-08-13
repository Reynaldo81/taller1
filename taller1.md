¿Qué es un servicio REST?
Un servicio REST (Representational State Transfer) es un estilo de arquitectura para diseñar servicios web que permite a los sistemas comunicarse a través de HTTP, usando recursos identificados por URIs (Uniform Resource Identifiers).

¿Cuáles son los principios del diseño RESTful?

Identificación de recursos: Cada recurso se identifica de manera única con un URI.
Uso de métodos HTTP: Los métodos HTTP (GET, POST, PUT, DELETE) se utilizan para realizar acciones sobre los recursos.
Representación de recursos: Los recursos se representan de manera consistente, generalmente en formatos como JSON o XML.
Sin estado (stateless): Cada solicitud del cliente al servidor debe contener toda la información necesaria para entender y procesar la solicitud. El servidor no almacena el estado de las sesiones.
Cacheabilidad: Las respuestas del servidor deben indicar si pueden ser almacenadas en caché para mejorar la eficiencia.
¿Qué es HTTP y cuáles son los métodos HTTP más comunes?
HTTP (HyperText Transfer Protocol) es el protocolo utilizado para enviar y recibir información a través de la web. Los métodos HTTP más comunes son:

GET: Recuperar datos de un servidor.
POST: Enviar datos al servidor para crear un nuevo recurso.
PUT: Actualizar un recurso existente en el servidor.
DELETE: Eliminar un recurso del servidor.
¿Qué es un recurso en el contexto de un servicio REST?
Un recurso es cualquier entidad que se puede identificar y manipular a través de un servicio REST. Por ejemplo, en un servicio de gestión de usuarios, un recurso podría ser un usuario específico.

¿Qué es un endpoint?
Un endpoint es una URL específica dentro de un servicio REST donde se accede a un recurso. Cada endpoint corresponde a una acción específica que se puede realizar sobre el recurso, como obtener datos o enviar actualizaciones.

Estructura de un Servicio REST
¿Qué es un URI y cómo se define?
Un URI (Uniform Resource Identifier) es una cadena de caracteres que identifica un recurso en la web de manera única. Se define en forma de URL (Uniform Resource Locator), como https://api.ejemplo.com/usuarios/123, donde "usuarios" es el recurso y "123" es el identificador específico del recurso.

¿Qué es una API RESTful?
Una API RESTful es una interfaz de programación de aplicaciones (API) que sigue los principios de REST. Permite a diferentes aplicaciones comunicarse entre sí utilizando HTTP y gestionando recursos a través de URIs.

¿Qué son los códigos de estado HTTP y cómo se usan en REST?
Los códigos de estado HTTP son números que el servidor envía al cliente para indicar el resultado de una solicitud. En REST, se usan para informar si la solicitud fue exitosa, si hubo un error, o si se necesita alguna acción adicional.

Código	Significado
200	OK - La solicitud fue exitosa.
201	Creado - Un nuevo recurso fue creado.
400	Solicitud incorrecta - Hay un error en la solicitud.
401	No autorizado - Se necesita autenticación.
404	No encontrado - El recurso no fue encontrado.
500	Error interno del servidor - Hubo un problema en el servidor.
¿Qué es JSON y por qué se usa comúnmente en APIs REST?
JSON (JavaScript Object Notation) es un formato de texto ligero para intercambiar datos. Se usa comúnmente en APIs REST porque es fácil de leer y escribir tanto para humanos como para máquinas, y es compatible con la mayoría de los lenguajes de programación.