Consiste en la sustracción física de activos de hardware (laptops, smartphones, servidores, unidades de backup) para extraer la información que contienen.

### A. Perfil del atacante

- **Quién:** Desde delincuentes comunes hasta espías corporativos.
    
- **Por qué:** Venta del hardware en el mercado negro o, más críticamente, extracción de secretos comerciales, claves de cifrado y bases de datos locales.
    

### B. Funcionamiento técnico interno

Si el almacenamiento no está cifrado, el atacante no necesita la contraseña del sistema operativo. Basta con extraer la unidad (SSD/HDD), conectarla a otra máquina como unidad externa y leer todos los archivos. Incluso con contraseñas de Windows/Linux, existen herramientas de bypass que permiten resetear la clave del usuario local si se tiene acceso al arranque (boot) del sistema.

### C. Impacto y consecuencias

- **Brecha de datos masiva:** Especialmente grave si el dispositivo contiene tokens de acceso VPN o archivos de configuración sin cifrar.
    
- **Incumplimiento legal:** Multas severas (GDPR, HIPAA) por pérdida de datos personales no protegidos.
    

### D. Mitigación y Respuesta

- **Mitigación:** Cifrado de disco completo (**FDE**) mediante BitLocker, FileVault o LUKS. Uso de ranuras de seguridad Kensington. Bloqueo de puertos USB en BIOS.
    
- **Respuesta:** Borrado remoto (Remote Wipe) a través de soluciones MDM (Mobile Device Management) y revocación inmediata de todos los certificados digitales asociados al dispositivo.
    

---
