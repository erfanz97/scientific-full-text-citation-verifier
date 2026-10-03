# Scientific Full-Text Citation Verifier

A reusable agent skill for checking whether scientific references support precise claims, using the actual article content.

It decomposes prose into atomic claims, searches for candidate papers, inspects accessible full text, matches evidence to the claim, checks reasons to reject a candidate, and reports a traceable verdict. It also helps find stronger references and qualify wording when evidence is narrower than the original claim.

## Evidence rules

- A title, search snippet, metadata record, or abstract cannot establish full-text verification.
- A Content Support Score is assigned only after the claim-relevant full text has been inspected.
- Inaccessible or incomplete articles remain `FULL TEXT NOT VERIFIED` and are not scored.
- Associations, predictions, and model-specific findings must retain their original evidentiary strength.
- When no suitable source is verified, the skill reports `NO ADEQUATE SUPPORTING EVIDENCE VERIFIED`.

The Content Support Score describes correspondence between a specific claim and inspected evidence. It is not a validated probability or a general study-quality rating.

## Install in Codex

Ask Codex:

```text
$skill-installer Install scientific-full-text-citation-verifier from the GitHub repository Erfanz97/scientific-full-text-citation-verifier, using the folder skills/scientific-full-text-citation-verifier.
```

Alternatively, download or clone this repository and copy the entire `skills/scientific-full-text-citation-verifier` folder into your user-level `.agents/skills` directory. For use in one project, copy it into that project's `.agents/skills` directory. Keep `references/` and `agents/` with `SKILL.md`.

If the skill does not appear after installation, restart Codex. See the [official skill documentation](https://learn.chatgpt.com/docs/build-skills) for current discovery and installation behavior.

## Use

```text
Use $scientific-full-text-citation-verifier to check whether the references in the following paragraph support each scientific claim. Inspect the actual article content, report evidence locations and limitations, and suggest stronger sources or cautious rewrites where needed.

[Paste the paragraph and its references here.]
```

You can also request supporting references for uncited claims or specify publication dates, study designs, populations, models, and databases. The skill supports both explicit invocation and automatic selection when a request matches its description.

## Requirements

This is an instruction-based skill. The package has no executable scripts, package dependencies, API-key requirement, or bundled MCP server. The host agent needs search and article-reading capabilities, or access to article files supplied by the user, to perform verification. PDF access is useful when evidence is available only in PDF form.

Full-text access depends on the papers and the host environment. The skill does not provide subscriptions or guarantee access to paywalled articles. Its instructions require access gaps to be reported explicitly.

## Repository contents

```text
skills/scientific-full-text-citation-verifier/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── search-and-verification-protocol.md
    ├── evidence-scoring.md
    ├── failure-modes.md
    └── output-template.md
```

`SKILL.md` contains the workflow and routes to the supporting references. `agents/openai.yaml` provides the display name, short description, and suggested invocation prompt. These skill files are preserved from the original local skill.

This repository distributes a standalone skill. Distribution through a plugin directory is a separate packaging step.
