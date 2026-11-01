# Gemini Pro OS Personal v2

Sistema operativo personal para convertir la suscripción **Google AI Pro** en producción real y medible, no solo en conversaciones con Gemini.

> Objetivo operativo: producir conocimiento, software, análisis y contenido audiovisual reutilizable, reduciendo al mínimo el trabajo manual de mover contexto entre herramientas.

**Última verificación de beneficios:** 2026-10-31.  
**Versión operativa:** v2 — job-oriented orchestration.

## North Star

Cada mes, la suscripción debe dejar activos concretos en cuatro frentes:

1. **Aprendizaje e investigación** — Gemini + Deep Research + Gemini Notebook.
2. **Análisis y experimentación** — Colab.
3. **Construcción** — Antigravity + Jules + AI Studio cuando corresponda.
4. **Distribución audiovisual** — Nano Banana 2.1 + Flow + Vids.

El éxito no se mide por prompts enviados, sino por artefactos terminados y reutilizables.

## Qué cambia en v2

v1 definía qué herramienta usar. v2 añade una capa de **orquestación por JOB**.

```text
INTENT
  ↓
JOB + manifest.yaml
  ↓
STATE + GATE + NEXT ACTION
  ↓
TOOL
  ↓
ARTIFACT
  ↓
NEXT STATE
```

Regla central:

> **No mover prompts gigantes entre aplicaciones. Mover artefactos entre estados.**

Cada proyecto importante tiene un `job_id`, un manifiesto, un estado actual, un gate y una siguiente acción explícita. El repo conserva el contexto reproducible; Google Drive conserva los binarios pesados.

Ver [`docs/04_v2_orchestration.md`](docs/04_v2_orchestration.md).

## Control plane v2

Componentes canónicos:

- [`templates/job_manifest.yaml`](templates/job_manifest.yaml) — fuente operativa de verdad por job.
- [`templates/storyboard.csv`](templates/storyboard.csv) — control por plano para producción audiovisual.
- [`templates/visual_bible.md`](templates/visual_bible.md) — identidad visual, continuidad y restricciones.
- [`dashboard.csv`](dashboard.csv) — vista ejecutiva de jobs activos, gates y próxima acción.

Primer job end-to-end:

- `JOB-2026-001-triple-alliance` — Guerra de la Triple Alianza como rap battle histórica.

## State machine

```text
IDEA
  ↓
RESEARCH
  ↓
EVIDENCE_READY
  ↓
SCRIPT
  ↓
VISUAL_BIBLE
  ↓
STORYBOARD
  ↓
ASSET_GENERATION
  ↓
ASSEMBLY
  ↓
QA
  ↓
READY
  ↓
PUBLISHED
  ↓
POSTMORTEM
```

No se avanza porque “ya abrimos otra app”. Se avanza cuando el gate del estado actual está satisfecho.

## Meta mensual: 10 outputs

| # | Output | Cantidad mínima | Herramienta principal | Definición de terminado |
|---|---|---:|---|---|
| 1 | Videos largos de alto valor | 4 | Gemini + Notebook + Nano Banana + Flow + Vids | 10–15 min, tesis clara, fuentes verificadas y publicación/export final |
| 2 | Shorts derivados | 12 | Gemini + Vids/Flow | 3 piezas por video largo, cada una con idea independiente |
| 3 | Dossier de investigación profunda | 1 | Gemini Deep Research | Documento con hallazgos, fuentes, contradicciones y preguntas abiertas |
| 4 | Notebook de conocimiento vivo | 1 actualización grande | Gemini Notebook | Fuentes depuradas + FAQ + síntesis + mapa de ideas del tema del mes |
| 5 | Notebook analítico reproducible | 1 | Colab | Código ejecutable, datos de entrada documentados, gráficos y conclusiones |
| 6 | Experimento cuantitativo o ML | 1 | Colab | Hipótesis, métrica, baseline, resultado y decisión siguiente |
| 7 | Mejora de software real | 1 | Jules / Antigravity | Issue o brief → implementación → tests → commit/PR o artefacto funcional |
| 8 | Prototipo interactivo | 1 | AI Studio / Antigravity | Demo utilizable que responda una pregunta o automatice una tarea concreta |
| 9 | Biblioteca audiovisual reusable | 20+ assets | Nano Banana + Flow | Personajes, fondos, B-roll, transiciones, hero shots o escenas catalogadas |
| 10 | Revisión mensual del sistema | 1 | Gemini + repo | Qué produjo valor, uso de créditos/cómputo, desperdicio y ajustes del próximo mes |

## Presupuesto operativo

### Flow

Google AI Pro incluye actualmente **1,000 créditos mensuales de Flow** y además **50 créditos diarios** que no se acumulan. Los costos oficiales pueden cambiar; la política de este repo es revisarlos antes de modificar el presupuesto.

**Reserva mensual de 1,000 créditos:**

- **400** → 4 hero shots Veo Quality (1 por video largo; 100 créditos c/u).
- **400** → hasta 20 generaciones Veo Fast (20 créditos c/u).
- **200** → hasta 20 generaciones Veo Lite (10 créditos c/u).

**Créditos diarios (50/día):** tratarlos como laboratorio que expira. Prioridad:

1. probar movimiento sobre frames ya aprobados;
2. generar variantes de B-roll;
3. validar continuidad;
4. crear assets reutilizables;
5. solo después consumir la reserva mensual.

Regla: **Quality nunca se usa para descubrir una idea.** La identidad y composición se resuelven primero con imagen; Flow se reserva para movimiento.

### Colab

Google AI Pro incluye actualmente **200 compute units por mes** y acceso ampliado a aceleradores/runtimes.

Presupuesto recomendado:

- **80 CU** → notebook analítico principal del mes.
- **60 CU** → experimento ML/IA.
- **40 CU** → visualizaciones, benchmarks o procesamiento para contenido.
- **20 CU** → contingencia.

CPU local/Colab gratuito primero; GPU/TPU solo cuando cambie materialmente el tiempo o el experimento.

## Qué herramienta hace qué

- **Gemini / Deep Research — THINK:** descubrir, investigar, cuestionar y convertir una pregunta en un brief sólido.
- **Gemini Notebook — KNOW:** trabajar con un corpus conocido; sintetizar fuentes, detectar contradicciones y conservar contexto temático.
- **Colab — PROVE:** calcular, probar, visualizar, medir y producir evidencia reproducible.
- **Antigravity — EXPLORE + BUILD:** trabajo agentic más abierto, iterativo y de exploración sobre proyectos.
- **Jules — IMPLEMENT:** delegación acotada de tareas de ingeniería con definición de terminado verificable.
- **AI Studio — PROTOTYPE:** prototipos con modelos Gemini, prompts estructurados y pruebas de interacción/modelo.
- **Nano Banana 2.1 — DESIGN:** concept art, personajes, variantes, storyboard, start/end frames y continuidad visual.
- **Flow — ANIMATE:** animar escenas ya diseñadas y construir biblioteca audiovisual; no escribir el argumento ni descubrir identidad visual cara.
- **Vids — ASSEMBLE:** ensamblar narración, clips, gráficos, capturas, voz y estructura del video final.

Ver detalles en:

- [`docs/01_monthly_system.md`](docs/01_monthly_system.md)
- [`docs/02_video_pipeline.md`](docs/02_video_pipeline.md)
- [`docs/03_tool_routing.md`](docs/03_tool_routing.md)
- [`docs/04_v2_orchestration.md`](docs/04_v2_orchestration.md)
- [`templates/video_brief.md`](templates/video_brief.md)

## Regla image-first para video largo

Un video de 10–15 minutos **no debe intentar ser 10–15 minutos de video generado por IA**.

La unidad de producción v2 es:

**tesis → evidencia → guion → Visual Bible → storyboard → frames aprobados → movimiento → montaje**

Antes de Flow:

1. Nano Banana 2.1 fija identidad de personajes.
2. Nano Banana 2.1 fija mundo, composición y estilo.
3. Se aprueban start/end frames cuando corresponda.
4. Flow recibe una intención de movimiento, no el problema completo de diseño.

## Cadencia semanal v2

- **Día 1 — THINK:** pregunta + Deep Research → `brief.md` / `research.md`.
- **Día 2 — KNOW:** Notebook + evidencia → `evidence.md`.
- **Día 3 — DESIGN:** guion + Visual Bible + storyboard + Nano Banana.
- **Día 4 — PRODUCE:** Colab + Nano Banana + Flow → assets.
- **Día 5 — ASSEMBLE:** Vids + QA + derivados + postmortem.

Meta: **1 video largo por semana**, sin comprar software adicional como condición de entrada.

## Asset lifecycle

Cada asset generado recibe un estado:

- `DRAFT` — todavía en evaluación.
- `KEEP` — entra en el job actual.
- `LIBRARY` — reusable fuera del job actual.
- `DISCARD` — no seguir invirtiendo en él.

Así, incluso los intentos no publicados dejan aprendizaje y la biblioteca audiovisual acumula valor.

## Nivel de automatización

v2 comienza intencionalmente en **L2 — structured automation**:

- crear jobs;
- crear estructura estándar;
- conservar estado;
- registrar gates;
- producir handoffs pequeños;
- mostrar la próxima acción.

No se salta directamente a un agente autónomo. Primero se construye una operación observable y reproducible.

## Fuentes oficiales verificadas

- Google AI plans (Perú): https://one.google.com/intl/es-419_pe/about/google-ai-plans/
- Google Flow credits/costs: https://support.google.com/flow/answer/16526234
- Gemini Notebook limits: https://support.google.com/gemininotebook/answer/17670842

Los límites y nombres de modelos cambian. Este repositorio guarda la estrategia; la documentación oficial de Google manda sobre cualquier número puntual.
