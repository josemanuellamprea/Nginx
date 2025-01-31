<h1 align="center"> INTRODUCCIÓN </h1>
<br>
<br>

![nginx1](./img/nginx1.png)

# Importancia de un Servidor Web en el Desarrollo Web y Monitorización

## 1. Importancia de un Servidor Web en el Desarrollo Web

Un **servidor web** es esencial en el desarrollo web porque actúa como el enlace que conecta las aplicaciones web con los usuarios. Los servidores web son responsables de recibir las solicitudes de los usuarios y devolver el contenido solicitado, como páginas web, archivos, imágenes o scripts.

### Funciones clave de un servidor web:

- **Gestión de peticiones HTTP/HTTPS**: Procesa solicitudes y responde con los recursos adecuados.
- **Servir contenido estático y dinámico**: Los servidores web pueden entregar tanto archivos estáticos (HTML, CSS, JS) como contenido generado dinámicamente (a través de PHP, Python, Node.js, etc.).
- **Seguridad**: Los servidores web gestionan certificados SSL/TLS para asegurar las comunicaciones mediante HTTPS.
- **Balanceo de carga**: Los servidores web modernos pueden distribuir el tráfico entre varios servidores para mejorar la eficiencia y la disponibilidad del sitio web.
- **Escalabilidad**: Permiten que las aplicaciones web crezcan fácilmente al distribuir el tráfico y las cargas de trabajo de manera efectiva.

### Ejemplos de servidores web comunes:

- **Apache**: Uno de los servidores web más populares y ampliamente utilizado.
- **NGINX**: Un servidor web conocido por su alto rendimiento y capacidad para manejar grandes volúmenes de tráfico con bajo consumo de recursos.
- **Microsoft IIS**: El servidor web de Microsoft integrado en sistemas Windows Server.

### Relevancia en el ciclo de desarrollo web:

- **Desarrollo y pruebas locales**: Los servidores web locales permiten a los desarrolladores probar aplicaciones antes de lanzarlas.
- **Despliegue de aplicaciones**: Sin un servidor web, no sería posible poner en producción una aplicación para que sea accesible por los usuarios finales.
- **Interacción con bases de datos y APIs**: Los servidores web también gestionan la interacción con bases de datos y otros servicios externos necesarios para la funcionalidad completa de una aplicación.

- # Monitorización en NGINX

NGINX es un servidor web y proxy inverso ampliamente utilizado por su alto rendimiento y capacidad para manejar múltiples conexiones simultáneas. Monitorizar NGINX es crucial para asegurar que esté funcionando de manera eficiente y para detectar problemas de rendimiento o disponibilidad antes de que afecten a los usuarios.

## 1. ¿Por qué es importante monitorizar NGINX?

La monitorización de NGINX proporciona visibilidad sobre el estado y el rendimiento del servidor web, permitiendo a los administradores de sistemas:

- **Detectar cuellos de botella**: Saber cuándo el servidor está sobrecargado o se están agotando los recursos.
- **Identificar errores en tiempo real**: Registrar y detectar fallos de configuración o errores en las solicitudes de los usuarios.
- **Optimizar el rendimiento**: Ajustar los parámetros de NGINX y del sistema operativo para maximizar el rendimiento.
- **Mantener la seguridad**: Detectar intentos de ataque, como DDoS, o intentos de acceso no autorizados.
- **Asegurar la disponibilidad**: Monitorear la disponibilidad del servidor para evitar caídas inesperadas.

## 2. Aspectos clave a monitorizar en NGINX

### 2.1. **Estado de las conexiones**

- **Conexiones activas**: El número de conexiones actuales que NGINX está manejando. Esto incluye conexiones en espera, en procesamiento y aceptadas.
- **Conexiones aceptadas y desechadas**: El número de conexiones aceptadas y desechadas, lo que puede indicar si NGINX está sobrecargado.
