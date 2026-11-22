# Design System Gate — Pre-Emit Checklist

This gate is mandatory. Any unwaived failure means the output is not shippable under anti-slop-strict.

## A. Direction Gate (must pass before pixels)

- [ ] Visual Thesis is stated in 1–2 concrete sentences (not “clean/modern/minimal”)
- [ ] One accent color is locked
- [ ] Neutral ramp is defined (3–5 steps)
- [ ] Type pairing or single family with strong contrast is chosen
- [ ] Spacing scale is locked
- [ ] Radius decision is explicit (one value or none)
- [ ] Shadow decision is explicit (one subtle or none)
- [ ] Exactly one signature element is named

## B. Ban Gate (instant fail if present)

- [ ] No purple / indigo / violet / pink gradients on any large surface
- [ ] No gradient text
- [ ] No decorative glassmorphism / backdrop-blur
- [ ] No emoji used as icons
- [ ] No three (or four) identical icon + text feature cards
- [ ] No Inter / Geist / system-ui as the sole or dominant voice without intentional pairing
- [ ] No soft colored / neon glows
- [ ] No eyebrow labels stacked above headings as default
- [ ] No zero-padded decorative numbers (01, 02, 03)
- [ ] No nested cards without clear hierarchy reason
- [ ] No side accent bars on generic cards
- [ ] No “Unlock / Supercharge / Seamless / Next-level / Elevate” copy
- [ ] No invented round metrics
- [ ] No low-contrast washed-out grey text

## C. Hierarchy & Craft Gate

- [ ] Primary action is visually obvious within 3 seconds
- [ ] Squint test passes (main message and CTA remain clear)
- [ ] Spacing comes only from the locked scale
- [ ] One clear visual volume for primary elements; secondary is quieter
- [ ] Empty / error / loading states are designed (or explicitly deferred with reason)

## D. Content Gate

- [ ] Every section contains real, specific content
- [ ] No section exists only to fill space
- [ ] Language is concrete and product-specific

## E. Signature Gate

- [ ] Exactly one signature element is present and intentional
- [ ] The signature is memorable without breaking the system

## Final declaration

Before emitting the final design or code, state:

```
GATE STATUS: PASS / FAIL
Failed items: [list]
Signature: [name]
Visual Thesis: [one sentence]
```

If status is FAIL, do not ship. Revise until every item is cleared or explicitly waived with written justification.
