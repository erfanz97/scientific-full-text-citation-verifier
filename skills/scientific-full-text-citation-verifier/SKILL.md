---
name: scientific-full-text-citation-verifier
description: "Find, verify, audit, replace, and evaluate references for specific scientific claims by decomposing claims and inspecting accessible article content. Use when asked to find references for scientific text; verify whether a citation supports a statement; replace old, weak, or misleading citations; find newer evidence for an existing statement; audit manuscript citations; grade how closely a paper supports a claim; verify evidence from article content rather than titles; or check citations used in an Introduction, Discussion, Results interpretation, or other manuscript section. Accept sentences, paragraphs, multiple claims, cited text, uploaded papers/manuscripts, and date/design/model/database constraints. Do not trigger for general scientific explanations, ordinary literature summaries, manuscript drafting without citation verification, grammar editing, translation, or reference formatting alone."
---

# Scientific Full-Text Citation Verifier

Verify exact scientific claims against actual article content. Treat every search hit as a candidate until inspected; never infer support from a title, keywords, snippet, topic, or abstract similarity alone.

## Non-negotiable rules

- Never fabricate a reference, bibliographic identifier, quotation, page, figure, table, section, or evidence location.
- Never say full text was inspected unless a complete article version (HTML or PDF) was actually accessible and the claim-relevant sections were examined.
- Never label a paper verified from its title, search snippet, metadata, or abstract alone.
- Label inaccessible content `FULL TEXT NOT VERIFIED`; describe exactly what was accessible.
- Do not force a citation. If none survives verification, report `NO ADEQUATE SUPPORTING EVIDENCE VERIFIED` and state what evidence is missing.
- Distinguish the study's findings from background claims that its Introduction or Discussion attributes to other papers.
- Preserve epistemic strength: do not upgrade association, prediction, or model-specific evidence into causation, mechanism, clinical efficacy, or confirmed human effect.
- Use short permissible excerpts only when useful; otherwise paraphrase precisely.

## Required working record

Maintain a claim ledger and candidate ledger throughout the task. For each candidate record the discovery source, content accessed, locations inspected, evidence found, disqualifiers checked, score, and verdict. Do not let an earlier optimistic judgment substitute for the final falsification pass.

## Workflow

### 1. Parse constraints and decompose claims

Record any requested field, date range, study design, population/model, article type, and databases. Break compound prose into atomic claims `C1`, `C2`, and so on; do not assume one citation supports an entire sentence.

For each claim record:

- entities and aliases;
- relationship and direction;
- biological or clinical context;
- measured or asserted outcome;
- population, specimen, or model;
- wording strength;
- claim type: associative, causal, mechanistic, prognostic, diagnostic, therapeutic, descriptive, or comparative.

If the claim is ambiguous, state the interpretation being tested. Ask only when competing interpretations would materially change the search or verdict.

### 2. Search broadly, then retrieve candidates

Read [search-and-verification-protocol.md](references/search-and-verification-protocol.md) before searching. Formulate multiple materially different searches per claim using synonyms, aliases, controlled-vocabulary-like terms, outcomes, mechanisms, models, and terminology discovered during searching.

Prefer primary literature for experimental or clinical claims. Use reviews for discovery and citation-chain tracing, not as an automatic substitute for original evidence. Mark every metadata-only hit `CANDIDATE`; do not score it highly.

### 3. Inspect actual paper content

Whenever technically accessible, inspect the paper itself. Search relevant concepts, then read enough surrounding material to preserve meaning. Examine the Abstract, Methods, Results, figures, legends, tables, supplementary results, and Discussion as applicable.

Prioritize evidence in this order:

1. direct Results;
2. study-generated figures and tables;
3. direct experimental or clinical findings;
4. authors' interpretation of their own findings;
5. Discussion statements;
6. Introduction or background statements.

Record the exact source version accessed and reliable evidence location. Do not invent page numbers for unpaginated HTML or transfer PDF page numbers to another version.

### 4. Match claim to evidence dimension by dimension

Evaluate each candidate independently for:

- **Entity:** same gene, protein, drug, pathway, disease, population, or system;
- **Direction:** same increase/decrease, activation/inhibition, or better/worse relationship;
- **Context:** same disease subtype, population, model, tissue/cell type, and treatment state;
- **Outcome:** the study measured the claimed endpoint;
- **Mechanism:** mechanistic wording has mechanistic evidence;
- **Time:** requested publication window is met;
- **Design:** study design justifies the wording.

Apply the causality guardrails and detailed scoring rubric in [evidence-scoring.md](references/evidence-scoring.md).

### 5. Attempt falsification

For every promising paper ask: **What would make this paper inappropriate for this exact claim?**

Actively check wrong disease, population, cell type, direction, endpoint, model, treatment context, gene/protein level, unsupported mechanism, secondary citation, exploratory sample, and causal overreach. Read [failure-modes.md](references/failure-modes.md) for the rejection checklist. Record the reason for every rejection.

### 6. Trace citation chains

When a review, Introduction, or Discussion makes the relevant assertion and cites another source:

1. identify the cited source;
2. retrieve it when possible;
3. inspect its actual content;
4. verify whether it supports the claim;
5. prefer the original source when scientifically appropriate.

Do not assume the citing paper accurately represents the cited study.

### 7. Score and classify

Assign a 0–100 Content Support Score ONLY when the claim-relevant
full text has been verified. For METADATA ONLY, ABSTRACT ONLY, or PARTIAL ARTICLE CONTENT, do not assign a Content Support Score.
Report instead:
Not scored — full text not verified
Never infer a Content Support Score from the title, abstract, search snippet, metadata, or topical similarity.

Use exactly one verdict per candidate:

- `VERIFIED PRIMARY`
- `VERIFIED SUPPORTING`
- `SUPPORTED WITH QUALIFICATION`
- `PARTIAL SUPPORT`
- `INDIRECT ONLY`
- `FULL TEXT NOT VERIFIED`
- `TITLE MATCH — CONTENT MISMATCH`
- `CONTRADICTED`
- `REJECT`

Do not assign a verified verdict when full text was not inspected. A score is not a substitute for a written rationale.

### 8. Expand or stop transparently

If no strong source survives, search again using terminology inside relevant papers, citation chains, related experimental terms, alternate disease names, biomarkers, author vocabulary, and cited/citing papers. Do not stop after one plausible candidate.

Honor any user Goal that specifies persistence, iteration count, or convergence. Otherwise stop when searches are reasonably saturated, constraints are exhausted, or remaining papers cannot be accessed; disclose which condition applies.

### 9. Report claim by claim

Read [output-template.md](references/output-template.md) before producing the answer. For every atomic claim provide the original claim, scientific interpretation, best verified reference and identifiers, evidence location, concise evidence, match rationale, limitations, score, verdict, manuscript action, and a cautious rewrite when appropriate.

End with a compact evidence matrix, `BEST REFERENCES TO USE`, and `REJECTED / MISLEADING CANDIDATES`. State exact rejection reasons. Separate verified evidence from unverified leads. Before sending, run the final completeness check in the output template; do not omit required fields merely to shorten the answer.

## Resource routing

- Read [search-and-verification-protocol.md](references/search-and-verification-protocol.md) for every verification task before searching or retrieving papers.
- Read [evidence-scoring.md](references/evidence-scoring.md) before assigning scores, verdicts, or manuscript actions.
- Read [failure-modes.md](references/failure-modes.md) during falsification and again before finalizing.
- Read [output-template.md](references/output-template.md) before composing the final response; adapt its length to the number of claims without dropping required fields.
