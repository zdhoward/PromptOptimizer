# Research register

Initial source review: 2026-10-29. These are documented capabilities and research directions, not locally reproduced results. Novelty remains unestablished.

## Existing work

- [Microsoft LLMLingua](https://github.com/microsoft/LLMLingua) and [LLMLingua-2 paper](https://arxiv.org/abs/2403.12968): prompt compression including encoder-based token classification. Relevant non-generative baseline; does not establish this project's conversational fidelity.
- [Prompt Enhancer](https://github.com/And1zle/prompt-enhancer): documents browser draft rewriting through local OpenAI-compatible servers, including LM Studio and Ollama. Runtime reliability and T3 compatibility were not verified.
- [Prompt Optimizer](https://github.com/linshenkx/prompt-optimizer): existing prompt optimization application with local-model connectivity. Review its overlap before building another editor.
- [Open WebUI filters](https://docs.openwebui.com/features/extensibility/plugin/functions/filter/): documented input modification extension point. Possible integration target, not evidence of a hook in T3 Code.
- [Anthropic prompt caching](https://platform.claude.com/docs/en/build-with-claude/prompt-caching): cache behavior must be accounted for when evaluating context changes. Smaller payloads alone do not establish lower total cost.

## Current hypotheses

- Explicitly preserving uncertainty, authorization, and provenance may improve reliability beyond generic rewriting.
- Relevant retained context plus current-message interpretation may outperform either layer alone.
- Rules and small classifiers may cover some stages; general interpretation may still need a local generative model.
- Playbooks may be sufficient initially; custom training is not yet justified.

## Open research

1. Verify Jev's authoritative sources and supported integration contract.
2. Survey competing intent extraction, prompt adaptation, and context tools; do not claim novelty yet.
3. Establish representative tasks and a held-out evaluation set.
4. Measure fidelity before optimizing size, speed, or cost.
5. Investigate actual subscription accounting separately from API token pricing.
6. Evaluate funding/sponsorship fit only after evidence and license requirements are clear.
