# 示例输出

下面是一次完整运行的缩略示例。真实运行截图见：

- [runs/ai-workflow-real-run/run-output.md](./runs/ai-workflow-real-run/run-output.md)
- [ai-workflow-case-study.md](./ai-workflow-case-study.md)

## 1. Visual Candidate Sheet

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
        "one_line_identity": "一个折页形态的信号裁缝，把松散 AI 工作流缝成可交付系统。",
        "why_it_fits": "绿色线束、缝线、断口和线结能长期承载 AI 工作流、可靠性、回退路径和人类判断点这些内容。",
        "image_prompt": "Character sheet for Signal Tailor, a small folded-paper field-note figure with a triangular folded hood, one square signal-green visor, off-white paper body, black stitch marks, a green thread spool, and a needle-like probe..."
      }
    ]
  }
}
```

## 2. User-Facing IP Card

## Signal Tailor

**一句话人设**：一个折页形态的信号裁缝，把松散 AI 工作流缝成可交付系统。

**看图识别点**

- 三角折页兜帽。
- 单个绿色方形目镜。
- 米白纸质身体和黑色缝线。
- 绿色线轴、针形探针、拖尾线束。

**它在内容里的角色**

- 修补工作流断点。
- 把输入边界、中间状态、回退路径缝起来。
- 标记人类判断应该停留的位置。

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
  "core_identity": "A folded field-note figure that stitches loose AI workflows into reliable delivery systems.",
  "silhouette": "Small upright folded-paper figure with a triangular hood, compact off-white body, one square signal-green visor, and a trailing green thread.",
  "palette": {
    "primary": ["off-white paper", "warm gray shadow", "black ink line"],
    "accent": ["signal green"],
    "forbidden": ["neon purple", "cyberpunk blue", "rainbow gradient"]
  },
  "signature_objects": [
    "green thread spool",
    "needle-like probe",
    "trailing green thread"
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
      "scene_brief": "Signal Tailor 跪在只缝了一针的 demo 节点旁，指出生产侧仍然开裂。"
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
  "ip_consistency_block": "Signal Tailor is a small folded-paper field-note figure with a triangular hood, one square signal-green visor, off-white paper body, black stitch marks, a green thread spool, needle-like probe, and a trailing green thread.",
  "scene_prompt": "Minimal ink-and-paper editorial illustration. Signal Tailor kneels beside a horizontal workflow strip made from off-white paper. The first demo node is lightly tacked with one green stitch, but the production side is open and fraying...",
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
    ├── article-visual-planning.md
    └── output-contracts.md
```
