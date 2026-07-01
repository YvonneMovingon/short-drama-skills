# 01 · General Narrative Breakdown

English | [简体中文](./prompt.zh-CN.md)

**Best for:** everyday plot progression / dialogue scenes / scene transitions  
**Includes:** generation logic + expected shot format + shot duration estimation

This skill breaks script narrative into executable continuous shot sequences. It includes shot-splitting principles, structured visual description rules, and duration estimation instructions, covering the full path from raw script to executable video prompts.

### Example

**Original script ↓**

![Original script](../../assets/script-before.png)

**→ Automatically broken into narrative units ↓**

![Broken-down narrative units](../../assets/script-after.png)

**[Use in LuxReal ->](https://luxreal.com?skill=01)**

---

## Full Skill

```markdown
## Constraints

### 0. Global Pacing Control (Highest Priority)

> **This prompt is designed for vertical short dramas / short-form video. The overall pacing is fast narrative pacing. The following two rules have the highest priority. If they conflict with any other rule, this section wins.**

#### 0-B. Information Density Principle (Highest Priority)

**Do not cut to a new shot unless the new shot provides new information.** A new shot must introduce plot progression, new environmental detail, or stronger emotional intensity. If there is no new information, allow the same shot size and camera position to continue. Do not force a cut.

#### 0-C. Non-Narrative Shot Limit

Within a single beat, non-narrative shots such as empty shots, transition shots, or relationship-establishing shots must account for **no more than 20%** of the total duration. If the ratio exceeds 20%, remove empty shots and transition shots first.

### 1. Shot-Splitting Principles

#### Narrative and Action

1. **Three-part breakdown for complex actions** — motivation / preparation -> execution -> result / reaction. Follow match-on-action logic.
2. **Spatial transitions require a cut** — every location change must create a new shot.
3. **Time jumps require a cut** — non-continuous time passage must be visualized.
4. **Relationship changes require a cut** — cut when character positions or dominance relationships change.
5. **Overloaded group shots require splitting** — if more than two people appear in the same frame, split the scene, prioritizing single-character close-ups or two-character medium shots.

#### Emotion and Performance

1. **Sudden emotional shifts cut to close-up** — intense instant emotional changes must use a close-up.
2. **Gradual emotional shifts use shot-size progression** — do not cut abruptly. Move closer to the character through progressively tighter framing.
3. **Dialogue eye-line ping-pong** — speaker -> listener -> speaker. Critical reaction shots are often more important than speaking shots.

#### Audiovisual Language

- J-cut: audio from the next scene begins before the visual cut.
- L-cut: audio from the current scene continues into the next shot.
- VFX-exclusive shot: the core visual-effect moment must receive its own shot.
- Beat control: tension and fights use shorter shots; lyrical or suspenseful scenes use longer shots.

#### Static Shot Forced Splitting

- A static image must not remain on screen for more than **6 seconds**.
- If dialogue duration exceeds 6 seconds, split it immediately into multiple sub-shots, each with its own visual image.

#### Long Dialogue Splitting Rule

Trigger: estimated duration exceeds 8 seconds.

**Core principle: preserve every word while keeping rhythm.** Do not compress, omit, rewrite, or reorder the original dialogue.

Split anchors, in priority order:

Topic shift -> emotional shift -> logical hierarchy shift -> natural breath point

Audiovisual technique allocation:

| ID | Technique | Use Case |
|----|-----------|----------|
| T1 | Frontal speaking shot | The speaker actively delivers key information |
| T2 | Reaction shot | Show the listener's reaction after information is delivered, with dialogue as V.O. |
| T3 | Prop / detail close-up | Dialogue mentions a concrete object, with dialogue as V.O. |
| T4 | Flashback / symbolic image | Dialogue refers to memory or past events, with dialogue as V.O. |
| T5 | Shot-size progression | Emotion escalates step by step |
| T6 | Action accompaniment | The character speaks while doing something |
| T7 | V.O. visual switching | Narration or voice-over paired with changing visuals |

Constraints:

- T1 must account for no more than 60%.
- T2 must not appear more than once in a row.
- T4 may only be used when there is a clear visual reference.

---

### 2. Five Rules for Visual Conversion

1. **Make dialogue concrete** — if dialogue refers to a specific past event, insert a flashback shot. Do not only film a talking-head close-up.
2. **Externalize subtext** — abstract emotions must become visible physical actions or prop interactions. For example, "anxious" -> "fingers repeatedly pick at the edge of the coat, nails turning pale".
3. **No imagined action gaps** — stay faithful to the original physical action. If an action jumps from one state to another, add a transition action. No teleporting.
4. **Lock the point of view** — unless the script explicitly says otherwise, do not switch locations on your own. When off-screen voice appears, focus the shot on the listener's reaction in the room.
5. **Close-up for key information** — any plot-driving prop must receive its own close-up. Do not bury key information in a wide shot.

---

### 3. Structured Visual Description

Each visual description must include the following four dimensions:

**[Camera and Composition]**  
Specify shot size (close-up / medium shot / wide shot), camera movement (push in / pull out / pan / tracking / handheld / locked-off), and angle (eye-level / low angle / high angle / over-the-shoulder / POV, etc.).

**[Subject Description]**  
Do not use vague phrasing such as "same as above", "then", "he", or "she". Merge the same character's action, expression, and prop interaction into one coherent long sentence, separated by commas. Do not split them with semicolons.

Correct: "Xiao Ming shuts his eyes tightly, his brows twitch violently, his fingers gripping the cracked bowl until the knuckles turn white."

Incorrect: "Xiao Ming shuts his eyes tightly; Xiao Ming's brows twitch; Xiao Ming grips the bowl."

**[Lighting / Atmosphere]**  
Only describe lighting that is necessary for the story, such as a key prop reflection or dramatic light effect. If there is no special need, omit this field.

**[Background]**  
Fill this in only for the first shot or when the shot direction changes significantly. Keep it short, around a few words, such as "basement corner" or "school track".

---

### 4. Shot Duration Estimation

| Shot Type | Formula / Duration |
|-----------|--------------------|
| Dialogue, normal pace | `round(character_count / 8) + 1s` |
| Dialogue, argument / urgent pace | `round(character_count / 10) + 1s` |
| Dialogue, intimate / final words | `round(character_count / 5) + 1s` |
| V.O. narration | `round(character_count / 7) + 1s` |
| Micro action / routine action | `2s` |
| Complex continuous action | `4s` |
| Strong emotional reaction | `3s` |
| Environment / empty shot / still object | `2s` |
| Slow-motion effect | `3-4s` |

**Conflict rule:** if a shot contains both dialogue and action, use the larger duration estimate.  
**Duration cap:** each shot must be strictly limited to 12 seconds or less.

---

## Workflow

1. Read the script carefully. Understand the plot, character relationships, and emotional tone. Refer to character and scene images to confirm the visual style.
2. Break down shots according to the shot-splitting principles. **Apply the forced static-shot splitting rule during breakdown.**
3. Estimate each shot's duration using the duration rules.
4. Write visual descriptions according to the structured visual description rules.
5. Check whether non-narrative shots exceed 20% within a single beat. If they do, simplify.
6. Add shot size, camera movement, dialogue, sound effects, and design intent.
7. Generate the final JSON.
```
