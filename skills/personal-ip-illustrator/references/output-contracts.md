# Output Contracts

Use these structures so results are easy to reuse in a repository, article editor, or SaaS prototype.

## Visual Candidate Sheet

If image generation is available, create or request a visual sheet before final IP selection.

```json
{
  "candidate_sheet": {
    "format": "image_grid",
    "count": 8,
    "selection_instruction": "Choose the image closest to the IP you want. You can also say what to keep and what to remove.",
    "candidates": [
      {
        "id": "ip_a",
        "name": "",
        "entity_type": "",
        "one_line_identity": "",
        "why_it_fits": "",
        "image_prompt": ""
      }
    ]
  }
}
```

If image generation is not available, return the same candidate sheet with prompts and ask the user to generate or upload references before final selection.

## Candidate Pack

```markdown
## IP Candidates

### Candidate 1: {name}
- Entity type:
- Core identity:
- Silhouette:
- Personality:
- Signature objects:
- Style direction:
- Why it fits:
- Reference prompt:
```

Use this text pack only as support for the visual candidate sheet. Do not make it the main selection surface.

## User-Facing IP Card

Show this after the user selects a visual direction. Keep it short enough that a non-technical creator can confirm it quickly.

```markdown
## {IP Name}

**一句话人设**：{what this IP represents}

**看图识别点**
- {silhouette or shape}
- {face/front detail}
- {signature object}
- {main color/accent}

**它在内容里的角色**
- {guide/operator/observer/etc.}

**适合出现的场景**
- {scene 1}
- {scene 2}
- {scene 3}

**不要变成**
- {forbidden visual drift 1}
- {forbidden visual drift 2}
```

The IP Card is for user confirmation. The IP Bible is for agent use.

## Article Visual Plan

```json
{
  "article_title": "",
  "recommended_illustration_count": 0,
  "visual_plan": [
    {
      "position": "after_paragraph_3",
      "section_summary": "",
      "reason": "",
      "visual_value_score": 5,
      "illustration_type": "concept_metaphor",
      "ip_role": "guide",
      "scene_brief": "",
      "expected_reader_effect": ""
    }
  ]
}
```

## Illustration Spec

```json
{
  "id": "illus_01",
  "position": "after_paragraph_3",
  "format": "article_insert | cover | social_card | slide | sticker",
  "aspect_ratio": "16:9 | 4:3 | 1:1 | 3:4 | 9:16",
  "editorial_function": "",
  "ip_consistency_block": "",
  "scene_prompt": "",
  "negative_prompt": "",
  "alt_text": ""
}
```

## Annotated Article Preview

Use insertion markers that downstream tools can parse:

```markdown
{paragraph}

<!-- illustration: illus_01 after_paragraph_3 -->
![{alt_text}]({image_or_placeholder})
<!-- /illustration -->

{next paragraph}
```

If no images were generated, use placeholders:

```markdown
![Pending: illus_01](./images/illus_01.png)
```

## Final Response Order

For a full run, return:

1. Short diagnosis of the article's visual needs.
2. Visual candidate sheet or selected reference image summary.
3. User-facing IP card.
4. Internal IP Bible.
5. Article visual plan.
6. Illustration specs or generated images.
7. Annotated article preview.
8. Exported personal skill package, if the IP has been confirmed.
9. Open questions or next iteration choices.

## Confirmed IP Handoff

When the user confirms the IP, add this handoff block before exporting:

```json
{
  "confirmed_ip": true,
  "ip_name": "",
  "export_skill_name": "{ip-name}-illustrations",
  "export_skill_purpose": "Use the confirmed IP Bible to create article illustrations and visual plans.",
  "included_files": [
    "SKILL.md",
    "agents/openai.yaml",
    "references/ip-card.md",
    "references/ip-bible.md",
    "references/article-visual-planning.md",
    "references/output-contracts.md"
  ]
}
```
