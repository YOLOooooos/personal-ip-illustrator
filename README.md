# Personal IP Illustrator

把创作者的视觉 IP，变成一个可以长期复用的配图 Skill。

这不是一个“帮你生成头像”的 prompt 仓库。它做的是一套完整工作流：

**参考图 / 风格选择 -> 可视化候选 IP -> 用户看图确认 -> IP Card -> 内部 IP Bible -> 文章配图位置判断 -> 个人专属配图 Skill**

## 解决什么问题

很多创作者已经会用 AI 生图，但仍然卡在三个地方：

- 每次生成的角色都不稳定，今天像 A，明天像 B。
- 不知道文章哪里该配图，只能凭感觉插几张好看的图。
- 最后只有一堆 prompt，没有沉淀成可复用的个人视觉系统。

`personal-ip-illustrator` 把这个过程抽象成一个开源 Skill。它先帮用户建立自己的视觉 IP，再把这个 IP 导出成一个专属 Skill，后续直接用自己的 IP 给文章、封面、社交卡片、PPT 配图。

## 它和普通配图 Skill 的区别

普通配图 Skill 通常是固定某个作者的角色和画风。

这个 Skill 是一个 **个人 IP 生成器**：

- 用户可以上传参考图。
- 用户可以选择不同风格。
- 用户看候选图选择，而不是读一堆设定。
- IP Bible 退到幕后，用户只看简单的 IP Card。
- 最终导出一个属于用户自己的 `{ip-name}-illustrations` Skill。

## 工作流

1. **输入创作者上下文**
   - 内容领域
   - 受众
   - 平台
   - 语气
   - 参考图，可选
   - 偏好的视觉风格，可选

2. **生成 Visual Candidate Sheet**
   - 生成 6-12 个可视化 IP 候选。
   - 每个候选只给短说明。
   - 用户通过看图选择，而不是阅读复杂设定。

3. **视觉选择与微调**
   - 用户选择一个候选。
   - 可以反馈：保留什么、删掉什么、更专业/更可爱/更克制/更锋利。
   - Skill 生成 3-6 个细化版本。

4. **确认 IP**
   - 输出用户可读的 IP Card。
   - 同时生成内部使用的 IP Bible。

5. **分析文章配图位置**
   - 拆分文章段落。
   - 给每段打 `visual_value_score`。
   - 只选择最值得视觉化的位置。

6. **生成配图规格**
   - 每张图包含位置、画幅、编辑功能、IP 角色、场景 prompt、negative prompt、alt text。

7. **导出个人专属 Skill**
   - 生成类似 `notebook-robot-illustrations` 的独立 Skill。
   - 后续用户直接用自己的 Skill 给文章配图。

## 安装

把 Skill 目录复制到 Codex skills 目录：

```bash
cp -R skills/personal-ip-illustrator ~/.codex/skills/
```

然后在 Codex 中使用：

```text
Use $personal-ip-illustrator to create a reusable visual IP for my AI engineering articles.
```

如果你的环境没有图像生成工具，它会先输出候选图 prompt 和配图 prompt。  
如果你的环境有图像生成工具，它可以进一步生成候选图和最终配图。

## 一个真实案例

我用一篇短文《为什么你的 AI 工作流总是跑不起来》跑了一轮。

这轮没有只输出“几张好看的图”，而是产出了一套可以继续复用的配图系统：

- 视觉 IP：`Circuit Guide`，一个小型电路向导。
- 用户确认物：一张短的 IP Card，而不是一堆角色设定。
- 内部契约：一份 IP Bible，用来限制角色漂移。
- 配图位置：从 8 个段落里选出 3 个真正值得配图的位置。
- 配图 prompt：每张图都说明放在哪里、解决什么理解问题。
- 导出结果：`circuit-guide-illustrations` 个人 Skill。

完整案例在这里：[examples/ai-workflow-case-study.md](./examples/ai-workflow-case-study.md)。

## 示例 Prompt

```text
Use $personal-ip-illustrator.

我写 AI 工程实践文章，读者是独立开发者和技术负责人。
我希望有一个不是人类的视觉 IP，风格克制、工程感、适合公众号和小红书。
先帮我生成 8 个候选 IP 图方向。
```

```text
Use $personal-ip-illustrator.

我上传了 3 张参考图。第一张是风格参考，第二张是颜色参考，第三张是角色气质参考。
请基于这些参考图生成一组原创 IP 候选，不要直接复制。
```

```text
Use $personal-ip-illustrator.

我已经选定第 3 个候选。请把它沉淀成 IP Card 和内部 IP Bible，
然后用这篇文章判断哪里最值得配图，最后导出我的个人专属 Skill。
```

## 输出内容

完整跑完一轮后，会得到：

- Visual Candidate Sheet
- 用户可读的 IP Card
- Agent 使用的 IP Bible
- Article Visual Plan
- Illustration Specs
- Annotated Article Preview
- 一个可独立安装的个人配图 Skill

## 仓库结构

```text
.
├── README.md
├── LICENSE
├── skills/
│   └── personal-ip-illustrator/
│       ├── SKILL.md
│       ├── agents/openai.yaml
│       └── references/
└── examples/
    ├── ai-workflow-case-study.md
    ├── demo-input-article.md
    ├── example-output.md
    └── exported-personal-skill-example.md
```

## 适合谁

- 写长文的创作者
- 做知识付费或咨询的个人品牌
- 想让公众号、小红书、PPT 配图长期统一的人
- 想把自己的 AI 配图流程沉淀成 Skill 的人

## 不适合谁

- 只想一次性生成头像的人
- 想完全复制别人 IP 的人
- 不在意内容表达，只想要“好看的图”的人

## 路线图

- [x] 补充第一个真实案例
- [ ] 增加候选图板模板
- [ ] 增加个人 Skill 自动导出脚本
- [ ] 增加网页预览 demo
- [ ] 增加小红书 / 公众号排版导出

## License

MIT
