# anti-slop-strict

**Zero-tolerance anti-AI-slop design skill.**

This is not another soft “avoid purple gradients” list.  
It is a strict operating protocol that:

1. Bans every known AI design tell (with full reverse-engineering of why models produce them)
2. Forces a named Visual Thesis + locked tokens before any pixels
3. Requires exactly one signature element
4. Enforces agency-grade craft (the standard expected by top brand agencies)
5. Gates every output with a hard pass/fail checklist and scoring system

## Why this exists

Existing anti-slop skills are good at subtraction.  
Most stop at “don’t do these things”.

anti-slop-strict goes further:

- It explains the sampling mechanics that create the tells
- It supplies the positive direction that top agencies actually use
- It treats the absence of tells as necessary but not sufficient
- It demands authorship, hierarchy, and one memorable signature

## Structure

```
anti-slop-strict/
├── SKILL.md                          ← Core contract (load this)
├── README.md
├── references/
│   ├── ai-slop-signals.md            ← Full catalogue + reverse engineering
│   ├── agency-design-principles.md   ← Positive craft rules
│   ├── design-system-gate.md         ← Mandatory pre-emit checklist
│   └── scoring.md                    ← 0–100 scoring + audit template
├── assets/
│   └── checklist-quick.md            ← 30-second scan
└── examples/
    └── before-after.md               ← Concrete reasoning examples
```

## How to use

1. Load `SKILL.md` into the agent context (or install as a skill).
2. For any new UI / landing / dashboard / deck, the agent must complete the Pre-Flight before generating.
3. After generation, run the Design System Gate.
4. For audits of existing work, use the scoring template in `references/scoring.md`.

## Core stance

> Absence of AI tells is not presence of design.  
> The work must also carry deliberate direction, strong hierarchy, and exactly one signature.

If the result still looks like it could have been produced by any other unconstrained agent, it has failed.

---

Built for professionals who refuse to ship the statistical average.
