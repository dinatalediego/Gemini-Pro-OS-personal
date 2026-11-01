# Gemini Pro OS Personal

Sistema operativo personal para convertir la suscripción **Google AI Pro** en producción real y medible, no solo en conversaciones con Gemini.

> Objetivo operativo: producir cada mes conocimiento, software, análisis y contenido audiovisual reutilizable usando lo que ya incluye la suscripción, sin añadir herramientas pagadas por defecto.

**Última verificación de beneficios:** 2026-10-31.

## North Star

Cada mes, la suscripción debe dejar activos concretos en cuatro frentes:

1. **Aprendizaje e investigación** — Gemini + Deep Research + Gemini Notebook.
2. **Análisis y experimentación** — Colab.
3. **Construcción** — Antigravity + Jules + AI Studio cuando corresponda.
4. **Distribución audiovisual** — Gemini + Flow + Vids.

El éxito no se mide por prompts enviados, sino por artefactos terminados y reutilizables.

## Meta mensual: 10 outputs

| # | Output | Cantidad mínima | Herramienta principal | Definición de terminado |
|---|---|---:|---|---|
| 1 | Videos largos de alto valor | 4 | Gemini + Notebook + Flow + Vids | 10–15 min, una tesis clara, fuentes verificadas y publicación/export final |
| 2 | Shorts derivados | 12 | Gemini + Vids/Flow | 3 piezas por video largo, cada una con idea independiente |
| 3 | Dossier de investigación profunda | 1 | Gemini Deep Research | Documento con hallazgos, fuentes, contradicciones y preguntas abiertas |
| 4 | Notebook de conocimiento vivo | 1 actualización grande | Gemini Notebook | Fuentes depuradas + FAQ + síntesis + mapa de ideas del tema del mes |
| 5 | Notebook analítico reproducible | 1 | Colab | Código ejecutable, datos de entrada documentados, gráficos y conclusiones |
| 6 | Experimento cuantitativo o ML | 1 | Colab | Hipótesis, métrica, baseline, resultado y decisión siguiente |
| 7 | Mejora de software real | 1 | Jules / Antigravity | Issue o brief → implementación → tests → commit/PR o artefacto funcional |
| 8 | Prototipo interactivo | 1 | AI Studio / Antigravity | Demo utilizable que responda una pregunta o automatice una tarea concreta |
| 9 | Biblioteca audiovisual reusable | 20+ assets | Flow | B-roll, fondos, transiciones, hero shots o escenas catalogadas por tema |
| 10 | Revisión mensual del sistema | 1 | Gemini + repo | Qué produjo valor, uso de créditos/cómputo, desperdicio y ajustes del próximo mes |

## Presupuesto operativo

### Flow

Google AI Pro incluye actualmente **1,000 créditos mensuales de Flow** y además **50 créditos diarios** que no se acumulan. Los costos oficiales pueden cambiar; la política de este repo es revisarlos antes de modificar el presupuesto.

**Reserva mensual de 1,000 créditos:**

- **400** → 4 hero shots Veo Quality (1 por video largo; 100 créditos c/u).
- **400** → hasta 20 generaciones Veo Fast (20 créditos c/u).
- **200** → hasta 20 generaciones Veo Lite (10 créditos c/u).

**Créditos diarios (50/día):** tratarlos como laboratorio que expira. Prioridad:

1. probar composición/personaje/cámara;
2. generar variantes de B-roll;
3. validar continuidad visual;
4. crear assets reutilizables;
5. solo después consumir la reserva mensual.

Regla: **Quality nunca se usa para descubrir una idea.** Primero Lite/Omni/Fast; Quality solo para un plano que ya se sabe que vale la pena.

El upscale a 1080p figura actualmente con costo de 0 créditos para Plus/Pro/Ultra, por lo que la resolución final debe mejorarse al final y no durante las pruebas.

### Colab

Google AI Pro incluye actualmente **200 compute units por mes** y acceso ampliado a aceleradores/runtimes.

Presupuesto recomendado:

- **80 CU** → notebook analítico principal del mes.
- **60 CU** → experimento ML/IA.
- **40 CU** → visualizaciones, benchmarks o procesamiento para contenido.
- **20 CU** → contingencia.

CPU local/Colab gratuito primero; GPU/TPU solo cuando cambie materialmente el tiempo o el experimento.

## Qué herramienta hace qué

- **Gemini / Deep Research:** descubrir, investigar, cuestionar y convertir una pregunta en un brief sólido.
- **Gemini Notebook:** trabajar con un corpus conocido; sintetizar fuentes, detectar contradicciones y conservar contexto temático.
- **Colab:** calcular, probar, visualizar, medir y producir evidencia reproducible.
- **Antigravity:** trabajo agentic de desarrollo más abierto, iterativo y de exploración sobre proyectos.
- **Jules:** delegación acotada de tareas de ingeniería con definición de terminado verificable.
- **AI Studio:** prototipos con modelos Gemini, prompts estructurados y pruebas de interacción/modelo.
- **Flow:** generar/editar escenas y construir biblioteca audiovisual; no escribir el argumento.
- **Vids:** ensamblar narración, clips, gráficos, capturas, voz y estructura del video final.

Ver detalles en:

- [`docs/01_monthly_system.md`](docs/01_monthly_system.md)
- [`docs/02_video_pipeline.md`](docs/02_video_pipeline.md)
- [`docs/03_tool_routing.md`](docs/03_tool_routing.md)
- [`templates/video_brief.md`](templates/video_brief.md)

## Regla de oro para video largo

Un video de 10–15 minutos **no debe intentar ser 10–15 minutos de video generado por IA**.

La unidad de producción es:

**tesis → guion → secuencias → planos → assets → edición**

Flow se reserva para los planos que elevan la historia. El resto puede ser narración, gráficos de Colab, capturas, diagramas, texto y material generado/reutilizado.

## Cadencia semanal sugerida

- **Día 1:** pregunta + Deep Research.
- **Día 2:** Notebook + argumento + evidencia.
- **Día 3:** guion + storyboard + shot list.
- **Día 4:** Colab/Flow + producción de assets.
- **Día 5:** montaje en Vids + revisión + derivados.

Meta: **1 video largo por semana**, sin comprar software adicional como condición de entrada.

## Fuentes oficiales verificadas

- Google AI plans (Perú): https://one.google.com/intl/es-419_pe/about/google-ai-plans/
- Google Flow credits/costs: https://support.google.com/flow/answer/16526234
- Gemini Notebook limits: https://support.google.com/gemininotebook/answer/17670842

Los límites y nombres de modelos cambian. Este repositorio guarda la estrategia; la documentación oficial de Google manda sobre cualquier número puntual.
