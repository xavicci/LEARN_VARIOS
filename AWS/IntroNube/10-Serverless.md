# SERVERLESS

Es la idea de que se puede ejecutar una aplicacion basada en servidor sin la necesidad de administrar un servidor.

Ventajas:
    - Escalabilidad, Seguridad y Fiabilidad: No tiene que planificar para capacidad futura
    - Los servicios tienen escalabilidad (considerar las cuotas de los cloud providers)
    - Pago por uso:
        - No se paga por tiempo de in por lo que se usa.
    - Ahorro de tiempo y dinero administrando servidores.
        - No gastar tiempo en administracion de servidores
        - Enfóquese en el código de su aplicacion
    - Mejora la productividad del desarrollador (facilitan entornos de desarrollo simples)

Retos:
    - Tiempo de Inicio frío. (pueden demorar 2 o 3 segundos en despertarse)
    - Tiempo de computo. (dependiendo del provedor cloud las funciones tienen un tiempo de vida de 15 minutos)
    - Conectividad: Su escalabilidad depende del consumo de direcciones IP. (ejecutar funciones fuera de ella para tener mas flexibilidad)
    - Vendor Lock-In: las funciones y los servicios no funcionan igual en todos los cloud providers.