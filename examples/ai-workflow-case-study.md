# Case study: 给一篇 AI 工作流文章做个人 IP 配图

这是一个真实跑法示例。输入是一篇短文：《为什么你的 AI 工作流总是跑不起来》。目标不是给文章随便插几张图，而是先建立一个可以复用的视觉 IP，再判断文章里哪些位置真的值得配图。

这版案例重点修正了第一版的问题：不能只是生成一个“技术感角色”。个人长期 IP 必须有强识别轮廓、稳定道具、可复用内容隐喻、动作范围和明确的防漂移规则。

## 输入

创作者上下文：

- 内容方向：AI 工程实践
- 读者：独立开发者、技术负责人、正在把 AI 工作流接进业务的人
- 平台：公众号、小红书、技术博客
- 语气：克制、具体、偏工程判断
- 风格偏好：极简线稿，少量信号色，不要赛博朋克，不要可爱吉祥物

文章：[demo-input-article.md](./demo-input-article.md)

完整输出记录：[runs/ai-workflow-real-run/run-output.md](./runs/ai-workflow-real-run/run-output.md)

下面的图片是从这次运行的结果页截出来的，不是另外生成的流程示意图。

## 第一步：生成候选 IP

先提取创作者人格，而不是直接从文章题材生成角色。

这次人格简报的核心判断：

- 冷静但挑剔，不吃“漂亮 demo”这一套。
- 重视可交付系统、可检查边界和长期复用资产。
- 表达方式直接、具体、反感空泛 AI 乐观主义。
- 视觉上偏好克制、工具感、过程痕迹，不要赛博朋克和可爱吉祥物。

这次选择了一个非人类角色：`Signal Tailor`。

它不是“AI 工程师”形象，也不是通用机器人。它是一个带诊断气质的折页信号裁缝：用绿色线束把松散的 AI 工作流缝成可以交付的系统。

这个方向比普通技术角色更适合作为长期 IP，因为它有自己的稳定隐喻：

- 线束：代表流程连接。
- 缝线：代表系统可靠性。
- 断口：代表 demo 和生产之间的缺口。
- 线结：代表人类判断点。

候选 IP 选择界面截图：

![Real run candidate sheet](../docs/assets/real-run-01-candidate-sheet.png)

## 第二步：用户可读的 IP Card

## Signal Tailor

一句话人设：一个折页形态的信号裁缝，把松散 AI 工作流缝成可交付系统。

看图识别点：

- 三角折页兜帽。
- 窄绿色方形目镜，像在审查问题。
- 米白纸质身体和黑色缝线。
- 绿色线轴、拆线针、拖尾线束。
- 黑色诊断标签。

它在内容里的角色：

- 修补工作流断点。
- 把输入边界、中间状态、回退路径缝起来。
- 标记人类判断应该停留的位置。

为什么像这个创作者：

- 它不是鼓掌型助手，而是会先检查哪里没缝牢。
- 它拿的是修补工具，不是魔法工具。
- 它的绿色线束代表把松散 prompt 和流程缝成可复用系统。
- 它的克制配色和诊断标签，比发光 AI 角色更接近这个项目的气质。

不要变成：

- 机器人
- 真人工程师
- 可爱玩偶吉祥物
- 幻想法师
- 普通纸片图标

IP Card 截图：

![Real run IP card](../docs/assets/real-run-02-ip-card.png)

## 第三步：内部 IP Bible 摘要

用户不用读完整 IP Bible，但 Agent 需要它来保证后续一致。

```json
{
  "ip_name": "Signal Tailor",
  "entity_type": "fictional_species",
  "core_identity": "A folded field-note figure that quietly audits and stitches loose AI workflows into reliable delivery systems.",
  "creator_personality_anchor": "A calm but unforgiving workflow craftsperson: anti-hype, anti-demo, direct, practical, and focused on turning messy ideas into reusable systems.",
  "content_role": "Help AI engineering readers see where a workflow is torn, where states need visibility, and where human judgment should be stitched into the system.",
  "silhouette": "Small upright folded-paper figure with a sharp triangular hood, compact off-white body, short legs, one narrow square signal-green visor, and a trailing green thread.",
  "signature_objects": [
    "green thread spool",
    "seam-ripper needle",
    "trailing green thread",
    "black diagnosis tags"
  ],
  "palette": {
    "primary": ["off-white paper", "warm gray shadow", "black ink line"],
    "accent": ["signal green"],
    "forbidden": ["neon purple", "cyberpunk blue", "rainbow gradient", "cute pastel palette"]
  },
  "forbidden_variations": [
    "Do not make it a robot.",
    "Do not add human eyes, a mouth, hair, or human clothing.",
    "Do not turn the triangular hood into a wizard hat.",
    "Do not remove the square green visor.",
    "Do not remove the thread spool or trailing green thread."
  ]
}
```

## 第四步：文章配图位置判断

文章一共有 8 个短段落。Skill 没有每段都配图，只选了 3 个位置。

配图位置分析截图：

![Real run article visual plan](../docs/assets/real-run-03-visual-plan.png)

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
      "section_summary": "生产级 AI 工作流需要输入边界、中间状态、回退路径。",
      "visual_value_score": 5,
      "illustration_type": "process_illustration",
      "ip_role": "operator",
      "scene_brief": "Signal Tailor 用同一根绿色线穿过输入边界、可观察状态和回退路径，动作像在工作台上做精细修补。"
    },
    {
      "position": "after_paragraph_7",
      "section_summary": "可靠工作流不是拿掉人，而是把人放到关键判断点。",
      "visual_value_score": 4,
      "illustration_type": "scenario",
      "ip_role": "recorder",
      "scene_brief": "Signal Tailor 在自动化路径上打出两个绿色判断结，并贴上小型诊断标签说明为什么这里需要人。"
    }
  ]
}
```

## 第五步：正文配图 prompt

### illus_01

放置位置：第 2 段后  
作用：解释“跑通一次”和“稳定交付”的差别

```text
Minimal ink-and-paper editorial illustration. Signal Tailor leans forward beside a horizontal workflow strip made from off-white paper. The first demo node is lightly tacked with one green stitch, but the production side is open and fraying. Signal Tailor points with a seam-ripper needle at the loose seam while a tiny black diagnosis tag marks the failed assumption. Large white space, black ink line, warm gray shadows, one signal-green thread accent.
```

### illus_02

放置位置：第 3 段后  
作用：把生产级 AI 工作流的三个要素可视化

```text
Minimal process illustration. Signal Tailor pulls one signal-green thread through three clean checkpoint panels: input boundary, observable middle state, fallback route. Each panel is a simple off-white paper shape with black ink outline. The thread visibly connects the system into one reliable seam. Large white space, restrained editorial style.
```

### illus_03

放置位置：第 7 段后  
作用：解释“人不应该被拿掉，而应该放在关键判断点”

```text
Minimal editorial scene. An automated workflow is shown as a clean black thread path. Signal Tailor pins two signal-green knots onto the path to indicate human judgment checkpoints. The rest of the path remains automated and quiet. Use paper texture, black ink, off-white body, green thread accent, no decorative clutter.
```

## 第六步：文章预览

```markdown
问题不在模型，也不在工具。真正的问题是：你把“能跑通一次”误以为“可以稳定交付”。

<!-- illustration: illus_01 after_paragraph_2 -->
![Signal Tailor points at a loose workflow seam where one demo run failed to become reliable production.](./images/illus_01.png)
<!-- /illustration -->

一个 AI 工作流要进入生产环境，至少需要三个东西：明确的输入边界、可观察的中间状态、失败后的回退路径。

<!-- illustration: illus_02 after_paragraph_3 -->
![Signal Tailor stitches input boundary, observable state, and fallback route into one workflow.](./images/illus_02.png)
<!-- /illustration -->
```

## 第七步：导出的个人 Skill

这轮确认后，会导出一个更窄的个人 Skill：

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

后续使用方式：

```text
Use $signal-tailor-illustrations.

帮我分析这篇 AI 工程文章最值得配图的位置，并生成 3 张正文配图 prompt。
```

导出结果截图：

![Real run exported personal skill](../docs/assets/real-run-04-exported-skill.png)

这个案例验证的是完整链路：先把 IP 稳定下来，再让它服务文章表达。不是先有图，再反过来解释图为什么存在。
