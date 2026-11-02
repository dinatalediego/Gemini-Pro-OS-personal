# Prompt Packet 01 — Paraguay

**Job:** JOB-2026-001-triple-alliance  
**Tool:** Google Flow → Nano Banana 2.1  
**Gate:** CHARACTER_LOCK_PARAGUAY  
**Goal:** obtener una identidad visual canónica antes de cualquier animación.

## Contexto mínimo

Paraguay es el contendiente de mayor intensidad dramática del rap battle. La referencia histórica es Francisco Solano López y la estética debe sentirse 1860s, militar y teatral; el gesto escénico puede tener swagger de rap battle, pero el vestuario no debe convertirse en streetwear moderno.

## Prompt base

Create a historically grounded cinematic character reference for PARAGUAY in an 1860s South American historical rap-battle universe, inspired by Francisco Solano López. Adult man, dark swept-back hair, full dark beard and mustache, severe charismatic expression, commanding posture. Dark navy/black 19th-century military coat with deep red collar and sash accents, restrained gold embroidery and epaulettes, polished black riding boots, ceremonial sword. Add only subtle performance attitude through pose and a vintage microphone prop; no modern streetwear, sneakers, headphones, sunglasses, modern jewelry or contemporary stage equipment. Premium realistic concept-art photography, dark neutral studio background, warm theatrical rim light, visible fabric and metal textures, historically plausible silhouette, coherent anatomy. Preserve the exact same face, hair, beard, proportions, uniform design, red accents, medals, belt and sword across all variants.

## Generaciones requeridas

### A — FULL BODY
Use the base prompt and add:

> Full body, head-to-toe, neutral three-quarter standing pose, both boots visible, costume silhouette completely readable, hands clearly visible, sword and belt visible. No typography, no poster layout, no extra characters.

### B — PORTRAIT
Use the approved FULL BODY image as the visual reference and request:

> Preserve this exact character identity and costume. Chest-up portrait, neutral but intense expression, direct or slightly off-camera gaze, face unobstructed, beard/hairline clearly visible, same lighting language and same uniform collar/epaulettes. No redesign.

### C — TURNAROUND / COSTUME
Use the approved FULL BODY image as the visual reference and request:

> Preserve this exact character identity and outfit. Create a clean character turnaround / costume reference showing front, three-quarter and back views of the same man, same proportions, same uniform construction, same sash, belt, sword placement, boots and embroidery. Neutral studio background. No redesign between views.

## Negative constraints

- no modern streetwear
- no sneakers
- no baseball caps
- no sunglasses
- no headphones
- no modern handheld wireless microphone
- no fantasy armor
- no steampunk
- no crown
- no national-flag costume
- no face changes between views
- no beard or hair changes
- no extra fingers or duplicated limbs
- no text unless requested separately

## Gate checklist

Mark each criterion PASS/FAIL:

- [ ] Same facial identity in A/B/C
- [ ] Same hair and beard
- [ ] Same body proportions
- [ ] Same coat construction and red accents
- [ ] Same belt/sword placement
- [ ] 1860s silhouette remains plausible
- [ ] Rap-battle attitude comes from pose, not modern clothes
- [ ] No accidental Brazil/Argentina/Uruguay visual coding
- [ ] Full body is usable as future image reference
- [ ] Portrait is usable as face reference
- [ ] Turnaround is usable as costume reference

**Gate rule:** 10/10 required. If any identity/costume criterion fails, iterate in Nano Banana 2.1 before moving to Brazil.

## Asset naming

```text
PARAGUAY_A_fullbody_v01.png
PARAGUAY_B_portrait_v01.png
PARAGUAY_C_turnaround_v01.png
```

Approved files become:

```text
PARAGUAY_CANON_fullbody.png
PARAGUAY_CANON_portrait.png
PARAGUAY_CANON_turnaround.png
```

## What NOT to do next

Do not animate this character in Veo/Flow video yet. The next step after PASS is `CHARACTER_LOCK_BRAZIL`.
