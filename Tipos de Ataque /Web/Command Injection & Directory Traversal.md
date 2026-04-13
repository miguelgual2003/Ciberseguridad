### A. Command Injection

Ocurre cuando una aplicación pasa datos de usuario a una shell del sistema operativo.

- **Ejemplo:** Una herramienta web de "Ping" que hace `system("ping " + userIP)`. Si el usuario envía `8.8.8.8 ; cat /etc/shadow`, el servidor ejecutará ambos comandos.
    
- **Consecuencia:** Control total de la consola del servidor.
    

### B. Directory Traversal (Path Traversal)

Es una variante del LFI centrada específicamente en navegar fuera del directorio raíz web (`/var/www/html`) usando secuencias `../`.

- **Objetivo:** Leer archivos fuera de la carpeta pública del servidor web.
