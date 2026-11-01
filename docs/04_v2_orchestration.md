# Gemini Pro OS Personal v2 — Orchestration

## Purpose

v2 changes the operating model from a collection of AI tools coordinated manually by the user into a job-oriented system with explicit state, artifacts, gates and handoffs.

The operating rule is:

> Do not move giant prompts between apps. Move artifacts between states.

## Core object: JOB

Every substantial piece of work gets a stable `job_id` and a `manifest.yaml` based on `templates/job_manifest.yaml`.

The job, not any specific chat, is the source of operational truth.

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

A state transition happens only when its gate is satisfied. The manifest records `current`, `current_gate`, `next_action` and `blocked_by`.

## Tool routing

| Need | Default tool | Primary output |
|---|---|---|
| Discover / investigate | Gemini + Deep Research | brief/research |
| Understand selected corpus | Gemini Notebook | evidence/claims |
| Calculate / simulate / graph | Colab | reproducible evidence |
| Prototype model interaction | AI Studio | validated prototype |
| Explore/build open software objective | Antigravity | working prototype |
| Implement scoped engineering task | Jules | tested change |
| Design image identity and frames | Nano Banana 2.1 | canonical images |
| Animate approved visual | Flow | video clips |
| Assemble final audiovisual | Vids | master + derivatives |

## Image-first production rule

For audiovisual jobs, v2 inserts a mandatory visual-design stage between script and video generation:

```text
SCRIPT
  ↓
VISUAL_BIBLE
  ↓
Nano Banana 2.1 exploration
  ↓
canonical character/world references
  ↓
approved start/end frames
  ↓
Flow animation
```

Do not spend video credits to discover a character, wardrobe, world or composition that can be solved first with images.

## Standard artifacts

Every job may use these canonical artifacts:

```text
brief.md
research.md
evidence.md
script.md
visual_bible.md
storyboard.csv
flow_prompts.md
qa.md
postmortem.md
manifest.yaml
```

Not every job type needs every file. The manifest records which are relevant.

## Storage split

### GitHub

Keep reproducible state:

- manifests;
- prompts;
- scripts;
- structured storyboard;
- decisions;
- source links;
- QA;
- postmortems;
- lightweight metadata.

### Google Drive

Keep heavy binaries:

- images;
- audio;
- Flow clips;
- Vids exports;
- large source files;
- publication masters.

Recommended Drive layout:

```text
Gemini Pro OS/
  Jobs/
    JOB-.../
      01_sources/
      02_images/
      03_audio/
      04_flow/
      05_exports/
      06_published/
  Asset Library/
    characters/
    environments/
    b_roll/
    graphics/
  Archive/
```

## Prompt packet contract

A handoff prompt should be small and reference stable artifacts rather than repeat the entire project context.

```text
JOB: JOB-2026-001
TASK: S07
CONTEXT: visual_bible.md + storyboard row S07
INPUT: approved start frame
ACTION: describe the requested movement
DO_NOT_CHANGE: list immutable visual traits
OUTPUT: expected artifact
```

## Storyboard contract

`templates/storyboard.csv` is the canonical shot-level control plane for video jobs. A row should answer:

- why the shot exists;
- what the viewer hears;
- what must be seen;
- which tool/model should create it;
- continuity requirements;
- maximum accepted credits;
- current status;
- asset lifecycle state.

## Asset lifecycle

Each generated asset receives exactly one state:

- `DRAFT`: still under evaluation;
- `KEEP`: belongs in the current job;
- `LIBRARY`: reusable beyond the current job;
- `DISCARD`: no further value.

The postmortem records what was learned from discarded attempts when useful.

## Dashboard

`dashboard.csv` is the initial v2 control center. One row per active job.

The dashboard is not a content database. It is a decision surface showing:

- current state;
- active gate;
- next action;
- blocker;
- priority;
- resource budget and spend.

## Automation maturity

### L0 — manual
User moves everything.

### L1 — guided
System recommends the next action.

### L2 — structured automation
System creates jobs, templates, folders, dashboards and standardized handoffs.

### L3 — execution automation
System executes safe repeatable tasks and updates state.

### L4 — supervised agent
System advances multiple stages autonomously and stops at explicit approval gates.

v2 starts at **L2**. Autonomy is intentionally not the first milestone.

## v2 success criteria

The system succeeds when:

1. a project can be resumed from repository state without reconstructing a chat;
2. the next action is visible from the manifest/dashboard;
3. prompts are short because stable context lives in artifacts;
4. visual consistency is solved before expensive video generation;
5. completed jobs leave reusable knowledge and assets;
6. postmortems improve the next job.
