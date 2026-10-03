# Evidence scoring and verdicts

A Content Support Score is always claim-specific.

Score the relationship:

CLAIM ↔ PAPER EVIDENCE

not the paper itself.

The same paper may receive different scores for different atomic claims.
Never reuse a paper-level score across multiple claims.

## Scoring procedure

Start from the closest band below, then adjust within the band for entity, direction, context, outcome, mechanism, temporal constraint, design fitness, evidence directness, and replication. Explain the decisive strengths and deductions. Do not present a formula as false precision.

| Score | Meaning |
|---|---|
| 90–100 | Direct evidence demonstrates essentially the same claim in the appropriate context. |
| 80–89 | Strong direct evidence with one minor limitation or contextual difference. |
| 70–79 | Good but incomplete support; one material element is missing or narrower than the wording. |
| 60–69 | Partial support; several elements match, but a substantive gap remains. |
| 40–59 | Indirect or weak support; useful for background, not the claim as written. |
| 1–39 | Topically relevant but inadequate evidence. |
| 0 | Content does not support the claim. |

When full text is unavailable, do not infer a score from the title or abstract. Prefer `Not scored — full text not verified`. If the user requires a numeric ranking of leads, label it separately as a provisional retrieval-priority score, never a Content Support Score.

## Causality guardrails

Do not upgrade:

- association to causation;
- correlation to regulation;
- expression difference to pathway activation;
- bioinformatic prediction to experimental validation;
- docking or binding prediction to therapeutic efficacy;
- animal evidence to confirmed human effect;
- mRNA abundance to protein abundance or activity;
- subgroup or exploratory findings to general population effects;
- retrospective prognostic association to clinical utility;
- surrogate endpoints to patient benefit.

Require design-appropriate evidence for stronger language. For example, mechanistic claims generally require perturbation plus a mechanism-relevant readout; therapeutic-efficacy claims require outcome evidence in an appropriate experimental or clinical design. When evidence is weaker, recommend narrower wording.

## Verdict definitions

- `VERIFIED PRIMARY`: The paper reports direct study-generated evidence for the claim in the appropriate context.
- `VERIFIED SUPPORTING`: The paper adds genuine direct support but is not the best or most complete primary source for the exact claim.
- `SUPPORTED WITH QUALIFICATION`: The paper supports a narrower or more cautious version of the claim.
- `PARTIAL SUPPORT`: Some claim components are supported, but a material component is absent or mismatched.
- `INDIRECT ONLY`: Evidence is background, adjacent, model-translated, predicted, or otherwise indirect.
- `FULL TEXT NOT VERIFIED`: Only metadata, abstract, snippet, inaccessible landing page, or insufficient article content was available.
- `TITLE MATCH — CONTENT MISMATCH`: The title looked relevant, but inspected content did not test or establish the claim.
- `CONTRADICTED`: Inspected content provides evidence against the claim or its stated direction in the relevant context.
- `REJECT`: The paper is unsuitable because of a decisive mismatch, retraction/integrity issue, lack of relevant evidence, or another stated reason.

## Manuscript actions

- `USE`: Exact claim is well supported by verified primary evidence.
- `USE WITH QUALIFICATION`: Cite only after narrowing wording or disclosing a limitation.
- `REWRITE CLAIM`: Evidence supports a materially weaker or different proposition.
- `FIND BETTER SOURCE`: Candidate has some value but cannot carry the intended claim.
- `REJECT`: Do not cite for this claim.

Use more than one paper when distinct atomic claims or evidence types require it. Do not average contradictory studies into a falsely confident score; report the conflict.
