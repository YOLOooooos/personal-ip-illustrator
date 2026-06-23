# Personal Skill Export

Use this reference after the user confirms an IP Bible. The output should be a dedicated personal skill that the creator can keep using without rerunning the IP discovery process.

## Exported Skill Purpose

The generator skill creates and calibrates an IP. The exported personal skill uses one confirmed IP.

The exported skill should:

- Analyze articles and select high-value illustration positions.
- Use the confirmed IP Bible as a consistency contract.
- Generate cover, article insert, social card, slide, and sticker prompts or images.
- Return annotated article previews with insertion markers.
- Refuse or revise outputs that drift away from the IP Bible.

The exported skill should not:

- Generate many new IP candidates by default.
- Change the IP's species, silhouette, palette, or core identity unless the user explicitly asks for a version update.
- Treat the IP as a decorative mascot detached from the article's argument.

## Folder Structure

```text
{skill-name}/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── ip-card.md
    ├── ip-bible.md
    ├── article-visual-planning.md
    └── output-contracts.md
```

## Skill Name

Use lowercase letters, digits, and hyphens only.

Good names:

- `lucas-illustrations`
- `orange-line-illustrations`
- `founder-fox-illustrations`
- `notebook-robot-illustrations`

Avoid:

- generic names like `ai-illustrator`
- names longer than 63 characters
- names that copy another creator's IP

## Exported SKILL.md Template

```markdown
---
name: {skill-name}
description: Create consistent illustrations using the confirmed {ip-name} visual IP. Use when the creator wants to analyze an article, choose the most valuable illustration positions, and generate cover, article insert, social card, slide, or sticker prompts/images in the established {ip-name} style.
---

# {IP Name} Illustrations

## Overview

Use the confirmed {ip-name} IP Bible to create consistent, editorially useful illustrations for the creator's content.

Do not redesign the IP unless the user explicitly asks for an IP Bible update.

## Workflow

1. Read `references/ip-bible.md`.
2. If the user wants a quick reminder of the IP, summarize `references/ip-card.md` instead of exposing the full Bible.
3. If the user provides an article, analyze it with `references/article-visual-planning.md`.
4. Select only high-value illustration positions.
5. For each selected position, define the image's editorial function, illustration type, IP role, aspect ratio, prompt, negative prompt, and alt text.
6. If image generation is available and requested, generate images. Otherwise return prompts.
7. Return an annotated article preview using `references/output-contracts.md`.

## Consistency Rules

- Preserve the IP's species, silhouette, palette, signature objects, and personality.
- Let pose, expression, camera angle, props, and scene change only within the IP Bible.
- Make the IP perform a useful editorial role: guide, operator, observer, diagnostician, recorder, challenger, narrator, or witness.
- Reject generic mascot poses that do not clarify the article.

## References

- Read `references/ip-bible.md` before generating any illustration.
- Read `references/article-visual-planning.md` when selecting article illustration positions.
- Read `references/output-contracts.md` when formatting deliverables.
```

## Exported ip-bible.md

Convert the confirmed IP Bible into Markdown. Include:

- IP name
- Core identity
- Entity type
- Content role
- Silhouette
- Face or front
- Body or structure
- Clothing or surface
- Signature objects
- Palette
- Style rules
- Personality
- Allowed expressions
- Allowed actions
- Default illustration roles
- Forbidden variations
- Consistency prompt block
- Negative prompt block
- Usage notes

## Exported ip-card.md

Create a short, creator-facing Markdown card. This is the file users can read and share.

Include:

- One-line identity
- Visual recognition points
- Content role
- Best-use scenes
- Forbidden drift
- Example thumbnail or candidate image path if available

## Exported openai.yaml

```yaml
interface:
  display_name: "{IP Name} Illustrations"
  short_description: "Create consistent {IP Name} content illustrations"
  default_prompt: "Use ${skill-name} to illustrate this article with my confirmed {IP Name} visual IP."
```

## Export Checklist

Before handing off the exported skill, verify:

- `SKILL.md` frontmatter has only `name` and `description`.
- The skill name matches the folder name.
- `references/ip-bible.md` contains the confirmed IP Bible, not a candidate draft.
- `references/ip-card.md` lets a non-technical user understand what was confirmed without reading the Bible.
- The personal skill can be used without loading the original generator skill.
- The user receives the folder path and, if useful, a zip file.
