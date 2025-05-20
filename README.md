Perfecto, acá tenés una versión más simple y directa del README:

---

### Control MQTT del dispositivo

El dispositivo se controla enviando mensajes a estos topics:

- `id/modo` → `1` para manual, `0` para automático  
- `id/destello` → tiempo en segundos o vacío para el tiempo por defecto
- `id/periodo` → número en segundos  
- `id/setpoint` → número (usar punto decimal, ej: `23.5`)  
- `id/rele` → `true` o `false` (solo en modo manual)

**Importante:** Si el valor enviado no es válido, el dispositivo responde con un mensaje de error.

**Respuestas:**  
El dispositivo publica todo en el tópico `id`. Ahí podés leer los estados y mensajes.
