# Componentes Serverless

- Streams (charts [unidad de medida])
    Para proyectos de Data o RealTime (Es una secuencia de eventos que pueden ser procesados una vez que ocurren.) pueden ser millones de eventos
- Cola: Metodo para retrasar el trabajo, utilizadas pra desacoplar un elemento de un sistema.
- Bucket: Es una estructura para almacenar y consultar objetos; costo depende cantidad de informacion que almacena y sus request.
- API es la puerta de entrada a la aplicacion comunicando entre deficiones y protocolos.
- DataStore: Espacio para almanecenar informacion
- Servicios de Identidad: Implementa administracion de acceso e identidad de los usuarios.
- Motor de Consulta: consultar una query a fuente de datos y cobran por la cantidad de data que escanearon.
- Balanceadores de Carga:Componente que distribuye el tráfico entre varios destinos, existen balanceadores de apps(capa 7) y de red (capa 3 y 4)
