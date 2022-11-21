# Communication Broker
  - Estatus: Aceptado
  - Fecha: 2022-11-06

## Requisitos 

[RF-11]

## Descripción

Es un software que permite a las aplicaciones, sistemas y servicios comunicarse entre sí e intercambiar información. Es un mecanismo mediador de la comunicación entre aplicaciones, permitiendo minimizar el grado de conocimiento mutuo que estas aplicaciones necesitan tener, para poder intercambiar mensajes, implementando así efectivamente su desacoplamiento.

## Argumentación

Hemos propuesto esta solución, ya que es la manera más efectiva de asegurar que los sensores, el procesador de eventos y el cockpit se comuniquen de manera efectiva. De manera que se pueden comunicar e intercambiar información sin la necesidad de conocer a los demás.

## Consecuencias Positivas

   - **Acoplamiento débil**: El cliente realiza una solicitud y no necesita conocer los otros servicios, por lo que no necesita usar un mecanismo de descubrimiento para encontrar la ubicación de las otras instancias de servicio.
   - Comunicación más flexible

## Consecuencias Negativas
   
   - **Posible cuello de botella de rendimiento**: Podría ser un cuello de botella de rendimiento. 
   - **Punto de fallo potencial**: Debe estar accesible continuamente. 
   - **Complejidad operativa adicional**: Communication Broker es otro componente de un sistema que debe instalarse, configurarse y mantenerse.
