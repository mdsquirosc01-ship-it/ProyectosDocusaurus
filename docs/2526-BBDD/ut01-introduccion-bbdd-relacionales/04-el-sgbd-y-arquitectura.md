---
title: El SGBD y su Arquitectura
sidebar_position: 4
description: Estudio del Sistema de Gestión de Bases de Datos, sus funciones y la arquitectura ANSI/SPARC.
---

El **Sistema de Gestión de Bases de Datos (SGBD)** o DBMS es el software que actúa como interfaz entre los datos, los usuarios y las aplicaciones. Sin él, estaríamos de vuelta en el caos de los sistemas de ficheros.

## Funciones Principales del SGBD

Un SGBD profesional (como MySQL) debe cumplir estas funciones críticas:

*   **Definición de datos:** Permitir especificar tipos de datos y estructuras.
*   **Manipulación de datos:** Atender las consultas de los usuarios de forma eficiente.
*   **Gestión de Transacciones:** Asegurar que las operaciones se realicen por completo o no se realicen (propiedades ACID).
*   **Control de Concurrencia:** Evitar que dos usuarios modifiquen el mismo dato al mismo tiempo y generen errores.
*   **Seguridad y Recuperación:** Proteger los datos ante accesos no autorizados y fallos del sistema (backups).

## Arquitectura de Tres Niveles (ANSI/SPARC)

Para lograr la ansiada **independencia de datos**, la arquitectura estándar divide el sistema en tres capas:

1.  **Nivel Externo (Vistas):** Es lo que ve el usuario o la aplicación. Solo se muestra la parte de la base de datos que le interesa.
2.  **Nivel Conceptual:** Es la visión global de toda la base de datos. Define qué datos se almacenan y sus relaciones (el esquema lógico).
3.  **Nivel Interno (Físico):** Define cómo se almacenan físicamente los datos, qué índices se crean y cómo se gestiona el espacio en disco.

:::info Separación de Responsabilidades
Gracias a esta arquitectura, puedes cambiar el servidor físico (Nivel Interno) sin que la aplicación de Android (Nivel Externo) tenga que cambiar ni una sola línea de código.
:::

## Estructura de un SGBD

Internamente, un SGBD es una pieza de ingeniería compleja que incluye:
*   **Procesador de consultas:** Optimiza y ejecuta tus sentencias SQL.
*   **Gestor de almacenamiento:** Gestiona el espacio en disco y el acceso a los ficheros.
*   **Gestor de transacciones:** Garantiza que los datos se mantengan consistentes incluso si se va la luz en medio de una operación.
