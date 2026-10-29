# Testbed proposal

## Question

Does structured intent adaptation improve downstream outcomes compared with the original message and a simple rewrite, without changing meaning or authorization?

## Experimental arms

- Original message, unchanged.
- Deterministic cleanup only.
- Simple local-model rewrite.
- Structured extraction, validation, and rendering without enrichment.
- Structured adaptation with attributable context.
- Jev alone and Jev plus adaptation, once a supported integration is verified.

Keep destination model/version, task inputs, available context, and output budget comparable. Record all prompts and configuration. Keep development and held-out cases separate; record repeat runs and variability. Do not select only favorable examples.

## Measurements

Primary: intent preservation, constraint retention, authorization preservation, unsupported additions, correct handling of uncertainty, and downstream task success.

Secondary: user corrections, preprocessing latency, total time to accepted result, input/output tokens, cache behavior where observable, and measured cost or allowance consumption. Unknown subscription accounting stays unknown; token reductions are not evidence of proportional subscription savings.

Human-reviewed expected behavior is the initial reference. Automated judges may supplement it, but must not be the only evidence. An authorization change or invented hard requirement is a critical failure even if an answer appears useful.

## Fixture format

Each JSONL record has an id, synthetic input, optional supplied context, expected behavior, and forbidden transformations. These are behavioral cases, not golden wording. Fixtures are public; real personal messages require explicit publication consent.

## First implementation slice

An offline inspect-only runner: load a case, produce a candidate representation and rendered prompt, show differences and provenance, and record reviewer acceptance/corrections. Do not intercept chats or send requests to a destination automatically.

Choose the implementation language and model/backend after a small baseline evaluation. Start with rules and playbooks; add training only when labeled failure evidence justifies it.

## Jev integration discovery

Before implementation, identify the authoritative Jev repository/docs, supported versions, license, extension points, and actual context formats. Verify whether an integration can retrieve source material, distinguish stale decisions, and preserve stable context/cache prefixes. Treat bidirectional updates as proposals requiring a defined acceptance policy. Do not assume undocumented hooks or compatibility.

## Execution policy

Fixtures have not been executed. Run tests only on an explicit owner request or owner-declared sprint end. Do not report a scaffold as a working optimizer.
