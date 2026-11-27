# Documento de Decisiones Técnicas y Boceto - Tema 3.1: Tabla de Datos Complejos

## 1. Contexto y Temática del Proyecto
- **Temática:** FitPlan Generator / Nutrición y Salud
- **Objeto de la tabla:** Distribución nutricional diaria y macronutrientes por toma de alimentos.

## 2. Boceto Inicial y Estructura Semántica

### Diagrama conceptual:
```text
Tabla: Distribución Nutricional Diaria
========================================================================================
[Caption]: Distribución diaria de tomas de alimentos, macronutrientes y aporte calórico
----------------------------------------------------------------------------------------
Encabezados de Columna (col): 
  | Toma / Hora | Alimentos Sugeridos | Proteínas (g) | Carbohidratos (g) | Grasas (g) | Energía (kcal) |

Encabezados de Fila (row):
  | Desayuno (08:30) | Almuerzo (14:00) | Merienda (17:30) | Cena (21:30) |

Pie de tabla (tfoot):
  | Cómputo Total Diario | - | 155 g | 230 g | 74 g | 2.210 kcal |
========================================================================================