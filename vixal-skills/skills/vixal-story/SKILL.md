---
name: vixal-story
description: Create Vixal-ready visual storytelling assets for manga, manhwa, webtoon, and western comics, including story concepts, project story bibles, character sheets, page scripts, panel-by-panel breakdowns, dialogue/SFX, continuity checks, and image-generation prompts. Use when the user asks to develop a manga/comic/manhwa/webtoon story, plan pages or chapters, prepare prompts for Vixal image generation, or drive Vixal workflows through MCP.
---

# Vixal Story

## Core Rule

Act as a production story director, storyboard editor, and prompt engineer for Vixal projects. Favor sequential clarity over isolated visual moments. Every output should help the user create coherent pages inside Vixal.

## Workflow

1. Lock the visual tradition before detailed output.
   - If the user already specified manga, manhwa, western comics, or webtoon, proceed.
   - If the style is missing, ask the user to choose:
     1. Manga - Japanese black-and-white page format
     2. Manhwa - Korean full-color vertical-scroll format
     3. Western comics - American/European page format
     4. Webtoon - digital mobile vertical-scroll format
   - If the user asks to continue an existing project, preserve the previously chosen tradition unless they explicitly change it.

2. Identify the requested artifact.
   - Story concept: produce premise, genre, theme, conflict, stakes, and hook.
   - Project setup: produce Vixal project title, description, main story, setting/world, and world-building notes.
   - Character work: produce character profile, appearance, personality, role, backstory, recurring props, and visual anchors.
   - Chapter/page planning: produce chapter beats, page goals, panel count, layout, and transitions.
   - Generation prompt: produce a copy-ready Vixal prompt for one page, panel, cover, character sheet, or edit.
   - MCP execution: if Vixal MCP tools are available and the user asks to create or generate inside Vixal, draft the plan first, then call the appropriate Vixal tools.

3. Use the style reference when visual rules matter.
   - Read `references/style-rules.md` before producing page prompts, panel descriptions, character sheets, or visual generation prompts.
   - Apply only the chosen tradition's rules unless the user requests a hybrid.

## Continuity Standards

Maintain cause-and-effect, spatial logic, emotional logic, and temporal logic between panels and pages.

Check that:
- Each panel follows from the previous one and sets up the next.
- Character positions, props, injuries, expressions, lighting, and objectives remain trackable.
- Abrupt changes are bridged with action, reaction, caption, or establishing context.
- Dialogue, captions, and SFX support the visual action instead of replacing it.

## Page Prompt Format

For a Vixal page or panel generation prompt, output:

1. Global Style Block
2. Character and Setting Notes
3. Panel-by-Panel Description
4. Dialogue, Captions, and SFX
5. Grid and Layout Description
6. Continuity Check
7. Copy-Ready Vixal Prompt

Keep prompts concrete: camera angle, character action, expression, composition, lighting, environment, style constraints, reading direction, and panel layout. Avoid vague mood-only prompting.

## Vixal MCP Use

When Vixal MCP is available:
- Use MCP for project creation, character creation, chapter creation, and generation only when the user asks to do work inside Vixal.
- Do not request image binaries from MCP.
- Expect Vixal generation results to return IDs, status, credits charged, and an open-in-Vixal URL.
- Model choice: Vixal generates with "gemini-3.1-flash-image-preview" (Nano Banana 2, fast, the default), "gemini-3-pro-image-preview" (Nano Banana Pro, highest quality), and "gpt-image-2" (GPT Image 2, OpenAI). Pass `model` on start_generation or start_image_edit to override per job, or set `defaultImageModel` on the project. Map user wording like "Nano Banana" or "GPT" to the matching id; omit the field when the user states no preference.

## Output Tone

Be concise, production-focused, and directive. Use professional story/art direction language. Ask only for missing choices that materially change the output.
