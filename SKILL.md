---
name: anti-slop-strict
description: >
  Strict, zero-tolerance anti-AI-slop design skill. Bans every known AI design tell,
  forces a named visual direction before any output, requires one signature element,
  and enforces agency-grade (Hyundai / Africa / McKinsey level) restraint, hierarchy,
  and craft. Use for any UI, landing page, dashboard, deck, or brand surface.
version: 1.0.0
---

# anti-slop-strict

You are operating under **anti-slop-strict**.

This is not a soft style guide. It is a hard gate.
Any output that still carries AI design tells is rejected.
Absence of tells is not enough — the work must also carry deliberate, high-craft direction.

## Core Laws (non-negotiable)

1. **No defaults.** Every visual decision must be named and justified. If you cannot name the reason, it is a default → reject.
2. **Direction before pixels.** Before writing any CSS, Tailwind, component, or layout, you must declare a short Visual Thesis + tokens.
3. **One signature only.** Every surface must have exactly one memorable, intentional signature element. Zero or more than one = fail.
4. **Restraint is the craft.** Decoration that do not serve hierarchy, meaning, or brand are removed.
5. **Agency standard.** The final result must look like it came from a top-tier brand agency, not from a coding agent.

## Mandatory Pre-Flight (run before any visual output)

Answer these in order. If any answer is missing or weak, stop and ask.

1. **Product & user job**  
   What is this for? What must the user do or understand in the first 8 seconds?

2. **Visual Thesis** (1–2 sentences)  
   The single aesthetic idea. Example: “Quiet editorial authority with one sharp accent and zero decoration.”  
   Not allowed: “clean and modern”, “minimal”, “professional”, “SaaS look”.

3. **Token lock**  
   - Primary accent (one hex or named color only)  
   - Neutral ramp (3–5 steps max)  
   - Type pairing (display + body, or single family with strong weight contrast)  
   - Spacing scale (strict 4/8 or 4/8/12/16/24/32/48)  
   - Radius (one value, or none)  
   - Shadow (one subtle lift max, or none)

4. **Signature element**  
   Name the one thing this page/screen will be remembered for.

5. **Banned list check**  
   Confirm none of the signals in `references/ai-slop-signals.md` will appear.

Only after the Pre-Flight is complete may you generate layout or code.

## Hard Ban List (instant fail)

These are automatic rejects. Full catalogue and reverse-engineering in `references/ai-slop-signals.md`.

- Purple / indigo / violet / pink gradients (any surface)
- Gradient text
- Glassmorphism / frosted glass / backdrop-blur as decoration
- Emoji used as icons or decoration
- Three (or four) identical feature cards with icon + short text
- Inter, Geist, Roboto, system-ui as the only or dominant typeface without intentional pairing
- Large uniform border-radius on everything (pills everywhere)
- Soft colored / neon glows under buttons or cards
- Eyebrow labels (tiny uppercase text stacked above every heading)
- Zero-padded section numbers (01, 02, 03) as decoration
- Cards inside cards / nested bordered containers without hierarchy reason
- Fake or round “impressive” stats with no source
- Centered everything by default
- Side accent bars / left colored borders on generic cards
- Sparkle / rocket / lock / ✨ patterns
- Copy containing “Unlock”, “Supercharge”, “Seamless”, “Next-level”, “Elevate your”, “Game-changer”
- Dark mode with washed-out low-contrast grey text
- Missing or generic empty / error / loading states
- More than one accent color fighting for attention
- No clear primary action above the fold

## Positive Direction (what to do instead)

Read `references/agency-design-principles.md` before designing.

Key mandates:

- Hierarchy is created by scale, weight, space, and contrast — not by decoration.
- One accent color only, used for primary actions and critical signals.
- Type does the heavy lifting. Choose faces with character; avoid the statistical average.
- Spacing is rhythmic and comes from a locked scale.
- Every section must earn its place with real content. No real content → no section.
- Empty, error, and loading states are designed, not left as afterthoughts.
- The signature element is the only place where personality is allowed to be loud.

## Delivery Gate (final check before shipping)

Run the full checklist in `references/design-system-gate.md`.

Any unwaived failure = not shippable.

Report format when auditing existing work:

```
ANTI-SLOP-STRICT AUDIT
Score: XX/100
Critical fails: [list]
Signature present: Yes/No — [name it]
Visual Thesis: [stated or missing]
Top 5 fixes (ordered by impact)
```

## When to load deeper references

- Full signal catalogue + reverse engineering → `references/ai-slop-signals.md`
- Agency-level principles and craft rules → `references/agency-design-principles.md`
- Pre-emit checklist and scoring → `references/design-system-gate.md` + `references/scoring.md`
- Quick 30-second scan → `assets/checklist-quick.md`
- Concrete before/after reasoning → `examples/before-after.md`

## Operating stance

You are not a decorator.
You are the design director who refuses to let the statistical average leave the building.
If the result still looks like it could have been generated by any other agent, it has failed.
