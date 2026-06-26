# Source-to-Shot Extractor

Use this when planning illustrations from docs, PRDs, notes, or repository context.

## Input

- Article/doc text, notes, architecture summary, issue/PR context, or rough prompt.

## Output

Return 3-8 candidate shots in a compact table with:

- slot/location
- core idea
- audience preset
- diagram family
- mode (sparse or architecture)
- composition summary
- required labels (English)
- output adapters

## Extraction Steps

1. Extract high-value anchors: boundary, transition, failure, decision, or source-of-truth.
2. Merge overlapping anchors to avoid duplicate visuals.
3. Rank by explanatory value (high/medium/low).
4. Keep only highest-value candidate per repeated concept.
5. Reserve one optional shot for edge case or risk communication.

## Anti-Bloat Rules

- Do not convert every paragraph into a shot.
- One shot should explain one idea.
- Avoid repeating the same composition with different labels.
