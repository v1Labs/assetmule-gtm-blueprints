# AssetMule GTM Blueprints

AssetMule GTM Blueprints is an open-source library of structured AI blueprints for generating high-quality go-to-market assets.

A blueprint is not just a prompt. It is a reusable rendering contract that packages layout, content rules, component constraints, design guidance, examples, and output requirements into a folder an AI tool can read.

The goal is to help teams generate useful GTM assets with more consistency, less reinvention, and fewer hallucinated design elements.

## Why blueprints exist

AI tools are getting better at design, but prompt-only workflows are still inconsistent.

A vague prompt often leaves too much open to interpretation. The model may invent sections, over-design the page, ignore visual hierarchy, or add conventional elements that were never requested.

Blueprints solve this by giving the AI a clearer contract:

- what artifact to create
- what sections are allowed
- what components may be used
- how content should be resolved from source material
- how the visual system should be derived
- what examples should influence the output
- what must not be invented
- how the final output should be audited

Prompts are instructions. Blueprints are reusable systems.

## What blueprints are for

These blueprints are designed for practical go-to-market work, including:

- product one-pagers
- technical specification sheets
- sales enablement assets
- comparison pages
- launch materials
- customer education documents
- internal alignment artifacts
- product marketing collateral

The first blueprint in this repo is a Product Overview + Technical Specs PDF blueprint.

## Who this is for

This project is for:

- founders
- product marketers
- GTM engineers
- sales enablement teams
- AI operators
- designers experimenting with AI-assisted asset generation
- builders creating repeatable content and design workflows

## Repository structure

    .
    ├── blueprints/
    │   └── product-overview_technical-specs/
    │       ├── README.md
    │       ├── blueprint.yaml
    │       ├── layout.yaml
    │       ├── components.yaml
    │       ├── content.yaml
    │       ├── design_kit.yaml
    │       ├── spec/
    │       │   └── structure-reference.png
    │       └── examples/
    │           └── apex-one-pager-technical-specs.pdf
    ├── CONTRIBUTING.md
    ├── LICENSE
    └── README.md

## Anatomy of a blueprint

Each blueprint is a folder-based contract. The current blueprint structure includes:

| File or folder | Purpose |
|---|---|
| `README.md` | Explains the blueprint’s purpose, use cases, workflow, and source material expectations |
| `blueprint.yaml` | Root manifest, output contract, rendering policy, imports, and audit requirements |
| `layout.yaml` | Page structure, explicit regions, placement rules, margins, and spatial constraints |
| `components.yaml` | Allowed components, required elements, prohibited defaults, and rendering behavior |
| `content.yaml` | Content requirements, source resolution rules, transformations, tone, and fallback behavior |
| `design_kit.yaml` | Visual system rules, typography, color, spacing, brand derivation, and style fallbacks |
| `spec/` | Instructional diagrams that explain structure and layout intent |
| `examples/` | Production-style references for visual hierarchy, density, restraint, and pacing |

## Design philosophy

Blueprints are built around a few core ideas.

### 1. Render only what is authorized

Blueprints should behave like closed-world contracts.

If a section, component, label, badge, header, footer, annotation, or decorative system is not explicitly allowed by the blueprint or requested by the user, the model should omit it.

Empty space is preferable to invented structure.

### 2. Use examples for taste, not copying

Examples are included to communicate visual hierarchy, density, pacing, restraint, and overall quality bar.

They should not be copied literally unless the blueprint explicitly says to do so.

### 3. Treat spec files as instructional references

Files in `spec/` explain structure and intent. They may include annotations, labels, arrows, dimensions, or schematic marks.

Those reference artifacts should not appear in the final output.

### 4. Preserve source truth

Blueprints should help generate polished assets, but they should not invent unsupported technical claims, statistics, compatibility details, dimensions, or performance metrics.

Source material should override blueprint defaults when reliable.

### 5. Make AI output easier to review

A good blueprint should make the first generation more useful, but review still matters. The model should audit its own output against the blueprint before delivery.

## How to use a blueprint

1. Choose a blueprint from `/blueprints`.
2. Read the blueprint’s `README.md`.
3. Provide the blueprint folder to an AI tool such as Claude, ChatGPT, or another AI design/code environment.
4. Provide source material for the specific asset, such as product pages, docs, notes, brand guidance, images, or technical details.
5. Ask the AI to read all blueprint files before generating.
6. Ask the AI to inspect `spec/` for structure and `examples/` for visual quality.
7. Generate the asset.
8. Review the output against the blueprint’s audit requirements.
9. Iterate on the blueprint when repeat issues appear.

## Example prompt

A reusable prompt should live with each blueprint. For example:

    You are generating an artifact from an AssetMule GTM Blueprint.

    Process:

    1. Read all files in this blueprint folder.
    2. Read `blueprint.yaml` first.
    3. Read `layout.yaml`, `components.yaml`, `content.yaml`, and `design_kit.yaml`.
    4. Inspect every file in `/spec` to understand structure, layout intent, component roles, and composition rules.
    5. Inspect every file in `/examples` to understand visual hierarchy, density, pacing, restraint, and quality bar.
    6. Treat `/spec` files as instructional references only. Do not reproduce annotations, arrows, labels, dimensions, placeholder text, or schematic marks from spec files.
    7. Treat `/examples` as visual taste references, not source material.
    8. Use the supplied user intent and source material as the primary context for this generation.
    9. Render only the sections, components, and elements explicitly allowed by the blueprint unless the user explicitly requests an extension.
    10. If an element is not specified, omit it.
    11. Empty space is preferable to invented structure.
    12. Before finalizing, audit the output against the blueprint requirements.

    Output format:
    PDF

    User intent:
    [Describe the asset to generate.]

    Source material:
    [Paste links, notes, files, product details, brand guidance, or other relevant context.]

## Current blueprints

### Product Overview + Technical Specs

Path:

    blueprints/product-overview_technical-specs/

Purpose:

Generate a concise, visually structured two-page PDF that combines a product overview with technical specifications.

Useful for:

- physical products
- software platforms
- infrastructure systems
- industrial equipment
- APIs
- AI systems
- operational offerings
- hardware/software hybrids

## Known limitations

Blueprints improve consistency, but they do not guarantee perfect output.

Current limitations:

- Output quality varies by model and design environment.
- Visual examples may be interpreted too literally unless the blueprint constrains reference usage.
- Technical claims still need human review.
- Some AI tools may add conventional design elements unless the render policy is explicit.
- Blueprints may need iteration after observing real generations.

The goal is not to eliminate human judgment. The goal is to make the starting point much stronger and the iteration loop more systematic.

## Contributing

Contributions are welcome.

Good contributions may include:

- new blueprints
- improvements to existing blueprint contracts
- clearer rendering constraints
- better audit requirements
- example prompts
- validation scripts
- documentation improvements
- generated output examples with notes on what worked or failed

Before contributing, read `CONTRIBUTING.md`.

## Roadmap ideas

Potential future improvements:

- blueprint validation scripts
- schema definitions for YAML files
- additional GTM blueprint types
- model-specific prompt templates
- generated output galleries
- versioned blueprint releases
- downloadable blueprint bundles
- community-submitted examples and critiques

## License

This project is open source under the MIT License.

AssetMule may eventually offer optional services around these blueprints, such as customization, hosting, sponsorships, or operational execution, while keeping the blueprint library itself open.