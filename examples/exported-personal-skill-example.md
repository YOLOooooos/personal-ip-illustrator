# 导出的个人 Skill 示例

当用户确认 `Circuit Guide` 这个 IP 后，生成器会导出一个更窄的个人 Skill。

这个个人 Skill 不再负责生成新 IP，而是只做一件事：

**用确认过的 Circuit Guide 给文章做配图规划和配图生成。**

## 目录

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

## 用户怎么用

```text
Use $circuit-guide-illustrations.

帮我分析这篇文章最值得配图的位置，并生成 3 张配图 prompt。
```

```text
Use $circuit-guide-illustrations.

给这篇文章做一张公众号封面图和两张正文配图。
正文配图要保留 Circuit Guide 的克制工程感，不要变得可爱。
```

## 为什么要导出个人 Skill

如果一直用通用生成器，用户每次都要重新解释自己的 IP。

导出个人 Skill 后，IP 设定变成固定上下文：

- 用户不用再读 IP Bible。
- Agent 不用每次重新猜角色。
- 后续所有文章都能保持同一个视觉身份。
