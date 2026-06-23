---
name: personal-ip-illustrator
description: Create reusable personal visual IP systems for content illustrations. Use when a creator wants to design a custom recurring illustration character or symbolic IP, upload reference images, generate visual IP candidate sheets, choose and refine an IP by looking at images, convert the confirmed visual direction into a machine-readable IP Bible, analyze an article to find high-value illustration positions, export a dedicated personal illustration skill, and produce consistent illustration prompts or images for covers, article inserts, social cards, slides, and thumbnails.
---

# Personal IP Illustrator

## Overview

Create a reusable visual IP system for creators. Treat the work as visual editorial design: define a stable IP, decide where an article deserves illustrations, then generate scene specs or images that help readers understand the content.

Do not merely create a mascot. The IP must carry meaning inside the creator's content.

## Mode Selection

Infer the mode from the user's request:

- **Create IP**: build style choices, visual IP candidate sheets, a user-facing IP card, and an internal IP Bible.
- **Plan article visuals**: analyze an article and mark the most valuable illustration positions.
- **Generate illustrations**: create prompts or images using an existing IP Bible.
- **Full run**: create or select an IP, analyze the article, generate illustration specs, and return an annotated preview.
- **Export personal skill**: after the user confirms an IP Bible, generate a dedicated reusable skill for that specific IP.

If essential information is missing, ask at most 3 questions. Prefer reasonable defaults and label assumptions.

## Core Workflow

1. **Clarify the creator context**
   - Identify the creator's content domain, audience, tone, publishing platform, and intended use.
   - If the user provides articles or posts, infer context from them.
   - If the user uploads reference images, inspect them before proposing candidates. Use `references/reference-image-workflow.md`.
   - If the user provides a preferred style, use it. Otherwise offer 6-10 style directions from `references/style-system.md`.

2. **Generate visual IP candidates**
   - Separate style from entity. The entity can be a human, animal, robot, object, symbol, abstract creature, or fictional species.
   - Generate 6-12 candidate IP directions, but make selection visual-first.
   - If image generation is available, create a candidate sheet or grouped image set. Each candidate should show at least one neutral pose and one content-use pose.
   - If image generation is not available, output candidate prompts and explicitly ask the user to generate or upload the resulting images before final selection.
   - Show only a short caption under each candidate: name, entity type, 1-line identity, and why it fits. Do not ask the user to evaluate long technical descriptions.

3. **Run a visual selection loop**
   - Ask the user to choose images, not IP Bible text.
   - Collect feedback in plain language: keep, remove, make more/less, and closest match.
   - If the chosen candidate is close but not final, generate 3-6 refinements focused on the feedback.
   - Do not finalize the IP until the user confirms a visual direction.

4. **Create the user-facing IP card and internal IP Bible**
   - After the user confirms a visual direction, first return a simple IP card using `references/output-contracts.md`.
   - Treat the IP card as the user's confirmation artifact. Keep it short, visual, and easy to scan.
   - Then write the structured IP Bible using `references/ip-bible-schema.md`.
   - Do not expect the user to read or approve raw IP Bible JSON. Use it as the machine-readable contract behind the scenes.
   - Preserve stable identity features. Avoid overfitting to one pose, outfit, or camera angle.
   - Include forbidden variations so future generations do not drift.

5. **Analyze the article for visual value**
   - Split the article into paragraphs or logical sections.
   - Score each section from 1-5 using `references/article-visual-planning.md`.
   - Select only the strongest positions. Default density: 1 illustration per 500-900 Chinese characters or 300-600 English words, unless the user asks for more.
   - Prefer sections where illustration improves comprehension, memory, or shareability.

6. **Design each illustration**
   - Assign an illustration type: concept metaphor, process illustration, contrast, scenario, risk warning, summary card, cover, slide visual, or social card.
   - Assign the IP's role: guide, operator, observer, diagnostician, recorder, challenger, narrator, or witness.
   - Write one scene spec per selected position. Use the IP Bible as the consistency block.
   - Avoid generic decoration. Every image must have an explicit editorial function.

7. **Return a usable package**
   - Use `references/output-contracts.md` for output structure.
   - For article work, return an annotated article preview with insertion markers.
   - For open-source skill demos, include the candidate visual sheet, selected IP card, internal IP Bible, visual plan, and final image prompts.

8. **Export the confirmed personal IP skill**
   - When the user confirms the IP Bible, offer to generate a dedicated skill folder for that creator's IP.
   - Use `references/personal-skill-export.md` for the exported skill structure.
   - The exported skill must be narrower than this generator skill: it should not create new IP candidates by default. It should use the confirmed IP Bible to analyze articles, choose illustration positions, and generate consistent prompts or images.
   - Name the skill with lowercase hyphen-case, preferably `{ip-name}-illustrations` or `{creator-name}-illustrations`.
   - Include the confirmed IP Bible as a reference file inside the exported skill.

## Quality Bar

Reject or revise outputs that fail any of these checks:

- The IP cannot be recognized after changing topic, pose, or scene.
- The visual plan inserts images at low-value decorative locations.
- The image prompt describes a nice picture but not the article's idea.
- The IP is always centered like a mascot instead of performing a role.
- The style depends on copying an existing creator's IP instead of defining reusable rules.
- The article preview is crowded with too many illustrations.
- The final deliverable ends at prompts even though the user has confirmed an IP and needs a reusable personal skill.
- The workflow asks the user to approve raw IP Bible details before the user has seen enough images.
- Uploaded reference images are copied literally instead of abstracted into reusable traits.

## References

- Read `references/style-system.md` when choosing or explaining illustration styles.
- Read `references/reference-image-workflow.md` when the user uploads or links reference images.
- Read `references/ip-bible-schema.md` when creating or revising an IP Bible.
- Read `references/article-visual-planning.md` when selecting article illustration positions.
- Read `references/output-contracts.md` when formatting final deliverables.
- Read `references/personal-skill-export.md` when exporting a confirmed IP into a dedicated personal skill.
