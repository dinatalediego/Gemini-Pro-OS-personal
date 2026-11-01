# Sistema mensual de producción

Este documento convierte Google AI Pro en una cartera mensual de entregables. La regla es simple: **cada capacidad debe producir un activo**.

## Scorecard mensual

| Output | Objetivo | KPI mínimo | Reutilización esperada |
|---|---:|---|---|
| Videos largos | 4 | 10–15 min, tesis + evidencia + cierre | Shorts, posts, demos, aprendizaje |
| Shorts | 12 | 3 por video largo | Distribución y testing de hooks |
| Dossier Deep Research | 1 | 10+ fuentes útiles y contradicciones explícitas | Guiones, decisiones, aprendizaje |
| Notebook de conocimiento | 1 actualización | corpus limpio + FAQ + síntesis | consultas futuras y scripting |
| Colab analítico | 1 | ejecutable de punta a punta | gráficos, evidencia, portafolio |
| Experimento ML/cuanti | 1 | baseline + métrica + conclusión | Medallio, aprendizaje, contenido |
| Mejora de software | 1 | tests + commit/PR/artefacto | productividad y portafolio |
| Prototipo interactivo | 1 | demo funcional | validación de producto |
| Assets audiovisuales | 20+ | catalogados y recuperables | próximos videos |
| Retro mensual | 1 | decisiones de mantener/cambiar/eliminar | mejora del OS |

## 1. Cuatro videos largos

No deben ser cuatro temas aleatorios. El mes debe tener un **arco editorial**.

Ejemplo para un mes centrado en Decision Intelligence inmobiliaria:

1. Cómo saber si un proyecto realmente está acelerando sus ventas.
2. Por qué “meses para agotar stock” puede engañar.
3. Cómo detectar desaceleración antes de que el acumulado la esconda.
4. Qué debería aprender una IA del ciclo comercial histórico.

Cada video debe producir al menos:

- 1 pieza larga de 10–15 min;
- 3 shorts;
- 1 gráfico o visual reusable;
- 1 idea que vuelva al Notebook como conocimiento;
- 1 mejora al banco de prompts/shot patterns.

## 2. Doce shorts

No son simples recortes. Cada uno debe poder entenderse sin ver el video largo.

Tipos recomendados:

- **Hook:** una contradicción sorprendente.
- **Concepto:** una explicación de 30–90 s.
- **Aplicación:** un caso de negocio o demo.

## 3. Un dossier de Deep Research

Debe responder una pregunta importante que valga más que una búsqueda normal.

Estructura mínima:

- pregunta de decisión;
- qué sabemos;
- evidencia a favor;
- evidencia en contra;
- conceptos relacionados;
- fuentes primarias o de alta autoridad;
- qué todavía no sabemos;
- 5 ideas de contenido o experimentos derivados.

No convertir Deep Research en acumulación de links. El output debe servir para tomar una decisión o crear algo.

## 4. Un Notebook de conocimiento vivo

Gemini Notebook se usa cuando importa **el corpus**, no cuando importa navegar la web abierta.

Cada mes:

- retirar fuentes obsoletas o pobres;
- agregar las mejores fuentes del dossier;
- incorporar documentos propios útiles;
- generar una síntesis ejecutiva;
- mantener una FAQ de conceptos difíciles;
- registrar contradicciones entre fuentes;
- extraer analogías y ejemplos reutilizables.

## 5. Un Colab analítico reproducible

Debe tener una pregunta real y generar evidencia.

Formato:

1. `00_contexto`
2. `01_datos`
3. `02_calidad`
4. `03_transformacion`
5. `04_analisis`
6. `05_visualizaciones`
7. `06_conclusiones`
8. `07_siguientes_pruebas`

Ejemplos adecuados:

- aceleración/desaceleración de absorción;
- cohortes comerciales;
- lead episodes y conversiones;
- simulaciones de stock;
- benchmarking de modelos;
- visuales explicativos para un video.

## 6. Un experimento cuantitativo o ML

Debe ser pequeño y falsable.

Plantilla:

- **Hipótesis**
- **Target / variable de interés**
- **Event time / cutoff**
- **Baseline**
- **Métrica**
- **Resultado**
- **Leakage checks**
- **Decisión**: descartar / iterar / productizar

La meta no es entrenar modelos por entrenarlos. La meta es comprar evidencia con compute.

## 7. Una mejora real de software

El trabajo delegado a Jules o Antigravity debe empezar desde un contrato de salida.

Ejemplos:

- agregar una prueba que cierre una brecha conocida;
- automatizar una tarea manual repetitiva;
- crear un pequeño parser;
- mejorar una exportación;
- construir un prototipo sobre un repo existente;
- documentar y resolver una deuda técnica delimitada.

**No delegar:** “mejora el repo”.

**Sí delegar:** “implementa X, conserva Y, agrega tests A/B/C y entrega evidencia Z”.

## 8. Un prototipo interactivo

AI Studio o Antigravity deben producir una prueba que permita sentir la propuesta, no un mockup bonito.

Ejemplos:

- explicar una métrica y responder por qué cambia con filtros;
- consultar un corpus técnico;
- transformar un brief en storyboard;
- clasificar una entrada y devolver evidencia;
- generar una recomendación con trazabilidad.

## 9. Veinte assets audiovisuales reutilizables

Guardar por intención, no solo por fecha.

Taxonomía sugerida:

- `hero/`
- `data/`
- `office/`
- `real_estate/`
- `ai/`
- `transitions/`
- `backgrounds/`
- `characters/`

Por asset registrar:

- prompt;
- modelo;
- duración;
- costo de créditos;
- tema;
- si mantiene continuidad con otro asset;
- calificación 1–5.

## 10. Una retro mensual

Preguntas obligatorias:

1. ¿Qué output generó más valor?
2. ¿Qué output quedó a medio terminar?
3. ¿Qué herramienta usamos para algo que otra hacía mejor?
4. ¿Dónde gastamos Flow sin obtener material usable?
5. ¿Dónde gastamos compute sin cambiar una decisión?
6. ¿Qué asset se reutilizó más?
7. ¿Qué tema merece convertirse en serie?
8. ¿Qué debemos dejar de producir el próximo mes?

## Presupuesto Flow

### Reserva mensual: 1,000 créditos

Plan base recomendado:

| Uso | Unidades | Costo unitario actual | Total |
|---|---:|---:|---:|
| Veo 3.1 Quality hero | 4 | 100 | 400 |
| Veo 3.1 Fast | 20 | 20 | 400 |
| Veo 3.1 Lite | 20 | 10 | 200 |
| **Total** | | | **1,000** |

Esto es una **envolvente**, no una obligación. Si Omni Flash produce el plano correctamente por menos créditos, se prefiere.

### Créditos diarios: 50

Su función es reducir incertidumbre antes de usar la reserva mensual.

Ejemplo de día creativo:

- 2 Lite = 20;
- 1 Fast = 20;
- 1 Omni Flash 6 s = 5–10 según resolución;
- saldo restante para variante adicional.

La regla es gastar primero en **preguntas visuales**: “¿funciona esta cámara?”, “¿este personaje es consistente?”, “¿este concepto se entiende?”.

## Presupuesto Colab: 200 CU

| Uso | Presupuesto objetivo |
|---|---:|
| Notebook analítico principal | 80 CU |
| Experimento ML/cuanti | 60 CU |
| Procesamiento/visuales/benchmarks | 40 CU |
| Reserva | 20 CU |

No quemar CU en preparación de datos que puede ejecutarse razonablemente en CPU.

## Cierre mensual

El mes está cerrado cuando existen artefactos recuperables y no solo sesiones de chat. Como mínimo deben quedar enlaces o archivos para los 10 outputs y una decisión explícita sobre qué repetir el siguiente mes.
