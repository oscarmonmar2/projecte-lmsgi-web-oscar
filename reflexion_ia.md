# Reflexión Crítica sobre el Uso de Inteligencia Artificial

Para la realización de esta práctica, asumí la responsabilidad directa del diseño conceptual, la maquetación HTML semántica y la definición de los atributos `scope="row"` y `scope="col"`. 

Utilicé la Inteligencia Artificial como herramienta de consulta para solicitar una estructura inicial de tabla accesible. La IA sugirió implementar identificadores únicos `id` en cada encabezado y asociarlos mediante el atributo `headers` celda por celda. 

Rechacé esa sugerencia tras verificar con el manual y las pautas del W3C que, para una tabla bidimensional estándar, el uso explícito de `<th>` con `scope` es suficiente, más eficiente y limpio. 

La prueba de navegabilidad con teclado y la validación en el W3C Markup Validator (0 errores) demuestran que el resultado final es funcional, estándar y accesible. Si la tabla creciera considerablemente en el futuro, consideraría el uso de `<colgroup>` para agrupamientos visuales adicionales.