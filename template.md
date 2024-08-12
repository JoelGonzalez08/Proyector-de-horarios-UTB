# Software Requirements Specification
## Proyector de horarios UTB

Version 0.1  
Prepared by <author>  
<organization>  
<date created>  

Table of Contents
=================
* [Revision History](#revision-history)
* 1 [Introducción](#1-introducción)
  * 1.1 [Propósito del documento](#11-proposito-del-documento)
  * 1.2 [Alcance del producto](#12-alcance-del-producto)
  * 1.3 [Definiciones, acrónimos y abreviaciones](#13-definiciones-acronimos-y-abreviaciones)
  * 1.4 [Referencias](#14-referencias)
  * 1.5 [Descripción general del documento](#15-descripcion-general-del-documento)
* 2 [Descripción general del producto](#2-descripcion-general-del-producto)
  * 2.1 [Perspectiva del producto](#21-perspectiva-del-producto)
  * 2.2 [Funciones del producto](#22-funciones-del-producto)
  * 2.3 [Características del usuario](#23-caracteristicas-del-usuario)
  * 2.4 [Supuestos y dependencias](#24-supuestos-y-dependencias)
  * 2.5 [Distribución de requisitos](#25-distribucion-de-requisitos)
* 3 [Requerimientos](#3-requerimientos)
  * 3.1 [Requerimientos funcionales](#31-requerimientos-funcionales)
  * 3.2 [Requerimientos no funcionales](#32-requerimientos-no-funcionales)
    * 3.2.1 [Rendimiento](#321-rendimiento)
    * 3.2.2 [Escalabilidad](#322-escalabilidad)
    * 3.2.3 [Disponibilidad](#323-disponibilidad)
    * 3.2.4 [Usabilidad](#324-usabilidad)
    * 3.2.5 [Portabilidad](#325-portabilidad)
  * 3.3 [Requerimientos del sistema](#33-requerimientos-del-sistema)
    * 3.3.1 [Compatibilidad](#331-compatibilidad)
    * 3.3.2 [Regulaciones y políticas](#332-regulaciones-y-politicas)
    * 3.3.3 [Seguridad](#333-seguridad)
    * 3.3.4 [Mantenimiento y actualización](#334-mantenimiento-y-actualizacion)
  * 3.4 [Interfaces externas](#34-interfaces-externas)
    * 3.4.1 [Interfaces de usuario](#341-interfaces-de-usuario)
    * 3.4.2 [Interfaces de hardware](#342-interfaces-de-hardware)
    * 3.4.3 [Interfaces de software](#343-interfaces-de-software)
  * 3.5 [Cumplimiento](#35-cumplimiento)
  * 3.6 [Diseño e implementación](#36-diseno-e-implementacion)
    * 3.6.1 [Instalación](#361-instalacion)
    * 3.6.2 [Distribución](#362-distribucion)
    * 3.6.3 [Mantenimiento](#363-mantenimiento)
    * 3.6.4 [Reutilización](#364-reutilizacion)
    * 3.6.5 [Portabilidad](#365-portabilidad)
    * 3.6.6 [Costo](#366-costo)
    * 3.6.7 [Fecha límite](#367-fecha-limite)
    * 3.6.8 [Prueba de concepto](#368-prueba-de-concepto)
* 4 [Verificación](#4-verificacion)
* 5 [Apéndice](#5-apendice)

## Revision History
| Name | Date    | Reason For Changes  | Version   |
| ---- | ------- | ------------------- | --------- |
|      |         |                     |           |
|      |         |                     |           |
|      |         |                     |           |

## 1. Introducción


### 1.1 Propósito del documento
El propósito de este documento es especificar los requisitos del software para el desarrollo de un planeador de horarios universitarios dirigido a los estudiantes de la Universidad Tecnológica de Bolívar (UTB) y a los directivos de la institución. Este documento tiene como objetivo principal establecer las características, funcionalidades y restricciones que debe cumplir el sistema, con el fin de asegurar que satisfaga las necesidades y expectativas tanto de los estudiantes como de la administración universitaria. Además, este documento servirá como una guía para los desarrolladores, asegurando que el software se diseñe y construya de manera coherente con los objetivos establecidos y con un enfoque en la optimización de la planificación académica, la satisfacción del usuario y la eficiencia en el uso de los recursos académicos. 

### 1.2 Alcance del producto
El producto cubierto por este documento es un software planeador de horarios universitarios para la Universidad Tecnológica de Bolívar (UTB), destinado a facilitar la planificación académica de los estudiantes. Este documento especifica los requisitos del software en su versión inicial, detallando tanto las funcionalidades esenciales como las restricciones y condiciones bajo las cuales el sistema operará.
El software permitirá a los estudiantes ingresar los códigos de sus materias y generará automáticamente todas las combinaciones posibles de horarios basados en las opciones disponibles de asignaturas, profesores y salones. Este sistema proporcionará a los estudiantes una herramienta eficaz para optimizar la selección de sus horarios, evitando conflictos y ajustándose a sus preferencias personales, como horarios preferidos y profesores específicos.
Además, el software se integrará con la base de datos existente de la UTB, permitiendo la actualización dinámica de la información sobre horarios, salones y disponibilidad de profesores. Los administradores designados podrán gestionar y modificar esta información de manera segura y eficiente.
Los beneficios esperados incluyen la reducción del tiempo y esfuerzo que los estudiantes dedican a la planificación de sus horarios, el aumento de la satisfacción estudiantil mediante una experiencia de usuario optimizada y la mejora en la gestión de los recursos académicos al evitar solapamientos y maximizar el uso de aulas y profesores.
Si bien este documento se centra en la versión inicial del software, se prevé la posibilidad de futuras expansiones que incluirán nuevas funcionalidades y mejoras en respuesta a las necesidades emergentes de los estudiantes.


### 1.3 Definiciones, acrónimos and abreviaciones

* **SRS**: Especificación de Requisitos de Software (Software Requirements Specification).
* **GUI**: Interfaz Gráfica de Usuario (Graphical User Interface).
* **Web Scraping**: Proceso automatizado de extracción de información desde sitios web. En el contexto de este proyecto, el web scraping se utilizará para obtener los horarios de cada clase desde la plataforma Banner de la Universidad Tecnológica de Bolívar (UTB). Este método permitirá al software planeador de horarios extraer datos relevantes, como horarios, aulas y profesores, directamente desde el sistema institucional, garantizando que la información utilizada en la planificación académica esté siempre actualizada y sea precisa.


### 1.4 Referencias


### 1.5 Descripción general del documento
Este documento está organizado de la siguiente manera:
* La Sección 2 proporciona una visión general del producto, incluyendo su contexto, funciones principales, restricciones y características del usuario.
* La Sección 3 detalla los requisitos específicos del software, incluyendo interfaces externas, requisitos funcionales y no funcionales, y otros aspectos técnicos.


## 2. Descripción general del producto


### 2.1 Perspectiva del producto
El proyector de horarios UTB es un producto nuevo y autónomo, diseñado para integrarse con los sistemas actuales de la UTB. Este software proporcionará una solución eficiente para la gestión de horarios estudiantiles, sin necesidad de reemplazar sistemas existentes. Su implementación mejorará la experiencia académica de los estudiantes y optimizará la utilización de recursos institucionales.

### 2.2 Funciones del producto
- **Generación de Horarios**: Crear todas las combinaciones posibles de horarios basados en materias, profesores, y salones disponibles.
- **Gestión de Información Universitaria**: Integrar y actualizar dinámicamente la información de la universidad.
- **Interacción con el Usuario**: Permitir a los estudiantes seleccionar y personalizar sus horarios.
- **Acceso a la Información**: Proporcionar acceso seguro y autenticado a los estudiantes.

### 2.3 Características del usuario
El sistema está destinado a ser utilizado por estudiantes universitarios, con diferentes niveles de experiencia técnica. Se espera que los usuarios tengan acceso regular a internet y dispositivos compatibles, y que estén familiarizados con la navegación básica en entornos digitales.

### 2.4 Supuestos y dependencias
- El sistema depende de la exactitud y actualización oportuna de los datos proporcionados por la UTB.
- Asume que los usuarios tendrán acceso a credenciales válidas para la autenticación.

### 2.5 Distribución de requisitos

## 3. Requerimientos

### 3.1 Requerimientos Funcionales
* **Generación de Horarios**: El sistema debe generar todas las combinaciones posibles de horarios basados en las materias seleccionadas. A su vez, dentro de los horarios, cada materia se deberá mostrar con código de la clase (NRC), profesor y salón asignado.
* **Gestión de Información**: El sistema debe permitir la actualización dinámica de datos de horarios, salones, y profesores proporcionados por la UTB.
* **Interacción con el Usuario**: Los usuarios deben poder filtrar entre sus preferencias (horario de clase preferido, profesores, etc) y recibir opciones de horarios personalizados.
* **Exportación**: El sistema también debe permitir guardar y exportar los horarios en formatos como PDF o JPG.
* **Notificación**: Los usuarios deben recibir una notificación vía e-mail sobre variaciones en sus horarios (cambio de salón, de profesor, etc.).


### 3.2 Requerimientos no funcionales

#### 3.2.1 Rendimiento
* El sistema debe ser capaz de procesar y generar horarios en tiempo real para al menos 5000 estudiantes simultáneamente.
* La respuesta del sistema ante las consultas de los estudiantes debe ser inferior a 2 segundos.

#### 3.2.2 Escalabilidad
* El sistema debe ser escalable para soportar un incremento en la cantidad de usuarios y de datos a lo largo del tiempo, especialmente durante períodos de inscripción y cambios de semestre.

#### 3.2.3 Disponibilidad
* El sistema debe estar disponible el 99.9% del tiempo, con una tolerancia mínima a fallos durante períodos críticos como la inscripción de materias.

#### 3.2.4 Usabilidad
* La interfaz de usuario debe ser diseñada para ser intuitiva, fácil de usar y accesible desde dispositivos móviles y de escritorio.
* Debe cumplir con estándares de accesibilidad para asegurar que todos los estudiantes, incluyendo aquellos con discapacidades, puedan utilizar el sistema sin inconvenientes.
*  La interfaz debe ser completamente funcional en una variedad de dispositivos, incluyendo PCs, laptops, tablets y smartphones, y ser compatible con los principales navegadores web (Chrome, Firefox, Safari, Edge).

#### 3.2.5 Portabilidad
*Despliegue en Diferentes Entornos: El software debe ser fácil de desplegar en diferentes entornos, incluyendo servidores locales de la universidad y plataformas en la nube, asegurando que pueda ser trasladado o escalado según sea necesario.
* Independencia de Plataforma: El código del software debe ser lo suficientemente flexible para funcionar tanto en diferentes sistemas operativos de escritorio como Windows, Linux o MacOS, como de sistemas operativos móviles como lo son Android y IOS, sin necesidad de modificaciones significativas.

### 3.3 Requerimientos del sistema

#### 3.3.1 Compatibilidad
* El sistema debe ser compatible con las plataformas tecnológicas actuales de la UTB, incluyendo el sistema de gestión académica y la base de datos de horarios.

#### 3.3.2 Regulaciones y políticas
* El sistema debe cumplir con las políticas de privacidad y protección de datos de la UTB y las regulaciones locales sobre manejo de información personal.
* Este conjunto de requerimientos proporciona una base sólida para comenzar el desarrollo de una aplicación o servicio que genere horarios estudiantiles de manera eficiente y que cumpla con las expectativas y necesidades tanto de los estudiantes como de la administración universitaria.

#### 3.3.3 Seguridad
* Autenticación y Autorización: El acceso al sistema estará restringido a usuarios autenticados mediante el sistema de autenticación de la UTB (correo institucional). Solo los estudiantes y directivos autorizados podrán acceder a la funcionalidad del software.
* Protección de Datos: Toda la información personal y académica extraída y utilizada por el sistema debe estar encriptada durante la transmisión y almacenamiento, cumpliendo con las normativas de protección de datos de la universidad.
* Privacidad: Los datos temporales almacenados en la base de datos serán eliminados periódicamente para evitar la retención innecesaria de información sensible.

#### 3.3.4 Mantenimiento y actualización
* Facilidad de Mantenimiento: El software debe estar diseñado de manera modular, permitiendo actualizaciones y mantenimiento sin afectar el funcionamiento global del sistema. El código debe ser bien documentado y seguir estándares de programación para facilitar el trabajo de los desarrolladores.
* Actualizaciones: El sistema debe ser capaz de recibir actualizaciones periódicas sin interrumpir el servicio. Estas actualizaciones pueden incluir mejoras de funcionalidad, parches de seguridad y optimizaciones de rendimiento.

### 3.4 Interfaces externas
El software proyector de horarios interactuará con varios sistemas y dispositivos externos para cumplir con sus funciones. A continuación, se detallan las interfaces externas clave:

#### 3.4.1 Interfaces de usuario
El sistema requerirá una interfaz gráfica de usuario (GUI) intuitiva y accesible, compatible con dispositivos móviles y de escritorio. La interfaz debe permitir a los estudiantes ingresar sus preferencias y seleccionar entre las combinaciones de horarios generadas.

* **Acceso Personalizado** : Los estudiantes deben poder acceder a la plataforma utilizando sus credenciales universitarias (correo institucional y contraseña).
Cada estudiante debe tener acceso a su plan de estudios y opciones de horario basadas en su carrera y semestre.

* **Soporte Multilingüe** : El sistema debe ofrecer soporte en varios idiomas, incluido el español y el inglés, para facilitar su uso por parte de estudiantes internacionales.

#### 3.4.2 Interfaces de hardware

#### 3.4.3 Interfaces de software

### 3.5 Cumplimiento

### 3.6 Diseño e implementación

#### 3.6.1 Instalación

#### 3.6.2 Distribución

#### 3.6.3 Mantenimiento

#### 3.6.4 Reutilización

#### 3.6.5 Portabilidad

#### 3.6.6 Costo

#### 3.6.7 Fecha límite

#### 3.6.8 Prueba de concepto

## 4. Verificación

## 5. Apéndice
