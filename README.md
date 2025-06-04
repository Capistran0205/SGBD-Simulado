# Acceso_SGBD y MuestraDatos1

## Descripción del Proyecto

Este proyecto es una aplicación de escritorio en Java que proporciona una interfaz gráfica de usuario (GUI) para conectarse a una base de datos SQL (MySQL o SQL Server) y ejecutar consultas.  
Es una aplicación cliente que utiliza la librería `TablasBD` (descrita en `README_TablasBD.txt` del repositorio correspondiente) para la gestión de la conexión, consultas y modelado de datos.  

Permite a los usuarios:
- Seleccionar una base de datos
- Introducir credenciales
- Interactuar con tablas y ejecutar sentencias SQL (`SELECT`, `INSERT`, `UPDATE`, `DELETE`, `DDL`)

---

## Tecnologías Utilizadas

El proyecto fue desarrollado utilizando **Java Development Kit (JDK) 8+**.

### Librerías y APIs de Java

- **JDBC API (`java.sql.*`)**: Comunicación con bases de datos (usada a través de la librería `TablasBD`)
- **Swing (`javax.swing.*`)**: Creación de la GUI
- **API de Fecha y Hora (`java.time.LocalDate`)**: Manejo moderno de fechas
- **Clases de utilidad (`java.util.ArrayList`, `java.util.Arrays`)**: Gestión de colecciones de datos

### Librerías Externas (Dependencias)

Para que esta aplicación funcione correctamente, requiere:

- **`TablasBD.jar`**: Debe ser compilado y añadido como JAR externo.
- **Drivers JDBC específicos**:
  - SQL Server: `mssql-jdbc-12.8.1.jre11.jar`
  - MySQL: `mysql-connector-j-8.4.0.jar`

> ⚠️ **Nota**: Estos drivers no están incluidos en el JAR de la aplicación; deben ser gestionados por el entorno de desarrollo y el desarrollador respectivamente.

---

## Estructura de Clases (Cliente GUI)

El proyecto se organiza en el paquete principal:  
`PruebaMuestraDatosSQL.app.com.View`

### Clases Principales

1. **`Acceso_SGBD.java`**
   - Gestiona la ventana de inicio de sesión.
   - Permite seleccionar la base de datos y establecer la conexión.
   - Punto de entrada de la aplicación.

2. **`MuestraDatos1.java`**
   - Ventana principal luego de una conexión exitosa.
   - Área para escribir y ejecutar consultas SQL (con resaltado de sintaxis).
   - Muestra tablas y columnas de la base de datos.
   - Presenta resultados de consultas `SELECT` en una `JTable`.
   - Permite abrir archivos de texto con sentencias SQL.

---

## Cómo Compilar y Ejecutar

### 1. Obtener `TablasBD.jar`

- Asegúrate de tener el proyecto **TablasBD** (ver `README_TablasBD.txt`).
- Compila el proyecto (por ejemplo, en NetBeans: `Clean and Build Project`).
- Esto generará `TablasBD.jar` en la carpeta `dist/` del proyecto TablasBD.

### 2. Configurar Este Proyecto (`Acceso_SGBD`)

- Abre el proyecto `PruebaMuestraDatosSQL.app.com.View` en tu IDE (ej. NetBeans).
- **Añadir `TablasBD.jar`**:
  - Clic derecho en "Libraries"
  - Selecciona `Add JAR/Folder...`
  - Añade el archivo `TablasBD.jar` generado previamente
- **Incluir Drivers JDBC**:
  - De igual forma, añade:
    - `mssql-jdbc-12.8.1.jre11.jar` (para SQL Server)
    - `mysql-connector-j-8.4.0.jar` (para MySQL)

### 3. Ejecutar la Aplicación

Una vez añadidas todas las dependencias:

- Limpia y construye el proyecto
- Ejecuta la clase `Acceso_SGBD` como una aplicación Java normal

---

## Créditos

Este proyecto fue desarrollado como una herramienta de apoyo para la interacción con bases de datos desde una interfaz gráfica Java.

---
