---
title: Roles y Gestión
sidebar_position: 5
description: Perfiles profesionales en el mundo de las bases de datos y responsabilidades del DBA.
---

En un entorno corporativo, la gestión de los datos no recae sobre una sola persona. Existen roles diferenciados con responsabilidades muy específicas.

## El Administrador de la Base de Datos (DBA)

El **DBA** es el responsable técnico del SGBD. Su trabajo es asegurar que el motor de base de datos funcione como un reloj suizo.

### Funciones del DBA:
*   **Instalación y configuración** del software del SGBD.
*   **Optimización del rendimiento (Tuning):** Crear índices y ajustar parámetros para que las consultas sean rápidas.
*   **Seguridad:** Gestión de usuarios, roles y permisos.
*   **Backup y Recovery:** Diseñar planes ante desastres para no perder nunca la información.

## Administración de Datos vs. BBDD

Es común confundir estos términos, pero operan en niveles distintos:
*   **Administración de Datos:** Es un rol más organizativo. Decide **qué** datos son necesarios para la empresa y define las reglas de negocio (ej: "un cliente no puede comprar sin DNI").
*   **Administración de BBDD (DBA):** Es un rol técnico. Se encarga de **cómo** implementar y mantener esos datos de forma eficiente en el servidor.

## Usuarios de las Bases de Datos

No todos los que interactúan con una BD tienen el mismo nivel técnico:

1.  **Usuarios Ingenuos (Finales):** Interactúan a través de una aplicación (ej: alguien usando Instagram). No saben que hay una BD detrás.
2.  **Usuarios Sofisticados:** Saben realizar consultas directas para obtener informes, pero no programan aplicaciones.
3.  **Programadores de aplicaciones:** Nosotros. Escribimos código (Java, Kotlin, Python) que se comunica con el SGBD mediante SQL.
4.  **Administradores (DBA):** Los "dueños" del sistema.

:::tip Motivación
Como desarrollador de DAM, tu rol principal será el de **Programador de aplicaciones**, pero entender las tareas del **DBA** te hará escribir código mucho más eficiente y escalable.
:::
