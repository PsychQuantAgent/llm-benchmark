# llm-benchmark

Model characteristics, benchmark results, and a module that derives model and effort recommendations from them, across vendors: Claude, OpenAI, Gemini, and local models.

## Why

Tools that call models (Claude Code skills, the codex-pro plugin, ensemble reviewers) each used to pin a default model in their own files. Those defaults went stale one by one and disagreed with each other. This repository replaces them with one source:

- **Characteristics** — what each model and effort level is, as recorded data with its source and the date it was checked.
- **Benchmarks** — results measured on our own tasks, with the conditions needed to reproduce or compare them.
- **Recommendations** — a module that takes a kind of task and returns a model and effort level computed from the data above. When it cannot compute one, it says so instead of guessing.

## Consumers

- [PsychQuant/codex-pro](https://github.com/PsychQuant/codex-pro) — no hardcoded default model; a call that names neither a role nor a model gets the recommendation for its kind of task (PsychQuant/codex-pro#17).
- [PsychQuantAgent/claude-code-logos](https://github.com/PsychQuantAgent/claude-code-logos) — the `model-effort` skill.

## Status

Just created. The design of the data format and of the recommendation module is open; see the issues.
