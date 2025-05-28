Proyecto-Programacion2.
Ginna Esmeralda Paez Lancheros , Ronald Armando Gutierres Murcia.



**MiUNISANGIL**

Titulo Aplicación Móvil para la Comunicación, Gestión de Eventos, Préstamos y Recursos Académicos en UNISANGIL.

Definicion de Modulo de sistema

Desarrollar una aplicación móvil utilizando React Native permite a los desarrolladores crear aplicaciones móviles multiplataforma utilizando JavaScrip; esta facilita la comunicación, la colaboración y el acceso a información y recursos académicos para estudiantes, profesores y personal administrativo de la universidad.

Modulo principales

Autenticación y Gestión de Usuarios: Este módulo gestionará el  inicio de sesión, roles y permisos de los usuarios (estudiantes, profesores, personal administrativo). Gestión de Datos: Este módulo será el corazón de la aplicación, responsable del almacenamiento y gestión de toda la información mediante el uso de bases de datos (Firebase Firestore) y framework EXPO.

Eventos: Detalles del evento, fecha, hora, ubicación, etc.

Préstamos: Información de los artículos prestados, usuarios involucrados, fechas de préstamo y devolución.

Noticias y Avisos: Publicaciones de la universidad.

Grupos de Estudio: Información de los grupos, miembros( fomentar la creacion o participacion de semilleros).

Recursos: Recomendaciones de libros, artículos.

Información Académica (proporcionada por la misma comunidad esducativa, como estudiantes reconocemos que a nivel de sede que seria valido).

Interfaz de Usuario: Este módulo se encargará de la experiencia del usuario. Se diseñará una interfaz intuitiva y amigable, con una navegación clara y sencilla.

Formularios para la solicitud de préstamos.

Sistema de notificaciones push.

Tegnologias

-React Native:

Framework para el desarrollo de la interfaz de usuario de tu aplicación móvil.

Librerías como React Navigation para gestionar la navegación entre pantallas.

-Firebase:

Firebase Firestore: Base de datos NoSQL para almacenar y gestionar los datos de tu aplicación en tiempo real.

Firebase Authentication: Para el manejo de inicio de sesión de usuarios (correo electrónico, etc.).

Firebase Cloud Messaging (FCM): Para enviar notificaciones push.

Firebase Hosting (opcional): Para alojar algún backend o archivo estático, si es necesario.

Control de versiones: GitHub.

Flujo

Inicio de sesión

Los usuarios deben iniciar sesion con el correo institucional.

Almacena la información en Firebase Authentication y, si necesitas más datos (como el rol), guarda esto en Firestore bajo una colección usuarios.

Implementación:

Usa Firebase Authentication para gestionar el inicio de sesión.

Cuando un usuario inicie sesion , se le cargara toda la infomacion disponible en los modulos .

Navegación principal
Un menú principal con opciones para acceder a los diferentes módulos (eventos, préstamos, grupos, documentacion.)

Implementación:

Usa React Navigation para manejar la navegación entre pantallas.

Implementa un menú de tipo pestañas (Tab Navigator) usando React Navigation.

Gestión de Módulos
a. Eventos: Mostrar una lista de eventos extraídos desde Firestore.

Permitir filtros por fecha, hora o ubicación.

Implementar creación de nuevos eventos para roles autorizados.

b. Noticias y Avisos: Pantalla para mostrar las últimas noticias publicadas.

Agregar notificaciones push automáticas para nuevas publicaciones.

c. Préstamos: Pantalla para registrar préstamos (artículo, usuario, fecha de vencimiento).

Consultar y filtrar préstamos vigentes.

Configurar recordatorios de vencimientos usando Firebase Cloud Messaging (FCM).

d. Grupos de Estudio(opcional)

Listar grupos existentes con detalles (miembros, temas).

Agregar funcionalidad para que los usuarios se unan a grupos existentes.

e. Recursos: Mostrar recomendaciones de libros, artículos o herramientas relacionadas.

Procesamiento de datos
Utilizar Firebase Firestore para guardar toda la información estructurada de los módulos (eventos, préstamos, noticias, grupos y recursos).

Activar la funcionalidad offline para que los datos estén disponibles sin conexión.

Consultas y Filtros:

Implementar consultas para filtrar información en cada módulo (por ejemplo, eventos por fecha, préstamos por usuario).

Notificaciones
Usar Firebase Cloud Messaging (FCM) para enviar notificaciones push.

Alertas automáticas: Nuevos eventos o noticias, Recordatorios de vencimientos de préstamos, Actividades importantes en grupos de estudio.

Cierre de sesión
Agregar un botón "Cerrar sesión" en el menú.

Usar el método signOut() de Firebase Authentication para cerrar la sesión y redirigir al usuario a la pantalla de inicio.

Diseño y Pruebas
Crear una interfaz amigable y coherente para los usuarios usando componentes nativos de React Native.

Pruebas:

Probar la funcionalidad en dispositivos físicos y emuladores.

Simular eventos como notificaciones y sincronización de datos.
