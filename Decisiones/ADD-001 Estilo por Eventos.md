# Estilo por Eventos
  - Estatus: Aceptado
  - Fecha: 2022-11-08

## Requisitos 

[RF-02], [RF-03], [RF-09]

## Descripción

Está compuesta por productores y consumidores de eventos. Una vez que se detecta un evento, este se transmite a una plataforma donde se procesa de manera asíncrona para procesar los eventos. La plataforma de procesamiento ejecutará la respuesta adecuada para el evento y enviará la actividad a los consumidores correspondientes.

## Alternativas

   - Estilo por Capas
   - Estilo Pipe and Filter

## Argumentación

Hemos tenido en cuenta el Estilo por Eventos porque según como está escrito nuestro problema es el que más cuadra. Ya que, tenemos el productor de eventos, en este caso serían los sensores. Los sensores envían datos al centro de notificaciones (Cockpit), funcionando como gestor de eventos. Finalmente, el Cockpit le envía órdenes a las diferentes máquinas y trabajadores.

## Consecuencias Positivas

   - **Escalabilidad**: La escalabilidad es uno de los puntos más fuertes de esta arquitectura, pues permite que cada consumidor (Event Consummer) puede escalar de forma independiente y reduce al máximo el acoplamiento entre los componentes.

   - **Despliegue**: Debido al bajo acoplamiento entre los componentes, es posible el despliegue sin preocuparse por dependencias o precondiciones, al final, los componentes solamente se suscriben para recibir eventos y reaccionar ante ellos.
   
   - **Performance**: Esta es que ventaja cuestionable, ya que al igual que en REST o SOA, EDA necesita pasar por una serie de pasos para completar una tarea, agregando retrasos en cada paso, desde colocar el Evento por parte del productor, esperar a que el consumidor lo tome, y generar nuevos Eventos, sin embargo, la naturaleza Asíncrona de EDA hace que esta desventaja se supere mediante el procesamiento en paralelo.

   - **Flexibilidad**: EDA permite responder rápidamente a un entorno cambiante, debido a que cada componente procesador de eventos tiene una sola responsabilidad y está completamente desacoplado de los demás, de esta forma, si ocurre un cambio, se puede aislar en un solo componente sin afectar al resto, además, si un nuevo requerimiento es requerido, solo es necesario regresar un nuevo tipo de procesador de eventos que escuche un determinado tipo de evento.
   
## Consecuencias Negativas
   - **Testabilidad**: Una arquitectura distribuida y asíncrona agrega cierta complejidad a las pruebas, pues no es posible generar un evento y esperar un resultado para validar el resultado, en su lugar, es necesario crear pruebas más sofisticadas que creen los eventos y esperen la finalización del procesamiento del evento inicial más toda la serie de eventos que se podrían generar como consecuencia del evento inicial para validar el resultado final.
   
   - **Desarrollo**: Codificar soluciones asíncronas es complicado, pero aún más, es la necesidad de crear manejadores de errores más avanzados que permitan recuperarse en una arquitectura asíncrona, donde la falla en un procesador no significa la falla en el resto, lo que puede ocasionar la inconsistencia entre los sistemas.
