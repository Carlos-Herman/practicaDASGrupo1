# Factory Method
  - Estatus: Rechazado
  - Fecha: 2022-11-08

## Requisitos 

[RF-05]

## Descripción

Es un patrón de diseño creacional que proporciona una interfaz para crear objetos en una superclase, mientras permite a las subclases alterar el tipo de objetos que se crearán.

## Alternativas

   - Abstract Factory

## Argumentación

Hemos pensado que podemos utilizar el Factory Method porque con la superclase podemos tener las funcionalidades compartidas y después los diferentes tipos de sensores siendo estos las subclases heredarían las funcionalidades y a parte estas podrían tener las suyas propias.

## Consecuencias Positivas

   - **Flexibilidad**: Crear los objetos dentro de una clase con un "Método de Fábrica" es siempre más flexible que hacerlo directamente, debido a que se elimina la necesidad de atar nuestra aplicación unas clases de productos concretos.
   - **Facilitan futuras ampliaciones**: Puesto que se ofrece las subclases la posibilidad de proporcionar una versión extendida de un objeto, con sólo aplicar en los Productos la misma idea del "Método de Fábrica".
   - **Conexión entre jerarquías de clases paralelas**: Son aquellas que se generan cuando una clase delega algunas de sus responsabilidades en una clase aparte. Ambas jerarquías de clases paralelas son creadas por un mismo cliente y el patrón Método de Fábrica establece la relación entre parejas de subclases concretas en las mismas.

## Consecuencias Negativas

   - **Desarrollo**: Puede ser que el código se complique, ya que debes incorporar una multitud de nuevas subclases para implementar el patrón. La situación ideal sería introducir el patrón en una jerarquía existente de clases creadoras.
   - **Subclases**: Se obliga al cliente a definir subclases de la clase "Creador" sólo para crear un producto concreto y esto puede no ser apropiado siempre.

