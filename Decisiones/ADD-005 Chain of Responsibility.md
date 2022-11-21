# Chain of Responsibility
  - Estatus: Aceptado
  - Fecha: 2022-11-16

## Requisitos 

[RF-08]

## Descripción

Es un patrón de diseño de comportamiento que te permite pasar solicitudes a lo largo de una cadena de manejadores. Al recibir una solicitud, cada manejador decide si la procesa o si la pasa al siguiente manejador de la cadena. Básicamente, este patrón ayuda a encapsular acciones secuenciales sobre un objeto.

## Argumentación

Hemos elegido el patrón de Chain of Responsibility porque el primer sensor envía información al segundo y este al tercero que finalmente lo envía al centro de notificaciones siendo esto acciones secuenciales, de manera que te permite que los sensores pasen información al siguiente.

## Consecuencias Positivas

   - **Controlable**: Puedes controlar el orden de control de solicitudes.
   - **Principio de responsabilidad única**: Puedes desacoplar las clases que invoquen operaciones de las que realicen operaciones.
   - **Principio de abierto/cerrado**: Puedes introducir nuevos manejadores en la aplicación sin descomponer el código cliente existente.

## Consecuencias Negativas
   
   - Algunas solicitudes pueden acabar sin ser gestionadas.
