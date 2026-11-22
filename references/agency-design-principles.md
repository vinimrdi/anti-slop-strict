# Agency-Grade Design Principles

This is the positive counterpart to the ban list.
Removing AI tells only gets you to “not generic”.
These principles get you to the standard of a top-tier brand agency (the level expected by clients of Hyundai, Africa, McKinsey Digital, Pentagram, Collins, etc.).

## 1. Hierarchy is the primary craft

Hierarchy is created by:

- Scale
- Weight
- Space
- Contrast
- Position

Never by decoration, color alone, or extra containers.

**Test:** Squint at the screen. The primary action and the main message must still be obvious. If they disappear, hierarchy is failing.

## 2. One accent, used with intention

- Exactly one accent color for primary actions and critical signals.
- Neutrals do the rest of the work.
- Accent is a signal, not a theme.

Agency work almost never uses more than one strong accent. Multiple competing accents read as indecision.

## 3. Type carries character

- Choose a display face (or strong weight contrast) that has a point of view.
- Body face prioritises readability and quiet confidence.
- Avoid the statistical average (Inter, Geist, system-ui as the sole voice).
- Measure (line length) stays comfortable: roughly 55–75 characters for body.

Typography is the fastest signal of authorship. A distinctive but restrained type pairing immediately distances the work from AI defaults.

## 4. Spacing is rhythmic, not arbitrary

Lock a scale early (recommended: 4 / 8 / 12 / 16 / 24 / 32 / 48 / 64).

Every gap, padding, and margin comes from the scale.
Off-scale spacing is one of the quietest but most reliable AI tells.

## 5. Radius and shadow are decisions, not defaults

- One radius value for the system, or none.
- One subtle shadow (or none). Soft colored glows are banned.
- Sharp corners are often stronger than soft ones for serious brands.

## 6. Every section must earn its place

If the content is not real, specific, and useful, the section does not ship.
No “features” block made of three generic statements.
No invented metrics.
No placeholder testimonials.

## 7. States are designed, not left behind

Empty, error, loading, success, and edge states are first-class.
Agency-level work treats them as part of the product, not as afterthoughts.

## 8. Signature element (exactly one)

Every surface needs one memorable, intentional signature.
It can be:

- A distinctive crop or treatment of photography
- A custom illustration language
- A bold but controlled use of type
- A structural idea (asymmetric layout, unusual grid, strong negative space)
- A single unexpected but coherent detail

Zero signatures = forgettable.
More than one = noisy.

The signature is the only place where the work is allowed to be loud.

## 9. Restraint as status

Top agencies signal quality through what they refuse to do.
Decoration that does not serve hierarchy, meaning, or brand is removed.
White space is not empty; it is active.

## 10. Content before composition

Real content drives layout.
Layout does not invent content.
If the brief has no real numbers, quotes, or product truth, the design stays quiet until they exist.

---

## Practical translation for agents

Before generating:

1. State the Visual Thesis in one or two sentences.
2. Lock tokens (accent, neutrals, type, spacing, radius, shadow).
3. Name the single signature element.
4. Confirm the primary user action and where it lives.
5. Only then produce layout or code.

During generation:

- Prefer fewer elements with stronger hierarchy over more elements with decoration.
- Use real product language, never the SaaS cliché list.
- Design the empty and error states in the same pass.

After generation:

- Run the Delivery Gate.
- If any Tier-1 signal remains, reject and revise.
- If the signature is missing or weak, the work is not finished.
