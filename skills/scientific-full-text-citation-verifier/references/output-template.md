# Output template

Adapt length to the task, but preserve these fields for every atomic claim. Use `Not available` or `Not reliably available` rather than inventing data.

## Claim C1

**Original claim:** [verbatim user text]

**Scientific interpretation:** [entities, relationship, direction, context, outcome, population/model, wording strength, claim type]

**Best verified reference:**

- Full citation: [authors, title, journal, year, volume/pages or article number when verified]
- Year: [year]
- Journal: [journal]
- DOI: [verified DOI or Not available]
- PMID: [verified PMID or Not available]
- Accessible source: [direct article or repository link]
- Access status: [FULL TEXT VERIFIED / FULL TEXT + SUPPLEMENT VERIFIED; otherwise state the nonverified access status]

**Evidence location:** [section, subsection, figure, table, supplement, and reliable page]

**Relevant evidence:** [precise paraphrase or short permissible excerpt]

**Why this evidence matches:** [entity, direction, context, outcome, mechanism, time, and design correspondence]

**Limitations:** [all material discrepancies, uncertainty, and generalizability limits]

**Content Support Score:** [XX/100, or Not scored — full text not verified]

**Verdict:** [allowed verdict]

**Recommended manuscript action:** [USE / USE WITH QUALIFICATION / REWRITE CLAIM / FIND BETTER SOURCE / REJECT]

**Recommended revised sentence:** [include when evidence supports narrower wording]

Repeat for `C2`, `C3`, and so on.

## Evidence matrix

| Claim | Paper | Full text verified | Entity | Direction | Context | Outcome | Evidence score | Verdict |
|---|---|---:|---|---|---|---|---:|---|
| C1 | [short citation] | Yes/No | Match/Partial/No | Match/Partial/Opposite | Match/Partial/No | Match/Partial/No | [score or N/S] | [verdict] |

## Best references to use

List only verified papers suitable for the stated or revised claims. Explain which claim each supports. If none qualify, write:

`NO ADEQUATE SUPPORTING EVIDENCE VERIFIED`

Then state the missing evidence and the searches/access limitations.

## Rejected / misleading candidates

| Paper | Candidate for | Access status | Verdict | Exact rejection reason |
|---|---|---|---|---|
| [paper] | [claim] | [status] | [verdict] | [wrong entity/direction/context/outcome/design, secondary only, inaccessible, contradicted, etc.] |

## Search and access note

Briefly state databases/sources searched, date constraints, content-access limits, and stopping condition. Keep unverified leads separate from verified recommendations.

## Verification state

For every atomic claim report:

| Claim | Best verified score | Strong primary source found | Independent confirmation | Search saturation | Current state | Next action |
|---|---:|---|---|---|---|---|
| C1 | 94 | Yes | Yes | Yes | CONVERGED | None |
| C2 | 82 | Yes | No | No | CONTINUE | Search alternative terminology |
| C3 | N/S | No | No | No | CONTINUE | Retrieve full text |
| C4 | 41 | No | No | Yes | INSUFFICIENT EVIDENCE | Rewrite claim |

Allowed Current state values:

CONVERGED
CONTINUE
INSUFFICIENT EVIDENCE
CONTRADICTED
ACCESS BLOCKED

## Goal handoff

OVERALL_GOAL_STATE: [CONVERGED / CONTINUE / BLOCKED]

UNRESOLVED_CLAIMS:
[List claim IDs]

NEXT_ITERATION_PRIORITY:
[Specify exactly what should be searched or verified next]

## Final completeness check

Before sending, confirm:

- every atomic claim has the original wording and scientific interpretation;
- every recommended paper has verified metadata, access status, evidence location, match rationale, limitations, score, verdict, and action;
- every inaccessible or partial-content paper is `FULL TEXT NOT VERIFIED` and has no Content Support Score;
- the evidence matrix uses all required columns;
- `BEST REFERENCES TO USE`, `REJECTED / MISLEADING CANDIDATES`, and the search/access note are present;
- no claim is represented as stronger than the inspected evidence.
