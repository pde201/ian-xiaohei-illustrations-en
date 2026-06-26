# Prompt Contract

Use this schema for repeatable, automation-friendly generation.

## Version

Current version: `v1`.

## Required Fields

- `mode`: `sparse-editorial` or `dense-architecture`
- `audience`: `exec` | `pm` | `engineer` | `customer`
- `diagram_family`: `workflow` | `sequence` | `state` | `deployment` | `data-lineage` | `incident-timeline` | `decision-tree` | `runbook-flow`
- `style_pack`: `xiaohei-default` | `minimal-monochrome` | `whiteboard-workshop` | `brand-neutral-enterprise`
- `core_idea`: one-sentence target insight
- `composition`: scene/layout instructions
- `english_labels`: array of English labels
- `color_semantics`: mapping for black/teal/orange/red/blue/green usage
- `accessibility_checks`: required checks list
- `output_adapters`: target adapter list

## Optional Fields

- `xiaohei_role`
- `boundaries`
- `primary_path`
- `failure_path`
- `source_context`

## Contract Rules

- Reject prompts missing required fields.
- Keep one image per core idea.
- Keep labels English-only.
- Preserve semantic color mapping across all adapter outputs.
