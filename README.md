# Martin_Robles_Jesus_Tarea4PSP_ServidorHTTPS_Juegos

Proyecto académico que implementa un servidor HTTPS multihilo en Java, con autenticación segura de usuarios, manejo de sesiones mediante cookies y juegos interactivos accesibles desde el navegador web. Toda la lógica está desarrollada en Java puro, sin frameworks externos.

🎮 Juegos disponibles

- 🎲 Lanzamiento de Dados – Gana el que más puntos consiga en 5 rondas.
- 🔢 Adivina el Número – Encuentra el número secreto en 10 intentos.
- ✂️ Piedra, Papel o Tijera – Juega 5 rondas contra el servidor.

🛠️ Tecnologías y herramientas
- Java	      Lógica del servidor, multihilo y control de sesiones
- TLS/SSL	    Comunicación HTTPS cifrada (SSLServerSocket)
- AES	        Encriptación simétrica de ficheros (clave de 128 bits)
- Bcrypt	    Hash seguro para contraseñas
- Cookies	    Mantenimiento de sesión por usuario
- Logger	    Registro de errores y eventos
- HTML + CSS	Interfaz embebida directamente en clases Java

📁 Estructura del proyecto

📦Martin_Robles_Jesus_Tarea4PSP_ServidorHTTPS_Juegos
- 📜 Paginas.java              ← HTML de los juegos y formularios
- 📜 SesionJuego.java          ← Clase que almacena el estado por sesión
- 📜 ServidorHttps.java        ← Lógica principal, sockets y rutas
- 📜 usuarios.txt              ← Registro de usuarios (local)
- 📜 logErrores.txt            ← Registro de errores con Logger

🧪 Cómo ejecutar el servidor

Requisitos:
 - Java 17 o superior
 - Navegador web
 - Archivo AlmacenSSL generado con keytool (ver paso 2)

Crear el almacén de claves (AlmacenSSL):
 Ejecuta este comando en terminal:

keytool -genkey -alias servidor -keyalg RSA -keystore AlmacenSSL -validity 365

- Contraseña: 123456
- Nombre del alias: servidor

Ejecutar el servidor:

- Ejecuta la clase ServidorHttps.java desde tu IDE (como NetBeans) o consola.

Probar la aplicación:

Abre el navegador y accede a:

- https://localhost:8443

    (Es posible que debas aceptar el certificado autofirmado)

🔐 Seguridad
- Contraseñas hasheadas con Bcrypt
- Encriptación AES-128 para ficheros
- Sesiones controladas mediante cookies
- Conexiones seguras vía HTTPS (TLS)

📌 Autor

👨‍💻 Jesús Martín Robles
📅 Julio 2024 – Proyecto académico del módulo PSP (Programación de Servicios y Procesos)

✨ Créditos adicionales
- jBCrypt – Librería Java para Bcrypt
- HTML embebido personalizado con CSS básico
- Proyecto realizado en entorno NetBeans
