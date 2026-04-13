Ataque de nivel de host (endpoint) que registra cada pulsación de tecla del usuario.

### A. Perfil del atacante

Espionaje industrial o atacantes que buscan acceso a cuentas con MFA (ya que pueden ver el código que el usuario escribe si este se introduce manualmente).

### B. Funcionamiento técnico interno

- **Software Keylogger:** Malware instalado en el sistema (vía phishing o troyano) que intercepta las interrupciones del teclado a nivel de kernel o mediante APIs del sistema operativo.
    
- **Hardware Keylogger:** Un dispositivo físico conectado entre el teclado y la computadora (muy común en ataques de acceso físico).
    

### C. Ciclo de vida del ataque (Kill Chain)

- **Distribución:** Phishing con un ejecutable malicioso.
    
- **Instalación:** El keylogger se oculta como un proceso legítimo.
    
- **Exfiltración:** Los logs de teclas se envían periódicamente al atacante por email o HTTP.
    

### D. Mitigación, detección y respuesta

- **Mitigación:** Teclados virtuales en pantalla (para operaciones críticas), gestores de contraseñas (el autocompletado evita teclear) y EDR (Endpoint Detection and Response).
    
- **Detección:** Análisis de comportamiento (heurística) que detecte procesos "enganchados" al flujo de entrada del teclado.
