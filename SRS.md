# Software Requirements Specifications

Versión: 1.0 

Autores: 

+ Rodrigo Alejandro Barrera Manjarrez (rbarrer1@itam.mx)
+ Fabio Giuseppe Calo Dizy (fcalodiz@itam.mx)
+ Axel Giuseppe Flores Aranda (aflore85@itam.mx)
+ Salvador Alejandro Uribe Calva (suribeca@itam.mx)

Equipo Meriyein 2.0

Última edición: 24 de noviembre de 2022


## Introducción
### Propósito
La plataforma AsesoríasITAM tiene como objetivo el crear un espacio donde alumnos con problemas en sus materias contacten con alumnos que ya hayan cursado dichas materias y las dominen. Del mismo modo, se busca que pueda ser usada fácilmente por cualquiera, ya sea que quiera dar asesorias o tomarlas, su uso depe presentar ser sencillo para el usuario. 

Esto es el siguiente paso al sistema de laboratorios que maneja el ITAM el cuál se puede implementar dentro de la plataforma.

### Definiciones
+ Alumno - Estudiante que puede suscribirse a grupos de asesores
+ Asesor - Alumnos que además pueden publicar sus propios grupos
+ Administrador - Persona que puede ver el directorio de alumnos, ver quienes son asesores y quienes no, y quien tiene el poder de dar de baja grupos.

Se busca que tanto alumnos como asesores sean beneficiados de esta aplicación para ayudar y ser ayudados. Es una aplicación sencilla que le permite a los alumnos buscar las materias que les interesan. A su vez, buscamos que la aplicación sea un lugar en donde la comunidad se sienta segura de utilizar no sólo impartiendo los cursos sino que tomándolos también, y remunerando a aquellos que se animen a dar las asesorías. Queremos que la aplciación sea lo más profesional y formal posible.

### Alcance
El propósito de la aplicación se logrará a través de un sistema donde los asesores publicarán sus grupos a los cuales otros alumnos podrán suscribirse y así contactar con el asesor para definir horas en las cuales verse.

## Descripción General

### Product Perspective
Se proyecta implementar una aplicación la cual cubra la necesidad de los alumnos que tienen problemas con el entendimiento o aprendizaje con las materias impartidas el Instituto Tecnológico Autónomo de México (ITAM) a través de una plataforma segura y confiable para aquellos que quieran impartir y tomar cursos. Se busca tener una aplicación que le brinde a los alumnos una forma de mejorar su entendimiento de diversas materias a un bajo costo, al mismo tiempo, que aquellos que tengan el coonocimiento, impartan estos cursos de la misma manera que los actuales laboratorios. La gran diferencia es que no sólo se implementan en la plataforma sino que se darían para cualquier materia que dominen que estén interesadxs en implartir.

### Product Functions
Alumnos que quieran tomar una asesoría:
 + Crear una cuenta con su correo institucional en caso de ser nuevos con la aplicación. 
 + Buscar una materia a la que quieran mejorar sus calificaciones.
 + Darse de alta a un curso.
 + Darse de bja de un curso.
 + Ver las publicaciones de los asesores

Alumnos que quieran ser asesores e impartir una asesoría:
 + Crear una cuenta con su correo institucional, con la opción de asesor, en caso de ser nuevos con la aplicación.
 + Crear un curso que quieran impartir, poniendo la materia y su descripción. 
 + Ver todos los grupos que tiene.
 + Poner el precio de sus asesorías.

Administrador:
 + Ver en un directorio todos los asesores que están registrados para impartir cursos.
 + Ver en un directorio todos los alumnos que están registrados para tomar los cursos.
 + Ver la descripción de los asesores.
 + Ver los grupos publicados por los asesores.
 + Elminar grupos.

Todos del mismo modo tienen la funcionalidad de cambiar el *modo* de su preferencia, es decir, modo escuro o claro.

### User Classes and Characteristics
Las clases principales las podemos dividir en 3:
 + Alumnos
 + Asesores
 + Administradores

Para los alumnos que quieran tomar una asesoría. Podrán crear una cuenta en la aplicación *Asesorías ITAM*. Estos alumnos podrán ver qué clases les interesan tomar y registrarse en ellas. Esto habilitará que puedan ver en la pantalla de *Mis Asesores* los grupos a los que están inscritos. Podrán ver los detalles de cada grupo y, si así lo desean, dejar el grupo de asesoría.

Para los asesores, estos podrán crear su cuenta en la aplicación como asesores, crear grupos de asesorías de materias de las que quieran impartir, ver todos los grupos que dan, así como hacer publicaciones en estos y cobrar por sus asesorías.

Finalmente, los administradores tienen acceso a los datos proporcionados por tanto los asesores como los alumnos. De cada persona registrada, los asesores pueden ver si son o no asesores, la carrera que estudia y su correo. Dentro de la pestaña de *Publicaciones* podrá ver cada curso y podrá eliminarlos o no, al eliminarla esto la borrara de la lista de materias. 

### Operating environment
La aplicación debe funcionar en todos los sistemas operativos (Mac, Microsoft, Linux) y en todos los buscadores (Chrome, Outlook, Firefox, etc) que se puedan usar en computadoras. 
Como plan a futuro queremos que la aplicación pueda ser accesada en otros dispotivos como celulares o tablets.

### Design and Implementation Constraints
En primer lugar, por cómo está echo, sólo se planea para alumnos con correos institucionales del ITAM por lo tanto restringimos su uso a aquellos que pertenezcan a esta comunidad. Del mismo modo, sólo se puede acceder mediante una computadora, pero, cómo bien se menciona anteriormente, en un futuro se quiere habilitar para dispositivos móviles y tablets. 

### Documentación de usuario

Ver el apartado Uso del ReadMe [aquí](https://github.com/Asesorias-ITAM/AsesoriasITAM/blob/main/README.md)

### Suposiciones y dependencias
Dependemos que todos los usuarios, tanto asesores como alumnos utilizan su correo institucional del ITAM. 

## External Interface Requirements

### Hardware Interfaces
Es necesario utilizar una computadora ya que esta versión de la aplicación no está pensada para dispositivos móviles o tablets. 

### Software Interfaces
Para poder utilizar la aplicación, se necesita de un navegador como Chrome, Outlook, Firefox, etc.

### Communications Interfaces
Se necesita el permiso para poder mandar correos a los correos de las personas que se registren a la aplicación ya que para confirmar la creación de su cuenta, se envía un correo con el código de verificación de correo.

## System Features

### Creación de grupos

El asesor puede crear grupos para darse a conocer al resto de usuarios. Prioridad Alta.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/55751739/203900661-3c057c78-3067-4cda-a56f-325239e30382.png">

Para realizar esta feature, se crea un objeto grupo localmente y al publicarse se envía a la base de datos. Cada usuario tiene una lista de publicaciones, al publicarse, se agrega a la lista. En Hygraph, se crea el objeto publicación y se agrega la conexión con su usuario creador

### Suscripción a grupos

Los usuarios pueden suscribirse a grupos de asesoría. Prioridad Media.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/86432413/203886876-7e8f0d64-118a-4d41-8a5b-3aa5fea86aa2.png">


Cada usuario debe tener una lista con los usuarios asesores a los que está suscrito. En Hygraph, se hace una conexión del objeto usuario con el objeto publicación.

### Creación de cuenta

Los usuarios podrán crear cuentas para validar su identidad, y guardar datos sobre las asesorías que dan o a las que están inscritos. Prioridad Alta.

<img width="500" alt="image" src="https://user-images.githubusercontent.com/86432413/203887156-f3e57908-1dc5-409c-aac8-97b7c4ae86ae.png">


Se crea un perfil de autentificación con AWS Cognito, y se agrega la información del alumno a la base de datos *directorio* que se encuentra en Hygraph.


## Other Requirements 
 
* Modo oscuro

Para esta funcionalidad, el botón hace que cada elemento visible pase de usar su configuración de modo claro a su configuración de modo oscuro.
