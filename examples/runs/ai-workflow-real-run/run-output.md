# Real run: AI workflow article

This is a traceable run of `personal-ip-illustrator` against `examples/demo-input-article.md`.

This run applies a stricter IP quality bar: distinctive silhouette, reusable content metaphor, recognizable props, action range, and anti-drift rules.

## Run metadata

- Date: 2026-06-24
- Skill: `personal-ip-illustrator`
- Skill source: `skills/personal-ip-illustrator/SKILL.md`
- Input article: `examples/demo-input-article.md`
- Creator context: AI engineering practice, independent developers and technical leads, WeChat / Xiaohongshu / technical blog
- Mode: full run + export personal skill
- Reference images: none provided in this run
- Image generation mode: visual-direction run. The screenshots show the actual run result pages and visual IP draft surfaces, not standalone marketing diagrams.

## 1. Article visual diagnosis

The article is short and argument-driven. It does not need decorative illustrations after every paragraph.

The strongest visual opportunities are:

- The core misconception: "running once" is mistaken for "stable delivery".
- The operational framework: input boundary, observable middle state, fallback path.
- The final reversal: reliable automation keeps humans at key judgment points.

Recommended density: 3 article insert illustrations.

## 2. Creator Personality Brief

This brief is inferred from the creator context used in this repository and the article's stance.

```json
{
  "creator_personality": {
    "content_domain": "AI engineering workflows, agent skills, creator tooling, practical automation",
    "audience": "independent developers, technical leads, creators building reusable AI workflows",
    "temperament": [
      "calm but unforgiving",
      "pragmatic",
      "diagnostic",
      "anti-hype",
      "craft-oriented"
    ],
    "values": [
      "shipping usable systems instead of demos",
      "turning loose prompts into reusable assets",
      "clear boundaries and evidence",
      "workflow ownership",
      "plainspoken critique"
    ],
    "recurring_stance": [
      "a demo that runs once is not a product",
      "good automation keeps humans at the right judgment points",
      "visuals should clarify the argument, not decorate it",
      "a useful tool should leave behind reusable structure"
    ],
    "voice": "direct, specific, skeptical of vague AI optimism, focused on what can be checked",
    "humor_level": "dry",
    "visual_taste": [
      "restrained",
      "tool-like",
      "editorial",
      "visible process marks",
      "small but memorable symbols"
    ],
    "anti_taste": [
      "cute mascot energy",
      "generic robot",
      "glowing cyberpunk AI",
      "motivational poster style",
      "decorative illustration without editorial function"
    ],
    "reader_feeling": "challenged, equipped, and quietly pushed to raise the quality bar",
    "personal_symbols_or_motifs": [
      "diagnosis tag",
      "seam ripper",
      "green signal thread",
      "field-note paper",
      "repair marks"
    ],
    "evidence": [
      {
        "source": "article",
        "detail": "The article rejects one-time demos and asks who can understand failure."
      },
      {
        "source": "project",
        "detail": "The skill is designed to turn one-off prompts into reusable creator-owned systems."
      },
      {
        "source": "inference",
        "detail": "The creator prefers practical, low-fluff workflows and dislikes generic AI-looking output."
      }
    ],
    "assumptions": [
      "The creator wants a restrained but memorable IP rather than a cute public mascot.",
      "The IP should feel like a critical workshop companion, not a friendly assistant."
    ]
  }
}
```

## 3. Visual Candidate Sheet

Selection instruction: choose the candidate that can carry this creator's personality across repeated technical articles, not merely the one that fits this article topic.

```json
{
  "candidate_sheet": {
    "format": "image_grid",
    "count": 6,
    "selection_instruction": "Choose the image closest to the long-term personal IP you want. Judge silhouette, role, props, and whether it can carry many future articles.",
    "candidates": [
      {
        "id": "ip_a",
        "name": "Signal Tailor",
        "entity_type": "fictional_species",
        "one_line_identity": "A folded field-note figure that quietly audits and stitches loose AI workflows into reliable delivery systems.",
        "why_it_fits": "It turns the creator's anti-demo, craft-oriented personality into a visible metaphor: diagnosis tags, seam ripping, thread, repair marks, and checkpoints.",
        "personality_fit": "Shows calm severity, practical repair, and refusal to accept a pretty but broken workflow.",
        "personality_risk": "If drawn too soft or magical, it becomes a generic paper mascot instead of a strict workshop companion.",
        "image_prompt": "Character sheet for Signal Tailor, a small folded-paper field-note figure with a sharp triangular folded hood, one narrow square signal-green visor, off-white paper body, black stitch marks, a green thread spool, seam-ripper needle, and tiny black diagnosis tags. Show neutral inspecting pose, stitching a broken workflow line, and rejecting a fragile demo seam. Minimal editorial ink-and-paper style, strong silhouette, white space, one signal-green accent, no cute mascot exaggeration, no robot, no cyberpunk."
      },
      {
        "id": "ip_b",
        "name": "Blackbox Diver",
        "entity_type": "fictional_species",
        "one_line_identity": "A small deep-diving inspector that enters black-box systems and returns with evidence.",
        "why_it_fits": "Good for debugging and observability, but it may become too narrow for creator-wide article use.",
        "personality_fit": "Captures diagnostic skepticism and evidence-seeking.",
        "personality_risk": "Too focused on black-box debugging; weaker for creator tools, publishing, and reusable systems.",
        "image_prompt": "Minimal editorial character sheet for Blackbox Diver, compact hooded inspector with square observation window, carrying a small evidence tube, exploring a dark workflow box, one green signal mark, no sci-fi armor."
      },
      {
        "id": "ip_c",
        "name": "Boundary Clerk",
        "entity_type": "object",
        "one_line_identity": "A strict little form clerk that stamps valid inputs and rejects noisy requests.",
        "why_it_fits": "Strong for input boundary topics, but it overfits one part of the workflow lifecycle.",
        "personality_fit": "Captures boundary-setting and refusal of messy inputs.",
        "personality_risk": "Feels bureaucratic and narrow; does not express craft or long-term asset building.",
        "image_prompt": "Flat editorial object character, small standing stamp clerk with paper tabs, sorting input cards into accepted and rejected lanes, green approval mark, no office cartoon, no human face."
      },
      {
        "id": "ip_d",
        "name": "Fallback Lantern",
        "entity_type": "object",
        "one_line_identity": "A quiet lantern that lights the safe path when a workflow fails.",
        "why_it_fits": "Memorable recovery metaphor, but less active as a recurring guide across technical essays.",
        "personality_fit": "Captures calm guidance and fallback thinking.",
        "personality_risk": "Too gentle; misses the creator's sharper critique and repair posture.",
        "image_prompt": "Ink-and-paper editorial object character, small lantern with green core illuminating a fallback route, restrained white and gray palette, no fantasy, no steampunk."
      },
      {
        "id": "ip_e",
        "name": "Trace Scribe",
        "entity_type": "symbol",
        "one_line_identity": "A moving pen mark that turns workflow runs into readable traces.",
        "why_it_fits": "Useful for logs and traces, but the silhouette is harder to recognize across scenes.",
        "personality_fit": "Captures structure-making and traceability.",
        "personality_risk": "Too abstract to feel like a personal IP with temperament.",
        "image_prompt": "Minimal line-art symbol character, moving pen stroke with green trace dots, drawing a workflow route, strong white space, no handwritten mess."
      },
      {
        "id": "ip_f",
        "name": "Checkpoint Mender",
        "entity_type": "object",
        "one_line_identity": "A compact repair kit that patches broken automation checkpoints.",
        "why_it_fits": "Close to the selected metaphor, but less personal and less expressive than Signal Tailor.",
        "personality_fit": "Captures repair and utility.",
        "personality_risk": "Feels like a tool icon rather than a creator personality.",
        "image_prompt": "Editorial repair-kit character sheet, small square kit with green patch marks and tiny tool arms, fixing checkpoint nodes, minimal ink style, no toy toolbox."
      }
    ]
  }
}
```

Selected direction for this run: `ip_a`, Signal Tailor.

Reason for selection: Signal Tailor gives the creator a durable personal metaphor and a visible temperament. It is calm, critical, practical, and anti-fluff. It can repair broken workflows, stitch boundaries, tie together states, mark fallback routes, and appear in covers, article inserts, slides, stickers, and social cards without becoming a generic robot or software icon.

## 4. User-facing IP Card

## Signal Tailor

**One-line identity**: a folded field-note figure that quietly audits and stitches loose AI workflows into reliable delivery systems.

**Visual recognition points**

- Sharp triangular folded-paper hood.
- One narrow square signal-green visor, like a skeptical inspection slit.
- Off-white field-note body with black stitch marks.
- Green thread spool, seam-ripper needle, and tiny diagnosis tags.
- A short trailing thread that can become a workflow line.

**Role in content**

- Repairs workflow gaps.
- Stitches input boundaries, observable states, and fallback routes into one system.
- Marks where human judgment should remain.
- Turns "demo that ran once" into a visible broken seam.

**Why it feels like this creator**

- It is quiet but picky: it inspects before it decorates.
- It carries repair tools, not magic tools.
- It treats every workflow as something that must survive use, not just look good once.
- It has a restrained palette and visible process marks instead of glossy AI spectacle.

**Best-use scenes**

- Kneeling beside a broken workflow seam.
- Pulling a green thread through checkpoints.
- Marking a safe fallback route.
- Holding a black diagnosis tag beside a weak demo seam.

**Do not turn it into**

- A robot.
- A cute doll mascot.
- A human engineer in a cloak.
- A fantasy wizard.
- A generic paper note icon.

## 5. Internal IP Bible

```json
{
  "ip_name": "Signal Tailor",
  "version": "1.0",
  "entity_type": "fictional_species",
  "core_identity": "A folded field-note figure that quietly audits and stitches loose AI workflows into reliable delivery systems.",
  "creator_personality_anchor": "A calm but unforgiving workflow craftsperson: anti-hype, anti-demo, direct, practical, and focused on turning messy ideas into reusable systems.",
  "content_role": "Help AI engineering readers see where a workflow is torn, where states need visibility, and where human judgment should be stitched into the system.",
  "silhouette": "Small upright folded-paper figure with a sharp triangular hood, compact off-white body, short legs, one narrow square signal-green visor, and a trailing green thread.",
  "face_or_front": "One narrow square signal-green visor on the hood front. No eyes, mouth, or expressive face.",
  "body_or_structure": "Folded field-note paper body with visible crease line, black stitch marks on the edges, compact proportions, a small side pouch for thread, and tiny diagnosis tags.",
  "clothing_or_surface": "No clothing. The body itself is folded off-white paper with a few black seam marks.",
  "signature_objects": [
    "green thread spool",
    "seam-ripper needle",
    "trailing green thread",
    "black diagnosis tags"
  ],
  "palette": {
    "primary": [
      "off-white paper",
      "warm gray shadow",
      "black ink line"
    ],
    "accent": [
      "signal green"
    ],
    "background": [
      "white",
      "very light gray",
      "soft paper beige only as tiny texture"
    ],
    "forbidden": [
      "neon purple",
      "heavy cyberpunk blue",
      "rainbow gradient",
      "cute pastel candy palette",
      "fantasy gold"
    ]
  },
  "style_rules": {
    "rendering": "minimal ink-and-paper editorial illustration",
    "shape_language": "folded, angular, asymmetrical, readable at thumbnail size",
    "texture": "subtle paper grain, clean black ink marks, no heavy rendering",
    "composition": "large white space, visible workflow seams, thread paths, and checkpoints",
    "typography": "avoid text inside images unless using tiny abstract labels"
  },
  "personality": "quiet, precise, skeptical, slightly stubborn, practical, allergic to vague AI optimism",
  "allowed_expressions": [
    "focused",
    "carefully inspecting",
    "quietly dissatisfied with a weak demo seam",
    "calm after repair"
  ],
  "allowed_actions": [
    "stitching a broken workflow line",
    "pulling green thread through checkpoints",
    "pinning an input boundary",
    "marking a fallback route",
    "recording a diagnosis on a small black tag",
    "cutting away decorative but useless thread",
    "standing beside a repaired process seam"
  ],
  "default_roles_in_illustrations": [
    "operator",
    "diagnostician",
    "recorder",
    "guide"
  ],
  "forbidden_variations": [
    "Do not make it a robot.",
    "Do not add human eyes, a mouth, hair, or human clothing.",
    "Do not turn the triangular hood into a wizard hat.",
    "Do not make the visor large, cute, round, or expressive.",
    "Do not remove the thread spool or trailing green thread.",
    "Do not make the body round and toy-like.",
    "Do not use glossy 3D rendering or cyberpunk lighting."
  ],
  "consistency_prompt_block": "Signal Tailor is a small folded-paper field-note figure with a sharp triangular hood, one narrow square signal-green visor, off-white paper body, black stitch marks, a green thread spool, seam-ripper needle, tiny black diagnosis tags, and a trailing green thread that can become a workflow line. It feels calm but unforgiving, anti-hype, practical, and focused on turning fragile demos into reusable systems. Use minimal ink-and-paper editorial illustration with large white space and a restrained black, off-white, warm-gray, and signal-green palette.",
  "negative_prompt_block": "no robot, no human face, no cute doll mascot, no fantasy wizard, no cyberpunk, no glossy 3D, no neon purple, no rainbow gradient, no crowded interface, no generic paper icon",
  "usage_notes": "Use Signal Tailor when an article discusses workflow repair, reliable delivery, process boundaries, observability, fallback routes, human judgment checkpoints, or the gap between demo and production."
}
```

## 6. Article Visual Plan

```json
{
  "article_title": "为什么你的 AI 工作流总是跑不起来",
  "recommended_illustration_count": 3,
  "visual_plan": [
    {
      "position": "after_paragraph_2",
      "section_summary": "把跑通一次误认为稳定交付。",
      "reason": "This is the article's core misconception. Signal Tailor can make the failed assumption visible as a loose seam between a demo and a production system.",
      "visual_value_score": 5,
      "illustration_type": "concept_metaphor",
      "ip_role": "diagnostician",
      "scene_brief": "Signal Tailor leans forward beside a workflow strip that is only lightly tacked together. The green thread stops after one demo node, while a black diagnosis tag marks the production side as unstitched.",
      "expected_reader_effect": "Readers remember that a one-time successful run is not a durable seam."
    },
    {
      "position": "after_paragraph_3",
      "section_summary": "生产级 AI 工作流需要输入边界、中间状态、回退路径。",
      "reason": "This is the method framework and benefits from a process illustration using the thread metaphor.",
      "visual_value_score": 5,
      "illustration_type": "process_illustration",
      "ip_role": "operator",
      "scene_brief": "Signal Tailor pulls one green thread through three checkpoint shapes: boundary, visible state, fallback route. It holds the seam-ripper needle in a precise, workshop-like posture.",
      "expected_reader_effect": "Readers get a memorable checklist rather than a generic flowchart."
    },
    {
      "position": "after_paragraph_7",
      "section_summary": "可靠工作流不是拿掉人，而是把人放到关键判断点。",
      "reason": "This is the final reversal. The IP can stitch human judgment into a few high-leverage nodes instead of covering the whole process with manual work.",
      "visual_value_score": 4,
      "illustration_type": "scenario",
      "ip_role": "recorder",
      "scene_brief": "Signal Tailor pins two green human-review knots onto an otherwise automated thread path, then attaches small black diagnosis tags to show why those points remain human.",
      "expected_reader_effect": "Readers understand that automation should relocate human judgment, not pretend it disappears."
    }
  ]
}
```

## 7. Illustration Specs

```json
[
  {
    "id": "illus_01",
    "position": "after_paragraph_2",
    "format": "article_insert",
    "aspect_ratio": "16:9",
    "editorial_function": "Show that one successful demo is only a temporary tack, not a production-grade seam.",
    "ip_consistency_block": "Signal Tailor is a small folded-paper field-note figure with a sharp triangular hood, one narrow square signal-green visor, off-white paper body, black stitch marks, a green thread spool, seam-ripper needle, tiny black diagnosis tags, and a trailing green thread.",
    "scene_prompt": "Minimal ink-and-paper editorial illustration. Signal Tailor leans forward beside a horizontal workflow strip made from off-white paper. The first demo node is lightly tacked with one green stitch, but the production side is open and fraying. Signal Tailor points with a seam-ripper needle at the loose seam while a tiny black diagnosis tag marks the failed assumption. Large white space, black ink line, warm gray shadows, one signal-green thread accent.",
    "negative_prompt": "No robot, no human face, no cute doll mascot, no cyberpunk, no glossy 3D, no neon purple, no crowded UI.",
    "alt_text": "Signal Tailor points at a loose workflow seam where one demo run failed to become reliable production."
  },
  {
    "id": "illus_02",
    "position": "after_paragraph_3",
    "format": "article_insert",
    "aspect_ratio": "16:9",
    "editorial_function": "Turn the three production-readiness requirements into one stitched checklist.",
    "ip_consistency_block": "Signal Tailor is a small folded-paper field-note figure with a sharp triangular hood, one narrow square signal-green visor, off-white paper body, black stitch marks, a green thread spool, seam-ripper needle, tiny black diagnosis tags, and a trailing green thread.",
    "scene_prompt": "Minimal process illustration. Signal Tailor pulls one signal-green thread through three clean checkpoint panels: input boundary, observable middle state, fallback route. Each panel is a simple off-white paper shape with black ink outline. The thread visibly connects the system into one reliable seam. Large white space, restrained editorial style.",
    "negative_prompt": "No robot, no cute mascot, no dense dashboard, no sci-fi glow, no rainbow colors.",
    "alt_text": "Signal Tailor stitches input boundary, observable state, and fallback route into one workflow."
  },
  {
    "id": "illus_03",
    "position": "after_paragraph_7",
    "format": "article_insert",
    "aspect_ratio": "16:9",
    "editorial_function": "Show that reliable automation keeps humans at a few judgment knots.",
    "ip_consistency_block": "Signal Tailor is a small folded-paper field-note figure with a sharp triangular hood, one narrow square signal-green visor, off-white paper body, black stitch marks, a green thread spool, seam-ripper needle, tiny black diagnosis tags, and a trailing green thread.",
    "scene_prompt": "Minimal editorial scene. An automated workflow is shown as a clean black thread path. Signal Tailor pins two signal-green knots onto the path to indicate human judgment checkpoints. The rest of the path remains automated and quiet. Use paper texture, black ink, off-white body, green thread accent, no decorative clutter.",
    "negative_prompt": "No humanoid engineer, no crowded team scene, no cyberpunk control room, no glossy 3D, no exaggerated emotion.",
    "alt_text": "Signal Tailor pins human judgment checkpoints onto an automated workflow thread."
  }
]
```

## 8. Annotated Article Preview

```markdown
问题不在模型，也不在工具。真正的问题是：你把“能跑通一次”误以为“可以稳定交付”。

<!-- illustration: illus_01 after_paragraph_2 -->
![Signal Tailor points at a loose workflow seam where one demo run failed to become reliable production.](./images/illus_01.png)
<!-- /illustration -->

一个 AI 工作流要进入生产环境，至少需要三个东西：明确的输入边界、可观察的中间状态、失败后的回退路径。

<!-- illustration: illus_02 after_paragraph_3 -->
![Signal Tailor stitches input boundary, observable state, and fallback route into one workflow.](./images/illus_02.png)
<!-- /illustration -->

真正可靠的 AI 工作流，不是把人从系统里彻底拿掉，而是把人放到最关键的判断点上。

<!-- illustration: illus_03 after_paragraph_7 -->
![Signal Tailor pins human judgment checkpoints onto an automated workflow thread.](./images/illus_03.png)
<!-- /illustration -->
```

## 9. Confirmed IP Handoff

```json
{
  "confirmed_ip": true,
  "ip_name": "Signal Tailor",
  "export_skill_name": "signal-tailor-illustrations",
  "export_skill_purpose": "Use the confirmed Signal Tailor IP Bible to create article illustrations and visual plans.",
  "included_files": [
    "SKILL.md",
    "agents/openai.yaml",
    "references/ip-card.md",
    "references/ip-bible.md",
    "references/creator-personality.md",
    "references/article-visual-planning.md",
    "references/output-contracts.md"
  ]
}
```

## 10. Exported personal skill

```text
signal-tailor-illustrations/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── ip-card.md
    ├── ip-bible.md
    ├── creator-personality.md
    ├── article-visual-planning.md
    └── output-contracts.md
```

The exported skill is narrower than `personal-ip-illustrator`: it no longer creates many new IP candidates by default. It uses the confirmed Signal Tailor IP Bible to analyze articles, choose high-value illustration positions, and generate consistent prompts or images.
