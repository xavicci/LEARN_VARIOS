ESCALABILIDAD: es la capacidad de incrementar o decrementar los recursos necesarios para complir la demanda cambiante en una aplicación o servicio.
Crecer y decrecer basado en la demanda que recibe nuestra aplicación.
Ejemplo: descuentos por pago en Black Friday. Entonces, los servicios que reciben pago crezcan y soporten al incremento de la cantidad de usuarios por la oferta y luego de pasada la oferta estos mismos servicios decrecen.

ESCALABILIDAD VERTICAL: es la escalabilidad de añadir más recursos a un nodo particular dentro de un sistema. Hay una caída del servicio mientras se hace el cambio. Ejemplo: A un determinado servidor lo apago, le aumento los recursos (cpu, ram, disco) y lo vuelvo a prender. Luego tendré que apagarlos para volver a los recursos a sus niveles anteriores.
No cambia la cantidad de servidores. Hubo caída del servicio cuando lo apago.

ESCALABILIDAD HORIZONTAL: es la capacidad de agregar más nodos para soportar una demanda creciente de solicitudes en un sistema. Ejemplo: replicar servidores en el momento de más carga. No tenemos DOWNTIME (caída del servicio).

¿Sirve ESCALABILIDAD sin alta DISPONIBILIDAD?
La ESCALABILIDAD está en más de una ZONA. Porque si solo escalamos en una zona perdemos ALTA DISPONIBILIDAD.