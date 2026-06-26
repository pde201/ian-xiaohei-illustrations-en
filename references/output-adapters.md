# Output Adapters

Generate a base 16:9 master image first, then adapt for target outputs.

## blog-hero

- Keep one dominant visual anchor.
- Leave clean negative space for optional headline overlay.

## slide-divider

- Strong central motif, minimal labels.
- Avoid tiny text that fails in presentation view.

## docs-inline

- Prioritize readability at smaller display width.
- Reduce decorative elements and keep labels very concise.

## social-crop

- Protect core meaning within center-safe region.
- Ensure the idea survives partial crops.

## dark-mode-variant

- Preserve white-background original and generate a dark-surface variant only when requested.
- Rebalance contrast; keep semantic color mapping consistent.

## Adapter Metadata

For each output, record:

- adapter name
- aspect/crop notes
- label density adjustment
- any color adjustments
