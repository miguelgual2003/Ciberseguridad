Este ataque obliga al navegador de una víctima autenticada a enviar una solicitud HTTP falsificada a una aplicación web vulnerable.

### A. Perfil del atacante

- **Quién:** Atacantes que conocen la estructura de las peticiones de un sitio específico.
    
- **Por qué:** Realizar acciones en nombre del usuario (ej. cambiar contraseña, hacer una transferencia) sin que este lo note.
    

### B. Vector de ataque (Paso a paso)

1. **Sesión activa:** La víctima inicia sesión en su banco.
    
2. **Engaño:** El atacante convence a la víctima de visitar un sitio malicioso en otra pestaña.
    
3. **Petición oculta:** El sitio malicioso contiene un formulario oculto que se envía automáticamente a la URL del banco (ej. `/transferir?monto=1000&to=Atacante`).
    
4. **Ejecución:** El banco recibe la petición y, como la cookie de sesión es válida, procesa el envío.
    

### C. Funcionamiento técnico interno

El ataque explota la forma en que los navegadores gestionan las cookies: si tienes una sesión abierta, el navegador enviará automáticamente las cookies de ese dominio con cada petición, sin importar quién la originó.

### D. Mitigación, detección y respuesta

- **Mitigación:** Implementación de **Anti-CSRF Tokens** (tokens únicos y secretos por sesión que deben incluirse en cada petición POST) y uso del atributo `SameSite=Lax` en las cookies.
    
- **Detección:** Peticiones sospechosas sin el token correspondiente en los logs del servidor.
    

---
