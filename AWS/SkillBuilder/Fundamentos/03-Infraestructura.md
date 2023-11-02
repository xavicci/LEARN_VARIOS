Objetivos de aprendizaje

En este módulo aprenderás lo siguiente:

Resumir los beneficios de la infraestructura global de AWS.
Describir el concepto básico de zonas de disponibilidad.
Describir los beneficios de las ubicaciones perimetrales y Amazon CloudFront.
Comparar los distintos métodos de aprovisionamiento de los servicios de AWS.

# INFRAESTRUCTURA Y FIABILIDAD GLOBALES

## REGIONES

Conformidad con los requisitos legales y de gestión de datos: Según tu empresa y tu ubicación, es posible que tengas que ejecutar los datos en áreas específicas. Por ejemplo, si tu empresa requiere que todos tus datos se encuentren dentro de los límites del Reino Unido, elegiría la región de Londres. No todas las empresas tienen regulaciones de datos relacionadas con la ubicación, por lo que es posible que tengas que centrarte más en los otros tres factores.

Proximidad a tus clientes: Seleccionar una región cercana a tus clientes te ayudará a enviarles contenido más rápido. Por ejemplo, tu empresa tiene sede en Washington, DC, y muchos de tus clientes viven en Singapur. Puedes considerar la posibilidad de ejecutar tu infraestructura en la región de Virginia del Norte para estar cerca de la sede de la empresa y ejecutar tus aplicaciones desde la región de Singapur.

Servicios disponibles dentro de una región: A veces, es posible que la región más cercana no tenga todas las características que deseas ofrecer a los clientes. AWS innova con frecuencia creando nuevos servicios y ampliando las características de los servicios existentes. No obstante, para que los nuevos servicios puedan estar disponibles en todo el mundo, a veces es necesario que AWS desarrolle hardware físico región a región. 
Supongamos que tus desarrolladores quieren crear una aplicación que utilice Amazon Braket (plataforma de computación cuántica de AWS). En este curso, Amazon Braket aún no está disponible en todas las regiones de AWS del mundo, por lo que tus desarrolladores tendrían que ejecutarlo en una de las regiones que ya lo ofrecen.

Precios: Supongamos que estás pensando ejecutar aplicaciones tanto en Estados Unidos como en Brasil. Por cómo está establecida la estructura tributaria de Brasil, podría costar un 50 % más ejecutar la misma carga de trabajo en la región de São Paulo que en la región de Oregón. Sabrás con más detalle que varios factores determinan los precios, pero por ahora no olvides que el coste de los servicios puede variar de una región a otra.

También, al usar AWS te recomendamos que uses al menos dos zonas de disponibilidad de una región. Es decir, que implementes tu infraestructura de modo redundante en dos AZ diferentes. 

Además, las regiones son más que lugares para ejecutar EC2. Muchos de los servicios de AWS se ejecutan a nivel de región, es decir, se ejecutan de forma síncrona en varias AZ sin que tengas que hacer nada. Veámoslo con ELB, algo de lo que ya hemos hablado. Es un constructo regional. Se ejecuta en todas las AZ comunicándose con las instancias EC2 que se ejecutan en una zona de disponibilidad específica. Los servicios regionales son de por sí altamente disponibles sin coste adicional y sin que tengas que hacer nada. 

## Ubicaciones permitrales

si tienes clientes en Bombay que necesitan acceder a tus datos, pero los datos se alojan en la región de Tokio, en lugar de hacer que todos los clientes de Bombay envíen solicitudes a Tokio para acceder a los datos, es mejor tener una copia local o almacenarla en caché en Bombay. Para almacenar en caché copias de datos más cerca de los clientes en todo el mundo, se usan las redes de entrega de contenido (CDN). 

Las CDN se usan habitualmente y la nuestra se llama Amazon CloudFront. Amazon CloudFront es un servicio que ayuda a entregar datos, vídeo, aplicaciones y API a clientes de todo el mundo con baja latencia y altas velocidades de transferencia. Amazon CloudFront utiliza ubicaciones perimetrales (SON TEMPORALES PARA BRINDAR UN SERVICIO)en todo el mundo para acelerar la comunicación con los usuarios, sin importar dónde se encuentren. Además, son independientes de las regiones.

Las ubicaciones perimetrales de AWS no solo se usan con CloudFront. Utilizan un servicio de nombres de dominio, o DNS, conocido como Amazon Route 53. Ayudamos a dirigir a los clientes hacia las ubicaciones web correctas, con una latencia baja y fiable. 

Pero ¿qué pasa si tu empresa quiere usar servicios de AWS en sus instalaciones? Pues que pueden. AWS ofrece ese servicio. Se llama AWS Outposts y consiste en que AWS instala una miniregión totalmente operativa en el centro de datos de tu empresa. Es de AWS, que también la opera, con toda la funcionalidad de AWS, pero aislada en tus instalaciones. No es lo que la mayoría necesita, pero si tienes cuestiones específicas que solo se pueden resolver en tus instalaciones.

## Aprovisionar recursos

En AWS, todo es una llamada a API. Una API es una interfaz de programación de aplicaciones. Esto significa que hay modos predeterminados de interactuar con los servicios de AWS. Puedes invocar o hacer llamadas a estas API para aprovisionar, configurar y administrar recursos de AWS. 

Puedes usar la AWS Management Console, la interfaz de línea de comandos de AWS, los kits de desarrollo de software u otras herramientas, como AWS CloudFormation, para crear y enviar solicitudes a las API y, así, generar y gestionar recursos de AWS. 

Primero, hablemos de la AWS Management Console. Se basa en el navegador y con ella puedes administrar los recursos de AWS de forma visual y sencilla. Es ideal para empezar e ir aprendiendo sobre los servicios. También es útil para crear entornos de prueba, ver facturas de AWS o el seguimiento, y trabajar con otros recursos no técnicos. Esta consola será seguramente el primer lugar al que irás cuando estés aprendiendo sobre AWS. 

Sin embargo, cuando tengas en marcha un entorno de producción, es mejor no contar tanto con el estilo visual de la consola a la hora de crear y administrar tus recursos de AWS. Por ejemplo, para crear una instancia EC2, debes hacer clic en varias pantallas, definir la configuración que quieras y, después, lanzar la instancia. Si más tarde quieres lanzar otra instancia EC2, tendrías que volver a la consola y hacer clic de nuevo en esas pantallas para ponerla en marcha. Si el aprovisionamiento lo hacen personas manualmente, aumenta la probabilidad de que haya errores. Es muy fácil olvidarse de marcar una casilla de verificación o escribir mal algo cuando se hace todo manualmente. La solución es utilizar herramientas para crear scripts que hagan llamadas a la API o programarlas. Una de esas herramientas es AWS Command Line Interface (CLI). La CLI permite hacer llamadas a la API mediante el terminal de tu equipo. Es distinto del estilo de navegación visual de la AWS Management Console. Escribir comandos con la CLI permite crear acciones codificables y repetibles. Así, puedes escribir y usar comandos para lanzar una instancia EC2. Si quieres lanzar otra, puedes volver a usar el comando ya escrito. Esto reduce la probabilidad de que haya errores humanos.

La automatización es clave para que la implementación en la nube sea correcta y predecible a lo largo del tiempo. Otra forma de interactuar con AWS es a través de los kits de desarrollo de software (SDK) de AWS. Los SDK permiten interactuar con los recursos de AWS mediante lenguajes de programación. Esto facilita a los desarrolladores crear programas que utilizan AWS sin tener que usar las API de bajo nivel, y que no tengan que crear recursos manualmente como acabo de explicar.

AWS Elastic Beanstalk es un servicio que ayuda a aprovisionar entornos basados en Amazon EC2. En lugar de hacer clic en la consola o escribir varios comandos para crear las redes, instancias EC2, el escalado y Elastic Load Balancers, puedes proporcionar el código de tu aplicación y la configuración que quieras al servicio AWS Elastic Beanstalk, que, con esa información, crea el entorno. Con Elastic Beanstalk, también es fácil almacenar configuraciones del entorno para volver a implementarlas fácilmente. AWS Elastic Beanstalk ofrece la comodidad de no tener que aprovisionar y administrar todo esto por separado, al tiempo que permite ver y controlar los recursos subyacentes. Así, puedes centrarte en tus aplicaciones en lugar de en la infraestructura. 
Elastic Beanstalk implementa los recursos necesarios para realizar las siguientes tareas:

- Ajuste de la capacidad.
- Equilibrio de carga.
- Escalado automático.
- Seguimiento del estado de las aplicaciones.

Otro servicio que puedes usar para crear implementaciones automatizadas y repetibles es AWS CloudFormation. AWS CloudFormation es una herramienta de infraestructura como código que permite definir distintos recursos de AWS de forma declarativa mediante documentos basados en texto JSON o YAML, llamados plantillas de CloudFormation. Un formato declarativo como este te permite definir lo que quieres crear sin especificar los detalles de cómo crearlo. CloudFormation te permite definir qué quieres y el motor de CloudFormation se encarga de los detalles, y hace las llamadas a las API para crear lo que hayas definido. 

Además, no se limita a soluciones básicas de EC2. CloudFormation se puede usar con muchos recursos de AWS distintos como almacenamiento, bases de datos, análisis o machine learning. Una vez definidos los recursos en una plantilla de CloudFormation, CloudFormation la analizará y aprovisionará en paralelo estos recursos que has definido. CloudFormation gestiona las llamadas a las API del backend de AWS. Puedes utilizar la misma plantilla de CloudFormation en varias cuentas o regiones y creará entornos idénticos en ellas. Así, hay menos margen de error, ya que es un proceso automatizado. 
Amazon CloudFront es un servicio de entrega de contenido. Utiliza una red de ubicaciones perimetrales para almacenar y entregar contenido a clientes de todo el mundo. El contenido se almacena localmente como una copia. Este contenido puede consistir en archivos de vídeo, fotos, páginas web, etc.
