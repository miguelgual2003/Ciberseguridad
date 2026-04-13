El ataque de fuerza bruta es el método más exhaustivo y menos sofisticado: consiste en probar todas las combinaciones posibles de caracteres hasta dar con la correcta.

### A. Perfil del atacante

- **Quién:** Desde "script kiddies" usando herramientas automatizadas hasta grupos organizados que buscan acceso a servidores SSH o paneles de administración.
    
- **Por qué:** Cuando otros vectores de ataque fallan, la fuerza bruta es la garantía matemática de éxito, siempre que se disponga de tiempo y potencia de cálculo.
    

### B. Vector de ataque (Paso a paso)

1. **Identificación del objetivo:** El atacante localiza un punto de entrada (login, puerto 22, archivo ZIP cifrado).
    
2. **Configuración de parámetros:** Define la longitud de la contraseña (ej. 6 a 8 caracteres) y el juego de caracteres (letras, números, símbolos).
    
3. **Ejecución:** El software (como `Hashcat` o `John the Ripper`) comienza a probar combinaciones secuencialmente.
    
4. **Acceso:** El sistema acepta una combinación y el atacante obtiene la clave.
    

### C. Funcionamiento técnico interno

El éxito depende totalmente de la **Entropía** de la contraseña.

- **Ataque Online:** El atacante realiza peticiones al servidor real. Es lento y fácil de detectar por los logs de fallos.
    
- **Ataque Offline:** El atacante roba el archivo de hashes de contraseñas de la base de datos y realiza las pruebas en su propio hardware (usando GPUs masivas), lo que permite probar miles de millones de combinaciones por segundo sin que nadie lo note.
    

### D. Impacto y consecuencias

- Compromiso total de la cuenta.
    
- Si la cuenta tiene privilegios elevados, compromiso total del sistema.
    

### E. Mitigación, detección y respuesta

- **Mitigación:** Políticas de contraseñas largas y complejas, bloqueo de cuentas tras _X_ intentos fallidos (Account Lockout) y uso de MFA (Autenticación de Múltiples Factores).
    
- **Detección:** Monitorización de picos inusuales en intentos de login fallidos desde una sola IP.
    

---
