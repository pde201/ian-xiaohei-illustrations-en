---
name: ian-xiaohei-illustrations-en
description: Generate or plan sparse English Ian Xiaohei-style article and workspace illustrations. Use when Codex should create hand-drawn conceptual diagrams, article illustrations, workflow explainers, product/system metaphors, shot lists, or image edits in a clean absurd Xiaohei style with English handwritten labels.
---

# Ian Xiaohei Illustrations EN

## Purpose

Create 16:9 horizontal editorial illustrations that turn one important idea, workflow, boundary, or metaphor into a clean hand-drawn English explainer. The default visual character is Xiaohei: a small solid-black deadpan operator who performs the core conceptual action.

This is not for polished commercial illustration, formal architecture diagrams, PPT infographics, realistic UI mockups, or cute mascot art.

## References

Load only the reference files needed for the task:

- `references/style-dna.md`: visual rules, color use, text density, and hard no-goes.
- `references/xiaohei-ip.md`: Xiaohei character rules, actions, and failure modes.
- `references/composition-patterns.md`: composition types and original metaphor generation.
- `references/prompt-template.md`: single-image generation and edit prompt templates.
- `references/qa-checklist.md`: post-generation checks and iteration guidance.

## Workflow

### 1. Understand the Source

Read the article, repository notes, screenshot, rough prompt, or page the user gives. Extract:

- the core idea or judgment
- the cognitive turn the image should anchor
- the input/output relationship, boundary, before/after state, or failure mode
- what should stay as text instead of becoming an image

Do not illustrate everything. Choose the highest-value cognitive anchor.

### 2. Produce a Shot List When Asked to Plan

If the user asks to analyze, plan, or suggest illustrations, return a concise shot list. For each image include:

- where it belongs
- theme
- core idea
- composition type
- what Xiaohei is doing
- suggested objects
- suggested English labels

Default to 4-8 shots for a long piece, 1-3 for a short piece. Avoid turning the source into a picture book.

### 3. Generate Images When Asked to Create

If the user explicitly asks to generate, create, make, or output illustrations, do not stop for confirmation. Generate each image separately with `image_gen`.

Each image must explain one idea only. The prompt must include:

- 16:9 horizontal article illustration
- pure white background
- black hand-drawn line art
- sparse red/orange/blue English handwritten annotations
- lots of empty space
- Xiaohei as the core action subject
- no PPT, commercial illustration, cute mascot poster, dense architecture diagram, realistic UI, or top-left title

Invent a fresh metaphor from the source. Do not copy prior examples or repeat stock compositions.

### 4. QA and Iterate

After generation, apply `references/qa-checklist.md`. Regenerate or edit if:

- Xiaohei is decorative instead of doing the work
- the image is too dense or looks like a slide
- there is a top-left type title such as "workflow" or "diagram"
- labels are too long or badly misspelled
- the background is textured, shaded, or not white
- the image looks generic rather than source-specific

### 5. Save Deliverables

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
- saved paths
- which images are strongest and which are optional

Keep the explanation short; the images should carry the idea.
