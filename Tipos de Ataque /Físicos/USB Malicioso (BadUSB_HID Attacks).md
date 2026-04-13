No se trata de un USB con un virus "normal", sino de un dispositivo que **emula ser un teclado** para ejecutar comandos a una velocidad sobrehumana.

### A. Perfil del atacante

Atacantes que utilizan la **Ingeniería Social** (dejar el USB "olvidado" en el parking de la empresa) o acceso físico rápido (menos de 5 segundos).

### B. Funcionamiento técnico interno

Aprovecha que los sistemas operativos confían ciegamente en cualquier dispositivo **HID** (Human Interface Device) como un teclado. Al conectarse, el microcontrolador del USB envía una ráfaga de pulsaciones de teclas:

1. Abre la terminal (`Win + R` -> `powershell`).
    
2. Descarga un script malicioso de internet.
    
3. Lo ejecuta y se cierra, todo en menos de 2 segundos.
    

### C. Impacto

Ejecución de código arbitrario con los privilegios del usuario que está frente a la máquina. Instalación de backdoors o robo de cookies del navegador.

### D. Mitigación

- Deshabilitar puertos USB no utilizados.
    
- Software de **Endpoint Protection** que bloquee la conexión de nuevos dispositivos HID o que requiera aprobación del administrador.
    
- Concienciación de empleados (no conectar dispositivos desconocidos).
    

---
