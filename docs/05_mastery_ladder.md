# Gemini Pro OS — Mastery Ladder

La maestría no significa usar más herramientas. Significa producir activos de alta calidad con menos retrabajo, más trazabilidad y decisiones reproducibles.

## North Star de maestría

> Una idea entra una sola vez; cada etapa sabe qué artefacto recibe, qué gate debe superar y qué evidencia deja para mejorar el siguiente ciclo.

## Niveles

### L0 — AD HOC

- prompts aislados;
- contexto reconstruido manualmente;
- copy/paste frecuente;
- no existe definición de terminado;
- no se registran intentos ni aprendizajes.

**Salida:** piezas puntuales.

### L1 — ROUTED

- cada herramienta tiene una función definida;
- existe un pipeline recomendado;
- todavía depende de memoria humana para los handoffs.

**Salida:** proceso comprensible.

### L2 — STRUCTURED

- cada trabajo es un JOB;
- existe manifest, estado, gate y next action;
- los masters y assets tienen nombres canónicos;
- se separan productos con objetivos distintos;
- GitHub conserva contexto reproducible y Drive los binarios.

**Salida:** proceso repetible.

### L3 — MEASURED

Además de L2:

- cada generación registra intento, KEEP/LIBRARY/DISCARD y motivo;
- se registran créditos gastados;
- cada gate tiene checklist PASS/FAIL;
- se mide retrabajo;
- se mide porcentaje de assets reutilizados;
- se mide cuántos prompts llegan a usable output sin reescritura completa.

**Salida:** proceso medible.

### L4 — LEARNING

Además de L3:

- los postmortems modifican templates y prompt packets;
- los prompts exitosos se convierten en patrones reutilizables;
- los fallos frecuentes generan negative constraints;
- el sistema recomienda herramienta, presupuesto y siguiente acción usando evidencia histórica propia;
- se comparan resultados entre jobs del mismo tipo.

**Salida:** proceso que mejora con la experiencia.

### L5 — MASTERY

Además de L4:

- la mayor parte del contexto estable no se copia manualmente;
- el usuario interviene sobre decisiones creativas y gates, no sobre transferencia mecánica de contexto;
- los handoffs importantes pueden reconstruirse desde artefactos versionados;
- existe una biblioteca reusable de personajes, estilos, prompts, gráficos, escenas y patrones de edición;
- el presupuesto se asigna por valor esperado, no por novedad del modelo;
- el sistema puede ejecutar múltiples jobs manteniendo calidad y trazabilidad;
- el aprendizaje acumulado reduce intentos promedio por asset y tiempo hasta producto terminado.

**Salida:** una fábrica personal de activos.

## Mastery Score

Cada job se evalúa sobre 100 puntos.

| Dimensión | Peso | Señal |
|---|---:|---|
| Trazabilidad | 20 | cada salida importante apunta a fuente/master/decisión |
| Gate discipline | 20 | no se saltan gates; PASS/FAIL explícito |
| Reproducibilidad | 15 | otro ciclo puede reconstruir el proceso desde repo + Drive |
| Eficiencia | 15 | créditos/compute/reintentos controlados |
| Reutilización | 10 | assets/patrones vuelven a usarse |
| Calidad | 10 | QA editorial/técnico aprobado |
| Aprendizaje | 10 | postmortem modifica el sistema o deja una regla nueva |

### Umbrales

- 0–39 → L0/L1
- 40–59 → L2
- 60–74 → L3
- 75–89 → L4
- 90–100 → L5 MASTERY

No se puede declarar L5 por una sola pieza excelente. Requiere **3 jobs consecutivos ≥90** y al menos un asset/patrón reutilizado entre ellos.

## Gates universales

### Gate A — PURPOSE

Antes de producir:

- ¿qué debe aprender, sentir o poder hacer el usuario/espectador?
- ¿qué artefacto demuestra que terminamos?

### Gate B — SOURCE

Antes de afirmar:

- ¿hay master, fuente, cálculo o decisión explícita?

### Gate C — LOCK

Antes de generar downstream:

- ¿el artefacto upstream está aprobado/congelado cuando corresponde?

### Gate D — SPEND

Antes de gastar créditos/compute:

- ¿la generación es necesaria?
- ¿existe opción más barata/no generativa?
- ¿el prompt y criterio de éxito ya están definidos?

### Gate E — QA

Antes de publicar:

- contenido correcto;
- continuidad visual/técnica;
- derechos/fuentes cuando correspondan;
- versión final identificable.

### Gate F — LEARN

Después de terminar:

- ¿qué reutilizamos?
- ¿qué falló?
- ¿qué template/prompt/regla cambia?

## Regla del OS

**No premiar actividad. Premiar reducción de incertidumbre y activos terminados.**

Abrir Gemini, Flow, Colab o AI Studio no cuenta como progreso por sí mismo. Un gate cerrado, un master aprobado, un asset canónico o una decisión reusable sí.

## Primer camino hacia L5

1. JOB-001 prueba el pipeline visual: Nano Banana → Character Locks → Visual Lock → Flow.
2. JOB-002 prueba el pipeline editorial: History Master → Letter Lock → Audio Lock → Storyboard → Flow.
3. Un tercer job reutiliza al menos un template, prompt packet o asset de los dos anteriores.
4. Comparar métricas y corregir el sistema.
5. Repetir hasta lograr 3 jobs consecutivos con Mastery Score ≥90.
