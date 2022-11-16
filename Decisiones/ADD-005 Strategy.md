# Strategy
  - Estatus: Aceptado
  - Fecha: 2022-11-08

## Requisitos 

[RF-10]

## Descripción

Es un patrón de diseño de comportamiento que te permite definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables.


## Alternativas

   - State

## Argumentación



## Consecuencias Positivas

   - **Puedes intercambiar algoritmos usados dentro de un objeto durante el tiempo de ejecución.
   - **Puedes aislar los detalles de implementación de un algoritmo del código que lo utiliza.
   - Puedes sustituir la herencia por composición.
   - **Principio de abierto/cerrado**: Puedes introducir nuevas estrategias sin tener que cambiar el contexto.

## Consecuencias Negativas
   - **
