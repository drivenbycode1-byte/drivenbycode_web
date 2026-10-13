# Infraestructura de DrivenByCode

**Arquitectura tecnológica, servicios digitales y principios de desarrollo.**

Este documento presenta la arquitectura tecnológica de DrivenByCode, las herramientas que forman parte de su ecosistema digital y las relaciones entre sus principales componentes.

DrivenByCode combina desarrollo de software, documentación técnica y una historia de reconstrucción personal. Su infraestructura representa la base sobre la que evoluciona el proyecto: una estructura que debe ser comprensible, mantenible y adaptable a nuevas necesidades.

> La forma cambia, el propósito se afina.

---

## Índice

* [1. Visión general](#1-visión-general)
* [2. Componentes tecnológicos](#2-componentes-tecnológicos)
* [3. Dominio y comunicaciones](#3-dominio-y-comunicaciones)
* [4. Protección de marca](#4-protección-de-marca)
* [5. Mapa de relaciones](#5-mapa-de-relaciones)
* [6. Seguridad y mantenimiento](#6-seguridad-y-mantenimiento)
* [7. Evolución de la infraestructura](#7-evolución-de-la-infraestructura)
* [8. Filosofía del proyecto](#8-filosofía-del-proyecto)

---

## 1. Visión general

La infraestructura de DrivenByCode reúne las herramientas necesarias para desarrollar, mantener y publicar sus componentes digitales.

La arquitectura documentada contempla las siguientes áreas:

* Control de versiones y gestión del código.
* Desarrollo de aplicaciones web.
* Backend y lógica de aplicación.
* Interfaces web.
* Servicios de alojamiento y despliegue.
* Administración del dominio.
* Comunicación profesional.
* Documentación y protección de la identidad de marca.

Los componentes descritos representan la arquitectura prevista o documentada del proyecto. Su implementación efectiva debe verificarse antes de considerar cada relación como operativa.

---

## 2. Componentes tecnológicos

### 2.1. GitHub

**Función:** control de versiones y gestión del código fuente.

GitHub permite mantener el historial de cambios, organizar el desarrollo y documentar la evolución de los componentes de software.

También puede utilizarse para automatizar procesos de integración y despliegue cuando existe una configuración compatible.

La visibilidad de los repositorios se determina de forma independiente según las necesidades de cada proyecto.

### 2.2. Render

**Función:** alojamiento y ejecución de aplicaciones y servicios web.

Render puede utilizarse para alojar el backend de DrivenByCode y ejecutar la aplicación en un entorno accesible desde Internet.

Cuando está configurada la integración correspondiente, los cambios publicados en un repositorio pueden iniciar procesos automáticos de despliegue.

La conexión entre GitHub y Render depende de la configuración concreta del servicio.

### 2.3. Django

**Función:** desarrollo del backend.

Django es un framework de Python que permite desarrollar aplicaciones web, gestionar solicitudes, definir rutas y conectar la lógica de negocio con los datos de una aplicación.

Dentro de DrivenByCode, puede encargarse de las funcionalidades del servidor y de generar respuestas para las interfaces y los consumidores de la API.

La implementación real depende de la versión y de la estructura del proyecto.

### 2.4. Frontend: HTML, CSS y JavaScript

**Función:** presentación e interacción con las personas usuarias.

HTML proporciona la estructura de las páginas, CSS define su presentación visual y JavaScript permite incorporar interactividad cuando es necesario.

La interfaz puede comunicarse con el backend para consultar o enviar información mediante los mecanismos definidos por la aplicación.

### 2.5. API

**Función:** comunicación entre componentes de software.

Una API permite que distintos componentes intercambien información mediante una interfaz definida.

En una aplicación Django, estos endpoints pueden formar parte del propio backend o implementarse mediante componentes adicionales.

Las rutas, los métodos HTTP, los formatos de respuesta y los mecanismos de autenticación deben documentarse según la implementación real.

No se publicarán detalles internos que puedan comprometer la seguridad de la aplicación.

---

## 3. Dominio y comunicaciones

### 3.1. NIC Chile

**Función:** gestión del dominio `.cl`.

NIC Chile es la entidad asociada al registro de dominios bajo la extensión `.cl`.

El dominio `drivenbycode.cl` constituye una parte central de la identidad digital del proyecto.

El registro de un dominio y su configuración técnica son funciones distintas: el registro identifica la titularidad del dominio, mientras que la configuración DNS determina cómo se resuelven sus servicios.

### 3.2. Hostinger

**Función:** servicios de alojamiento o gestión de DNS, según la configuración contratada.

Hostinger puede intervenir en la administración de los registros DNS o en otros servicios asociados al dominio.

Los registros concretos deben verificarse en la configuración vigente.

La resolución DNS no equivale necesariamente a una redirección web: los registros DNS indican a qué infraestructura deben dirigirse las consultas, mientras que las redirecciones HTTP se configuran mediante los servicios que las gestionan.

### 3.3. Google Workspace

**Función:** correo electrónico y herramientas de productividad.

Google Workspace puede proporcionar servicios de correo corporativo asociados al dominio.

La entrega del correo depende de la configuración de los registros DNS correspondientes, incluidos los registros MX y las configuraciones de autenticación del correo cuando proceda.

Los valores de configuración deben mantenerse actualizados de acuerdo con las instrucciones del proveedor.

---

## 4. Protección de marca

### INAPI

**Función:** gestión de la protección de la propiedad industrial en Chile.

INAPI es el Instituto Nacional de Propiedad Industrial de Chile.

La documentación de DrivenByCode puede registrar información general sobre la situación de la marca y sus antecedentes administrativos, cuando corresponda.

El alcance de la protección depende del estado efectivo del trámite o registro, de las clases pertinentes y de la normativa aplicable.

La mención de INAPI en este documento no constituye por sí sola una acreditación de registro vigente ni implica que todos los elementos de la identidad estén protegidos de manera automática.

Los antecedentes legales y administrativos que no se desee divulgar deberán mantenerse fuera de los repositorios públicos.

---

## 5. Mapa de relaciones

El siguiente mapa resume las relaciones funcionales que pueden existir entre los componentes del proyecto.

| Origen           | Destino             | Función                                                                                        |
| ---------------- | ------------------- | ---------------------------------------------------------------------------------------------- |
| GitHub           | Render              | Integración y despliegue, cuando están configurados.                                           |
| Render           | Django              | Ejecución de la aplicación backend.                                                            |
| Django           | API                 | Exposición de endpoints, cuando están implementados.                                           |
| Frontend         | API                 | Intercambio de información con el backend.                                                     |
| Frontend         | Navegador           | Presentación e interacción con la interfaz.                                                    |
| NIC Chile        | Dominio `.cl`       | Registro y administración del dominio.                                                         |
| DNS              | Servicios asociados | Resolución del dominio hacia los destinos configurados.                                        |
| Google Workspace | Dominio             | Servicios de correo y productividad asociados.                                                 |
| INAPI            | Marca               | Tramitación y protección de derechos de propiedad industrial, según el estado correspondiente. |

Este mapa describe relaciones funcionales generales. No sustituye un diagrama de despliegue ni acredita que todas las conexiones estén activas en el entorno productivo.

---

## 6. Seguridad y mantenimiento

La infraestructura de DrivenByCode debe evolucionar siguiendo buenas prácticas de desarrollo y administración.

### Principios de seguridad

* No almacenar contraseñas ni claves privadas en repositorios públicos.
* Utilizar variables de entorno para gestionar secretos de configuración.
* Revisar los permisos de acceso a los repositorios y servicios.
* Mantener actualizadas las dependencias.
* Configurar adecuadamente los dominios permitidos y los orígenes de confianza.
* Utilizar HTTPS para las comunicaciones públicas.
* Revisar los registros de aplicación y los errores de despliegue.
* Evitar publicar configuraciones internas que no sean necesarias para comprender el proyecto.

### Configuración de Django

Cuando Django se utiliza en producción, deben revisarse, entre otros aspectos:

* `ALLOWED_HOSTS`.
* `CSRF_TRUSTED_ORIGINS`, cuando corresponda.
* `DEBUG` desactivado.
* Gestión segura de `SECRET_KEY`.
* Configuración HTTPS y de los encabezados de proxy cuando exista un proxy inverso.
* Políticas de autenticación y autorización.
* Gestión de errores y registros.

Los valores concretos no se publican en este documento. Deben definirse según la infraestructura real y las recomendaciones oficiales de Django y del proveedor de alojamiento.

---

## 7. Evolución de la infraestructura

### 15 de septiembre de 2025 — Resolución de un problema de acceso en producción

Según el registro de desarrollo del proyecto, durante esta fecha se trabajó en la resolución de un error HTTP 400 al acceder a la aplicación mediante el dominio personalizado.

Las tareas documentadas incluyeron ajustes relacionados con:

* Dominios permitidos en Django.
* Orígenes de confianza para solicitudes protegidas por CSRF.
* Encabezados de proxy y reconocimiento de HTTPS.

El objetivo fue restablecer el acceso correcto a la aplicación mediante el dominio oficial.

Este antecedente constituye un registro histórico de desarrollo. No implica que la configuración actual sea idéntica ni que todos los componentes hayan permanecido sin cambios desde esa fecha.

---

## 8. Filosofía del proyecto

La infraestructura no es únicamente un conjunto de servicios.

Es la base que permite transformar una idea en una aplicación, mantener el trabajo organizado y documentar las decisiones que acompañan su evolución.

Cada componente cumple una función. Cada decisión técnica debe responder a una necesidad. Cada cambio debería contribuir a que el proyecto sea más comprensible, seguro y sostenible.

DrivenByCode conecta esa dimensión técnica con una experiencia personal de reconstrucción, aprendizaje y transformación.

La tecnología aporta herramientas; la documentación conserva el conocimiento; la reflexión permite comprender el propósito.

**No se trata solo de construir algo que funcione, sino de entender cómo está construido y por qué existe.**

---

*DrivenByCode — La forma cambia, el propósito se afina.*
