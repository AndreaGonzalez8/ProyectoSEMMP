# ProyectoSEMMP

Este proyecto consiste en el desarrollo de un **sistema web** que permite la **gestión de usuarios, equipos y solicitudes de soporte técnico**.  
Incluye funcionalidades como el **registro, login, consultas, gestión de equipo, entre otras**, conectando un **frontend** responsivo con un **backend** en Java usando **Servlets, JDBC y MySQL**.

---

## Contenido del Proyecto

El proyecto está dividido en dos carpetas principales:

- **📂 frontend/** → Contiene todo el código del lado del cliente.
  - Diseñado con **HTML5**, **CSS3**, **Bootstrap** y **JavaScript**.
  - Incluye páginas para **registro**, **login**, **gestión de equipos**, **solicitud de soporte**.
  - Totalmente responsivo y adaptable a distintos dispositivos.

- **📂 backend/** → Contiene el código del lado del servidor.
  - Desarrollado en **Java** utilizando **Servlets**.
  - Conexión a la base de datos **MySQL** mediante **JDBC**.
  - Arquitectura basada en **MVC** para facilitar el mantenimiento y escalabilidad.

---

## Tecnologías Utilizadas

### **Frontend**
- HTML5
- CSS3 (con diseño moderno y responsivo)
- Bootstrap 5
- JavaScript (validaciones y consumo de API)
- Fetch API para comunicar con el backend

### **Backend**
- Java 17+
- Servlets y JSP
- JDBC (para conexión a MySQL)
- NetBeans 

### **Base de Datos**
- **MySQL** (usando **XAMPP**)
  
### **Configurar**

- **Configurar la base de datos en XAMPP**

  - Abre phpMyAdmin desde http://localhost/phpmyadmin.

  - Crea una nueva base de datos:

    - CREATE DATABASE nombreBaseDatos;
      
  - Importa el script SQL.
  - Configura tu usuario y contraseña de MySQL en el archivo ConexionBD.java:
    - Por ejemplo:
      - private static final String URL = "jdbc:mysql://localhost:3306/semmp_db";
      - private static final String USER = "root";
      - private static final String PASSWORD = "";

- **Ejecutar el backend en NetBeans**

  - Abre NetBeans y selecciona Abrir proyecto existente.

  - Ve a la carpeta backend/ y selecciona el proyecto.

  - Configura tu Tomcat:
    - Servidor: Apache Tomcat 9+
    - URL base: http://localhost:8080

  - Ejecuta el proyecto.

- **Ejecutar el frontend en Visual Studio Code**

  - Abre la carpeta frontend/ selecciona el proyecto y abrirlo en VS Code.

  - Instala la extensión Live Server.

  - Haz clic derecho en index.html y selecciona "Open with Live Server".

### Conexión entre Frontend y Backend

- Para permitir que el frontend y el backend trabajen juntos desde orígenes diferentes, se añadieron encabezados CORS en los Servlets.
  
  - Ejemplo en LoginServlet.java:
    
    - response.setHeader("Access-Control-Allow-Origin", "*");
    - response.setHeader("Access-Control-Allow-Methods", "POST, GET, OPTIONS, DELETE");
    - response.setHeader("Access-Control-Allow-Headers", "Content-Type, Accept, Authorization");
    - response.setHeader("Access-Control-Allow-Credentials", "true");

