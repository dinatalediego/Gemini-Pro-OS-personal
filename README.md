# Gemini Pro OS Personal v2

Sistema operativo personal para convertir la suscripción **Google AI Pro** en producción real y medible, no solo en conversaciones con Gemini.

> Objetivo operativo: producir conocimiento, software, análisis y contenido audiovisual reutilizable, reduciendo al mínimo el trabajo manual de mover contexto entre herramientas.

**Última verificación de beneficios:** 2026-10-31.  
**Versión operativa:** v2.1 — governed jobs + mastery ladder.

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
- [`dashboard.csv`](dashboard.csv) — vista ejecutiva de jobs activos, gates, madurez y próxima acción.
- [`docs/05_mastery_ladder.md`](docs/05_mastery_ladder.md) — camino medible L0 → L5 MASTERY.

## Jobs de validación

- `JOB-2026-001-triple-alliance` — rap battle histórica; valida **image-first → Character Locks → Visual Lock → Flow**.
- `JOB-2026-002-parana-callao` — canción histórica narrativa; valida **History Master → Letter Lock → Audio Lock → Storyboard → Flow**.

Los dos jobs pueden compartir hechos históricos, pero **no comparten guion ni gates**. Perú no se presenta como miembro de la Triple Alianza militar.

## State machine base

```text
IDEA
  ↓
RESEARCH
  ↓
EVIDENCE_READY
  ↓
SCRIPT / MASTER
  ↓
LOCK
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

Cada tipo de job especializa esta máquina. No se avanza porque “ya abrimos otra app”; se avanza cuando el gate del estado actual está satisfecho.

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
- [`docs/05_mastery_ladder.md`](docs/05_mastery_ladder.md)
- [`templates/video_brief.md`](templates/video_brief.md)

## Regla image-first para video largo

Un video de 10–15 minutos **no debe intentar ser 10–15 minutos de video generado por IA**.

La unidad de producción v2 es:

**tesis → evidencia/master → lock → storyboard → frames aprobados → movimiento → montaje**

Para jobs visuales como JOB-001:

1. Nano Banana 2.1 fija identidad de personajes.
2. Cada personaje supera Character Lock.
3. Se fijan mundo, composición y lineup.
4. `VISUAL_LOCK = PASS`.
5. Flow recibe una intención de movimiento sobre referencias aprobadas.

Para jobs editoriales como JOB-002:

1. History Master gobierna hechos.
2. Letter Master debe aprobarse y congelarse.
3. Solo entonces se diseña música/audio.
4. Audio aprobado gobierna storyboard y duración.
5. Flow aparece únicamente después del storyboard y del gate de gasto generativo.

## Cadencia

La semana de 5 días sigue siendo una guía para jobs que ya tienen sus gates upstream resueltos. **Nunca reemplaza el orden canónico de un job.** Si una letra no está aprobada, el calendario no autoriza saltar a video.

## Asset lifecycle

Cada asset generado recibe un estado:

- `DRAFT` — todavía en evaluación.
- `KEEP` — entra en el job actual.
- `LIBRARY` — reusable fuera del job actual.
- `DISCARD` — no seguir invirtiendo en él.

Así, incluso los intentos no publicados dejan aprendizaje y la biblioteca audiovisual acumula valor.

## Camino a maestría

v2.1 parte en **L2 — STRUCTURED**. El objetivo no es saltar a autonomía, sino progresar:

**L0 AD HOC → L1 ROUTED → L2 STRUCTURED → L3 MEASURED → L4 LEARNING → L5 MASTERY**

La regla para declarar L5 es exigente: **3 jobs consecutivos con Mastery Score ≥90** y al menos un patrón/asset reutilizado entre ellos. Ver [`docs/05_mastery_ladder.md`](docs/05_mastery_ladder.md).

## Fuentes oficiales verificadas

- Google AI plans (Perú): https://one.google.com/intl/es-419_pe/about/google-ai-plans/
- Google Flow credits/costs: https://support.google.com/flow/answer/16526234
- Gemini Notebook limits: https://support.google.com/gemininotebook/answer/17670842

Los límites y nombres de modelos cambian. Este repositorio guarda la estrategia; la documentación oficial de Google manda sobre cualquier número puntual.
