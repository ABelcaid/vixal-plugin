# Style Rules

Use this reference when producing Vixal-ready story, page, panel, character, or image-generation prompts. For page structure and panel count, read `panel-layout-rules.md`.

## Global Rendering Rules

These apply to every style and every genre (fantasy, sci-fi, horror, romance, action, slice of life, and so on), not only to the four traditions below, unless the user explicitly asks for a realistic, painted, or 3D look.

Image models drift toward a generic semi-realistic AI-illustration look in every genre: glossy digital painting, purple and orange grading, bloom, colored rim lights, haze, particles, shards, pseudo-HDR contrast, plastic skin, and decoration nobody asked for. Write prompts that describe a drawn illustration in the chosen style instead:

- Describe the rendering method: line weight, ink style, cel or tone shading, color treatment, paper or print look, background treatment.
- Light comes from believable sources in the scene. Genre and mood words (fantasy, sci-fi, horror, romance, action, epic, dramatic, cinematic) describe the story, not the rendering; they are not a request for neon, glow, particles, or color grading.
- Add effects only when the story, environment, a character's ability, or the user requires them. Keep a supernatural effect on the character, object, or area that causes it; never spread it across the page or use it to fill empty space.
- Not every surface is shiny, textured, or equally detailed. Keep simple areas and negative space so the important subject dominates, and keep backgrounds from competing with characters.
- Prefer deliberate comic illustration over painted or 3D-looking rendering, plastic skin, oversharpening, or pseudo-HDR contrast.
- Put these rules into the prompt as positive rendering language. Do not paste a list of banned effects into the image prompt; naming them can pull the model toward them. One short line such as "no added effects or color grading" is enough when needed.
- Skip empty quality boosters ("masterpiece", "8K", "ultra detailed", "highly detailed", "stunning", "epic", "cinematic masterpiece") unless they describe an actual requirement.

## Manga

Use for Japanese manga style.

Visual rules:
- Strict black-and-white grayscale.
- Black ink lineart with screentone shading.
- No color accents, neon, or colored lighting.
- Hand-drawn finish with G-pen or maru-pen feel, organic line wobble, and strong lineweight variation.
- Use crosshatching in deep shadows and textured black fills.
- Paper should be pure white, not yellowed, sepia, beige, or parchment.

Layout rules:
- Right-to-left reading direction.
- Asymmetrical, dynamic layouts that stay readable. Panel count follows pacing (see `panel-layout-rules.md`).

SFX rules:
- Use manga-style graphic SFX. If writing in English, describe it as katakana-style lettering rather than inventing untranslated Japanese text.

## Manhwa

Use for Korean manhwa style.

Visual rules:
- Full-color Korean comic illustration.
- Clean, controlled linework.
- Controlled cel shading or soft painted shading.
- Natural skin and material rendering; highlights describe form instead of making every object glossy.
- Harmonized but restrained palette.
- Scene-motivated lighting by default. Glow, rim light, haze, bloom, and dramatic color lighting only when the scene motivates them.
- Backgrounds simplified or semi-realistic depending on narrative importance.

Layout rules:
- Vertical scroll canvas, top-to-bottom flow, left-to-right reading inside panels.
- Spacing between panels controls timing (see `panel-layout-rules.md`).

SFX rules:
- Integrate SFX as polished graphic design elements.

## Western Comics

Use for American or European comics.

American default:
- Confident ink lines and selective hatching.
- Controlled flat colors or restrained cel shading.
- Clear silhouettes, readable forms, strong but believable contrast.
- Ben-Day dots or flat digital color when a print or retro look fits.

European bande dessinee:
- Clean linework (ligne claire) or expressive ink.
- Restrained natural palette; watercolor or gouache influence where appropriate.
- Strong environmental and architectural clarity.

Use extremely saturated color, harsh chiaroscuro, or superhero lighting only when the project actually calls for that look.

Layout rules:
- Left-to-right, top-to-bottom reading direction.
- Start from a readable underlying grid and break it only for a narrative reason. Clear gutters.
- Splash panels and pages for key moments only.

SFX rules:
- Use hand-lettered SFX that interact with action and panel composition.

## Webtoon

Use for digital vertical-scroll storytelling.

Visual rules:
- Full color optimized for mobile reading.
- Clear silhouettes and readable facial acting at phone size.
- Style can lean manhwa soft shading or flat graphic illustration; ask for the sub-style if it changes the output.
- Simplified backgrounds for dialogue, detailed backgrounds for establishing or story-critical moments.
- Motion blur, glow, particles, speed lines, debris, haze, and digital lighting appear only when they communicate a specific action, ability, weather condition, emotion, or story event. Never add them just because the scene is dramatic.

Layout rules:
- Strict top-to-bottom vertical scroll, left-to-right reading inside panels.
- Usually one major visual beat per screen; white space, color blocks, or scenic transitions instead of boxed page gutters.

SFX rules:
- Integrate SFX into the scroll as graphic design, not as detached labels.

## Dialogue And Captions

For all traditions:
- Put dialogue only in speech balloons.
- Use `Speaker:` labels for clarity.
- Separate dialogue, captions, and SFX.
- Keep captions purposeful: time, location, internal thought, or transition.
- Do not use dialogue to explain what the image already shows clearly.
