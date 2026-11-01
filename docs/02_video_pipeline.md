# Pipeline semanal — 1 video largo realmente bueno

Objetivo: producir **1 video de 10–15 minutos por semana** usando el ecosistema incluido en Google AI Pro y sin depender de software pagado adicional.

La tesis central del sistema es esta:

> Un video largo de calidad no se genera de una sola vez. Se diseña como argumento y se produce como una secuencia de assets.

## Arquitectura del video

Duración objetivo: **10–15 min**.

Distribución recomendada:

| Bloque | Duración | Propósito |
|---|---:|---|
| Hook | 0:00–0:45 | abrir una tensión o contradicción |
| Problema | 0:45–2:30 | explicar por qué importa |
| Modelo mental | 2:30–5:00 | enseñar el concepto |
| Caso / evidencia | 5:00–8:00 | demostrarlo con datos o ejemplo |
| Giro / objeción | 8:00–11:00 | mostrar dónde falla la intuición |
| Aplicación | 11:00–13:30 | qué hacer con lo aprendido |
| Cierre | 13:30–15:00 | síntesis + pregunta siguiente |

No todos los videos necesitan llegar a 15 minutos. Se corta cuando la tesis ya quedó demostrada.

## Mezcla visual objetivo

No intentar cubrir toda la duración con video generativo.

Para 12 minutos, una mezcla razonable es:

- **60–120 s** de escenas Flow/Veo;
- **2–4 min** de gráficos, diagramas o animaciones simples;
- **2–4 min** de capturas/demos/pantalla;
- **resto** narración, títulos, imágenes, texto y reutilización de assets.

Flow se usa donde el plano aporta emoción, metáfora, contexto, continuidad o un momento memorable.

## Presupuesto por video

La reserva mensual de 1,000 créditos se divide conceptualmente en **250 créditos por video**:

| Tipo | Generaciones por video | Créditos |
|---|---:|---:|
| Veo Quality | 1 | 100 |
| Veo Fast | 5 | 100 |
| Veo Lite | 5 | 50 |
| **Total máximo reservado** | 11 | **250** |

Los **50 créditos diarios** se usan para pruebas y variantes antes de tocar esta reserva.

No es obligatorio gastar 250. Si un video funciona con 90, los 160 restantes vuelven a la reserva mensual.

## Día 1 — Pregunta y evidencia

### Herramientas

Gemini + Deep Research.

### Resultado del día

Un `research brief` de una página que contenga:

1. pregunta central;
2. por qué debería importarle a alguien;
3. intuición común;
4. posible contradicción;
5. evidencia necesaria;
6. mejores fuentes encontradas;
7. qué podría demostrar que la tesis es incorrecta.

### Gate

No pasar a guion si todavía no existe una frase del tipo:

> “Este video demuestra que ______, aunque normalmente pensamos que ______.”

### Ejemplo

> Este video demuestra que vender más unidades este mes no necesariamente significa que un proyecto se esté acelerando, aunque el acumulado comercial parezca mejorar.

## Día 2 — Corpus y argumento

### Herramienta

Gemini Notebook.

### Qué entra

- mejores fuentes del Deep Research;
- documentación propia;
- notas;
- papers o PDFs relevantes;
- métricas/definiciones;
- resultados previos si existen.

### Qué sale

1. 10 afirmaciones respaldadas;
2. 5 objeciones;
3. 3 ejemplos concretos;
4. 3 analogías;
5. contradicciones entre fuentes;
6. vocabulario que necesita explicación;
7. estructura argumental preliminar.

### Gate

Cada afirmación importante del futuro video debe tener una fuente, un cálculo, una demo o quedar marcada explícitamente como interpretación.

## Día 3 — Guion y storyboard

### Herramienta

Gemini.

Crear dos capas separadas:

### A. Guion de narración

Debe sonar como explicación, no como informe leído.

Cada bloque debe responder al menos una de estas preguntas:

- ¿qué acaba de descubrir el espectador?
- ¿qué duda nueva se abre?
- ¿qué evidencia viene ahora?
- ¿qué estaba entendiendo mal?

### B. Storyboard / shot list

Para cada fragmento definir:

- timestamp aproximado;
- narración;
- función visual;
- asset necesario;
- fuente del asset;
- si requiere Flow;
- modelo sugerido;
- costo máximo aceptado;
- prompt;
- continuidad requerida.

### Regla de densidad

No generar una escena Flow porque “se ve bonita”. Debe cumplir al menos una función:

- abrir;
- explicar;
- emocionar;
- conectar dos secciones;
- representar una idea abstracta;
- crear identidad visual.

## Día 4 — Evidencia y producción de assets

Se ejecutan dos pistas en paralelo.

### Pista A — Colab

Usar Colab para producir evidencia que no debería inventarse visualmente:

- gráficos;
- simulaciones;
- curvas;
- cohortes;
- mapas de calor;
- animaciones simples exportables;
- tablas reducidas;
- benchmarks.

Cada gráfico debe responder una pregunta del guion.

No hacer gráficos decorativos.

### Pista B — Flow

Orden de generación:

1. **Lite / Omni 360p** para explorar;
2. **Omni 720p / Fast** para cerrar composición;
3. **Quality** solo para el hero shot validado;
4. upscale al final.

### Selección

Por cada asset guardar:

- `KEEP` — entra al video;
- `LIBRARY` — no entra, pero sirve después;
- `DISCARD` — no aporta.

Un intento fallido debe dejar aprendizaje sobre el prompt. Si no, fue desperdicio.

## Día 5 — Montaje, QA y derivados

### Herramienta principal

Google Vids, con Gemini como asistente de revisión.

### Primera pasada

Montar primero la lógica:

1. voz/narración;
2. cortes principales;
3. gráficos;
4. capturas;
5. Flow;
6. música/ambiente;
7. títulos.

No empezar por efectos.

### QA de contenido

Preguntar:

- ¿la tesis se entiende antes del minuto 2?
- ¿hay una afirmación sin evidencia?
- ¿hay 60+ segundos sin cambio conceptual o visual?
- ¿el ejemplo realmente prueba lo que decimos?
- ¿hay una sección que solo existe porque costó producirla?
- ¿el final cambia lo que el espectador entiende?

### QA de ritmo

Eliminar:

- introducciones ceremoniales;
- definiciones demasiado largas;
- repeticiones;
- B-roll sin función;
- escenas generativas que compiten con la narración;
- conclusiones que solo repiten el inicio.

## Derivación obligatoria: 3 shorts

Cada video largo genera tres piezas.

### Short 1 — Contradicción

La idea que rompe la intuición.

### Short 2 — Explicación

Un concepto que puede entenderse solo.

### Short 3 — Aplicación

Un caso, una visualización o una regla práctica.

Los shorts no deben terminar con “mira el video completo” como única propuesta de valor.

## Plantilla de shot budget

Antes de abrir Flow:

| Shot | Función | Modelo prueba | Modelo final | Máx. créditos | Estado |
|---|---|---|---|---:|---|
| S01 | Hero / hook | Fast | Quality | 120 | pendiente |
| S02 | Metáfora | Lite | Fast | 30 | pendiente |
| S03 | Contexto | Omni 360 | Omni 720 | 20 | pendiente |
| S04 | Transición | Lite | Lite | 20 | pendiente |
| S05 | Caso | Fast | Fast | 40 | pendiente |

El presupuesto se asigna a la **función narrativa**, no al entusiasmo por el modelo.

## Qué debe quedarse en el repo después de cada video

Carpeta lógica recomendada:

```text
videos/
  YYYY-MM-topic/
    brief.md
    research_notes.md
    script.md
    storyboard.csv
    flow_prompts.md
    sources.md
    postmortem.md
```

No es necesario guardar binarios pesados en Git. Guardar prompts, decisiones, enlaces y metadata para poder reproducir el proceso.

## Postmortem de 5 minutos

Después de publicar/exportar:

- mejor momento del video;
- sección más débil;
- créditos Flow gastados;
- CU Colab gastadas;
- assets que entraron;
- assets que pasan a biblioteca;
- prompt que más funcionó;
- qué cambiar en el siguiente video.

## Principio editorial

La meta no es “hacer videos con IA”.

La meta es **explicar ideas difíciles de una forma que alguien quiera terminar de ver**. La IA solo reduce el costo de investigación, análisis, producción y reutilización.
