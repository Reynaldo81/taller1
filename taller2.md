Sección 1: Introducción a Servicios en Quarkus
¿Qué es @ApplicationScoped en Quarkus?
Es una anotación que define un bean de alcance de aplicación, es decir, una instancia única que se comparte y se reutiliza a lo largo del ciclo de vida de la aplicación.

¿Cómo funciona la inyección de dependencias en Quarkus?
La inyección de dependencias en Quarkus se gestiona a través de CDI (Contextos e Inyección de Dependencias), permitiendo la inyección automática de beans en otros componentes mediante anotaciones como @Inject.

¿Cuál es la diferencia entre @ApplicationScoped, @RequestScoped, y @Singleton en Quarkus?

@ApplicationScoped: Crea una única instancia del bean para toda la aplicación.
@RequestScoped: Crea una nueva instancia para cada petición HTTP.
@Singleton: Similar a @ApplicationScoped, pero más cercano al patrón Singleton, con diferencias en el ciclo de vida y la inicialización.
¿Cómo se define un servicio en Quarkus utilizando @ApplicationScoped?
Se define una clase con la anotación @ApplicationScoped, convirtiéndola en un servicio gestionado por CDI, disponible durante todo el ciclo de vida de la aplicación.

¿Por qué es importante manejar correctamente los alcances (scopes) en Quarkus al crear servicios?
Para garantizar eficiencia y control sobre los recursos, evitando la creación innecesaria de instancias y asegurando que los beans se compartan o renueven según sea apropiado.

Sección 2: Creación de un ApiResponse Genérico
¿Qué es un ApiResponse genérico y cuál es su propósito en un servicio REST?
Es una clase genérica que encapsula la estructura de la respuesta de una API, incluyendo datos, mensajes y códigos de estado, proporcionando consistencia en las respuestas.

¿Cómo se implementa una clase ApiResponse genérica en Quarkus?
Se crea una clase genérica con atributos como data, message, y status, que puede ser reutilizada en diferentes endpoints para estructurar las respuestas de manera uniforme.

¿Cómo se modifica un recurso REST en Quarkus para que utilice un ApiResponse genérico?
Se cambia el tipo de retorno de los métodos REST para que devuelvan instancias de ApiResponse<T>, donde T es el tipo de datos específicos que se está retornando.

¿Qué beneficios ofrece el uso de un ApiResponse genérico en términos de mantenimiento y consistencia de código?
Facilita el mantenimiento al estandarizar las respuestas, reduce la duplicación de código y mejora la legibilidad al tener un formato de respuesta común.

¿Cómo manejarías diferentes tipos de respuestas (éxito, error, etc.) utilizando la clase ApiResponse?
Se pueden crear métodos estáticos en la clase ApiResponse para construir fácilmente respuestas de éxito o error, estableciendo los mensajes y códigos de estado correspondientes.

Sección 3: Integración y Buenas Prácticas
¿Qué consideraciones se deben tener al inyectar servicios en un recurso REST en Quarkus?
Asegurarse de utilizar el alcance adecuado para evitar problemas de concurrencia y asegurar que los servicios inyectados se gestionen correctamente en cuanto a ciclo de vida y dependencia.

¿Cómo se pueden manejar excepciones en un servicio REST utilizando ApiResponse?
Utilizando un ExceptionMapper para capturar excepciones y retornar una instancia de ApiResponse con el mensaje de error y el código de estado HTTP correspondiente.