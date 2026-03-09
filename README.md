# To-Do Application 📝

Esta es una aplicación web de gestión de tareas (To-Do List) desarrollada con **Java** y **Spring Boot**. El proyecto permite a los usuarios crear, visualizar, cambiar el estado (completado/pendiente) y eliminar tareas de forma sencilla.

## 🚀 Tecnologías Utilizadas

El proyecto emplea las siguientes tecnologías y herramientas:

* **Java 21**: Lenguaje de programación principal.
* **Spring Boot 4.0.3**: Framework para el desarrollo de la aplicación.
    * **Spring Data JPA**: Para la persistencia de datos y comunicación con la base de datos.
    * **Spring Web**: Para el manejo de controladores y peticiones HTTP.
* **Thymeleaf**: Motor de plantillas para renderizar las vistas HTML en el servidor.
* **MySQL**: Sistema de gestión de bases de datos relacionales.
* **Bootstrap 5.3.8**: Framework de CSS para un diseño responsivo y moderno.
* **Lombok**: Librería para reducir el código repetitivo (Boilerplate) en las entidades.
* **Maven**: Herramienta de gestión y construcción de proyectos.

## 📋 Funcionalidades

* **Listado de Tareas**: Visualización de todas las tareas almacenadas.
* **Creación de Tareas**: Formulario para añadir nuevas tareas con un título.
* **Toggle de Estado**: Cambia rápidamente entre estado "Pendiente" y "Completada" (incluye estilo visual tachado).
* **Eliminación**: Opción para borrar tareas existentes con confirmación de seguridad.

## 🛠️ Configuración e Instalación

### Requisitos Previos

1.  Tener instalado **Java 21**.
2.  Tener instalado y configurado un servidor **MySQL**.

### Configuración de la Base de Datos

1.  Crea una base de datos llamada `todo-app` en tu servidor local.
2.  Configura tus credenciales de base de datos en las variables de entorno o directamente en el archivo `src/main/resources/application.properties`:

```
spring.datasource.url=jdbc:mysql://localhost:3306/todo-app
spring.datasource.username=TU_USUARIO
spring.datasource.password=TU_CONTRASEÑA
```

### Ejecución

Puedes ejecutar la aplicación utilizando el Maven Wrapper incluido:

En Windows:
```./mvnw.cmd spring-boot:run```

En Linux/macOS:
```./mvnw spring-boot:run```

Una vez iniciada, accede a la aplicación en tu navegador a través de: http://localhost:8080/tasks.

## 📂 Estructura del Proyecto

* src/main/java/com/app/todoapp/controller: Maneja las rutas y peticiones web.
* src/main/java/com/app/todoapp/model: Define la entidad Task mapeada a la base de datos.
* src/main/java/com/app/todoapp/repository: Interfaz para operaciones CRUD con JPA.
* src/main/java/com/app/todoapp/service: Contiene la lógica de negocio de la aplicación.
* src/main/resources/templates: Archivos HTML procesados por Thymeleaf.
