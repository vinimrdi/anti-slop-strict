# Scoring System — anti-slop-strict

Score out of 100.  
Any Tier-1 ban present automatically caps the score at 40.

## Scoring breakdown

| Category | Points | How to score |
|----------|--------|--------------|
| **Direction & Thesis** | 15 | Clear, specific Visual Thesis + locked tokens = 15. Vague or missing = 0–5. |
| **Ban compliance** | 30 | Zero Tier-1 or Tier-2 signals = 30. Each Tier-1 signal = –10. Each Tier-2 = –5. |
| **Hierarchy & Craft** | 20 | Strong squint-test hierarchy, rhythmic spacing, one primary action = 20. Weak or flat = 0–10. |
| **Signature** | 15 | Exactly one strong, intentional signature = 15. Missing or multiple = 0. |
| **Content integrity** | 10 | Real, specific content only = 10. Any invented stats or generic filler = 0–4. |
| **States & completeness** | 10 | Empty/error/loading considered = 10. Only happy path = 0–3. |

## Interpretation

| Score | Meaning | Action |
|-------|---------|--------|
| 90–100 | Agency-grade | Ship |
| 75–89 | Strong, minor refinements | Polish and ship |
| 60–74 | Acceptable base, still carries some defaults | Targeted fixes required |
| 40–59 | Noticeable slop remains | Major revision |
| 0–39 | Clear AI default aesthetic | Reject and restart from Pre-Flight |

## Audit report template

```
ANTI-SLOP-STRICT AUDIT
Score: XX/100

Critical fails:
- ...

Tier-1 signals found:
- ...

Tier-2 signals found:
- ...

Signature: present / missing — [description]
Visual Thesis: [stated or “missing”]

Top fixes (ordered by impact):
1. ...
2. ...
3. ...
4. ...
5. ...

Gate status: PASS / FAIL
```
