# AssetMule GTM Blueprints

AssetMule GTM Blueprints is an open-source library of practical AI blueprint templates for go-to-market work.

A blueprint is a simple folder-based contract that helps AI tools generate a specific GTM artifact more reliably, such as:

- one-pagers
- sales decks
- comparison pages
- product launch kits
- follow-up sequences

## Why blueprints exist

AI tools can produce GTM assets quickly, but output quality is often inconsistent when prompts are vague or ad hoc.

Blueprints solve that by packaging reusable guidance into a clear structure:

- **intent** (what job the asset must do)
- **content** (what source material is required)
- **style** (how it should sound and look)
- **output** (what the final deliverable must include)
- **examples** (reference artifacts)

This gives teams a repeatable contract instead of rewriting prompt logic from scratch each time.

## Who this is for

- GTM operators
- founders
- product marketers
- sales enablement teams
- AI builders creating practical content workflows

## How to use a blueprint

1. Pick a blueprint folder in `/blueprints`.
2. Read its `README.md` to understand scope and usage.
3. Gather your source material based on `content.md`.
4. Copy guidance from `intent.md`, `content.md`, `style.md`, and `output.md` into your prompt context.
5. Run it in ChatGPT, Claude, Copilot, or another AI assistant.
6. Review output against the acceptance criteria and iterate.

## Open source and long-term direction

These blueprints are free and open source under the MIT License.

AssetMule may eventually offer optional services around these blueprints (such as customization, hosting, sponsorships, or operational execution), while keeping the blueprint library itself open.

## Repository structure

- `Blueprints.md/README.md` — recommended blueprint anatomy
- `blueprints/` — blueprint library
- `blueprints/product-overview-technical-specs/` — starter blueprint
- `CONTRIBUTING.md` — contribution guidance
- `LICENSE` — MIT license
