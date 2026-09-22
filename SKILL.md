---
name: generate-vehicle-diorama
description: Generate a square, 45-degree isometric 3D collectible miniature diorama poster for a classic vehicle or an IP-themed vehicle. Use when the user says “载具微缩图”, asks to turn a named car, aircraft, ship, spacecraft, fictional machine, character, mascot, brand, or IP into a premium vehicle diorama, or wants the reusable vehicle-miniature prompt applied to generate an image.
---

# Generate Vehicle Diorama

Create the image, not merely a prompt, unless the user explicitly asks only for prompt text.

## Collect inputs

Accept natural-language requests. Treat only the subject as required.

- `subject`: named vehicle or source theme/IP
- `vehicle_type`: optional; infer a fitting type when the subject is not itself a vehicle
- `scene`: optional; infer the most recognizable environment
- `background_color`: optional; infer a contrasting solid color
- `title`: optional; default to the subject or vehicle name
- `subtitle`: optional; generate a concise 8–16 Chinese-character line in the user's language
- `reference_images`: optional; use them to guide identity, silhouette, materials, or visual language

If `subject` is missing, ask one focused question. Otherwise, infer missing inputs and generate immediately without reconfirmation.

## Resolve the subject

Choose exactly one mode:

1. **Existing vehicle** — faithfully preserve its iconic silhouette, proportions, signature colors, and recognizable parts.
2. **Fictional machine or craft** — recreate the canonical vehicle as a premium collectible while preserving recognizability.
3. **Character, mascot, brand, or non-vehicle IP** — design an original themed vehicle inspired by its recognizable palette, motifs, energy, and world. Keep the result unmistakably a vehicle; do not place an ordinary full-size character alone on the base. A tiny stylized figure may appear only as supporting context.

For ambiguous requests such as “皮卡丘载具微缩图”, prefer mode 3 and create a yellow electric adventure vehicle with ear-like forms, red cheek accents, lightning motifs, and a Pokémon-inspired grass battle environment.

## Build the scene

- Use a clear 45° elevated isometric view showing the top, front/side, and the complete base.
- Make the vehicle the dominant focal point and occupy roughly 45–60% of the image area.
- Place it on a compact raised base with visible thickness and clean beveled edges.
- Match the base to the vehicle's most recognizable context: road, racetrack, garage, runway, ocean, spaceport, desert, forest, city, bedroom, workshop, or battle arena.
- Add only 3–6 small contextual props. Keep all props subordinate to the vehicle.
- Use refined PBR materials with clear metal, paint, rubber, glass, plastic, wood, fabric, or terrain separation as appropriate.
- Light it like premium product photography: soft cinematic key light, restrained reflections, natural contact shadows, and no harsh overprocessing.
- Use one clean solid-color background with no gradient or environmental backdrop.

## Compose the poster

- Output a centered 1:1 square composition, intended for 1080×1080.
- Reserve generous clean space at the top.
- Add a large bold centered title and one smaller centered subtitle beneath it.
- Use black type on light backgrounds and white type on dark backgrounds.
- Keep title and subtitle exact. Do not add extra labels, logos, watermarks, signatures, UI, or random lettering.
- Add an original decorative badge only when it improves the design. Do not fabricate an official logo.

## Generate

Use the image-generation tool with the user's reference images when provided. Translate the resolved design into one cohesive generation prompt. Include these quality constraints:

> premium collectible diorama, crisp 45-degree isometric view, physically based materials, miniature manufacturing detail, soft cinematic studio lighting, complete raised base, centered composition, solid-color background, clean commercial poster, high recognizability, square 1:1

Also include these exclusions:

> no gradient, no clutter, no cropped base, no low-resolution texture, no cheap plastic look, no warped wheels or mechanical parts, no duplicate vehicle, no distorted proportions, no illegible or extra text, no watermark

Do not expose a long internal prompt before generation unless the user asks to see it.

## Check the result

Verify visually after generation:

- the subject reads instantly;
- the vehicle remains the main focus;
- the view is approximately 45° isometric;
- the complete raised base is visible;
- the background is a single flat color;
- the title and subtitle are legible and correctly spelled;
- no unwanted text or major geometry errors appear.

If a major requirement fails, make one targeted regeneration correcting only the failed items. Return the strongest result with a short note naming the chosen vehicle concept, scene, and background color.

## Example requests

- “用载具微缩图做一张 AE86，秋名山，深灰背景。”
- “生成皮卡丘载具微缩图，其他细节你自动决定。”
- “把蝙蝠车做成黑色收藏级微缩场景海报。”
- “只给我一份可复制的载具微缩图提示词，不要生成图片。”
