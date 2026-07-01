# Short Drama Skills

Production-tested prompt rules for AI short drama generation.

Turn raw scripts into structured shot sequences, cinematic video prompts, and reusable production workflows.

These skills come from LuxReal's internal short drama pipeline. They are designed for creators, studios, prompt engineers, and developers building script-to-video or AI video production tools.

English | [简体中文](./README.zh-CN.md)

[![Stars](https://img.shields.io/github/stars/YvonneMovingon/short-drama-skills?style=flat-square)](https://github.com/YvonneMovingon/short-drama-skills/stargazers)
[![Skills](https://img.shields.io/badge/Skills-7-blue?style=flat-square)](#skills)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](./LICENSE)

---

## What Problem Does This Solve?

Most AI video workflows can generate a single clip.

The hard part is making a story work across many shots:

- How many shots should a script be split into?
- What should each shot show?
- How long should each shot last?
- How do you handle dialogue, reactions, emotional beats, action scenes, and scene transitions?
- How do you keep the output structured enough for a real production pipeline?

**Short Drama Skills** is a collection of reusable prompt rules for turning scripts into executable video production instructions.

Instead of asking an AI model to "write a storyboard", these skills tell the model how to break down narrative beats, estimate shot duration, describe camera language, and generate structured outputs.

---

## Core Skill: General Narrative Breakdown

This is the most broadly useful skill in the repo.

It turns a script segment into a structured shot sequence. Each shot includes:

- **Shot type, camera movement, and angle**
- **Subject description**, including character action, expression, and prop interaction
- **Lighting and atmosphere**, only when relevant to the story
- **Estimated duration**, based on dialogue length and action type
- **Structured output**, ready for downstream video generation workflows

Use it for:

- Everyday dialogue scenes
- Short drama plot progression
- Scene transitions
- Script-to-shot-sequence workflows

[View the skill ->](./skills/01-通用叙事拆解/prompt.md)

---

## Quick Start

You can use these skills in any LLM that supports long prompts.

1. Open a skill under `/skills`
2. Copy the content from `prompt.md`
3. Paste it into ChatGPT, Claude, or your own LLM pipeline
4. Add your script after the prompt
5. Use the structured output in LuxReal or another AI video generation workflow

You can also use the skills directly in LuxReal:

[Use in LuxReal ->](https://www.luxreal.com/festatic/create_ads?utm_source=GitHub&utm_medium=website&utm_campaign=shortdrama_skills)

---

## Skills

### Storyboard Generation

| # | Skill | What It Does | Best For |
|---|-------|--------------|----------|
| 01 | [General Narrative Breakdown](./skills/01-通用叙事拆解/prompt.md) | Turns scripts into structured shot sequences with duration estimates | Dialogue, plot progression, scene transitions |
| 02 | [Emotional Scene Breakdown](./skills/02-深度情绪刻画/prompt.md) | Breaks emotional dialogue scenes through power shifts, reactions, and close-ups | Confession, argument, interrogation, negotiation |
| 03 | [Action Scene Description](./skills/03-详细动态描述/prompt.md) | Converts action-heavy scenes into detailed motion and camera descriptions | Fight scenes, chase scenes, physical conflict |
| 04 | [Episode Continuity Splitting](./skills/04-按剧情连贯拆分副本/prompt.md) | Groups continuous clips into coherent shots while preserving pacing and continuity | Multi-episode short dramas |

### Video Prompt Polishing

| # | Skill | What It Does | Best For |
|---|-------|--------------|----------|
| 05 | [Video Prompt Polishing](./skills/05-单视频提示词润色/prompt.md) | Turns rough scene descriptions into structured video prompts | General video generation |
| 06 | [High-Impact Drama Polishing](./skills/06-高能戏剧化情节润色/prompt.md) | Creates high-intensity cinematic prompts for dramatic moments | Action peaks, strong openings, viral hooks |
| 07 | [Slow Cinematic Polishing](./skills/07-慢节奏细腻质感润色/prompt.md) | Creates subtle, emotional, slow-paced cinematic prompts | Inner monologue, poetic scenes, quiet emotional beats |

---

## Who Is This For?

- **AI video developers** building script-to-video workflows
- **Short drama studios** producing episodic content at scale
- **Prompt engineers** designing reusable video generation pipelines
- **Creators** who need professional shot planning without a full production crew
- **Tool builders** looking for MIT-licensed prompt logic to integrate into their products

---

## How This Is Different

| Approach | What It Can Do | Limitation |
|----------|----------------|------------|
| Asking an LLM to "write a storyboard" | Produces a basic result | Shot count, duration, pacing, and camera logic are often random |
| Generic video prompt templates | Gives a reusable format | Does not handle narrative pacing, long dialogue, multi-character scenes, or action logic |
| **Short Drama Skills** | Provides production-tested rules for narrative breakdown, emotional beats, action scenes, and prompt polishing | Works best when paired with an AI video generation tool such as LuxReal |

---

## Repository Structure

```txt
short-drama-skills/
├── README.md
├── README.zh-CN.md
├── skills/
│   ├── 01-通用叙事拆解/
│   │   ├── prompt.md
│   │   ├── prompt.zh-CN.md
│   │   ├── skill.md
│   │   └── example/
│   ├── 02-深度情绪刻画/
│   ├── 03-详细动态描述/
│   ├── 04-按剧情连贯拆分副本/
│   ├── 05-单视频提示词润色/
│   ├── 06-高能戏剧化情节润色/
│   └── 07-慢节奏细腻质感润色/
├── assets/
└── CONTRIBUTING.md
```

---

## About LuxReal

LuxReal is an AI short drama production platform.

Upload a script, extract characters and scenes, generate storyboard previews, keep character consistency across episodes, and produce short drama videos at scale.

These skills are part of the prompt logic behind LuxReal's internal production workflow.

[Try LuxReal ->](https://www.luxreal.com?utm_source=GitHub&utm_medium=website&utm_campaign=shortdrama_skills)

---

## Contributing

We welcome skills that have been tested in real AI video or short drama production workflows.

To contribute:

1. Fork this repository
2. Add a new skill under `/skills`
3. Include a clear use case, prompt file, and example input/output
4. Open a pull request explaining when and how the skill should be used

Please avoid submitting generic prompts. This repo is focused on production-ready rules that solve specific video generation problems.

---

## License

MIT
