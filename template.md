# Software Requirements Specification
## For <project name>

Version 0.1  
Prepared by <author>  
<organization>  
<date created>  

Table of Contents
=================
* [Revision History](#revision-history)
* 1 [Introducción](#1-introducción)
  * 1.1 [Document Purpose](#11-document-purpose)
  * 1.2 [Product Scope](#12-product-scope)
  * 1.3 [Definitions, Acronyms and Abbreviations](#13-definitions-acronyms-and-abbreviations)
  * 1.4 [References](#14-references)
  * 1.5 [Document Overview](#15-document-overview)
* 2 [Product Overview](#2-product-overview)
  * 2.1 [Product Perspective](#21-product-perspective)
  * 2.2 [Product Functions](#22-product-functions)
  * 2.3 [Product Constraints](#23-product-constraints)
  * 2.4 [User Characteristics](#24-user-characteristics)
  * 2.5 [Assumptions and Dependencies](#25-assumptions-and-dependencies)
  * 2.6 [Apportioning of Requirements](#26-apportioning-of-requirements)
* 3 [Requirements](#3-requirements)
  * 3.1 [External Interfaces](#31-external-interfaces)
    * 3.1.1 [User Interfaces](#311-user-interfaces)
    * 3.1.2 [Hardware Interfaces](#312-hardware-interfaces)
    * 3.1.3 [Software Interfaces](#313-software-interfaces)
  * 3.2 [Functional](#32-functional)
  * 3.3 [Quality of Service](#33-quality-of-service)
    * 3.3.1 [Performance](#331-performance)
    * 3.3.2 [Security](#332-security)
    * 3.3.3 [Reliability](#333-reliability)
    * 3.3.4 [Availability](#334-availability)
  * 3.4 [Compliance](#34-compliance)
  * 3.5 [Design and Implementation](#35-design-and-implementation)
    * 3.5.1 [Installation](#351-installation)
    * 3.5.2 [Distribution](#352-distribution)
    * 3.5.3 [Maintainability](#353-maintainability)
    * 3.5.4 [Reusability](#354-reusability)
    * 3.5.5 [Portability](#355-portability)
    * 3.5.6 [Cost](#356-cost)
    * 3.5.7 [Deadline](#357-deadline)
    * 3.5.8 [Proof of Concept](#358-proof-of-concept)
* 4 [Verification](#4-verification)
* 5 [Appendixes](#5-appendixes)

## Revision History
| Name | Date    | Reason For Changes  | Version   |
| ---- | ------- | ------------------- | --------- |
|      |         |                     |           |
|      |         |                     |           |
|      |         |                     |           |

## 1. Introducción


### 1.1 Document Purpose
El propósito de este documento es especificar los requisitos del software para el desarrollo de un planeador de horarios universitarios dirigido a los estudiantes de la Universidad Tecnológica de Bolívar (UTB) y a los directivos de la institución. Este documento tiene como objetivo principal establecer las características, funcionalidades y restricciones que debe cumplir el sistema, con el fin de asegurar que satisfaga las necesidades y expectativas tanto de los estudiantes como de la administración universitaria. Además, este documento servirá como una guía para los desarrolladores, asegurando que el software se diseñe y construya de manera coherente con los objetivos establecidos y con un enfoque en la optimización de la planificación académica, la satisfacción del usuario y la eficiencia en el uso de los recursos académicos. 

### 1.2 Product Scope
El producto cubierto por este documento es un software planeador de horarios universitarios para la Universidad Tecnológica de Bolívar (UTB), destinado a facilitar la planificación académica de los estudiantes. Este documento especifica los requisitos del software en su versión inicial, detallando tanto las funcionalidades esenciales como las restricciones y condiciones bajo las cuales el sistema operará.
El software permitirá a los estudiantes ingresar los códigos de sus materias y generará automáticamente todas las combinaciones posibles de horarios basados en las opciones disponibles de asignaturas, profesores y salones. Este sistema proporcionará a los estudiantes una herramienta eficaz para optimizar la selección de sus horarios, evitando conflictos y ajustándose a sus preferencias personales, como horarios preferidos y profesores específicos.
Además, el software se integrará con la base de datos existente de la UTB, permitiendo la actualización dinámica de la información sobre horarios, salones y disponibilidad de profesores. Los administradores designados podrán gestionar y modificar esta información de manera segura y eficiente.
Los beneficios esperados incluyen la reducción del tiempo y esfuerzo que los estudiantes dedican a la planificación de sus horarios, el aumento de la satisfacción estudiantil mediante una experiencia de usuario optimizada y la mejora en la gestión de los recursos académicos al evitar solapamientos y maximizar el uso de aulas y profesores.
Si bien este documento se centra en la versión inicial del software, se prevé la posibilidad de futuras expansiones que incluirán nuevas funcionalidades y mejoras en respuesta a las necesidades emergentes de los estudiantes.


### 1.3 Definitions, Acronyms and Abbreviations

* **SRS**: Especificación de Requisitos de Software (Software Requirements Specification).
* **GUI**: Interfaz Gráfica de Usuario (Graphical User Interface).
* **Web Scraping**: Proceso automatizado de extracción de información desde sitios web. En el contexto de este proyecto, el web scraping se utilizará para obtener los horarios de cada clase desde la plataforma Banner de la Universidad Tecnológica de Bolívar (UTB). Este método permitirá al software planeador de horarios extraer datos relevantes, como horarios, aulas y profesores, directamente desde el sistema institucional, garantizando que la información utilizada en la planificación académica esté siempre actualizada y sea precisa.


### 1.4 References


### 1.5 Document Overview
Este documento está organizado de la siguiente manera:
* La Sección 2 proporciona una visión general del producto, incluyendo su contexto, funciones principales, restricciones y características del usuario.
* La Sección 3 detalla los requisitos específicos del software, incluyendo interfaces externas, requisitos funcionales y no funcionales, y otros aspectos técnicos.


## 2. Product Overview


### 2.1 Product Perspective
El proyector de horarios UTB es un producto nuevo y autónomo, diseñado para integrarse con los sistemas actuales de la UTB. Este software proporcionará una solución eficiente para la gestión de horarios estudiantiles, sin necesidad de reemplazar sistemas existentes. Su implementación mejorará la experiencia académica de los estudiantes y optimizará la utilización de recursos institucionales.

### 2.2 Product Functions
- **Generación de Horarios**: Crear todas las combinaciones posibles de horarios basados en materias, profesores, y salones disponibles.
- **Gestión de Información Universitaria**: Integrar y actualizar dinámicamente la información de la universidad.
- **Interacción con el Usuario**: Permitir a los estudiantes seleccionar y personalizar sus horarios.
- **Acceso a la Información**: Proporcionar acceso seguro y autenticado a los estudiantes.

### 2.4 User Characteristics
El sistema está destinado a ser utilizado por estudiantes universitarios, con diferentes niveles de experiencia técnica. Se espera que los usuarios tengan acceso regular a internet y dispositivos compatibles, y que estén familiarizados con la navegación básica en entornos digitales.

### 2.5 Assumptions and Dependencies
- El sistema depende de la exactitud y actualización oportuna de los datos proporcionados por la UTB.
- Asume que los usuarios tendrán acceso a credenciales válidas para la autenticación.

### 2.6 Apportioning of Requirements

## 3. Requirements

### 3.1 Requisitos Funcionales
- **Generación de Horarios**: El sistema debe generar todas las combinaciones posibles de horarios basados en las materias seleccionadas. A su vez, dentro de los horarios, cada materia se deberá mostrar con código de la clase (NRC), profesor y salón asignado.
- **Gestión de Información**: El sistema debe permitir la actualización dinámica de datos de horarios, salones, y profesores proporcionados por la UTB.
- **Interacción con el Usuario**: Los usuarios deben poder filtrar entre sus preferencias (horario de clase preferido, profesores, etc) y recibir opciones de horarios personalizados.
 El sistema también debe permitir guardar y exportar los horarios en formatos como PDF o JPG.
Los usuarios deben recibir una notificación vía e-mail sobre variaciones en sus horarios (cambio de salón, de profesor, etc.).


### 3.2 Requerimientos No Funcionales

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

### 3.3 Requerimientos del Usuario

#### 3.3.1 Acceso Personalizado
* Los estudiantes deben poder acceder a la plataforma utilizando sus credenciales universitarias (correo institucional y contraseña).
* Cada estudiante debe tener acceso a su plan de estudios y opciones de horario basadas en su carrera y semestre.

#### 3.3.2 Soporte Multilingüe
* El sistema debe ofrecer soporte en varios idiomas, incluido el español y el inglés, para facilitar su uso por parte de estudiantes internacionales.

### 3.4 Requerimientos del sistema

#### 3.4.1 Compatibilidad
* El sistema debe ser compatible con las plataformas tecnológicas actuales de la UTB, incluyendo el sistema de gestión académica y la base de datos de horarios.

#### 3.4.2 Regulaciones y Políticas
* El sistema debe cumplir con las políticas de privacidad y protección de datos de la UTB y las regulaciones locales sobre manejo de información personal.
* Este conjunto de requerimientos proporciona una base sólida para comenzar el desarrollo de una aplicación o servicio que genere horarios estudiantiles de manera eficiente y que cumpla con las expectativas y necesidades tanto de los estudiantes como de la administración universitaria.

#### 3.4.3 Seguridad
* Autenticación y Autorización: El acceso al sistema estará restringido a usuarios autenticados mediante el sistema de autenticación de la UTB (correo institucional). Solo los estudiantes y directivos autorizados podrán acceder a la funcionalidad del software.
* Protección de Datos: Toda la información personal y académica extraída y utilizada por el sistema debe estar encriptada durante la transmisión y almacenamiento, cumpliendo con las normativas de protección de datos de la universidad.
* Privacidad: Los datos temporales almacenados en la base de datos serán eliminados periódicamente para evitar la retención innecesaria de información sensible.

#### 3.4.4 Mantenimiento y actualización
* Facilidad de Mantenimiento: El software debe estar diseñado de manera modular, permitiendo actualizaciones y mantenimiento sin afectar el funcionamiento global del sistema. El código debe ser bien documentado y seguir estándares de programación para facilitar el trabajo de los desarrolladores.
* Actualizaciones: El sistema debe ser capaz de recibir actualizaciones periódicas sin interrumpir el servicio. Estas actualizaciones pueden incluir mejoras de funcionalidad, parches de seguridad y optimizaciones de rendimiento.

### 3.5 External Interfaces
El software proyector de horarios interactuará con varios sistemas y dispositivos externos para cumplir con sus funciones. A continuación, se detallan las interfaces externas clave:

#### 3.5.1 User interfaces
El sistema requerirá una interfaz gráfica de usuario (GUI) intuitiva y accesible, compatible con dispositivos móviles y de escritorio. La interfaz debe permitir a los estudiantes ingresar sus preferencias y seleccionar entre las combinaciones de horarios generadas.

* **Acceso Personalizado** : Los estudiantes deben poder acceder a la plataforma utilizando sus credenciales universitarias (correo institucional y contraseña).
Cada estudiante debe tener acceso a su plan de estudios y opciones de horario basadas en su carrera y semestre.

* **Soporte Multilingüe** : El sistema debe ofrecer soporte en varios idiomas, incluido el español y el inglés, para facilitar su uso por parte de estudiantes internacionales.

#### 3.5.2 Hardware interfaces

#### 3.5.3 Software interfaces

### 3.6 Compliance

### 3.7 Design and Implementation

#### 3.7.1 Installation

#### 3.7.2 Distribution

#### 3.7.3 Maintainability

#### 3.7.4 Reusability

#### 3.7.5 Portability

#### 3.7.6 Cost

#### 3.7.7 Deadline

#### 3.7.8 Proof of Concept

## 4. Verification

## 5. Appendixes
