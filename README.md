# Character Casting Studio Skill

Material-reference-driven character generation for original, photorealistic human characters.

## Default Workflow

The default function generates the person first. It focuses on face, temperament, makeup, hair, clothing, age, identity, and photographic quality. A single character image is the default output.

Multi-view assets are opt-in. Use the multi-view workflow only when the user explicitly requests a three-view image, white-background character image, character breakdown, or character turnaround. In that mode, use the already approved character as the source of truth and change only the requested viewing angle.

## Core Rules

- Original fictional identity, never a copied real person or celebrity likeness.
- Source-material synthesis for distinctive, production-grade faces.
- Clear identity separation across batches; avoid sibling, twin, or triplet faces.
- Natural semi-matte skin with subtle pores and restrained highlights.
- No waxy skin, plastic skin, oily face, beauty-filter finish, yellow/orange cast, or mannequin-like rendering.
- Clean cinematic exposure: the face remains readable, environmental color stays separate from core skin tone, and texture never becomes dirty or muddy.
- Real commercial makeup instead of airbrushed beauty-filter makeup.

## Repository Layout

- `SKILL.md`: complete execution rules
- `agents/openai.yaml`: Codex invocation metadata
- `references/`: extended casting rules, material index, and face-realism patch
- `assets/reference-library/`: bundled broad visual source materials

## Use

Install or copy this directory into the Codex skills directory, then invoke it with `$character-casting-studio`.
