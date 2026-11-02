# QA — Paraguay — Attempt 01

**Job:** JOB-2026-001-triple-alliance  
**Gate:** CHARACTER_LOCK_PARAGUAY  
**Source:** Google Flow / Nano Banana 2.1 outputs supplied by user on 2026-11-01  
**Status:** ITERATE

## Assets reviewed

- `Man_holding_microphone_in_costume_638fbac8_2K.jpg` — single full-body candidate.
- `Man_holding_vintage_microphone_ddc2a3b8_2K.jpg` — three-view collage, but all views are frontal/three-quarter variants; not a true turnaround.

## What works

- Strong face continuity across the provided variants.
- Hair and beard are visually stable.
- Body proportions are coherent.
- Dark military coat + deep red accents + sword language is consistent enough for a first pass.
- No modern streetwear, sneakers, headphones, sunglasses or fantasy armor.
- Performance attitude comes from pose and microphone rather than modern clothing.
- Single full-body asset is clean enough to use as the anchor for the next iteration.

## Gate checklist — attempt 01

| Criterion | Result | Note |
|---|---|---|
| Same facial identity across required A/B/C | INCOMPLETE | Portrait B missing; C not valid turnaround. |
| Same hair and beard | PASS | Stable in supplied images. |
| Same body proportions | PASS | No meaningful drift observed. |
| Same coat construction and red accents | FAIL | Epaulettes/medals/shoulder treatment vary between the collage and single full-body image. |
| Same belt/sword placement | PASS | Broad placement remains coherent. |
| 1860s silhouette remains plausible | PASS | Military silhouette reads nineteenth-century; microphone is treated as theatrical prop. |
| Rap-battle attitude comes from pose, not modern clothes | PASS | Good. |
| No accidental Brazil/Argentina/Uruguay visual coding | PASS | Paraguay identity remains distinct. |
| Full body usable as future image reference | PASS | Use the single full-body image as the working anchor. |
| Portrait usable as face reference | FAIL | Missing. |
| Turnaround usable as costume reference | FAIL | No true rear view; collage is three near-frontal variants. |
| Historical reference alignment | FAIL | Before canon, align face/uniform more closely with period portraits and documented Solano López gala uniform. |

**Provisional result:** 7 PASS / 12 total criteria; gate not passed.

## Historical alignment note

Period portraits and later documentation consistently show Solano López with formal military epaulettes, decorations/medals and a sash across the torso; descriptions of gala dress also mention a blue coat with red facings, gold trim, close-fitting blue trousers with gold stripes, polished boots, sword and a feathered bicorne. For this fictional rap-battle universe we can simplify these details, but the final canon should visibly inherit them rather than drift into a generic officer design.

## Decision

Do **not** move to Brazil yet.

Use the single full-body image as the visual anchor for Attempt 02, but revise the canonical costume specification before generating B/C.

## Next action

Run `prompt_packets/01b_paraguay_retry.md` using the single full-body asset as image reference. Generate:

1. corrected canonical full-body if needed;
2. chest-up portrait with identical face/costume;
3. true turnaround with front + 3/4 + back views.

Then repeat QA. `CHARACTER_LOCK_PARAGUAY` requires all criteria PASS.
