# Product Overview + Technical Specs

A blueprint for generating concise, visually structured product overview and technical specification PDF assets.

This blueprint is designed for physical products, software platforms, infrastructure systems, industrial equipment, APIs, AI systems, operational offerings, and hardware/software hybrids.

The output should help readers quickly understand:

- What the product is
- What it does
- How it works
- Why it matters
- Important technical or operational considerations

## Primary Output

A professionally structured 2-page, US Letter, portrait PDF designed for:

- Sales enablement
- Product communication
- Internal alignment
- Vendor documentation
- Customer education
- Technical reference
- Executive overviews

The document should feel clear, technical but approachable, visually organized, concise, and operationally useful.

## Blueprint Files

| File | Purpose |
|---|---|
| `blueprint.yaml` | Root manifest, output contract, runtime assumptions, and source precedence rules |
| `layout.yaml` | Page structure, section placement, regions, margins, and spatial rules |
| `components.yaml` | Allowed components, elements, structural requirements, and rendering expectations |
| `content.yaml` | Content resolution, transformation, validation, tone, and fallback behavior |
| `design_kit.yaml` | Visual system, style derivation rules, fallback colors, typography, and spacing |
| `spec/` | Instructional reference diagrams that explain blueprint structure, layout intent, component roles, and composition rules. These are not visual targets for the final output. |
| `examples/` | Production-style reference outputs that communicate visual taste, hierarchy, density, pacing, and rhythm. These should guide final output appearance. |

## Suggested Workflow

1. Read `blueprint.yaml` first.
2. Read the remaining contract files: `layout.yaml`, `components.yaml`, `content.yaml`, and `design_kit.yaml`.
3. Inspect all files in `spec/` to understand structure, layout intent, component roles, and composition rules.
4. Inspect all files in `examples/` to understand the desired final-output style, visual hierarchy, density, pacing, and rhythm.
5. Treat `spec/` files as instructional diagrams only. Do not reproduce annotations, arrows, labels, callouts, wireframe marks, or schematic styling from `spec/` files in the final artifact.
6. Use supplied user intent and source material as the primary context for the specific generation.
7. Resolve content and style from source material where available.
8. Use blueprint fallbacks only when source material is incomplete or unavailable.
9. Generate the asset within the allowed layout, component, content, and design constraints.
10. Audit the final output against the blueprint before delivery.

## Source Material

At minimum, this blueprint can operate from a user intent prompt describing the desired asset.

Useful optional source materials include:

- Product webpages
- Technical specifications
- Product documentation
- Existing sell sheets
- Internal notes
- Brand guidelines
- Design references
- Product imagery
- Diagrams or screenshots
- Spreadsheets or structured product data

Source material does not need to follow exact filenames. The blueprint defines semantic resolution rules for deriving the required content and visual system from whatever source files are available.

## Generation Principles

- Preserve factual consistency with supplied source material.
- Do not invent unsupported technical claims, specifications, dimensions, compatibility details, or performance metrics.
- Favor concise grouped content over long paragraphs.
- Use the examples to infer visual density, hierarchy, and restraint.
- Treat the document as a designed PDF canvas, not an auto-flowing report.
- Keep the asset practical, scannable, and technically credible.
- Render only the sections, components, and elements explicitly allowed by this blueprint unless explicitly requested in prompt.
- If the blueprint does not mention an element, assume it is prohibited.
