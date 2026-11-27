# Registro de Casos de Prueba - Validación de Formulario

**Archivo probado:** `/proyecto/formulario.html`  
**Navegador:** Google Chrome / Mozilla Firefox  
**Fecha de ejecución:** 22/11/2026  

---

### Caso 1 (CP-01): Caso Válido Estándar
* **Datos introducidos:**
  * Email: `marc.gym@ejemplo.com`
  * Teléfono: `+34 612 345 678`
  * Fecha de nacimiento: `2002-05-14` (24 años)
  * Contraseña: `MiClaveSegura2026` (17 caracteres)
  * Peso: `78.5`
* **Resultado esperado:** Todos los campos muestran borde verde de validación y el formulario permite el envío mostrando el mensaje de confirmación.
* **Resultado real:** ✅ **ACEPTADO.** Se muestra el aviso: *"¡Perfil validado correctamente! Generando tu dieta y rutina adaptada..."*.

---

### Caso 2 (CP-02): Caso Inválido — Email Vacío o Mal Formado
* **Datos introducidos:**
  * Email: *(vacío)* / `marc.gym.ejemplo.com`
  * Resto de campos: Válidos.
* **Resultado esperado:** El navegador bloquea el envío, enfoca el campo Email y muestra el aviso de error nativo y el mensaje accesible.
* **Resultado real:** ✅ **RECHAZADO.** El formulario no se envía y exige completar/corregir el formato de correo electrónico.

---

### Caso 3 (CP-03): Caso Inválido — Teléfono Incorrecto
* **Datos introducidos:**
  * Teléfono: `abc123` (y segunda prueba con `612345678` sin prefijo ni espacios).
  * Resto de campos: Válidos.
* **Resultado esperado:** El atributo `pattern="^\+34 [0-9]{3} [0-9]{3} [0-9]{3}$"` rechaza la entrada.
* **Resultado real:** ✅ **RECHAZADO.** Se resalta el borde en rojo y aparece el mensaje: *"El teléfono debe seguir exactamente el formato +34 XXX XXX XXX"*.

---

### Caso 4 (CP-04): Caso Inválido — Fecha Futura / Menor de Edad
* **Datos introducidos:**
  * Fecha de nacimiento: `2012-06-10` (menor de 18 años).
  * Resto de campos: Válidos.
* **Resultado esperado:** El atributo `max="2008-11-22"` impide seleccionar la fecha en el calendario y rechaza el envío si se escribe manualmente.
* **Resultado real:** ✅ **RECHAZADO.** El navegador indica que el valor debe ser igual o anterior al `22/11/2008`.

---

### Caso 5 (CP-05): Caso Edge — Solo Campos Obligatorios Mínimos
* **Datos introducidos:**
  * Email: `a@b.es`
  * Teléfono: `+34 600 000 000`
  * Fecha de nacimiento: `2008-11-22` (justo 18 años cumplidos hoy)
  * Contraseña: `12345678` (exactamente 8 caracteres)
  * Peso: *(vacío, campo opcional)*
* **Resultado esperado:** Al cumplir los valores límite exactos y omitir el campo opcional, el formulario debe aceptarse.
* **Resultado real:** ✅ **ACEPTADO.** El formulario valida todos los requisitos mínimos y completa el envío sin errores.