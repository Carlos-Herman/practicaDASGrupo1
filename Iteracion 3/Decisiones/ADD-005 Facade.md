# Facade
  - Estatus: Acepatdo
  - Fecha: 2022-11-16

## Requisitos 

[RF-01]

## Descripción

Este patrón se utiliza para proporcionar una interfaz unificada de alto nivel para un conjunto de clases en un subsistema, lo que permite una mayor facilidad de uso. Simplifica el acceso a dicho conjunto de clases, ya que el cliente sólo se comunica con ellas a través de una única interfaz.

## Argumentación

Necesitamos un componente de visualización de datos, y ya que el patrón facade nos ofrece una interfaz simplificada de un conjunto de datos complejo, al añadirle una función "-mostrar()", podríamos ocultar la información que no sea necesaria a la hora de visualizar datos y por el contrario, mostrar todos aquellos datos que veamos necesarios.

## Consecuencias Positivas

   - Al separar al cliente de los componentes del subsistema, se reduce el número de objetos con los que el cliente trata, facilitando así el uso del subsistema.
   - Se promueve un acoplamiento débil entre el subsistema y sus clientes, eliminándose o reduciéndose las dependencias.
   - No existen obstáculos para que las aplicaciones usen las clases del subsistema que necesiten. De esta forma podemos elegir entre facilidad de uso y generalidad.
   - Puedes aislar tu código de la complejidad de un subsistema.

## Consecuencias Negativas
   
   - Se tiene considerar el caso en que varios clientes necesiten acceder a subconjuntos diferentes de la funcionalidad que provee el sistema, podrían acabar usando sólo una pequeña parte de la fachada, por lo que sería conveniente utilizar varias fachadas más específicas en lugar de una única global.
