# Tool routing — qué dejarle a cada herramienta

El objetivo de esta matriz es evitar el error más caro del ecosistema: usar todas las herramientas como si fueran “otro chat”.

## Regla de enrutamiento

Elegir herramienta según la naturaleza del trabajo:

| Si la pregunta es… | Herramienta por defecto |
|---|---|
| “¿Qué sabemos del tema y qué dice la web?” | Gemini + Deep Research |
| “¿Qué dicen exactamente estas fuentes que elegí?” | Gemini Notebook |
| “¿Qué pasa si calculo, simulo, entreno o grafico esto?” | Colab |
| “¿Puedes implementar este cambio concreto en un repo?” | Jules |
| “¿Puedes explorar/construir iterativamente este proyecto?” | Antigravity |
| “¿Cómo pruebo una interacción/modelo rápidamente?” | AI Studio |
| “¿Cómo convierto esta idea en una escena?” | Flow |
| “¿Cómo convierto todos los assets en una pieza terminada?” | Vids |

## Gemini + Deep Research

### Sí

- explorar temas nuevos;
- comparar enfoques;
- buscar evidencia actual;
- detectar tendencias;
- construir un mapa inicial del problema;
- generar briefs;
- formular mejores preguntas.

### No

- usarlo como repositorio estable de fuentes;
- delegarle cálculos que deberían ser reproducibles;
- aceptar afirmaciones críticas sin fuente;
- pedirle directamente “haz un video largo” y saltar el diseño argumental.

### Output esperado

`research_brief.md`

## Gemini Notebook

### Sí

- trabajar con PDFs, documentos y fuentes seleccionadas;
- preguntar sobre un corpus delimitado;
- comparar documentos;
- construir síntesis;
- extraer preguntas frecuentes;
- descubrir contradicciones internas;
- preparar material de estudio;
- crear una base temática que siga viva durante semanas o meses.

### No

- usarlo como sustituto de Deep Research cuando falta explorar la web;
- meter fuentes sin curarlas;
- convertirlo en un depósito infinito de documentos irrelevantes.

### Regla

**Deep Research descubre. Notebook consolida.**

## Colab

### Sí

- análisis de datos;
- simulación;
- ML;
- embeddings/benchmarks;
- procesamiento de archivos;
- gráficos aesthetic;
- generación de evidencia cuantitativa para videos;
- experimentos con GPU/TPU cuando sea necesario.

### No

- gastar compute para tareas que un script local resuelve fácilmente;
- entrenar algo sin baseline;
- correr GPU porque está disponible;
- usarlo para producir una conclusión que no queda reproducible.

### Regla

**Compute debe comprar evidencia.**

### Budget mensual

- 80 CU análisis principal;
- 60 CU experimento ML/cuanti;
- 40 CU procesamiento/visuales;
- 20 CU reserva.

## Jules

### Mejor uso

Tareas de ingeniería **bien delimitadas**.

Ejemplo de buen encargo:

> En este repo, agrega validación X al pipeline Y. Conserva comportamiento Z. Añade tests para A/B/C. No cambies el contrato público. Entrega diff, tests ejecutados y cualquier limitación.

### Evitar

> Mejora este proyecto.

### Delegar

- issues acotados;
- refactors pequeños con contrato claro;
- tests;
- documentación técnica ligada al código;
- automatizaciones discretas;
- reparaciones reproducibles.

## Antigravity

### Mejor uso

Trabajo agentic más abierto que requiere explorar, probar e iterar.

Delegar cuando la tarea necesita:

- entender varias partes de un proyecto;
- probar hipótesis de implementación;
- construir un prototipo;
- hacer varias iteraciones conectadas;
- navegar un problema con más autonomía que un issue cerrado.

### Diferencia práctica con Jules

- **Jules:** “aquí está el contrato; implementa esta pieza”.
- **Antigravity:** “aquí está el objetivo; explora el proyecto y encuentra una ruta para conseguirlo”.

No usar Antigravity para una tarea de dos líneas perfectamente especificada.

## AI Studio

### Sí

- probar prompts estructurados;
- comparar comportamiento de modelos;
- experimentar con inputs multimodales;
- diseñar una interacción antes de llevarla a producto;
- construir demos pequeñas con Gemini;
- validar si una idea merece convertirse en software.

### No

- convertir cada experimento en una aplicación;
- confundir una demo con un producto listo para usuarios.

### Output esperado

Una demo que permita responder “¿esto funciona suficientemente bien para seguir?”

## Flow

### Sí

- hero shots;
- B-roll difícil de conseguir;
- metáforas visuales;
- transiciones narrativas;
- escenas imposibles o costosas de filmar;
- consistencia estilística;
- construir una biblioteca de assets.

### No

- generar cada segundo de un video largo;
- gastar Quality en pruebas;
- repetir prompts fallidos sin registrar qué cambió;
- usarlo como sustituto del guion.

### Escalera de costo

1. Lite / Omni 360 para descubrir;
2. Omni 720 / Fast para validar;
3. Quality para hero final;
4. upscale final.

## Vids

### Sí

- montaje;
- estructura final;
- narración/voz;
- integrar clips Flow;
- integrar gráficos Colab;
- integrar capturas y texto;
- producir versiones derivadas.

### No

- decidir la tesis después de haber empezado a editar;
- reemplazar la investigación por un template visual.

## Ejemplos de routing completos

### Caso A — Video sobre absorción inmobiliaria

1. Gemini Deep Research → definición, literatura y conceptos comparables.
2. Notebook → corpus seleccionado + tus notas/metodología.
3. Colab → curva de absorción, aceleración y simulaciones.
4. Gemini → guion/storyboard.
5. Flow → 8–12 planos con función narrativa.
6. Vids → video final + 3 shorts.

### Caso B — Nueva capacidad de Medallio

1. Gemini → brief de producto y criterios de aceptación.
2. Notebook → contratos/docs del dominio si hay corpus amplio.
3. AI Studio → validar interacción si usa LLM.
4. Antigravity → prototipo exploratorio.
5. Jules → cerrar tareas acotadas/tests cuando el contrato ya está claro.
6. Colab → benchmark si hay componente ML/cuanti.

### Caso C — Aprender un tema de maestría

1. Notebook → material oficial del curso.
2. Gemini → analogías y preguntas de comprobación.
3. Colab → experimentar matemáticamente cuando aplique.
4. Gemini → convertir el aprendizaje en una explicación propia.
5. Flow/Vids → solo si el tema merece convertirse en pieza audiovisual.

## Anti-patrones

- Abrir cinco herramientas para la misma pregunta.
- Usar Notebook sin fuentes curadas.
- Usar Colab sin hipótesis.
- Usar Jules sin definición de terminado.
- Usar Antigravity para tareas triviales.
- Usar Flow antes de tener storyboard.
- Usar Quality para iterar prompts.
- Crear video antes de saber qué debe aprender el espectador.

## Decisión rápida en 20 segundos

1. ¿Necesito **descubrir**? → Gemini/Deep Research.
2. ¿Necesito **entender mis fuentes**? → Notebook.
3. ¿Necesito **probar con números/código**? → Colab.
4. ¿Necesito **construir software**? → Jules/Antigravity.
5. ¿Necesito **probar una interacción IA**? → AI Studio.
6. ¿Necesito **crear escenas**? → Flow.
7. ¿Necesito **entregar la pieza audiovisual**? → Vids.
