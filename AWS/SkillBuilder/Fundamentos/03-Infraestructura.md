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

## 