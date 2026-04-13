Es el "hermano sigiloso" de la fuerza bruta. En lugar de probar muchas contraseñas para un solo usuario, prueba **una sola contraseña común para muchos usuarios**.

### A. Perfil del atacante

Atacantes que buscan infiltrarse en redes corporativas sin activar las alarmas de bloqueo de cuentas.

### B. Vector de ataque (Paso a paso)

1. **Recolección de nombres:** El atacante obtiene una lista de correos de la empresa (vía LinkedIn o metadatos).
    
2. **El "Spray":** Prueba una contraseña extremadamente común (ej. `Marzo2026!` o `Empresa2026`) contra _todos_ los usuarios una sola vez.
    
3. **Sigilo:** Como solo hay un fallo por usuario, no se activan las políticas de bloqueo de cuenta.
    

### C. Mitigación y Detección

- **Detección:** Analizar intentos de login fallidos a través de _múltiples_ nombres de usuario desde la misma IP o zona geográfica en un periodo corto de tiempo.
    
- **Mitigación:** Prohibir el uso de contraseñas que contengan el nombre de la empresa o el año en curso.
    

---
