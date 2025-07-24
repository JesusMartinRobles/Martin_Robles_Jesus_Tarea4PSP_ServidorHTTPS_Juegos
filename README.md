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
 ┣ 📜 Paginas.java              ← HTML de los juegos y formularios
 ┣ 📜 SesionJuego.java          ← Clase que almacena el estado por sesión
 ┣ 📜 ServidorHttps.java        ← Lógica principal, sockets y rutas
 ┣ 📜 usuarios.txt              ← Registro de usuarios (local)
 ┣ 📜 logErrores.txt            ← Registro de errores con Logger
