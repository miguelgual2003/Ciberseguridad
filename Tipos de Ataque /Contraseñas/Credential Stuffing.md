Este ataque es uno de los más exitosos hoy en día y se basa en la **reutilización de contraseñas**.

### A. Perfil del atacante

Actores que compran bases de datos de filtraciones antiguas (ej. una filtración de LinkedIn o Adobe de hace años) en la Dark Web.

### B. Vector de ataque (Paso a paso)

1. **Obtención de datos:** El atacante consigue un volcado de correos y contraseñas de un sitio "A" que fue hackeado.
    
2. **Automatización:** Usa herramientas como `SilverBullet` o `OpenBullet` para probar automáticamente esas mismas combinaciones en sitios "B", "C" y "D" (ej. bancos, PayPal, Netflix).
    
3. **Éxito:** Debido a que la gente usa la misma clave para todo, el atacante entra en cuentas que nunca fueron hackeadas directamente.
    

### C. Impacto y consecuencias

- Acceso masivo a múltiples servicios de un mismo usuario.
    
- Ataques de "toma de control de cuenta" (Account Takeover).
    

### D. Mitigación

- **MFA (obligatorio):** Hace que las credenciales robadas sean inútiles por sí solas.
    
- **Chequeo de brechas:** Servicios como "Have I Been Pwned" integrados en la empresa para forzar cambios de clave si una cuenta aparece en una filtración.
    

---
