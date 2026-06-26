# Prompt Template

Generate each image separately. Replace the braces with task-specific content.

Before writing a generation prompt, select:

- audience preset (`exec` / `pm` / `engineer` / `customer`)
- diagram family (`workflow` / `sequence` / `state` / `deployment` / `data-lineage` / `incident-timeline` / `decision-tree` / `runbook-flow`)
- style pack (`xiaohei-default` / `minimal-monochrome` / `whiteboard-workshop` / `brand-neutral-enterprise`)
- output adapter target(s) (`blog-hero` / `slide-divider` / `docs-inline` / `social-crop` / `dark-mode-variant`)

## Sparse Xiaohei Editorial Template (Default)

```text
Generate one standalone 16:9 horizontal article illustration.

Visual DNA:
Pure white background. Minimalist black hand-drawn line art. Slightly wobbly pen lines. Lots of empty white space. Sparse Carbonclear-aligned handwritten English annotations: deep teal/slate for product or source-of-truth emphasis, muted clay/orange for the main path, red only for blockers, blue/cyan only for secondary notes. Clean absurd product-operations sketch feeling. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Recurring IP character required:
Xiaohei, a small solid-black absurd creature with white dot eyes, tiny thin legs, blank serious expression, slightly uneven hand-drawn body shape. Xiaohei must perform the core conceptual action, not decorate the scene. Make Xiaohei serious, deadpan, and slightly bizarre, not cute.

Theme:
{illustration theme}

Audience preset:
{exec / pm / engineer / customer}

Structure type:
{workflow / system detail / before-after / character state / concept metaphor / method layers / map route / comic strip}

Diagram family:
{workflow / sequence / state / deployment / data-lineage / incident-timeline / decision-tree / runbook-flow}

Style pack:
{xiaohei-default / minimal-monochrome / whiteboard-workshop / brand-neutral-enterprise}

Core idea:
{one sentence describing what the image must make obvious}

Composition:
{where Xiaohei is, what Xiaohei is doing, main objects, how information or action moves}

Suggested elements:
{element 1} / {element 2} / {element 3} / {element 4}

English handwritten labels:
{label 1} / {label 2} / {label 3} / {label 4} / {optional label 5}

Output adapters:
{blog-hero / slide-divider / docs-inline / social-crop / dark-mode-variant}

Color use:
Black for main line art and Xiaohei. Deep teal/slate for Carbonclear / Zero Ledger product or system emphasis. Muted clay/orange for main flow/path/arrows. Red only for key warnings/problems/results. Blue/cyan only for secondary notes or system state. Green only for verified/pass states when needed.

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten English labels. If the subject is Carbonclear, use accurate product language: Zero Ledger is the product, Midnight is only the theme. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, dashboard mockup, or dense explainer. Do not copy prior examples or reuse known case compositions unless explicitly requested. Invent a fresh visual metaphor for this source. It should be clear but not instructional, interesting but not childish, strange but clean.
```

## Dense Architecture Diagram Template (Explicit Request)

```text
Generate one standalone 16:9 horizontal dense architecture diagram illustration.

Visual DNA:
Pure white background. Readable technical diagram style (hand-drawn or clean line style). Dense but scannable component layout. Group related components into bounded regions. Use directional arrows with consistent semantics. No gradients, no shadows, no decorative background, no PPT title block, no realistic UI screenshot.

Mode:
Dense architecture diagram.

Theme:
{architecture theme}

Audience preset:
{exec / pm / engineer / customer}

Diagram family:
{deployment / sequence / state / data-lineage / incident-timeline / decision-tree / runbook-flow / workflow}

Style pack:
{brand-neutral-enterprise / minimal-monochrome / whiteboard-workshop / xiaohei-default}

Architecture scope:
{system context and what boundary this diagram should cover}

Core idea:
{one sentence describing what this architecture must make obvious}

Required components:
{service/component 1} / {service/component 2} / {store/queue 1} / {interface/protocol} / {boundary/trust zone}

Flow paths:
{primary data path} / {control path} / {failure or fallback path if relevant}

English labels:
Use concise technical labels only. Prefer component names, protocols, and responsibilities. Keep labels short and unambiguous.

Output adapters:
{blog-hero / slide-divider / docs-inline / social-crop / dark-mode-variant}

Color use:
Black for line art and primary labels. Deep teal/slate for core systems or source-of-truth components. Muted clay/orange for primary data flow. Red for failure/risk paths or blocked states. Blue/cyan for secondary/control-plane annotations. Green only for verified/pass states when needed.

Constraints:
One diagram explains one architecture boundary or interaction model. Favor structural accuracy and readability over visual novelty. Include clear boundaries/trust zones where relevant. Avoid mascot styling. Xiaohei is optional and should only appear if it directly clarifies an operation. Do not write a top-left title such as "Architecture". Do not turn this into a slide template or UI mockup.
```

## Prompt Contract Wrapper (v1)

When generating in automation pipelines, wrap the prompt intent with this contract:

```text
prompt_contract_version: v1
mode: {sparse-editorial | dense-architecture}
audience: {exec | pm | engineer | customer}
diagram_family: {workflow | sequence | state | deployment | data-lineage | incident-timeline | decision-tree | runbook-flow}
style_pack: {xiaohei-default | minimal-monochrome | whiteboard-workshop | brand-neutral-enterprise}
core_idea: {one sentence}
composition: {layout and action}
english_labels: [{label1}, {label2}, {label3}]
color_semantics:
  black: main line art and primary labels
  teal: core system emphasis
  orange: primary path
  red: blockers/failure
  blue: secondary notes
  green: verified pass state (optional)
accessibility_checks:
  - color meaning not color-only
  - readable labels
  - grayscale clarity
output_adapters: [{adapter1}, {adapter2}]
```

## Image Edit Prompts

Remove a title:

```text
Edit the provided image. Remove only the handwritten title "{text to remove}" and its underline from the top-left corner. Fill that area with the same clean white background, matching the surrounding blank paper. Preserve everything else exactly: characters, labels, paths, line style, composition, aspect ratio, and image quality. Do not add any new text or objects.
```

Make Xiaohei more central:

```text
Regenerate this illustration with the same core meaning and simple layout, but make Xiaohei more central to the conceptual action. Xiaohei should be doing the strange work that explains the idea, not standing beside the diagram. Keep it clean, sparse, hand-drawn, and not cute.
```

Reduce label density:

```text
Regenerate with the same concept, but cut the labels down to the 4-6 most important short English phrases. Preserve white space. Keep deep teal/slate only for product or system emphasis, clay/orange only for the main path, red only for the warning, and blue/cyan only for the secondary note.
```
