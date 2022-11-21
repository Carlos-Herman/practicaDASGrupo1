# Observer
  - Estatus: Aceptado
  - Fecha: 2022-11-08

## Requisitos 

[RF-07], [RF-06]

## Descripción

Es un patrón de diseño de comportamiento que te permite definir un mecanismo de suscripción para notificar a varios objetos sobre cualquier evento que le suceda al objeto que están observando.

## Alternativas

   - Publish-Suscribe

## Argumentación

Ya que las notificaciones solo tienen que llegar en momentos específicos (como a la hora de hacer el log-in) y no debe tener en cuenta el tipo de usuario, sino que notifica a todo aquel que esté suscrito al evento en cuestión.

## Consecuencias Positivas

   - **Principio abierto/cerrado**: Puedes modificar las clases que reciben las notificaciones sin necesidad de modificar al notificador.
   
   - **Fácil adición de relaciones entre objetos**
   
## Consecuencias Negativas
   - **Herencia**: El propio patrón te obliga a usar herencias al crear el notificador
   
   - **Complejidad**: En caso de tener un programa ya desarrollado y querer implementar un observer, la complejidad del software puede aumentar mucho.

   - **Fuga de memoria**: A la hora de añadir o quitar observadores, habría que hacerlo de manera explícita, lo que puede generar fugas de memoria.

   - **Aleatoriedad**: A la hora de notificar a los suscriptores, estas notificaciones llegarían en un orden aleatorio.
