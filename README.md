# PromptOptimizer

An open research project exploring local, intent-preserving prompt adaptation.

Write naturally. Inspect how your request is interpreted. Send a prompt suited to the receiving system.

**Status: research scaffold, version 0.1.0. No runnable optimizer or measured benefits yet.**

## Hypothesis

A local pipeline can interpret conversational requests, attach supported context, and render useful instructions without changing intent. The result may be longer or shorter. Quality is the primary goal; cost and time to a satisfactory outcome also matter.

Jev integration is a research priority. Compatibility, interfaces, and combined performance are unverified. This project is independent and does not imply affiliation or endorsement.

## Proposed pipeline

1. Preserve the original message and extract intent before deleting language.
2. Represent goals, constraints, uncertainty, alternatives, dependencies, and authorization.
3. Enrich with relevant, attributable context; distinguish stated, retrieved, and inferred information.
4. Check contradictions, missing references, and changes in meaning.
5. Render for the destination; apply optional compression only where justified.

JSON is a candidate internal representation, not a requirement for every outgoing prompt. No schema or architecture is final.

## Project map

- [Research and sources](research/README.md)
- [Testbed design](docs/TESTBED.md)
- [Synthetic cases](fixtures/cases.jsonl)
- [Roadmap](ROADMAP.md)
- [Decisions and project log](CHANGELOG.md)
- [Handoff](HANDOFF.md)
- [Contributing](CONTRIBUTING.md)

## Boundaries

Do not invent missing facts, silently turn suggestions into requirements, or treat task extraction as execution authorization. Unknown, not applicable, deliberately unspecified, and conflicting values must be distinguishable.

Local operation is a design goal. Any future remote processing must be explicit. Public fixtures must be synthetic or intentionally contributed with publication rights; never upload private chat histories, credentials, or personal context by default.

Released under the MIT license. Sponsorship is welcome, but there are no sponsors or validated subscription-multiplication claims at this stage.
