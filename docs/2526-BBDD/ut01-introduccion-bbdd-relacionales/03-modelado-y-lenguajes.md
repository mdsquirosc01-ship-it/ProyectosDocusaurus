---
title: Modelado y Lenguajes
sidebar_position: 3
description: Introducción a los modelos de datos, su clasificación y los lenguajes de interacción con la BD.
---

Como desarrollador, raramente interactuarás directamente con los bits en el disco. En su lugar, trabajarás con diferentes niveles de abstracción para representar la realidad mediante modelos.

## Modelos de Datos

Un **modelo de datos** es un conjunto de herramientas conceptuales para describir los datos, sus relaciones, su semántica y sus restricciones. No todos los modelos son iguales; dependen del momento del diseño en el que te encuentres.

### Niveles de Abstracción
Para que el diseño sea robusto, seguimos tres niveles (de más abstracto a más técnico):

1.  **Nivel Conceptual:** Describe "qué" datos se almacenan y qué relaciones existen. Es independiente de la tecnología. El estándar es el **Modelo Entidad-Relación (E/R)**.
2.  **Nivel Lógico:** Adapta el modelo conceptual a un tipo de tecnología (ej: relacional, documental). Aquí es donde hablamos de tablas, filas y columnas.
3.  **Nivel Físico:** Describe "cómo" se guardan los datos en el almacenamiento (índices, estructuras de ficheros). De esto suele encargarse el SGBD automáticamente.

## Clasificación de Modelos

A lo largo de la historia han coexistido varios enfoques:

*   **Modelos Clásicos (Jerárquicos y en Red):** Datos organizados en padres/hijos o grafos. Muy rápidos pero muy rígidos.
*   **Modelo Relacional:** El estándar actual (MySQL, PostgreSQL). Los datos se ven como tablas bidimensionales. Su gran ventaja es la simplicidad matemática.
*   **Modelos NoSQL:** Documentales (JSON), Clave-Valor o Grafos. Ideales para grandes volúmenes de datos no estructurados.

## Lenguajes de Bases de Datos

Para comunicarte con el sistema, utilizarás lenguajes especializados. En el mundo relacional, el estándar es **SQL**, que se divide en tres sublenguajes:

### 1. DDL (Data Definition Language)
Sirve para definir o modificar la **estructura** de la base de datos (el "contenedor").
*   Comandos clave: `CREATE`, `ALTER`, `DROP`.

### 2. DML (Data Manipulation Language)
Sirve para gestionar los **datos** que hay dentro de las estructuras.
*   Comandos clave: `SELECT`, `INSERT`, `UPDATE`, `DELETE`.

### 3. DCL (Data Control Language)
Sirve para gestionar la **seguridad** y los permisos.
*   Comandos clave: `GRANT`, `REVOKE`.

:::tip Clave Pedagógica
Recuerda: Si vas a crear una tabla, usas **DDL**. Si vas a meter un cliente en esa tabla, usas **DML**.
:::
