---
name: ian-xiaohei-illustrations-en
description: Generate or plan English editorial illustrations in flexible modes: sparse Ian Xiaohei-style explainers, dense architecture diagrams, and reusable diagram families. Use when Codex should create hand-drawn conceptual diagrams, formal architecture visuals, article illustrations, workflow explainers, product/system metaphors, shot lists, or image edits with English labels.
---

# Ian Xiaohei Illustrations EN

## Purpose

Create 16:9 horizontal editorial illustrations that turn one important idea, workflow, boundary, or architecture into a clear English explainer.

Default visual character is Xiaohei: a small solid-black deadpan operator who performs the core conceptual action in sparse editorial mode.

Use one of two rendering modes:

- **Sparse Xiaohei Editorial (default):** minimalist hand-drawn metaphor style with lots of whitespace.
- **Dense Architecture Diagram (on explicit request):** formal, component-rich, architecture-first diagrams with higher node and edge density and compact technical labels.

This skill is still not for polished commercial illustration, realistic UI mockups, or cute mascot art.

## Capability Add-ons

When useful, layer these add-ons on top of rendering mode:

- **Audience presets:** exec, PM, engineer, customer.
- **Diagram families:** workflow, sequence, state, deployment, data lineage, incident timeline, decision tree, runbook flow.
- **Source-to-shot extractor:** propose 3-8 visual candidates from source content before generating.
- **Style packs:** Xiaohei default, minimal monochrome, whiteboard workshop, brand-neutral enterprise.
- **English label pipeline:** English-only label generation and normalization.
- **Accessibility guardrails:** color meaning checks, contrast-safe accents, readable label limits.
- **Output adapters:** blog hero, slide divider, docs inline, social crop, dark-mode variant.
- **Prompt contracts:** versioned prompt schema for repeatable automation.

## References

Load only the reference files needed for the task:

- `references/style-dna.md`: visual rules, color use, text density, and hard no-goes.
- `references/carbonclear-design.md`: Carbonclear / Zero Ledger visual-system cues to use for this workspace or when the user asks for Carbon Clear alignment.
- `references/xiaohei-ip.md`: Xiaohei character rules, actions, and failure modes.
- `references/composition-patterns.md`: composition types and original metaphor generation.
- `references/prompt-template.md`: single-image generation and edit prompt templates.
- `references/qa-checklist.md`: post-generation checks and iteration guidance.
- `references/audience-presets.md`: audience-aware density, terminology, and tone rules.
- `references/diagram-families.md`: family-specific layout and labeling guidance.
- `references/source-to-shot.md`: source analysis and shot candidate extraction process.
- `references/style-packs.md`: optional visual packs and switching rules.
- `references/english-labels.md`: English-only label writing and normalization rules.
- `references/accessibility.md`: contrast and semantic accessibility checks.
- `references/output-adapters.md`: target-format export and crop guidance.
- `references/prompt-contract.md`: versioned prompt schema for reliable automation.

## Workflow

### 1. Understand the Source

Read the article, repository notes, screenshot, rough prompt, or page the user gives. Extract:

- the core idea or judgment
- the cognitive turn the image should anchor
- the input/output relationship, boundary, before/after state, or failure mode
- what should stay as text instead of becoming an image

Do not illustrate everything. Choose the highest-value cognitive anchor.

### 2. Choose Rendering Mode

Default to **Sparse Xiaohei Editorial**.

Switch to **Dense Architecture Diagram** only when the user explicitly asks for architecture diagrams, formal system diagrams, or higher technical density.

### 3. Choose Add-ons

Pick only needed add-ons:

- audience preset
- diagram family
- style pack
- output adapter(s)
- prompt contract version

English labels are always required.

### 4. Produce a Shot List When Asked to Plan

If the user asks to analyze, plan, or suggest illustrations, return a concise shot list. For each image include:

- where it belongs
- theme
- core idea
- composition type
- mode
- key actors/components
- data flow or interaction path
- suggested English labels
- target output adapter(s)

Default to 4-8 shots for a long piece, 1-3 for a short piece. Avoid turning the source into a picture book.

For sparse mode, include what Xiaohei is doing.

For architecture mode, include explicit boundaries, stores, services, interfaces/protocols, and trust or deployment zones when relevant.

Use audience presets to tune label vocabulary and technical depth.

### 5. Generate Images When Asked to Create

If the user explicitly asks to generate, create, make, or output illustrations, do not stop for confirmation. Generate each image separately with `image_gen`.

Each image must explain one idea only. The prompt must include mode-specific constraints:

#### Sparse Xiaohei Editorial mode

- 16:9 horizontal article illustration
- pure white background
- black hand-drawn line art
- sparse Carbonclear-aligned accent annotations: deep teal for product/system emphasis, muted orange for flow, red for blockers, blue only for secondary notes
- lots of empty space
- Xiaohei as the core action subject
- no PPT, commercial illustration, cute mascot poster, dense architecture diagram, realistic UI, or top-left title

#### Dense Architecture Diagram mode

- 16:9 horizontal article illustration
- pure white background
- crisp legible diagram style (hand-drawn or clean technical line style)
- denser but readable component layout with clear grouping and routing
- compact technical labels for services, stores, queues, APIs, jobs, and boundaries
- restrained Carbonclear-aligned accent annotations: deep teal for core systems, muted orange for principal data paths, red for risk/failure paths, blue for secondary/control-plane notes
- explicit boundaries/trust zones/deployment zones when relevant
- avoid lines overlapping as far as possible.
- use abstractions or simplification in favour of clarity
- optional Xiaohei only if it improves comprehension; architecture clarity takes precedence
- no decorative mascot poster styling, no realistic UI screenshot, no top-left type title

Invent a fresh metaphor from the source. Do not copy prior examples or repeat stock compositions.

When asked to design before generating, run `references/source-to-shot.md` and present candidate shots first.

When generating in a pipeline context, follow the schema in `references/prompt-contract.md`.

### 6. QA and Iterate

After generation, apply `references/qa-checklist.md`. Regenerate or edit if:

- sparse mode: Xiaohei is decorative instead of doing the work
- sparse mode: the image is too dense or looks like a slide
- architecture mode: the image is dense but unreadable, ambiguous, or structurally inconsistent
- there is a top-left type title such as "workflow" or "diagram"
- labels are too long or badly misspelled
- the background is textured, shaded, or not white
- the image looks generic rather than source-specific
- accessibility checks fail (contrast, overloaded color meaning, illegible labels)

### 7. Save Deliverables

When working inside a local workspace, copy final images into:

```text
assets/<source-slug>-illustrations/
```

Use ordered filenames:

```text
01-topic-name.png
02-topic-name.png
```

Preserve original generated files. Do not overwrite existing assets unless the user explicitly asks.

## Delivery Format

After generating, report:

- how many images were created
- each image's purpose
- each image mode (sparse or architecture)
- audience preset and diagram family used
- saved paths
- adapter outputs generated
- which images are strongest and which are optional

Keep the explanation short; the images should carry the idea.
