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

# Requisitos para realizar las pruebas

## 14. Necesidades de equipo y entrenamiento
* Se requiere haber leído el documento README de este proyecto que se puede encontrar [aquí](https://github.com/Asesorias-ITAM/AsesoriasITAM/blob/main/README.md)
* Se va a proporcionar una versión del código para realizar las pruebas y realizar cambios sin modificar inmediatamente el código principal
* Se va a dar acceso a la base de datos de prueba

## 15 Responsabilidades

Rodrigo Barrera, está a cargo y es quién decide decide tanto los riesgos del proyecto como el alcance de las pruebas.
Fabio Calo dará el entrenamiento para utilizar la aplicación y será quien proporcionará los elementos para realizar las pruebas.
Alejandro Uribe se encargará de diseñar las pruebas y organizar tiempos para realizarlas.
Axel Flores tomará las decisiones sobre cualquier cosa que no esté escrita en este plan de calidad

## 16. 

# BOCETO
[1] Este es el plan -> Referencias (Documentos posteriores, planes, maquetas, SRS) ->
[2] Test Items (pantallas a probar, las 5 funcionalidades) -> Riesgos del Software
[3] Features que se van y no se van a probar -> Approach (Caja negra/gris, manual automatizado)
[4 - LAS PRUEBAS] Item Pass and Fail criteria
	Funcionalidad		Escenario	Semáforo
  	  [REDACTED]		[REDACTED]	Verde / Amarillo / Rojo
						"Se debe pasar un X% de las pruebas
No hay servicio con el 100%

[5] Suspension Criteria (mínimo aceptable) -> Test Deliverables (entregables)
[6] Remaining Tests -> Necesidades Extra del ambiente -> 
    Equipo -> Responsabilides-> Horarios -> Riesgos planeados -> Approvals -> Glosario	
