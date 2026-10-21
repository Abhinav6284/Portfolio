---
name: design-md-library
description: Library of 84 DESIGN.md design-system analyses of real sites (Stripe, Linear, Vercel, Apple, Notion, Supabase, Raycast…). Use when the user wants UI "like <brand>", "in the style of X", a DESIGN.md for a project, or a ready token set (colors, type, spacing, radii, components) to build from.
---

# DESIGN.md library

Source: VoltAgent/awesome-design-md (MIT). A DESIGN.md is a plain-markdown design system
(Google Stitch format): YAML frontmatter with tokens (`colors`, `typography`, spacing, radii,
components) followed by prose rules on layout, components, imagery and do/don't.

## Procedure

1. **Select.** Read `INDEX.md` (one line per system: slug, primary colour, type families, character).
   - Brand named → use `designs/<slug>.md` directly.
   - Vibe described ("dark dev-tool", "editorial", "fintech") → shortlist 2–3 slugs from the index,
     state the pick in one line, proceed. Ask only when the choice is genuinely ambiguous and costly.
2. **Load** the chosen `designs/<slug>.md` in full. Never build from the index line alone.
3. **Apply.**
   - Map frontmatter tokens to the target stack: CSS custom properties on `:root`, or
     `tailwind.config` `theme.extend` (colors, fontFamily, fontSize, borderRadius, spacing).
   - Follow the prose rules (hierarchy, density, shadow/gradient policy, component anatomy) over
     generic defaults.
   - Proprietary fonts (SF Pro, Circular, Söhne, brand faces) → substitute the closest free face
     (Inter, Geist, Manrope, IBM Plex, etc.) and state the substitution.
4. **Deliverable option.** If the user wants a DESIGN.md for their own project, copy the file to
   the project root as `DESIGN.md`, then replace brand name, logo references and primary colour
   with the user's brand while keeping the structure.

## Constraints

- These are style analyses, not brand assets. Do not reproduce logos, wordmarks, trademarked
  names or proprietary copy; build an original product in the borrowed design language.
- Blend at most two systems (e.g. tokens from A, layout rules from B) and say which came from where.
- Pairing: `design-taste-frontend` for art direction / anti-slop gate, `web-design-guidelines`
  for the post-build audit.

## Files

| Path | Content |
|---|---|
| `INDEX.md` | 84 one-line summaries |
| `designs/<slug>.md` | Full DESIGN.md per system |
| `LICENSE` | MIT, VoltAgent |
