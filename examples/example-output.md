# 示例输出

下面是一次完整运行的缩略示例。真实运行时可以生成图片；这里用 prompt 和占位符展示结构。

## 1. Visual Candidate Sheet

```json
{
  "candidate_sheet": {
    "format": "image_grid",
    "count": 4,
    "selection_instruction": "请选择最接近你想要的 IP，也可以说要保留或删除什么。",
    "candidates": [
      {
        "id": "ip_a",
        "name": "Circuit Guide",
        "entity_type": "symbolic robot",
        "one_line_identity": "一个在复杂系统里帮读者找到信号路径的电路向导。",
        "why_it_fits": "适合 AI 工程文章，能自然承担引导、诊断和流程解释角色。",
        "image_prompt": "A minimal editorial character sheet of Circuit Guide, a small symbolic robot made of clean circuit lines, one neutral pose and one pose pointing at a workflow board..."
      },
      {
        "id": "ip_b",
        "name": "Console Lamp",
        "entity_type": "object mascot",
        "one_line_identity": "一盏照亮系统黑箱的控制台小灯。",
        "why_it_fits": "适合讲调试、可观察性、工程判断。",
        "image_prompt": "A restrained flat illustration candidate sheet of Console Lamp, a small desk-lamp-like object with console UI details..."
      }
    ]
  }
}
```

## 2. User-Facing IP Card

## Circuit Guide

**一句话人设**：在复杂 AI 工作流里帮读者找到信号路径的电路向导。

**看图识别点**

- 小型机器人轮廓，头部像简化电路节点。
- 主色为冷灰和白，只有一处绿色信号灯作为强调。
- 经常拿着小型探针或站在流程板旁边。
- 表情克制，不夸张卖萌。

**它在内容里的角色**

- 引导读者穿过复杂系统。
- 指出失败点。
- 把抽象流程整理成可观察结构。

**适合出现的场景**

- 工作流地图前
- 调试面板旁
- 输入边界和失败回退路径之间

**不要变成**

- 赛博朋克机器人
- 过度可爱的玩具角色
- 全身发光的科幻角色

## 3. Internal IP Bible

实际输出会包含完整 `ip-bible.md`。用户通常不需要阅读它，它主要给 Agent 保持角色一致性。

```json
{
  "ip_name": "Circuit Guide",
  "entity_type": "robot",
  "core_identity": "A calm guide for navigating AI engineering workflows.",
  "silhouette": "Small compact robot, circuit-node head, simple body, probe accessory.",
  "palette": {
    "primary": ["cool gray", "white"],
    "accent": ["signal green"],
    "forbidden": ["neon purple", "heavy cyberpunk blue"]
  },
  "forbidden_variations": [
    "Do not make it a humanoid engineer.",
    "Do not turn it into a cute toy robot.",
    "Do not use crowded sci-fi backgrounds."
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
      "reason": "这是文章核心反常识判断，适合做概念隐喻图。",
      "visual_value_score": 5,
      "illustration_type": "concept_metaphor",
      "ip_role": "diagnostician",
      "scene_brief": "Circuit Guide 站在一条只跑通一次的临时轨道旁，指出轨道后面没有支撑结构。",
      "expected_reader_effect": "让读者记住演示和生产系统的差异。"
    },
    {
      "position": "after_paragraph_3",
      "section_summary": "生产级工作流需要输入边界、中间状态、回退路径。",
      "reason": "三要素适合流程图式插画。",
      "visual_value_score": 5,
      "illustration_type": "process_illustration",
      "ip_role": "guide",
      "scene_brief": "Circuit Guide 站在三段式工作流地图前，依次标出输入边界、可观察状态、回退路径。",
      "expected_reader_effect": "帮助读者形成可复用框架。"
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
  "editorial_function": "Show the difference between a demo that works once and a workflow that can reliably deliver.",
  "ip_consistency_block": "Circuit Guide is a small calm robot with a circuit-node head, cool gray and white body, one signal-green accent light, and a small probe accessory.",
  "scene_prompt": "Minimal editorial illustration. Circuit Guide stands beside a fragile temporary track labeled 'one successful demo', pointing to missing support beams underneath. In the background, a stable production pipeline is shown as a clean structured path with checkpoints. Large white space, restrained line work, one signal-green accent.",
  "negative_prompt": "No cyberpunk, no cute toy robot, no crowded interface, no neon purple, no generic humanoid engineer.",
  "alt_text": "Circuit Guide points out the missing support structure behind a one-time AI workflow demo."
}
```

## 6. Annotated Article Preview

```markdown
问题不在模型，也不在工具。真正的问题是：你把“能跑通一次”误以为“可以稳定交付”。

<!-- illustration: illus_01 after_paragraph_2 -->
![Circuit Guide points out the missing support structure behind a one-time AI workflow demo.](./images/illus_01.png)
<!-- /illustration -->
```

## 7. Exported Personal Skill

```text
circuit-guide-illustrations/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── ip-card.md
    ├── ip-bible.md
    ├── article-visual-planning.md
    └── output-contracts.md
```
