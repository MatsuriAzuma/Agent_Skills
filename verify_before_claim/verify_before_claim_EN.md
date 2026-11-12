---
name: verify-before-claim-en
description: Before giving any definitive conclusion (especially about whether a product/tool/API/path "can do something", "has a certain feature", or "supports a certain operation"), verify the facts first to avoid hallucination from unverified assertions. Use this skill when answering "Can X do Y", "Does X have feature Z", "Is this path actually usable", or when the user points out a previously given unverified/wrong assertion. Trigger words: verify, fact-check, hallucination, really, is there this feature, can it, does it support, you were wrong before.
agent_created: true
---

# Verify Before Claim

## Purpose

Prevent making definitive assertions about the reality of a product, tool, API, path, feature, or command without verifying the facts first, which leads to hallucination and misleads the user.

## When to Use

Use the verification flow of this skill in any of these cases:

- Answering a capability/existence question such as "Can X do Y", "Does X have feature Z", or "Does X support operation W".
- Asserting that a product (software, app, service, platform) has a certain capability, menu, entry point, or accelerator.
- Claiming that a certain path, command, API parameter, or config item is "definitely usable / definitely correct".
- The user questions or points out a previously given unverified conclusion (hallucination).

## Core Principles

1. **When unsure, look it up — don't guess.** For any capability/existence assertion, if it cannot be confirmed from a reliable source, clearly say "I'm not sure / needs verification" instead of giving a seemingly definitive answer.
2. **Distinguish "I know" from "I infer".** A generalized impression from training data is not the current ground truth. Product features, menus, and paths change over time.
3. **Prefer admitting you don't know.** A confidently wrong answer does far more harm than "I'm not sure".
4. **When corrected, admit the mistake first, then fix it.** When the user points out an error, acknowledge it immediately without defending, then provide the verified facts.

## Verification Flow (in order)

1. **Classify the assertion**: Is this a "factual assertion" (needs verification) or a "verifiable inference"? Any claim about a concrete capability or existence of an external product/tool/API/path is a factual assertion.
2. **Find a reliable source**: Prefer WebSearch / WebFetch on official docs, official help centers, or official feature lists; do not rely on vague impressions or second-hand retellings.
3. **Provide high-credibility evidence**: When giving a definitive conclusion, always attach self-verifiable sources, for example:
   - Official URL / official documentation page link (first choice)
   - Official help center, official feature list, official announcement
   - Official repository (official org on GitHub) documentation
   Evidence priority: **official primary source > authoritative third-party > personal blog/forum post**. If only a second-hand source is available, label it "according to X, no official confirmation found".
4. **Determine certainty**:
   - Official source clearly supports it → give a definitive conclusion and attach the official link as evidence.
   - Cannot find / sources conflict → clearly say "cannot confirm, needs further verification"; do not give a definitive conclusion and do not fabricate sources.
   - Conflicts with the user's description → prefer the user's current real-world feedback and correct your own statement.
5. **Grade your wording**: Clearly distinguish 「verified (with evidence)」, 「pending verification」, and 「uncertain」. Without evidence, do not use definitive language like "definitely", "certainly", "it is".

## Abstracted Counterexamples (for recognizing the same class of mistake)

- Treating "product X supports capability Y" as fact and claiming "search keyword Z in the app to find the entry", when the product actually has no such entry, or the entry name differs from the keyword used → asserted a product capability without verification.
- Attributing a capability that belongs to one tool to a different tool, causing the user to follow instructions and find no such entry.
- The user's approach is roughly correct but uses the wrong **keyword / option name / entry name** (searched the wrong name); going along with the user's wrong keyword and concluding "can't find it means not supported", instead of first giving the verified standard entry name → misjudging "wrong keyword" as "feature doesn't exist".

## Key Rule: Distinguish "right idea" from "wrong keyword"

When the path the user asks about is **broadly correct after verification**, but has an error in a **keyword, option name, setting name, or menu name**:

1. **Do not rush to confirm or deny the user.** Do not conclude "the feature doesn't exist" just because the user says "I searched X and found nothing".
2. **First give the standard, verified method**: clearly tell the user the correct keyword / entry name / operation path, with an official or reliable source as evidence.
3. **Ensure the user will definitely succeed by following it**, before giving a definitive conclusion.
4. **Point out the keyword difference**: e.g., "the correct entry is named A, not the B you searched, so it's normal that searching B finds nothing".

In one sentence: **first give the verified standard method (with the correct name and evidence), then confirm; never echo a possibly-wrong keyword from the user to deny the feature.**

## Pre-Claim Self-Check

Before outputting a definitive conclusion, ask yourself:

- Did I actually verify this feature/entry/path exists, or am I inferring from impression?
- If the user follows my instructions and can't find it, could my assertion be wrong?
- Can I offer a fallback plan for "what to do if it doesn't exist"?
- Is my definitive conclusion backed by a self-verifiable source (official URL / official docs), or is it just an unsupported claim?

If any of these cannot be answered, downgrade to "I'm not sure" or verify first, instead of giving a definitive answer. When giving a definitive answer, always attach an official source link as evidence.
