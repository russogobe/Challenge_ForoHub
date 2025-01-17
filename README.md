# 🗨️ ForoHub API 

**ForoHub API** es un backend RESTful diseñado para gestionar un foro interactivo en el que los usuarios pueden crear tópicos, responder preguntas y participar en debates. La API incluye un sistema robusto de autenticación JWT para proteger los recursos y ofrece operaciones CRUD completas para usuarios, tópicos y respuestas. 

---

## 📋 **Índice**

1. [Características](#-características)
2. [Requisitos Previos](#-requisitos-previos)
3. [Instalación y Configuración](#-instalación-y-configuración)
4. [Rutas Principales](#-rutas-principales)
5. [Modelo de Datos](#-modelo-de-datos)
6. [Contribuciones](#-contribuciones)
7. [Licencia](#-licencia)

---

## ✨ **Características**

- ✅ Gestión de usuarios con creación, actualización y eliminación.
- ✅ Creación y administración de tópicos y respuestas.
- ✅ Soporte para validación y manejo de excepciones.
- ✅ Autenticación basada en JWT para proteger los endpoints.
- ✅ Estructura clara y modular utilizando principios de diseño limpio.
- ✅ Endpoints optimizados para búsquedas y filtros.

---

## 🛠️ **Requisitos Previos**

Asegúrate de tener instalado lo siguiente:

- **Java 17+**
- **Maven** o **Gradle**
- **MySQL** o cualquier otra base de datos compatible con JPA.
- Un cliente REST como [Postman](https://www.postman.com/) o [Insomnia](https://insomnia.rest/).

---

## 🚀 **Instalación y Configuración**

### 1️⃣ **Clonar el repositorio**

```bash
git clone https://github.com/tu_usuario/ForoHub-API.git
cd ForoHub-API

### 2️⃣ **Configurar la base de datos**

Actualiza el archivo application.properties con tus credenciales de base de datos:

properties
spring.datasource.url=jdbc:mysql://localhost:3306/forohub
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña

### 3️⃣ **Compilar y ejecutar**
Compila el proyecto con Maven y ejecuta la aplicación:

mvn clean install
mvn spring-boot:run

El servidor estará disponible en http://localhost:8080.

🔗 Rutas Principales

🔐 Autenticación
Método	Ruta	Descripción
POST	/auth/login	Iniciar sesión (obtener JWT)
POST	/auth/register	Registrar un nuevo usuario

👤 Usuarios
Método	Ruta	Descripción
GET	/usuarios	Listar todos los usuarios
GET	/usuarios/{id}	Obtener un usuario por ID
POST	/usuarios	Crear un nuevo usuario
PUT	/usuarios/{id}	Actualizar información de usuario
DELETE	/usuarios/{id}	Eliminar un usuario

📚 Tópicos
Método	Ruta	Descripción
GET	/topicos	Listar todos los tópicos
GET	/topicos/{id}	Obtener un tópico por ID
POST	/topicos	Crear un nuevo tópico
PUT	/topicos/{id}	Actualizar información del tópico
DELETE	/topicos/{id}	Eliminar un tópico

💬 Respuestas
Método	Ruta	Descripción
GET	/respuestas	Listar todas las respuestas
GET	/respuestas/{id}	Obtener una respuesta por ID
POST	/respuestas	Crear una nueva respuesta
PUT	/respuestas/{id}	Actualizar información de la respuesta
DELETE	/respuestas/{id}	Eliminar una respuesta

🗂️ Modelo de Datos
Usuario
{
  "id": 1,
  "nombre": "Juan Pérez",
  "correoElectronico": "juan.perez@example.com",
  "perfil": "ADMIN"
}

Tópico
{
  "id": 1,
  "titulo": "¿Cómo configurar Spring Boot?",
  "mensaje": "Estoy teniendo problemas con mi configuración inicial...",
  "fechaCreacion": "2025-01-15T12:30:00",
  "autor": 1,
  "curso": 2
}

Respuesta
{
  "id": 1,
  "mensaje": "Puedes usar `spring-boot-starter` para comenzar.",
  "fechaCreacion": "2025-01-15T13:00:00",
  "autor": 2,
  "topico": 1,
  "solucion": false
}

🤝 Contribuciones
¡Las contribuciones son bienvenidas! Para contribuir:

Haz un fork del repositorio.
Crea una nueva rama: git checkout -b feature/nueva-funcionalidad.
Realiza tus cambios y haz commit: git commit -m "Añadida nueva funcionalidad".
Haz push a tu rama: git push origin feature/nueva-funcionalidad.
Abre un Pull Request.

🌟 Agradecimientos
Agradecemos a todos los desarrolladores y colaboradores que han hecho posible este proyecto. ¡Gracias por formar parte de ForoHub! 🧡


