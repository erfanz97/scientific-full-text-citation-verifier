# Search and verification protocol

## 1. Build a claim-specific search map

For each atomic claim, list:

- canonical entities and aliases;
- relationship and direction terms;
- disease, tissue, cell, population, and model terms;
- measured outcomes and common assay names;
- study-design terms appropriate to the claim;
- mechanism terms only when the claim is mechanistic.

Create several materially different formulations. Include narrow exact-concept searches, broader synonym searches, and design/outcome-focused searches. Revise them using terminology found inside papers. Never rely on one query.

## 2. Search source types deliberately

Use appropriate scholarly databases, publisher pages, repositories, DOI/PMID resolution, reference lists, and cited/citing-paper tools when available. Prefer authoritative bibliographic records for metadata and the publisher or trusted repository for article content.

Prefer primary studies for experimental and clinical claims. Use systematic reviews, reviews, guidelines, and consensus documents to map a field or discover original studies, while distinguishing synthesis from primary evidence.

Record user-specified database restrictions. If database access is unavailable, disclose the substitution and its likely coverage limits.

## 3. Keep retrieval status explicit

Assign one access state before evaluating support:

- `METADATA ONLY`
- `ABSTRACT ONLY`
- `PARTIAL ARTICLE CONTENT`
- `FULL TEXT VERIFIED`
- `FULL TEXT + SUPPLEMENT VERIFIED`

Only the last two can justify a verified verdict, and only if the inspected content includes the evidence needed for the claim. Label `PARTIAL ARTICLE CONTENT` as `FULL TEXT NOT VERIFIED`; partial access may identify a promising lead but cannot receive a verified verdict or Content Support Score. A nominal “full text” page that omits claim-relevant methods, results, figures, tables, or supplements is insufficient. If the claim depends on evidence available only in an inaccessible supplement, keep the candidate `FULL TEXT NOT VERIFIED`.

Record the URL or source, accessed version, and content inspected. Do not equate browser-visible text with complete article access without checking coverage.

## 4. Inspect the paper in context

Search for entities and outcome terms, then read surrounding paragraphs and the corresponding Methods/Results. For figures and tables, inspect captions, group definitions, axes, units, sample sizes, statistical comparisons, and relevant methods. Check supplementary material when the central evidence is referenced there.

Extract only what the study itself shows. Separate:

- study-generated evidence;
- authors' interpretation of their data;
- background statements attributed to other work;
- hypotheses or speculation;
- limitations.

Capture reliable section, subsection, figure, table, and page information only when visible in the accessed version.

## 5. Verify identity and metadata

Cross-check title, authors, journal, year, DOI, PMID, version, correction, and retraction status against authoritative records when available. Distinguish preprints from peer-reviewed versions and use the version actually inspected. Do not guess missing identifiers.

## 6. Follow evidence chains

When a relevant assertion is secondary:

1. capture the cited source exactly;
2. retrieve the original source;
3. locate the original result;
4. compare the citing paper's wording with the original evidence;
5. prefer the original source if it is the scientifically appropriate citation.

If the chain cannot be completed, label the unresolved link and do not upgrade it to verified evidence.

## 7. Expand searches systematically

If support remains weak, search:

- terminology used in direct Results or figure legends;
- gene/protein aliases and assay-specific terms;
- disease subtype and treatment-state variants;
- references cited for the exact assertion;
- papers citing the best near-match;
- closely related endpoints without changing the claim silently;
- authors or cohorts associated with the evidence.

Keep near-matches visible as rejected or qualified candidates. Search expansion must not mutate the original claim to make a paper fit.

## 8. Document stopping conditions

Stop under the user's Goal conditions, or after reasonable saturation when repeated independent formulations return the same candidate set and citation chains add no stronger accessible evidence. Also stop when constraints make all remaining candidates ineligible or inaccessible. Report scope, access gaps, and unresolved uncertainty.
