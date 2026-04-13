Este ataque consiste en la inserción de código SQL malicioso a través de las entradas de la aplicación para manipular la base de datos subyacente.

### A. Perfil del atacante

- **Quién:** Atacantes externos que buscan acceso a datos sensibles o control total del servidor de base de datos.
    
- **Por qué:** Exfiltración de bases de datos de usuarios, robo de secretos comerciales, o escalada de privilegios para obtener una shell en el sistema operativo (vía `xp_cmdshell` en MSSQL, por ejemplo).
    

### B. Vector de ataque (Paso a paso)

1. **Identificación:** El atacante busca parámetros en la URL o formularios que interactúen con la base de datos (ej. `id=1`).
    
2. **Prueba de vulnerabilidad:** Introduce caracteres especiales como `'` o `"` para observar si la aplicación devuelve errores de sintaxis SQL.
    
3. **Extracción de estructura:** Usa comandos `UNION SELECT` para determinar el número de columnas y la versión de la base de datos.
    
4. **Exfiltración:** Ejecuta consultas para volcar tablas completas de usuarios y contraseñas.
    

### C. Funcionamiento técnico interno

El fallo ocurre cuando la aplicación **concatena** directamente la entrada del usuario en una consulta SQL en lugar de usar sentencias preparadas. Ejemplo de código vulnerable: `"SELECT * FROM users WHERE id = " + userInput;` Si el usuario envía `1 OR 1=1`, la consulta se convierte en: `SELECT * FROM users WHERE id = 1 OR 1=1;` (devolviendo todos los registros).

### D. Ciclo de vida del ataque (Kill Chain)

- **Reconocimiento:** Fuzzing de parámetros con herramientas como `sqlmap`.
    
- **Explotación:** Inyección de payloads para bypass de login o dump de tablas.
    
- **Acciones sobre objetivos:** Descarga de la base de datos o borrado de información.
    

### E. Mitigación, detección y respuesta

- **Mitigación:** Uso de **Consultas Preparadas (Prepared Statements)** y Parámetros, validación estricta de tipos de datos y el principio de mínimo privilegio en la base de datos.
    
- **Detección:** WAF (Web Application Firewall) detectando palabras clave como `UNION`, `SELECT`, `SLEEP()`.
    
- **Respuesta:** Bloqueo de la IP atacante y auditoría de qué datos fueron comprometidos.
    

---
