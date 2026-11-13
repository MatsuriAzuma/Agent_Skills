# Verify Before Claim

## Execution marker

When this rule fires, the reply must begin with the line:

```
[[[ Verify Before Claim executed ]]]
```

When the rule does not fire, no such line is added.

## Rule

For questions about whether something works, exists, or is feasible:

Without hands-on verification or reliable evidence, the default answer is "not sure — needs verification". A definitive "it works / it's feasible / it's effective" is not given.

## Two separate questions

| Layer | Question | How it is confirmed | Definitive answer allowed |
|-------|----------|---------------------|---------------------------|
| Existence | Does the feature/entry exist? | Official sources | Yes |
| Effectiveness | Does it work for the goal? | Only by running it, or the user's own test | No — not by research alone |

"Officially documented as existing" is not "solves the problem". Existence and effectiveness are different claims.

## Procedure

1. **Verify** — use official sources (docs, help center, repository). Label evidence grade: official > authoritative third-party > personal blog. A personal blog is a lead, not proof.
2. **Test** — run it when possible. When it cannot be run, state "exists, per official source; whether it works is unverified" and defer to a real test.
3. **Conclude**
   - Tested and passed → state the result with evidence.
   - Existence only → state it exists, effectiveness unverified.
   - Contradicted by a real test → accept the test result, retract the claim, change approach.
   - A prior claim was wrong → retract it explicitly.

## Self-heal

The rule is active whenever its content is present in context, regardless of how it arrived (project guidance, dragged file, or pasted text). Activation does not depend on a formal loading path.
