# Prompt Template

Generate each image separately. Replace the braces with task-specific content.

```text
Generate one standalone 16:9 horizontal article illustration.

Visual DNA:
Pure white background. Minimalist black hand-drawn line art. Slightly wobbly pen lines. Lots of empty white space. Sparse Carbonclear-aligned handwritten English annotations: deep teal/slate for product or source-of-truth emphasis, muted clay/orange for the main path, red only for blockers, blue/cyan only for secondary notes. Clean absurd product-operations sketch feeling. No gradients, no shadows, no paper texture, no complex background, no commercial vector style, no PPT infographic look, no cute mascot poster, no children's illustration, no realistic UI.

Recurring IP character required:
Xiaohei, a small solid-black absurd creature with white dot eyes, tiny thin legs, blank serious expression, slightly uneven hand-drawn body shape. Xiaohei must perform the core conceptual action, not decorate the scene. Make Xiaohei serious, deadpan, and slightly bizarre, not cute.

Theme:
{illustration theme}

Structure type:
{workflow / system detail / before-after / character state / concept metaphor / method layers / map route / comic strip}

Core idea:
{one sentence describing what the image must make obvious}

Composition:
{where Xiaohei is, what Xiaohei is doing, main objects, how information or action moves}

Suggested elements:
{element 1} / {element 2} / {element 3} / {element 4}

English handwritten labels:
{label 1} / {label 2} / {label 3} / {label 4} / {optional label 5}

Color use:
Black for main line art and Xiaohei. Deep teal/slate for Carbonclear / Zero Ledger product or system emphasis. Muted clay/orange for main flow/path/arrows. Red only for key warnings/problems/results. Blue/cyan only for secondary notes or system state. Green only for verified/pass states when needed.

Constraints:
One image explains only one core structure. Keep the main subject around 40%-60% of the canvas. Preserve at least 35% blank white space. Use at most 5-8 short handwritten English labels. If the subject is Carbonclear, use accurate product language: Zero Ledger is the product, Midnight is only the theme. Do not write a title in the top-left corner. Do not write the structure type on the image. Do not make it a formal diagram, course slide, dashboard mockup, or dense explainer. Do not copy prior examples or reuse known case compositions unless explicitly requested. Invent a fresh visual metaphor for this source. It should be clear but not instructional, interesting but not childish, strange but clean.
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
