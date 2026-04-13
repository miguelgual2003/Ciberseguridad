Es una variante refinada de la fuerza bruta que, en lugar de probar combinaciones aleatorias, utiliza una lista predefinida de palabras probables.

### A. Perfil del atacante

Atacantes que buscan eficiencia. Saben que los humanos suelen usar palabras reales, nombres, fechas o contraseñas comunes.

### B. Funcionamiento técnico interno

El atacante utiliza listas llamadas "wordlists" (como la famosa `rockyou.txt`). Muchas veces se aplican **reglas de mutación**. Por ejemplo, si la palabra es "password", el software probará automáticamente "Password123", "p4ssword!", etc.

### C. Mitigación

Uso de **Salts** (sal) al hashear contraseñas. Un "salt" es un dato aleatorio único añadido a la contraseña antes de pasarla por la función hash, lo que invalida los diccionarios pre-calculados (Rainbow Tables).

---
