# AI Slop Signals — Full Catalogue + Reverse Engineering

This document is the forensic map of why models produce the same look, and exactly which patterns mark a surface as AI-generated.

## Why the same look appears

Models optimise for statistical likelihood, not for authorship.
When no strong direction is given, they sample the densest region of their training data for “modern web UI / SaaS landing / dashboard”.

That region is dominated by:

- Tailwind + shadcn/ui defaults
- 2023–2025 SaaS template aesthetics
- “Make it pop” and “premium dark” prompt patterns
- Inter / system font stacks
- Purple-indigo as the safest accent that still feels “tech”

Result: every unconstrained generation converges on the same cluster of decisions.
The cluster is now so recognisable that humans detect it in under 3 seconds.

This is not a taste failure. It is a sampling failure.
The cure is to force the model out of the dense region before it starts generating.

---

## Signal Catalogue (ranked by detection frequency)

### Tier 1 — Instant recognition (highest frequency)

| # | Signal | What it looks like | Why models do it | Strict replacement |
|---|--------|--------------------|------------------|--------------------|
| 1 | Purple / indigo / violet gradient | Hero background, button, text, or accent going purple→blue or purple→pink | Most over-represented “tech accent” in training data + “make it pop” | One flat, intentional accent. No multi-stop gradients on large surfaces. |
| 2 | Gradient text | Headline with color stop from white/light → purple/cyan | Same statistical pull + perceived “premium” | Solid color. Hierarchy via size/weight, not color gradient. |
| 3 | Glassmorphism / frosted cards | `backdrop-filter: blur`, translucent panels, 1px light border | Trendy in 2021–2024 training data; easy to generate | Solid surfaces. Blur only for true floating overlays (modals, menus). |
| 4 | Emoji as icons | 🚀 🔒 ✨ ⚡ in feature cards or as “icons” | Zero import cost; models treat emoji as free visual assets | One consistent icon set (stroke or filled), or no icons. |
| 5 | Three identical feature cards | Icon + short title + 1–2 lines, repeated 3× or 4× | Default “features section” template in almost every SaaS example | Numbered process, comparison table, alternating rows, or real product screenshots. |
| 6 | Inter / Geist / system-ui monopoly | Entire interface in one of these faces with no pairing | Highest-frequency screen fonts in training data | Intentional pairing or a single family with strong weight contrast. Display face with character. |
| 7 | Soft colored / neon glow | Violet or cyan blur under primary button or cards | “Premium dark mode” aesthetic in training set | One subtle neutral shadow max, or none. |
| 8 | Eyebrow labels | Tiny uppercase label stacked above every heading (“OUR SERVICES”, “FEATURES”) | Learned pattern for “section labelling” | One heading. No stacked micro-label unless it carries real information. |

### Tier 2 — Strong tells (still very common)

| # | Signal | What it looks like | Why models do it | Strict replacement |
|---|--------|--------------------|------------------|--------------------|
| 9 | Zero-padded numbers | 01, 02, 03 as section or card decoration | “Process” template + visual filler | Number only real sequential steps. No leading zero. No giant faded background numbers. |
| 10 | Cards inside cards | Bordered box nested inside another bordered/shadowed box | Every content group gets a container by default | Flatten. Use space and hierarchy instead of extra boxes. |
| 11 | Side accent bar / left colored border | Vertical colored stripe on the left of every card | Old alert pattern generalised to everything | Reserve for true status (error, warning, success). Never decorative. |
| 12 | Uniform large radius | Everything `rounded-2xl` or `rounded-3xl` / pill shapes everywhere | “Friendly” mapped to “round” | One radius value (or none). Sharp corners are allowed and often stronger. |
| 13 | Centered everything | Headlines, paragraphs, cards all text-align center | Lowest-decision layout | Left or right aligned body. Center only when it serves a specific compositional goal. |
| 14 | Fake / round stats | “10,000+ users”, “99.9% uptime”, “4.9★” with no source | Models invent impressive numbers | Real numbers only, or remove the section. |
| 15 | Sparkle / rocket / lock pattern | Same three emoji or icon metaphors repeated across sites | Highest-frequency “feature icon” set | Custom or consistent stroke icons that actually relate to the content. |
| 16 | Low-contrast grey text on dark | Body or caption in washed-out grey | “Elegant dark mode” default | Meet WCAG AA. Prefer higher contrast neutrals. |

### Tier 3 — Structural and content tells

| # | Signal | What it looks like | Why models do it | Strict replacement |
|---|--------|--------------------|------------------|--------------------|
| 17 | No primary action hierarchy | Multiple buttons of equal visual weight | Models treat every CTA as equal | One clear primary. Secondary is quieter. |
| 18 | Missing empty / error / loading states | Only the “happy path” is designed | Training data is full of perfect demos | Design all three states deliberately. |
| 19 | Bento grid as default | Everything forced into a bento layout | Trendy layout in recent data | Use bento only when the content density justifies it. |
| 20 | “Unlock / Supercharge / Seamless” copy | Marketing clichés in headlines and subheads | Highest-frequency SaaS language | Specific, concrete language about the actual product. |
| 21 | No signature element | Page is competent but forgettable | Models optimise for “correct”, not “memorable” | Force exactly one intentional signature. |
| 22 | Beige + serif “anti-purple” slop | New emerging default: warm beige background + tasteful serif | Models are already learning the anti-purple reaction | Still a default. Direction must be specific to the brand, not a reaction. |

---

## Reverse Engineering — How the model arrives at each tell

1. **Prompt contains no strong visual constraint** → model samples the mode of the distribution.
2. **“Modern / clean / premium / SaaS”** → maps directly onto the purple-gradient + Inter + three-card cluster.
3. **No design system tokens supplied** → model invents values one element at a time → inconsistent greys, off-scale spacing, multiple radii.
4. **No icon library referenced** → emoji become the path of least resistance.
5. **No real content supplied** → model fills with plausible but generic text and invented metrics.
6. **Dark mode requested without contrast rules** → washed-out greys appear because they look “soft” in isolation.

The single highest-leverage intervention is therefore:

> Force a named Visual Thesis + locked tokens **before** any layout or component is generated.

Everything else is downstream of that decision.

---

## Detection heuristics (for audits)

- If you can swap the logo and the page still feels familiar → high slop probability.
- If three or more Tier-1 signals are present → automatic fail.
- If the page has no signature element and uses Inter + purple accent → almost certain AI default.
- Squint test: if hierarchy disappears when you squint, decoration was doing the work instead of scale/weight/space.

---

## Emerging (2026) signals to watch

- Beige/stone backgrounds + “tasteful” serif as the new safe anti-purple
- Over-use of very thin hairline borders
- Excessive use of `tracking-tight` or negative letter-spacing on large headlines
- “Instrument Serif” or similar as the new default display face
- Status pills and badges on every card

These are already entering the training distribution. Treat them with the same suspicion.
