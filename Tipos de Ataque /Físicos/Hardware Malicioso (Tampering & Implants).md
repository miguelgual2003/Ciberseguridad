Este ataque implica la modificación física de un dispositivo o la inserción de componentes electrónicos ocultos para interceptar datos o comprometer el sistema.

### A. Perfil del atacante

Suele ser un ataque de **insider** (empleado descontento) o un agente con acceso temporal al área (personal de mantenimiento, limpieza o un falso técnico).

### B. Vector de ataque (Paso a paso)

1. **Acceso:** El atacante abre el chasis de un servidor o estación de trabajo.
    
2. **Implantación:** Conecta un pequeño dispositivo (ej. un implante en el bus PCIe o un interceptor en el cable de red interno).
    
3. **Exfiltración:** El hardware malicioso captura el tráfico o las pulsaciones de teclas y las transmite vía radiofrecuencia (RF) o Wi-Fi independiente.
    

### C. Mitigación y Detección

- **Mitigación:** Sellos de seguridad (tamper-evident seals) que muestran si un chasis ha sido abierto. Sensores de intrusión en la placa base que desactivan el sistema si se abre la tapa.
    
- **Detección:** Inspecciones físicas periódicas y auditoría de inventario de hardware.
    

---
