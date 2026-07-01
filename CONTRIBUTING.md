# Contributing

English | [简体中文](./CONTRIBUTING.zh-CN.md)

We welcome skills that have been tested in real short drama or AI video production workflows.

This repository is focused on reusable, production-ready prompt rules. Please avoid submitting generic prompts that only describe a style or ask an LLM to "make it better".

## Submission Flow

1. Fork this repository.
2. Create a new folder under `skills/`.
3. Add a clear `prompt.md` file.
4. If possible, include an example input and output under an `example/` or `examples/` folder.
5. Update the skill list in the root `README.md`.
6. Open a pull request and explain the production scenario where this skill is useful.

## Skill Format

Each skill should include:

- **Purpose:** one sentence explaining the problem this skill solves.
- **Best for:** 2-3 concrete scenarios where the skill should be used.
- **Full prompt:** complete and directly copyable.
- **Usage notes:** important parameters, constraints, or input expectations.
- **Example:** preferred, especially if the skill produces structured output.

## Quality Standard

- The skill must have been tested in a real or realistic production workflow.
- The prompt must be complete and usable without hidden internal context.
- Do not leave unresolved placeholders.
- Preserve original dialogue and character information when the skill is designed for narrative or video generation.
- Before submitting, test the prompt with at least one input and check whether the output is structured and executable.

## Translation Notes

This repository uses English as the default public entry point and keeps Chinese versions alongside the English files.

Recommended file pattern:

```txt
prompt.md        # English default
prompt.zh-CN.md  # Simplified Chinese version
```

If you submit a Chinese-only skill, that is still welcome. Please mention it in the pull request so maintainers can help adapt it for English users.
