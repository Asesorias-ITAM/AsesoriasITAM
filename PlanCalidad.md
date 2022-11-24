# Plan de Calidad

# Presentación 

## 1. Identificadores del plan de calidad

Versión: 1.0 

Autores: 

+ Rodrigo Alejandro Barrera Manjarrez (rbarrer1@itam.mx)
+ Fabio Giuseppe Calo Dizy (fcalodiz@itam.mx)
+ Axel Giuseppe Flores Aranda (aflore85@itam.mx)
+ Salvador Alejandro Uribe Calva (suribeca@itam.mx)

Equipo Meriyein 2.0

Última edición: 24 de noviembre de 2022

## 2. Referencias

Este documento está basado en los estándares de calidad del IEEE-829 y en el SRS que puede ser consultado [aquí](https://github.com/Asesorias-ITAM/AsesoriasITAM/blob/main/SRS.md).

## 3. Introducción

# Elementos a probar
Se va a probar la correcta implementación del software en la página de AsesoríasITAM, esto incluye todas las pantallas en modo Asesor y modo No Asesor 
* Validaciones del sistema 
* Funcionalidades relacionadas con la Base de datos
* UI de cada pantalla

## 4. Funcionalidades a probar

* Creación de cuentas
* Inicio de sesión 
* Navegación por interfaz
* Búsqueda de grupos
* Creación de grupos
* Suscripción a grupos


## 5. Riesgos del Software

* No implementamos medidas de seguridad dentro de la aplicación, solo en la creación de cuentas.
* Se pueden iniciar múltiples sesiones distintas en un mismo navegador
* Dependemos de AWS

# Sobre las pruebas

## 6. Pruebas que se van a realizar
Funcionamiento de la aplicación desde la perspectiva del asesor y el no asesor.

## 7. Pruebas que no se van a realizar

* Funcionamiento de la aplicación desde la perspectiva del administrador, ya funciona correctamente
* Agregar y quitar notas, no estará disponible en esta versión del software

## Estrategia de las pruebas

Se harán pruebas a la aplicación con la estrategia Grey Box Testing, aplicando principalmente la técnica de regression testing para identificar rápidamente qué es lo que no está funcionando y si es un problema del código o de un mal uso de la aplicación.

Los pasos a seguir son:

1. Identificar qué inputs estámos dando
2. Identificar qué outputs deberían salir
3. Identificar qué camino toma la funcionalidad a probar
4. Identificar subfuncionalidades relacionadas con la prueba
5. Desarrollar inputs prueba para las subfucionalidades
6. Desarrollar outputs prueba para las subfuncionalidades
7. Hacer casos prueba para las subfuncionalidades
8. Verificar el resultado de las subfuncionalides
9. Repetir pasos 4 a 8 para el resto de subfucionalidades
10. Hacer pruebas con la funcionalidad completa.

# Las pruebas

## 9. Criterios de éxito y fracaso
| Funcionalidad     | Escenario   | Semáforo      |
|-------------------|-------------|---------------|
| Creación de cuentas     | Creo una cuenta con correo del ITAM y otra con correo externo                                       | Verde    |
| Inicio de sesión        | Al introducir mis credeciales pienso que tengo un error y doy clic en la lupa para ver si voy bien  | Amarillo |
| Navegación por interfaz | Navego entre las distintas pestañas con facilidad                                                   | Amarillo |
| Búsqueda de grupos      | Busco grupos para la materia Economía II                                                            | Verde    |
| Creación de grupos      | Al crear un grupo quiero poner una foto de mi horario                                               | Rojo | 
| Suscripción a grupos    | Me inscribo a un grupo por accidente y lo quiero dar de baja                                        | Verde |

# Entregables

## 10. Criterios de suspensión y de reanudación de pruebas

* Suspensión: La funcionalidad no presenta fallos en el uso que un usuario le daría contando posibles accidentes como introducir datos erróneos en campos.
* Reanudación: La funcionalidad presenta un fallo crítico que evita el uso de la plataforma.

## 11. Entregables de las pruebas

* Documento de plan de calidad
* Resultados de las pruebas
* Especificación del diseño de cada prueba
* Error logs
* Reporte de los problemas encontrados y soluciones propuestas

# Por hacer

## 12. Pruebas pendientes

* Probar funcionalidad de modo administrador
* Probar funcionalidad de añadir y quitar notas
* Probar cambios en sección de Ajustes

## 13. Necesidades extra del ambiente

Para realizar las pruebas se proporcionará una base de datos inicial para experimentar, también se proporcionaran cuentas de prueba para realizar las pruebas.

# Especificaciones de la realización de las pruebas

## 14. Necesidades de equipo y entrenamiento
* Se requiere haber leído el documento README de este proyecto que se puede encontrar [aquí](https://github.com/Asesorias-ITAM/AsesoriasITAM/blob/main/README.md)
* Se va a proporcionar una versión del código para realizar las pruebas y realizar cambios sin modificar inmediatamente el código principal
* Se va a dar acceso a la base de datos de prueba

## 15 Responsabilidades

Rodrigo Barrera, está a cargo y es quién decide decide tanto los riesgos del proyecto como el alcance de las pruebas.
Fabio Calo dará el entrenamiento para utilizar la aplicación y será quien proporcionará los elementos para realizar las pruebas.
Alejandro Uribe se encargará de diseñar las pruebas y organizar tiempos para realizarlas.
Axel Flores tomará las decisiones sobre cualquier cosa que no esté escrita en este plan de calidad

## 16. Itinerario
Al estar usando la metodología Feature Driven, las pruebas se realizarán al día siguiente de haber acabado una Feature para asegurar su correcta implementación.

## 17. Riesgos planeados
* Tenemos un equipo limitado por lo que debemos trabajar lo mejor posible alrededor de los requerimientos
* Ante un tiempo prolongado en el desarrollo de una feature, se reducirá el tiempo de pruebas para seguir con la feature siguiente.
* En caso de tener que regresar a rehacer otra feature en etapas avanzadas del desarrollo, se dividirá el equipo en pruebas y desarrollo para reparar todo lo más rápido posible.
* En caso de un problema que retrase el desarrollo, se dejarán features para una versión posterior y se ajustará el MVP
* Se debe mantener un buen ritmo de trabajo para asegurar la entrega de la primera versión el 25 de noviembre de 2022 y evitar sobrecarga de trabajo

## 18. Personas que pueden aprobar las pruebas
Para poder pasar a la siguiente parte del desarrollo, necesitamos la aprobación de alguno de nuestros clientes:
* Paulina Bustos
* Alejandro Baillères

## 19. Glosario

* ITAM - Instituto Tecnológico Autónomo de México
* Grey Box Testing - Pruebas tanto al código como a la interfaz, teniendo ambos disponibles para editar
* AWS - Amazon Web Services
* MVP - Entregable con funcionalidad mínima
