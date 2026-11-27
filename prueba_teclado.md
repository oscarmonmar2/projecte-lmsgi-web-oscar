# Caso de Prueba de Navegación con Teclado

## ID del Caso de Prueba: CP-ACC-01
- **Objetivo:** Verificar la navegabilidad secuencial y la relación contextual de celdas mediante teclado.
- **Fecha de ejecución:** 15/10/2026
- **Entorno de pruebas:** Mozilla Firefox / Google Chrome con teclado físico.

### Pasos ejecutados:
1. Abrir `tabla.html` en el navegador.
2. Pulsar la tecla `Tab` para enfocar la primera celda del encabezado (`Toma / Hora`).
3. Continuar pulsando `Tab` secuencialmente hasta la fila "Almuerzo (14:00)" en la columna "Proteínas (g)".
4. Observar el comportamiento del foco visual (`outline`) y la interacción.

### Resultados:
- **Caso de prueba específico:** Navegar a la celda de valor "48" (Proteínas del Almuerzo).
- **Resultado Esperado:**
  1. El anillo de enfoque (`outline`) es claramente visible sobre la celda.
  2. La celda está conceptual y estructuralmente vinculada a los encabezados `scope="row"` (Almuerzo) y `scope="col"` (Proteínas).
- **Resultado Real:** ✅ **PASADO CON ÉXITO.** El indicador visual azuleja la celda enfocado y las tecnologías de asistencia asocian correctamente los encabezados.