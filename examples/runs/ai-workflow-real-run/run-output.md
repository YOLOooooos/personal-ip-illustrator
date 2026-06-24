# Real run: AI workflow article

This is a traceable run of `personal-ip-illustrator` against `examples/demo-input-article.md`.

## Run metadata

- Date: 2026-06-24
- Skill: `personal-ip-illustrator`
- Skill source: `skills/personal-ip-illustrator/SKILL.md`
- Base commit before this run was recorded: `c658ce8`
- Input article: `examples/demo-input-article.md`
- Creator context: AI engineering practice, independent developers and technical leads, WeChat / Xiaohongshu / technical blog
- Mode: full run + export personal skill
- Reference images: none provided in this run
- Image generation mode: prompt-first. This run records the candidate selection surface and final prompts, without pretending that final model-rendered artwork exists.

## 1. Article visual diagnosis

The article is short and argument-driven. It does not need decorative illustrations after every paragraph.

The strongest visual opportunities are:

- The core misconception: "running once" is mistaken for "stable delivery".
- The operational framework: input boundary, observable middle state, fallback path.
- The final reversal: reliable automation keeps humans at key judgment points.

Recommended density: 3 article insert illustrations.

## 2. Visual Candidate Sheet

Selection instruction: choose the candidate that feels closest to the creator's long-term visual IP. Feedback should be visual and simple: keep, remove, make more/less, or combine.

```json
{
  "candidate_sheet": {
    "format": "image_grid",
    "count": 6,
    "selection_instruction": "Choose the image closest to the IP you want. You can also say what to keep and what to remove.",
    "candidates": [
      {
        "id": "ip_a",
        "name": "Circuit Guide",
        "entity_type": "robot",
        "one_line_identity": "A calm circuit guide that helps readers find the signal path inside messy AI workflows.",
        "why_it_fits": "It naturally explains systems, failure points, observability, and workflow structure without becoming a generic human lecturer.",
        "image_prompt": "Minimal editorial character sheet for Circuit Guide, a small calm robot made from clean circuit-line shapes, compact silhouette, circuit-node head, cool-gray and white body, one signal-green accent light, small probe accessory, one neutral pose and one pose pointing at a workflow board, large white space, thin black lines, no cyberpunk, no cute toy style."
      },
      {
        "id": "ip_b",
        "name": "Log Lens",
        "entity_type": "object",
        "one_line_identity": "A quiet inspection lens that makes hidden workflow states visible.",
        "why_it_fits": "Good for observability and debugging posts, but weaker when the article needs an active guide.",
        "image_prompt": "Minimal line editorial character sheet for Log Lens, a compact magnifying lens with a small status light and clean handle, one neutral pose and one pose hovering above a workflow trace, cool gray, white, one signal-green accent, no detective costume, no busy dashboard."
      },
      {
        "id": "ip_c",
        "name": "Input Gate",
        "entity_type": "symbol",
        "one_line_identity": "A small gatekeeper symbol that separates valid inputs from unstable noise.",
        "why_it_fits": "Strong for boundary-setting content, but too narrow for articles about end-to-end workflows.",
        "image_prompt": "Minimal geometric symbol mascot, small input gate with two clean panels and signal-green validation dot, one neutral front pose and one pose sorting cards into accepted and rejected lanes, restrained technical editorial style, no fantasy castle, no shield logo."
      },
      {
        "id": "ip_d",
        "name": "State Lantern",
        "entity_type": "object",
        "one_line_identity": "A small lantern that illuminates the middle state of a process.",
        "why_it_fits": "Memorable for visibility and diagnosis, but may feel too poetic for engineering operations.",
        "image_prompt": "Minimal editorial object character sheet, compact lantern with simple wireframe handle and one signal-green core, shown standing quietly and illuminating a hidden middle stage in a workflow map, thin black line work, cool-gray shadows, no warm fantasy lighting, no steampunk."
      },
      {
        "id": "ip_e",
        "name": "Rollback Shuttle",
        "entity_type": "object",
        "one_line_identity": "A small shuttle that can return a failed workflow to a safe point.",
        "why_it_fits": "Useful for failure recovery topics, but it over-indexes on fallback paths.",
        "image_prompt": "Minimal technical editorial character sheet, tiny rollback shuttle with loop-arrow detail, cool gray body, one signal-green checkpoint light, neutral pose and pose returning to a previous workflow node, no sci-fi spaceship, no neon, no dramatic speed lines."
      },
      {
        "id": "ip_f",
        "name": "Trace Cartographer",
        "entity_type": "abstract_creature",
        "one_line_identity": "A map-making trace node that turns a workflow run into a readable route.",
        "why_it_fits": "Strong metaphor for tracing, but less instantly recognizable at small social-card sizes.",
        "image_prompt": "Minimal abstract character sheet, small map-like trace node with folded path silhouette, one tiny pointer arm, cool-gray and white palette, signal-green route highlight, neutral pose and pose drawing a workflow map, no fantasy creature features, no excessive detail."
      }
    ]
  }
}
```

Selected direction for this run: `ip_a`, Circuit Guide.

Reason for selection: it is the broadest fit for AI engineering articles. It can guide, diagnose, record, and point at system structure without becoming a generic person or a one-topic object.

## 3. User-facing IP Card

## Circuit Guide

**One-line identity**: a calm circuit guide that helps readers find the signal path inside messy AI workflows.

**Visual recognition points**

- Small compact robot silhouette.
- Head shaped like a simplified circuit node.
- Cool gray and white body with thin black line work.
- One signal-green accent light.
- Small probe accessory or workflow board nearby.

**Role in content**

- Guide readers through AI workflow structure.
- Diagnose missing boundaries, hidden states, and weak fallback paths.
- Turn abstract reliability problems into visible system checkpoints.

**Best-use scenes**

- In front of a workflow map.
- Beside a debugging panel.
- Between an input boundary and a fallback route.
- Pointing to a missing support structure in a demo pipeline.

**Do not turn it into**

- A cyberpunk robot.
- A cute toy mascot.
- A human engineer.
- A glowing sci-fi character with crowded backgrounds.

## 4. Internal IP Bible

```json
{
  "ip_name": "Circuit Guide",
  "version": "1.0",
  "entity_type": "robot",
  "core_identity": "A calm circuit guide that helps readers find the signal path inside messy AI workflows.",
  "content_role": "Guide AI engineering readers through workflow structure, failure points, observability, and recovery paths.",
  "silhouette": "Small compact robot with a rounded-square circuit-node head, simple short body, and a small probe accessory.",
  "face_or_front": "Minimal face/front with two tiny node marks or a single calm status line, never expressive cartoon eyes.",
  "body_or_structure": "Clean white and cool-gray body panels, thin black circuit-line details, simple arms suitable for pointing at maps or panels.",
  "clothing_or_surface": "No clothing. Smooth technical surface with restrained circuit traces.",
  "signature_objects": [
    "small probe accessory",
    "workflow board",
    "signal-green status dot"
  ],
  "palette": {
    "primary": [
      "white",
      "cool gray",
      "thin black line"
    ],
    "accent": [
      "signal green"
    ],
    "background": [
      "white",
      "very light gray"
    ],
    "forbidden": [
      "neon purple",
      "heavy cyberpunk blue",
      "rainbow gradients",
      "warm fantasy gold"
    ]
  },
  "style_rules": {
    "rendering": "minimal line editorial illustration",
    "shape_language": "compact, geometric, readable at thumbnail size",
    "texture": "clean flat fills with no heavy texture",
    "composition": "large white space, diagrammatic scenes, clear article function",
    "typography": "avoid text in generated images unless a tiny label is essential"
  },
  "personality": "calm, precise, observant, practical, never theatrical",
  "allowed_expressions": [
    "neutral",
    "focused",
    "quietly concerned",
    "satisfied after locating a problem"
  ],
  "allowed_actions": [
    "pointing with probe",
    "standing beside workflow map",
    "marking checkpoints",
    "recording a diagnosis",
    "highlighting a fallback route"
  ],
  "default_roles_in_illustrations": [
    "guide",
    "diagnostician",
    "recorder",
    "observer"
  ],
  "forbidden_variations": [
    "Do not make it a humanoid engineer.",
    "Do not turn it into a cute toy robot.",
    "Do not add expressive cartoon eyes.",
    "Do not use crowded sci-fi backgrounds.",
    "Do not change the accent color away from signal green.",
    "Do not remove the compact circuit-node head."
  ],
  "consistency_prompt_block": "Circuit Guide is a small calm robot with a compact circuit-node head, cool gray and white body, thin black line work, one signal-green accent light, and a small probe accessory. It appears in restrained minimal editorial illustrations with large white space and clear workflow diagrams.",
  "negative_prompt_block": "no cyberpunk, no cute toy mascot, no humanoid engineer, no expressive cartoon eyes, no neon purple, no crowded sci-fi UI, no rainbow gradients, no dramatic action pose",
  "usage_notes": "Use Circuit Guide when the article explains AI workflow structure, reliability, observability, failure recovery, or system diagnosis. The IP should clarify the argument, not decorate the page."
}
```

## 5. Article Visual Plan

```json
{
  "article_title": "为什么你的 AI 工作流总是跑不起来",
  "recommended_illustration_count": 3,
  "visual_plan": [
    {
      "position": "after_paragraph_2",
      "section_summary": "把跑通一次误认为稳定交付。",
      "reason": "This is the core misconception of the article and needs a visual anchor that separates a one-time demo from a production system.",
      "visual_value_score": 5,
      "illustration_type": "concept_metaphor",
      "ip_role": "diagnostician",
      "scene_brief": "Circuit Guide stands beside a fragile one-time track and points at the missing support structure beneath it.",
      "expected_reader_effect": "Readers remember that a successful demo is not the same thing as reliable delivery."
    },
    {
      "position": "after_paragraph_3",
      "section_summary": "生产级 AI 工作流需要输入边界、中间状态、回退路径。",
      "reason": "This is the method framework and benefits from a clear process illustration.",
      "visual_value_score": 5,
      "illustration_type": "process_illustration",
      "ip_role": "guide",
      "scene_brief": "Circuit Guide stands in front of a three-part workflow map: input boundary, observable middle state, fallback path.",
      "expected_reader_effect": "Readers get a reusable checklist for evaluating workflow readiness."
    },
    {
      "position": "after_paragraph_7",
      "section_summary": "可靠工作流不是拿掉人，而是把人放到关键判断点。",
      "reason": "This is the article's final reversal and prevents a common misunderstanding about automation.",
      "visual_value_score": 4,
      "illustration_type": "scenario",
      "ip_role": "recorder",
      "scene_brief": "Circuit Guide marks two human review checkpoints in an otherwise automated workflow path.",
      "expected_reader_effect": "Readers understand that human judgment should move to the highest-leverage points."
    }
  ]
}
```

## 6. Illustration Specs

```json
[
  {
    "id": "illus_01",
    "position": "after_paragraph_2",
    "format": "article_insert",
    "aspect_ratio": "16:9",
    "editorial_function": "Show the difference between a demo that works once and a workflow that can reliably deliver.",
    "ip_consistency_block": "Circuit Guide is a small calm robot with a compact circuit-node head, cool gray and white body, thin black line work, one signal-green accent light, and a small probe accessory.",
    "scene_prompt": "Minimal editorial illustration for an AI engineering article. Circuit Guide stands beside a fragile temporary track labeled one successful demo, pointing to missing support beams underneath. In the background, a stable production pipeline appears as a clean structured path with checkpoints. Large white space, restrained thin line work, one signal-green accent.",
    "negative_prompt": "No cyberpunk, no cute toy robot, no crowded interface, no neon purple, no generic humanoid engineer.",
    "alt_text": "Circuit Guide points at missing support beams under a one-time AI workflow demo."
  },
  {
    "id": "illus_02",
    "position": "after_paragraph_3",
    "format": "article_insert",
    "aspect_ratio": "16:9",
    "editorial_function": "Turn the three production-readiness requirements into a readable workflow map.",
    "ip_consistency_block": "Circuit Guide is a small calm robot with a compact circuit-node head, cool gray and white body, thin black line work, one signal-green accent light, and a small probe accessory.",
    "scene_prompt": "Minimal process illustration. Circuit Guide stands in front of a clean three-part workflow map. The three sections are input boundary, observable middle state, and fallback path. Use simple boxes, arrows, and checkpoint dots. Circuit Guide points at the middle section with a small probe.",
    "negative_prompt": "No sci-fi glow, no decorative clutter, no neon purple, no expressive cartoon face.",
    "alt_text": "Circuit Guide explains input boundary, observable middle state, and fallback path."
  },
  {
    "id": "illus_03",
    "position": "after_paragraph_7",
    "format": "article_insert",
    "aspect_ratio": "16:9",
    "editorial_function": "Show that reliable automation keeps humans at key judgment points.",
    "ip_consistency_block": "Circuit Guide is a small calm robot with a compact circuit-node head, cool gray and white body, thin black line work, one signal-green accent light, and a small probe accessory.",
    "scene_prompt": "Minimal editorial scene. Circuit Guide sits beside a quiet control console, marking two small human review checkpoints in an otherwise automated AI workflow. The workflow is a clean horizontal path; most steps are automated, but two decision nodes are highlighted in signal green.",
    "negative_prompt": "No futuristic crowd, no cute mascot expression, no cyberpunk room, no dramatic lighting.",
    "alt_text": "Circuit Guide marks human review checkpoints inside an automated AI workflow."
  }
]
```

## 7. Annotated Article Preview

```markdown
问题不在模型，也不在工具。真正的问题是：你把“能跑通一次”误以为“可以稳定交付”。

<!-- illustration: illus_01 after_paragraph_2 -->
![Circuit Guide points at missing support beams under a one-time AI workflow demo.](./images/illus_01.png)
<!-- /illustration -->

一个 AI 工作流要进入生产环境，至少需要三个东西：明确的输入边界、可观察的中间状态、失败后的回退路径。

<!-- illustration: illus_02 after_paragraph_3 -->
![Circuit Guide explains input boundary, observable middle state, and fallback path.](./images/illus_02.png)
<!-- /illustration -->

真正可靠的 AI 工作流，不是把人从系统里彻底拿掉，而是把人放到最关键的判断点上。

<!-- illustration: illus_03 after_paragraph_7 -->
![Circuit Guide marks human review checkpoints inside an automated AI workflow.](./images/illus_03.png)
<!-- /illustration -->
```

## 8. Confirmed IP Handoff

```json
{
  "confirmed_ip": true,
  "ip_name": "Circuit Guide",
  "export_skill_name": "circuit-guide-illustrations",
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

## 9. Exported personal skill

```text
circuit-guide-illustrations/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── ip-card.md
    ├── ip-bible.md
    ├── article-visual-planning.md
    └── output-contracts.md
```

The exported skill is narrower than `personal-ip-illustrator`: it no longer creates many new IP candidates by default. It uses the confirmed Circuit Guide IP Bible to analyze articles, choose high-value illustration positions, and generate consistent prompts or images.
