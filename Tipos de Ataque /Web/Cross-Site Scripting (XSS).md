El XSS permite ejecutar scripts maliciosos (generalmente JavaScript) en el navegador de un usuario que visita una página web legítima.

### A. Perfil del atacante

- **Quién:** Atacantes que buscan comprometer las cuentas de usuarios específicos o distribuir malware.
    
- **Por qué:** Secuestro de sesiones, robo de cookies, defacement de sitios o redirecciones maliciosas.
    

### B. Vector de ataque (Paso a paso)

1. **Reflejado:** El atacante envía un enlace con el script en la URL a la víctima.
    
2. **Persistente (Stored):** El atacante guarda el script en la base de datos del sitio (ej. en un comentario o perfil).
    
3. **Ejecución:** Cuando la víctima carga la página, su navegador ejecuta el código del atacante creyendo que proviene del servidor legítimo.
    

### C. Funcionamiento técnico interno

El navegador confía en el contenido que llega del servidor. Si el servidor no "sanea" la entrada y la devuelve tal cual al HTML, el atacante puede inyectar etiquetas `<script>`.

- **XSS Persistente:** Es el más peligroso; el script se ejecuta para _cada_ usuario que vea el contenido infectado.
    

### D. Impacto y consecuencias

- **Robo de Cookies:** Acceso a la sesión del usuario (Session Hijacking).
    
- **Phishing interno:** Modificación del DOM para mostrar formularios de login falsos sobre la página real.
    

### E. Mitigación, detección y respuesta

- **Mitigación:** **Output Encoding** (convertir `<` en `&lt;`), uso de la directiva **Content Security Policy (CSP)** para restringir de dónde se pueden cargar scripts.
    
- **Detección:** Escaneos DAST (Dynamic Application Security Testing) y logs de WAF.
    
- **Respuesta:** Limpieza de la base de datos de entradas maliciosas e invalidación de sesiones de usuario.
    

---
