# Strategy
  - Estatus: Aceptado
  - Fecha: 2022-11-16

## Requisitos 

[RF-10]

## Descripción

Es un patrón de diseño de comportamiento que te permite definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables.


## Alternativas

   - State

## Argumentación

Hemos propuesto el patrón Strategy ya que debemos poder definir dos tipos de algoritmos y hacer que el sistema elija cuál de ellos utilizar en cada momento. Por tanto, a nuestro parecer este es el que mejor le vendría este patrón, ya que podemos definir una serie de familias de algoritmos y hacerlos de manera independiente al ser dos clases separadas y después seleccionar el algoritmo más adecuado.

## Consecuencias Positivas

   - **Intercambiables**: Puedes intercambiar algoritmos usados dentro de un objeto durante el tiempo de ejecución.
   - **Aislables**: Puedes aislar los detalles de implementación de un algoritmo del código que lo utiliza.
   - **Sustituibles**: Puedes sustituir la herencia por composición.
   - **Principio de abierto/cerrado**: Puedes introducir nuevas estrategias sin tener que cambiar el contexto.
   - **Ahorro en memoria**: El cliente no va a necesitar todas las estrategias en todo momento, de modo que no necesitamos cargar un objeto con toda esa lógica dentro cada vez que queramos usarlo.
   - **Reutilización**: La misma estrategia puede usarse en diferentes contextos, evitando la duplicidad del código.

## Consecuencias Negativas
   - Si solo tenemos un par de estrategias a implementar, puede ser un poco exagerado o excesivo implementar este patrón, ya que complicamos en exceso la casuística.
   - El cliente debe de conocer las diferencias entre las estrategias.
