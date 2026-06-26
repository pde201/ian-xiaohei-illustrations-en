# QA Checklist

## Must Pass

For all modes:

- 16:9 horizontal image.
- Clean white background.
- Fresh metaphor for the source; not copied from old examples.
- One image explains one idea.
- Deep teal/slate is used only for product, system, or source-of-truth emphasis.
- Clay/orange is used only for main path or movement.
- Red is used only for warnings, problems, or key results.
- Blue/cyan is used only for secondary notes, feedback, or system state.
- Green is used only for verified/pass states when needed.
- Carbonclear illustrations use accurate language: Zero Ledger for the product, Midnight only for the theme.
- Labels are English-only and consistently named.
- Accessibility checks pass: readable labels, non-color-only meaning, grayscale clarity.

Sparse Xiaohei Editorial mode:

- Xiaohei is present.
- Xiaohei performs the core action, not decoration.
- Strange, memorable, and clean.
- Main subject does not exceed about 60% of the canvas.
- English labels are sparse, short, and readable.

Dense Architecture Diagram mode:

- Structural readability is high at a glance: groups, boundaries, and arrow direction are clear.
- Component labels are concise technical names, not narrative sentences.
- Diagram density supports architecture understanding without becoming visually chaotic.
- Xiaohei is optional; if present, it supports understanding and does not distract from architecture.

## Failure Signals

Regenerate or edit if:

- The top-left has a type title like "Workflow", "Diagram", "Architecture", or "Common Pitfalls".
- Xiaohei looks like a mascot, emoji, or children's cartoon.
- In sparse mode, the image looks like a slide, course handout, formal flowchart, or dense explainer.
- In sparse mode, there are too many nodes, arrows, labels, or props.
- In architecture mode, edges overlap excessively and key paths cannot be followed.
- In architecture mode, boundaries/trust zones are required but missing.
- In architecture mode, labels are verbose, inconsistent, or non-technical.
- Labels mix English with another language.
- Key meaning depends on color alone.
- Text becomes paragraph-like.
- The background has texture, shadow, gradient, beige tone, or noise.
- It uses a real UI screenshot or futuristic dashboard style.
- It looks like a dashboard mockup instead of a hand-drawn physical metaphor.
- It uses Midnight as a product label.
- Labels are badly misspelled or unreadable.
- The image is stiff and lacks an absurd metaphor.

## Iteration Moves

- Too ordinary: make Xiaohei perform a stranger physical action that still explains the idea.
- Too complex: delete nodes and keep one action plus 3-5 labels.
- Too cute: emphasize deadpan, blank serious expression, not mascot.
- Too PPT-like: remove title, grid, formal boxes, and excess arrows; turn it into a hand-drawn scene.
- Too generic: replace abstract boxes with a source-specific object or action.
- Text is wrong: edit locally if minor; regenerate with fewer labels if many labels are wrong.
- Architecture unreadable: regroup components into zones, reduce edge crossings, and enforce one primary data path.
- Accessibility weak: add textual/structural cues and rebalance contrast.
- Adapter output unclear: regenerate with adapter-specific crop-safe composition.

## Delivery Standard

A strong image should feel slightly strange at first glance, then become clear within one second.

If it looks like a tutorial slide instead of an odd product sketch on a blank sheet of paper, it fails.
