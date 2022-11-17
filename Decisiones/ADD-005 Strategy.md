# Strategy
  - Estatus: Propuesto
  - Fecha: 2022-11-16

## Requisitos 

[RF-10]

## Descripción

Es un patrón de diseño de comportamiento que te permite definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables.


## Alternativas

   - State

## Argumentación



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
