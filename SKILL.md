---
name: character-casting-studio
description: Create original, material-reference-driven, consistent, photorealistic character casting sheets for commercial, advertising, cinematic, model, occupational, everyday, historical, traditional-cultural, literary, or lightly fantastical character concepts. Use when the user wants a designed person, a casting reference, a character asset sheet, a model card, or a single image containing front, side, back, and facial-detail views with coherent identity, wardrobe, body type, source-material synthesis, and photographic quality.
---

# Character Casting Studio

Use this skill to turn a natural-language character brief into an original, reusable human character asset. Treat the result as a casting sheet or character design reference, not as a random portrait.

## Core Direction

Build every output on this combined foundation:

- photorealistic commercial photography
- believable cinematic character presence
- polished advertising production value
- high-end model-casting clarity

Prioritize:

`character accuracy > beauty`

`realism > perfection`

`recognizable design > generic AI face`

`original identity > resemblance to a real person`

Avoid influencer faces, e-commerce model clichés, game-concept styling, anime or fantasy illustration, plastic skin, excessive retouching, and generic facial templates.

## Input Handling

Accept either:

1. **Broad brief**: gender, age range, region or cultural appearance, role, and general mood.
2. **Detailed character brief**: any combination of identity, facial structure, distinctive marks, hair, makeup, body type, pose, wardrobe, and visual treatment.

Parse the brief into these fields:

- identity: gender presentation, age range, region or nationality direction, occupation, social role, model/civilian/advertising/cinematic emphasis
- face: face shape, brows, eyes, nose, lips, jaw, cheekbones, facial tension or softness
- distinctive details: moles, freckles, scars, wrinkles, pores, asymmetry, sun marks, uneven skin, or other restrained identifiers
- hair and makeup: hairstyle, hair color, texture, makeup intensity, blush, natural or styled finish
- body and pose: height impression, slim/muscular/soft/heavy build, model proportions, relaxed or controlled posture, confidence, tension, age-appropriate weight distribution
- wardrobe: garment type, color, material, fit, accessories, cultural or occupational logic
- image treatment: commercial, cinematic, advertising, casting, everyday, documentary, or realistic historical/fantastical treatment

Follow the user's explicit details exactly. Fill only unspecified fields. Do not silently change age, gender, regional direction, face features, hair, makeup, body type, wardrobe, or role.

## Source Material Gate

For film, commercial, advertising, fashion, or model-grade character work, use source materials before final image generation. Do not rely on a generic text-only face when distinctive casting quality is required.

For production-grade output, require a small source packet with a minimum of three complementary inputs. Never silently fall back to a text-only generic face:

When a local or explicitly authorized reference library is available, read [references/material-reference-library.md](references/material-reference-library.md) and select only the relevant assets for the current character or batch. Do not commit private reference images, clipboard screenshots, personal photos, or source files containing identifying information to a public repository.

1. **Face or person references:** two or three different faces, portraits, or broad human-feature references. Extract face geometry, eye and brow spacing, nose and lip proportions, age cues, asymmetry, skin texture, and hair tendencies. Do not copy any one person's identity.
2. **Wardrobe / body / pose references:** garments, silhouettes, accessories, posture, occupation, or movement references that define the character's casting logic.
3. **World / material / light references:** locations, architecture, objects, fabric, color, film stills, photographic light, or surface textures that define the visual world.

Create an internal source map before writing the final prompt, for example: `Source A = cheekbone and brow structure; Source B = hair and skin detail; Source C = coat construction; Source D = light and palette`. Recombine at least three sources, perturb facial proportions, and add a new identifying detail so the result is an original person rather than a composite copy.

If the user provides only one face image, use it as a limited reference for broad traits, skin or lighting direction, and request or create additional non-identity material references before calling the result production-ready. If no source material is available, label the output as an exploratory draft and do not present a generic face as a finished film, commercial, or model casting result.

## Batch Identity Diversity Gate

For a set of characters, share the world and casting direction but force identity separation. Never let the batch collapse into siblings, twins, or repeated AI faces unless the user explicitly requests that relationship.

- Build an identity matrix before prompting: face shape, eye shape and spacing, brow structure, nose profile, lip shape, jaw, hair length and texture, skin-tone range, age impression, body silhouette, posture, and one small identifying detail.
- Change at least five of those dimensions between adjacent characters. Do not repeat the same combination of oval face, straight black hair, almond eyes, high cheekbones, and neutral expression across the set.
- Do not reuse one face reference as the dominant face source for every character. Use a different source combination for each character; a single uploaded portrait may inform skin or lighting only for the rest of the batch.
- State `distinct unrelated individuals, not sisters, not twins, not triplets, not the same face` in multi-character prompts unless the story requires family resemblance.
- If two close-ups still read as the same person, regenerate the less distinctive character before returning the batch.

## Generation Workflow

### Step 1 - Default: Generate the Person

For an ordinary character request, generate the person as the primary output. Focus on face, temperament, makeup, hair, clothing, age, identity, and photographic quality. Use a single character image unless the user explicitly requests another layout. Do **not** automatically generate a three-view, four-view, white-background character sheet, or character breakdown.

The default output should read as a finished character portrait or full-body character photograph. Use the user's requested framing and setting; if framing is unspecified, choose the framing that best shows the requested identity and styling.

### Step 2 - On-Demand: Character Breakdown / Multi-View Asset

Activate this mode only when the user explicitly asks for terms such as `做三视图`, `生成人物三视图`, `白底角色图`, `角色拆解`, `character turnaround`, `three-view character sheet`, or an equivalent multi-angle asset request.

When activated, use the already approved/generated person as the source of truth. Do not redesign the character. Keep the face shape, facial features, moles, hairstyle, makeup, skin tone, clothing, age, body proportions, and overall temperament consistent; change only the observation angle or the explicitly requested asset view.

Default multi-view instruction:

> 根据已确定的人物形象生成角色多视图资产。保持人物身份和视觉特征一致，不重新设计五官、发型、妆容或服装。使用干净白色背景，无文字、无信息栏、无额外装饰。根据用户要求输出正面、侧面、背面或其他指定角度。该功能仅在用户明确提出时触发，不作为默认人物生成流程的一部分。

For this mode, use a clean white background with no text, information panels, labels, or decorative elements unless requested. Output only the angles requested by the user. The upper full-body row and lower facial close-up camera split applies only when the user explicitly requests that casting-sheet layout.

## Rendering Rules

### Realistic Foundation

- Use believable skin texture and restrained retouching.
- Keep pores, fine lines, freckles, moles, scars, wrinkles, and subtle asymmetry when specified or useful.
- Make clothing complete, wearable, and physically coherent.
- Use clean, controlled, believable light with readable facial planes and garment materials.
- Keep posture and gestures natural, controlled, and appropriate to the character.

### NO WAX SKIN / 禁止蜡像感

Apply this as a hard rule to every human face, especially Chinese and East Asian characters:

**中文版：** 面部皮肤必须真实自然，禁止蜡像感、塑料感、油腻高光感和过度磨皮。保留轻微毛孔、细小纹理、自然色差与真实皮肤起伏，整体为自然半哑光质感。

**English:** Skin realism is critical. Avoid waxy skin, plastic skin, oily highlights, over-smoothed beauty retouching, and mannequin-like facial rendering. Use natural semi-matte skin with subtle pores, fine texture, slight tonal variation, and believable real-photography skin detail.

Enforce these constraints in the prompt and quality gate:

- no oily forehead, no glossy cheeks, no shiny nose bridge, restrained skin highlights
- subtle pores, slight natural skin texture, realistic under-eye texture, gentle tonal variation
- no over-retouching, no porcelain skin, no beauty-filter effect, no mannequin face
- Allow mild asymmetry, small imperfections, and slight color variation around the nose wings, mouth corners, and under-eyes.
- Keep makeup readable as real commercial makeup, never as a beauty-filter finish.

### Anti-Gloss Fallback

When fashion, couture, luxury, or advertising direction conflicts with skin realism, skin realism has priority. Treat skin as a factual material, not a beauty effect.

- Do not use or imply `glowing skin`, `dewy skin`, `luminous complexion`, `radiant skin`, `flawless skin`, `glass skin`, `polished skin`, `wet look skin`, or `beauty lighting`.
- Prefer an unretouched backstage casting-test look: diffuse north-window light or broad soft light, low specular reflection, moderate contrast, and natural exposure.
- Require visible microtexture at the facial close-up: pores, tiny vellus hairs, faint dry areas, lip texture, natural under-eye folds, and uneven tonal response.
- State explicitly that the face must remain matte-to-satin and slightly imperfect even under couture lighting.

### Neutral Skin Color and Specular Control

- Keep facial specular reflection very low: no bright white patches on the forehead, nose bridge, cheekbones, or upper lip. Use broad diffuse light and preserve local skin texture instead of adding shine.
- Use neutral daylight white balance on skin. Warm bars, tungsten lamps, wood, and amber interiors may color the environment, but must not turn the face yellow, orange, bronze, or artificially golden.
- Prefer accurate neutral-to-natural Chinese skin tones with subtle local red or olive variation, never a uniform yellow cast or orange color grade on the face.
- Add the prompt constraints: `neutral white balance on skin, accurate skin tone, no yellow cast, no orange cast, no amber skin, no golden skin, no warm color grade on face, no tungsten spill on face, very low facial specular reflection`.

### Neutral Skin Color and Specular Control

- Keep facial specular reflection very low: no bright white patches on the forehead, nose bridge, cheekbones, or upper lip. Use broad diffuse light and preserve local skin texture instead of adding shine.
- Use neutral daylight white balance on skin. Warm bars, tungsten lamps, wood, and amber interiors may color the environment, but must not turn the face yellow, orange, bronze, or artificially golden.
- Prefer accurate neutral-to-natural Chinese skin tones with subtle local red or olive variation, never a uniform yellow cast or orange color grade on the face.
- Add the prompt constraints: `neutral white balance on skin, accurate skin tone, no yellow cast, no orange cast, no amber skin, no golden skin, no warm color grade on face, no tungsten spill on face, very low facial specular reflection`.

### Anti-Gloss Fallback

When fashion, couture, luxury, or advertising direction conflicts with skin realism, skin realism has priority. Treat skin as a factual material, not a beauty effect.

- Do not use or imply `glowing skin`, `dewy skin`, `luminous complexion`, `radiant skin`, `flawless skin`, `glass skin`, `polished skin`, `wet look skin`, or `beauty lighting`.
- Prefer an unretouched backstage casting-test look: diffuse north-window light or broad soft light, low specular reflection, moderate contrast, and natural exposure.
- Require visible microtexture at the facial close-up: pores, tiny vellus hairs, faint dry areas, lip texture, natural under-eye folds, and uneven tonal response.
- State explicitly that the face must remain matte-to-satin and slightly imperfect even under couture lighting.

### v1.1.1 CLEAN CINEMATIC PORTRAIT PATCH

This patch is a hard override for cinematic, advertising, fashion, and head-and-shoulders portrait generation.

#### Total Rule

> 人物可以粗粝，摄影必须干净；环境可以昏暗，脸必须清楚；皮肤可以不完美，但不能显脏；去掉网红感，不等于去掉高级完成度。

The operational meaning is:

- cinematic mood does not mean low exposure;
- environmental color must not contaminate the core skin tone;
- real texture must not become dirt, noise, or muddy detail;
- removing influencer gloss must not remove commercial photography polish.

#### Exposure and Facial Readability

- Keep the eyes, nose, mouth, cheek planes, and jawline clearly readable even in a dark or dramatic environment.
- Use controlled cinematic contrast, not crushed facial shadows, blacked-out eye sockets, or underexposed skin.
- Let the environment fall darker or softer while keeping the face correctly exposed and visually primary.
- Prefer clean key/fill separation, readable catchlights, moderate shadow density, and a deliberate exposure balance.

#### Environmental Color Separation

- Separate environmental color from the core face and neck skin. Colored walls, neon, tungsten, foliage, and practical lights may tint the background and clothing, but must not turn skin yellow, orange, green, blue, bronze, or gray.
- Keep neutral-to-natural skin white balance on the face. Use color contrast in the environment rather than color contamination on the skin.
- Avoid heavy amber, green, cyan, magenta, or mixed-light spill across the forehead, cheeks, nose, lips, and under-eyes.

#### Clean Texture and Commercial Finish

- Preserve subtle pores, fine lines, vellus hairs, under-eye structure, lip texture, and restrained tonal variation.
- Keep the texture clean, legible, and photographic. Do not stack pores, grain, blemishes, grime, harsh sharpening, or muddy noise into a dirty-looking face.
- Remove beauty-filter gloss and influencer styling while retaining controlled makeup, precise grooming, clean lens rendering, coherent wardrobe materials, and high-end advertising finish.
- The face may be lived-in, weathered, asymmetrical, or psychologically tense, but it must remain clean, believable, and professionally photographed.

#### v1.1.1 Prompt Additions

Add these positive constraints to cinematic or advertising portraits:

```text
clean cinematic exposure, face clearly readable, controlled contrast, readable facial planes, neutral skin white balance, environmental color separation, clean real-photography texture, subtle pores, fine detail without dirt, polished commercial photography, refined lens rendering, psychologically specific human presence
```

Add these negative constraints:

```text
no underexposed face, no crushed facial shadows, no blacked-out eye sockets, no muddy contrast, no dirty-looking skin, no grime texture, no excessive skin grain, no harsh sharpening, no green color spill on face, no amber color spill on face, no cyan color spill on face, no magenta color spill on face, no yellow/orange skin contamination, no gray dead skin, no low-detail cinematic darkness, no influencer gloss, no beauty-filter finish, no loss of commercial polish
```

### Character Presence

- Give the character a specific life history through gaze, facial tension, grooming, posture, clothing logic, and restrained imperfections.
- Make the face distinctive through structure and proportion rather than exaggerated beauty.
- Preserve adult, elderly, adolescent, or child proportions appropriate to the requested age.
- For model-oriented characters, emphasize bone structure, silhouette, proportion, styling, and controlled presence.
- For role-oriented characters, emphasize occupation, daily life, social position, and believable wardrobe choices.
- For cinematic characters, allow lived-in texture, fatigue, old injuries, sun exposure, age, or emotional restraint without turning the result into a game character.

### Originality and Identity Safety

Create an original fictional person. References may contribute only broad attributes such as age impression, temperament, styling direction, facial tendency, or social role.

Do not directly reproduce:

- a named celebrity, actor, model, public figure, or influencer
- a recognizable film or television character
- a specific supermodel's face or a single real person's complete feature set
- a copied costume, signature hairstyle, or instantly identifiable character design

Blend multiple broad sources and introduce controlled variation in facial proportions, skin details, asymmetry, styling, and wardrobe. Preserve the intended human quality, not a recognizable likeness.

## Special Subjects

For mythic, literary, historical, traditional-cultural, or lightly fantastical prompts:

1. Establish the subject as a believable real person photographed in a real setting.
2. Express the concept through facial design, wardrobe, grooming, props, posture, and social identity.
3. Keep fantasy or symbolism grounded in materials, construction, and practical styling.
4. Do not use game concept art, magical effects, CG glow, dramatic fantasy backgrounds, or illustration language unless the user explicitly asks for those.

## Visual Direction by Mode

Choose the dominant treatment from the user's brief:

- **Commercial**: clean light, controlled color, clear wardrobe, polished but believable skin.
- **Cinematic**: richer facial texture, lived-in expression, restrained wear, story-bearing wardrobe.
- **Advertising**: precise grooming, complete styling, elegant light, controlled pose, product-ready clarity.
- **Model casting**: strong bone structure, distinct proportions, professional posture, clean presentation.
- **Everyday / role**: natural grooming, socially plausible clothing, relaxed expression, realistic body language.
- **Documentary / realistic**: less beautification, more skin and material truth, observational presence.

When no mode is specified, blend commercial, cinematic, advertising, and high-end casting qualities in that order.

## Prompt Construction

When an image-generation tool is available, construct the final prompt in this order:

1. original fictional character identity
2. explicit user-specified features
3. face structure and distinctive details
4. hair, makeup, body, and pose
5. complete wardrobe and accessories
6. photographic treatment and lighting
7. requested single-image framing, or the explicitly requested multi-view layout
8. identity-consistency requirements
9. source-material synthesis map
10. batch identity diversity matrix when generating a set
11. negative constraints

Use concrete visual nouns and measurable layout language. For ordinary single-image generation, do not add extra views. For explicitly requested multi-view generation, state the same-person constraint explicitly and mention that all requested angles must match the approved character.

Useful negative constraints:

Always include the NO WAX SKIN negatives: `no waxy skin, no oily forehead, no glossy cheeks, no shiny nose bridge, no porcelain skin, no beauty-filter effect, no over-retouching, no mannequin face`.

For fashion or supermodel prompts, also include: `no glowing skin, no dewy skin, no luminous complexion, no radiant skin, no flawless skin, no glass skin, no polished skin, no wet look skin, no beauty lighting, no skin smoothing, no airbrushed face`.

For fashion or supermodel prompts, also include: `no glowing skin, no dewy skin, no luminous complexion, no radiant skin, no flawless skin, no glass skin, no polished skin, no wet look skin, no beauty lighting, no skin smoothing, no airbrushed face`.

`no celebrity likeness, no recognizable existing character, no duplicate person, no plastic skin, no beauty-filter face, no influencer look, no e-commerce cliché, no anime, no game concept art, no illustration, no fantasy VFX, no inconsistent clothing, no mismatched face, no extra limbs, no text labels`

## v1.1 Face Realism Patch

Hard override for real-person face generation, especially Chinese and East Asian characters.

### Reference-to-Original Face Rules

Default reference distance is **Level 2: same type, original character**. Preserve broad temperament, age impression, styling direction, and useful memory cues, but do not preserve the complete face map.

- Replace at least **3 facial feature fields**: face shape/width, eye shape/spacing, eyelid type, brow structure, nose bridge/tip, lip ratio, chin length, cheekbones, or jaw ratio.
- Replace at least **1 identity anchor**: distinctive mark position, eye signature, mouth-corner movement, nose-tip/nostril combination, facial proportion, hair silhouette, parting, or signature accessory.
- Add **2-3 new memorable traits**: a different face proportion, mild asymmetry, new mole/freckle placement, eyebrow growth pattern, eye expression, hair silhouette, or believable lip ratio.
- Preserve the character's temperament through neighboring substitutions. The output should read as the same broad character type at first glance and clearly a different person at second glance.
- Level 1 is only for an explicitly requested same-character variation. Level 3 is for mood-only references.

### Camera Split for Casting Sheets

- Upper front/side/back full-body row: 50-70mm editorial lens feeling, f/4-f/5.6, readable body proportions and wardrobe materials.
- Lower face close-up: 85-105mm portrait lens feeling, f/1.8-f/2.4, precise eye focus, shallow depth of field, strong subject-background separation, soft natural bokeh.
- Defocus the close-up background. Keep only broad color blocks and blurred structure; no sharp shelves, windows, furniture, or room details behind the face.

### Natural Imperfections and Priority

Add only 1-2 restrained human variations per character, distributed across the batch: mild eye asymmetry, different eyelid depth, tiny mole, faint freckles, subtle under-eye texture, small healed mark, slight nose redness, uneven eyebrow density, fine hairline detail, subtly asymmetric chin, or slight tonal variation. Keep them clean, natural, and believable.

Resolve conflicts in this order:

`character temperament > identity memory anchors > realistic human bone structure > reference distance > skin texture > makeup > commercial polish`

### Default Positive Face Block

```text
real human facial anatomy, natural semi-matte skin, subtle pores, fine skin texture, restrained professional retouching, slight tonal variation, believable under-eye texture, natural eyebrow hair, realistic lip texture, subtle facial asymmetry, individual nose geometry, distinctive but believable facial features, clean commercial photography, authentic human presence, neutral white balance on skin, very low facial specular reflection
```

### Default Negative Face Block

```text
avoid waxy skin, avoid plastic skin, avoid oily face, avoid porcelain skin, avoid excessive skin highlights, avoid beauty-filter face, avoid over-retouched skin, avoid generic AI Asian face, avoid identical V-shaped jawlines, avoid oversized artificial eyes, avoid overly tiny nose, avoid glossy lips, avoid mannequin-like facial rendering, avoid excessive facial symmetry, avoid uniform skin tone, avoid influencer makeup, avoid yellow cast, avoid orange cast, avoid amber skin, avoid golden skin, avoid warm color grade on face, avoid tungsten spill on face
```

### v1.1 Quality Gate Additions

Before returning a reference-driven character, confirm 3+ facial fields and 1+ identity anchor were replaced for Level 2, 2-3 new memory points were added, micro-imperfections are restrained, and the batch remains visibly unrelated rather than sister-like or triplet-like. Check the camera split only when multi-view mode was explicitly triggered.

## Quality Gate

Before returning the result, verify:

- the character is original and not a recognizable real-person copy
- the user's explicit constraints are preserved
- at least three source-material categories informed the face, styling, or visual world for production-grade work
- no single source person's face, identity, signature styling, or costume dominates the result
- the character has distinctive source-derived design genes rather than a generic AI face
- characters in a batch are visibly unrelated individuals with different face geometry, hair, age cues, and identifying details
- no two close-ups read as twins, triplets, or the same generated face
- if multi-view mode was explicitly triggered, all requested views depict one identical person
- age, gender presentation, skin tone, body type, face, hair, makeup, clothing, and accessories remain consistent
- if multi-view mode was explicitly triggered, the requested angle views are readable and the facial close-up preserves the approved identity
- the clothing is complete and wearable
- the scene reads as real photography rather than game art or concept art
- skin retains subtle pores, fine texture, natural tonal variation, and a semi-matte real-photography finish
- the face has no waxy, plastic, oily, porcelain, mannequin-like, or beauty-filter appearance
- fashion lighting has not turned the forehead, nose bridge, cheeks, or lips into glossy artificial surfaces
- the face remains neutral in white balance and is not yellow, orange, bronze, or golden from the environment
- the face remains neutral in white balance and is not yellow, orange, bronze, or golden from the environment
- fashion lighting has not turned the forehead, nose bridge, cheeks, or lips into glossy artificial surfaces
- the character has a clear role, mood, and casting value
- no unnecessary text, measurements, labels, or biography panels appear

For the full source specification and extended examples, read [references/original-spec.md](references/original-spec.md) when the request needs finer-grained casting rules.
