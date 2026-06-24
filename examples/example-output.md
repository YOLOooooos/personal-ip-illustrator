# 示例输出

下面是一次完整运行的缩略示例。真实运行截图见：

- [runs/ai-workflow-real-run/run-output.md](./runs/ai-workflow-real-run/run-output.md)
- [ai-workflow-case-study.md](./ai-workflow-case-study.md)

## 1. Visual Candidate Sheet

先生成 Creator Personality Brief：

```json
{
  "temperament": ["calm but unforgiving", "pragmatic", "diagnostic", "anti-hype"],
  "values": ["shipping usable systems instead of demos", "turning loose prompts into reusable assets"],
  "anti_taste": ["cute mascot energy", "generic robot", "glowing cyberpunk AI", "decorative illustration without editorial function"]
}
```

```json
{
  "candidate_sheet": {
    "format": "image_grid",
    "count": 6,
    "selection_instruction": "请选择最接近长期个人 IP 的方向，重点看轮廓、道具、动作范围和内容隐喻。",
    "candidates": [
      {
        "id": "ip_a",
        "name": "Signal Tailor",
        "entity_type": "fictional_species",
        "one_line_identity": "一个带诊断气质的折页信号裁缝，把松散 AI 工作流缝成可交付系统。",
        "why_it_fits": "绿色线束、缝线、断口和线结能长期承载 AI 工作流、可靠性、回退路径和人类判断点这些内容。",
        "personality_fit": "表现创作者冷静但挑剔、反 demo、重交付的气质。",
        "personality_risk": "如果画得太软或太可爱，会变成普通纸片吉祥物。",
        "image_prompt": "Character sheet for Signal Tailor, a small folded-paper field-note figure with a sharp triangular folded hood, one narrow square signal-green visor, off-white paper body, black stitch marks, a green thread spool, seam-ripper needle, and tiny black diagnosis tags..."
      }
    ]
  }
}
```

## 2. User-Facing IP Card

## Signal Tailor

**一句话人设**：一个带诊断气质的折页信号裁缝，把松散 AI 工作流缝成可交付系统。

**看图识别点**

- 三角折页兜帽。
- 窄绿色方形目镜，像在审查问题。
- 米白纸质身体和黑色缝线。
- 绿色线轴、拆线针、拖尾线束。
- 黑色诊断标签。

**它在内容里的角色**

- 修补工作流断点。
- 把输入边界、中间状态、回退路径缝起来。
- 标记人类判断应该停留的位置。

**为什么像这个创作者**

- 它安静但挑剔，先检查哪里没缝牢。
- 它拿的是修补工具，不是魔法工具。
- 它反感漂亮但脆弱的 demo。

**不要变成**

- 机器人
- 真人工程师
- 可爱玩偶吉祥物
- 幻想法师
- 普通纸片图标

## 3. Internal IP Bible

实际输出会包含完整 `ip-bible.md`。用户通常不需要阅读它，它主要给 Agent 保持角色一致性。

```json
{
  "ip_name": "Signal Tailor",
  "entity_type": "fictional_species",
  "core_identity": "A folded field-note figure that quietly audits and stitches loose AI workflows into reliable delivery systems.",
  "creator_personality_anchor": "A calm but unforgiving workflow craftsperson: anti-hype, anti-demo, direct, practical, and focused on turning messy ideas into reusable systems.",
  "silhouette": "Small upright folded-paper figure with a sharp triangular hood, compact off-white body, one narrow square signal-green visor, and a trailing green thread.",
  "palette": {
    "primary": ["off-white paper", "warm gray shadow", "black ink line"],
    "accent": ["signal green"],
    "forbidden": ["neon purple", "cyberpunk blue", "rainbow gradient"]
  },
  "signature_objects": [
    "green thread spool",
    "seam-ripper needle",
    "trailing green thread",
    "black diagnosis tags"
  ]
}
```

## 4. Article Visual Plan

```json
{
  "article_title": "为什么你的 AI 工作流总是跑不起来",
  "recommended_illustration_count": 3,
  "visual_plan": [
    {
      "position": "after_paragraph_2",
      "section_summary": "把跑通一次误认为稳定交付。",
      "visual_value_score": 5,
      "illustration_type": "concept_metaphor",
      "ip_role": "diagnostician",
      "scene_brief": "Signal Tailor 前倾检查只缝了一针的 demo 节点，用黑色诊断标签标出生产侧仍然开裂。"
    },
    {
      "position": "after_paragraph_3",
      "section_summary": "生产级工作流需要输入边界、中间状态、回退路径。",
      "visual_value_score": 5,
      "illustration_type": "process_illustration",
      "ip_role": "operator",
      "scene_brief": "Signal Tailor 用同一根绿色线穿过输入边界、可观察状态、回退路径。"
    }
  ]
}
```

## 5. Illustration Spec

```json
{
  "id": "illus_01",
  "position": "after_paragraph_2",
  "format": "article_insert",
  "aspect_ratio": "16:9",
  "editorial_function": "Show that one successful demo is only a temporary tack, not a production-grade seam.",
  "ip_consistency_block": "Signal Tailor is a small folded-paper field-note figure with a sharp triangular hood, one narrow square signal-green visor, off-white paper body, black stitch marks, a green thread spool, seam-ripper needle, tiny black diagnosis tags, and a trailing green thread.",
  "scene_prompt": "Minimal ink-and-paper editorial illustration. Signal Tailor leans forward beside a horizontal workflow strip made from off-white paper. The first demo node is lightly tacked with one green stitch, but the production side is open and fraying...",
  "negative_prompt": "No robot, no human face, no cute doll mascot, no fantasy wizard, no cyberpunk, no glossy 3D.",
  "alt_text": "Signal Tailor points at a loose workflow seam where one demo run failed to become reliable production."
}
```

## 6. Annotated Article Preview

```markdown
问题不在模型，也不在工具。真正的问题是：你把“能跑通一次”误以为“可以稳定交付”。

<!-- illustration: illus_01 after_paragraph_2 -->
![Signal Tailor points at a loose workflow seam where one demo run failed to become reliable production.](./images/illus_01.png)
<!-- /illustration -->
```

## 7. Exported Personal Skill

```text
signal-tailor-illustrations/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── ip-card.md
    ├── ip-bible.md
    ├── creator-personality.md
    ├── article-visual-planning.md
    └── output-contracts.md
```
