# Base de Datos MySQL
  - Estatus: Propuesto
  - Fecha: 2022-11-20

## Requisitos 

[RF-04]

## Descripción

Es un sistema de gestión de bases de datos relacionales de código abierto con un modelo cliente-servidor. Esto quiere decir que la información se encuentra centralizada en un servidor (normalmente tu hosting) que recibe y procesa las peticiones. Estas peticiones son realizadas por los diferentes clientes (usuarios que realizan consultas a la base de datos a través de herramientas como phpMyAdmin, por ejemplo) en forma de sentencias SQL.

## Argumentación

Hemos propuesto MySQL como base de datos ya que hemos podido trabajar más con este tipo de base de datos y al ser gratuita y de uso libro podemos encontrar mucha documentación al respecto.

## Alternativas

   - MariaDB
   - Oracle Database

## Consecuencias Positivas

   - MySQL es de uso libre y gratuito.
   - Bajo costo en requerimientos para la elaboración y ejecución del programa.
   - No se necesita disponer de Hardware o Software de alto rendimiento para la ejecución del programa.
   - Velocidad al realizar las operaciones y buen rendimiento.
   - Facilidad de instalación y configuración.
   - Soporte en casi el 100% de los sistemas operativos actuales.
   - Baja probabilidad de corrupción de datos.
   - Entorno con seguridad y encryptación.

## Consecuencias Negativas
   
   - Al ser de Software Libre, muchas de las soluciones para las deficiencias del software no están documentados ni presentan documentación oficial.
   - Muchas de sus utilidades tampoco presentan documentación.
   - Se debe controlar/monitorizar el rendimiento de las aplicaciones en búsca de fallos.
   - No es el más intuitivo de los programas que existen actualmente para todos los tipos de desarrollos.
   - No es tan eficaz en aplicaciones que requieran de una constante modificación de escritura en BD.
