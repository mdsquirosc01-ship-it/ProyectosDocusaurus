---
title: Contexto y Evolución de las Bases de Datos
sidebar_position: 1
description: Breve historia del almacenamiento de información y la transición de sistemas de ficheros a bases de datos.
---

En el mundo del desarrollo de software, los datos son el activo más valioso. Como futuro desarrollador, no basta con saber programar lógica; debes entender dónde y cómo reside esa información de forma segura, eficiente y escalable.

## Introducción a las Bases de Datos

Una **Base de Datos (BBDD)** es una colección organizada de datos relacionados entre sí, almacenados sistemáticamente para facilitar su uso posterior. 

Pero no pienses solo en "tablas". Una base de datos es el corazón de casi cualquier sistema: desde la lista de contactos de tu móvil hasta el inventario global de Amazon. Su importancia radica en que permite transformar datos aislados en **información** útil para la toma de decisiones.

## Evolución Histórica

La forma en que almacenamos información ha cambiado drásticamente conforme aumentaba nuestra capacidad de cómputo:

*   **Años 50 - 60 (Era de las Tarjetas Perforadas):** El almacenamiento era secuencial y físico. No existía el concepto de "consulta" aleatoria; había que leer todo desde el principio.
*   **Años 60 (Modelo Jerárquico y de Red):** Aparecen las primeras estructuras. Los datos se organizaban en árboles o grafos, pero eran extremadamente rígidos: si la estructura cambiaba, había que reescribir todo el código de acceso.
*   **Años 70 (El Modelo Relacional):** Edgar F. Codd (IBM) publica las reglas del modelo relacional. Se separa la estructura física de la lógica. Es el nacimiento de las tablas y el lenguaje SQL.
*   **Años 90 - Actualidad (BBDD Orientadas a Objetos y NoSQL):** Con la explosión de la web y el Big Data, surgieron necesidades que el modelo relacional no cubría bien (escalabilidad horizontal masiva, datos no estructurados), dando paso a MongoDB, Cassandra o Redis.

## Sistemas de Ficheros vs. BBDD

Antes de las BBDD modernas, se utilizaban **Sistemas de Ficheros** tradicionales (archivos .txt, .csv, o formatos binarios propios). Aunque para un script sencillo pueden bastar, en aplicaciones empresariales presentan problemas críticos:

### 1. Redundancia e Inconsistencia
En los ficheros, los datos suelen repetirse en diferentes lugares. 
> [!CAUTION]
> Si cambias el teléfono de un cliente en el fichero de "Ventas" pero olvidas hacerlo en el de "Facturación", tienes **inconsistencia de datos**.

### 2. Dificultad en el Acceso
Si quieres obtener "los clientes que compraron más de 500€ en martes", en un sistema de ficheros tendrías que programar un algoritmo completo de búsqueda. En una BBDD, solo necesitas una línea de SQL.

### 3. Aislamiento de los Datos
Los datos están repartidos en ficheros con formatos distintos. Es muy difícil cruzar información entre ellos sin escribir código complejo.

### 4. Problemas de Seguridad y Concurrencia
¿Qué pasa si dos usuarios intentan escribir en el mismo .txt a la vez? Los sistemas de ficheros no suelen gestionar bien el acceso simultáneo, lo que puede corromper los datos.

:::tip Conclusión
Las Bases de Datos surgieron para solucionar todos estos problemas, proporcionando una capa de abstracción que nos permite olvidarnos de **cómo** se guardan los bits y centrarnos en **qué** información necesitamos.
:::
