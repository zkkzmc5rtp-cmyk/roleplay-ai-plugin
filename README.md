# roleplay-ai-plugin

> 让 AI 真正「像」那个角色说话的 Agent Skills 合辑。

这里的每个技能都是纯提示词（Markdown），不含代码、不含正文，装上就能用。
适用于任何支持 Agent Skills 的工具：Claude Code、Cherry Studio、Cursor、Codex、Gemini CLI 等。

---

## 技能列表

| 技能 | 角色 | 出处 | 说明 |
| --- | --- | --- | --- |
| [`sheng-caier`](skills/sheng-caier/) | 圣采儿 | 《神印王座》 | 轮回圣女。话极少，冷，情绪只写在动作里 |

---

## 安装

### 安装全部

```bash
npx skills add zkkzmc5rtp-cmyk/roleplay-ai-plugin --skill '*' -g
```

### 只装某一个

```bash
npx skills add zkkzmc5rtp-cmyk/roleplay-ai-plugin --skill sheng-caier
```

### 先看看有哪些

```bash
npx skills add zkkzmc5rtp-cmyk/roleplay-ai-plugin --list
```

### Cherry Studio

把 `skills/` 下对应的技能文件夹（如 `sheng-caier`）整个复制到 Cherry Studio 的技能目录：

```
<Cherry Studio 数据目录>/Data/Skills/sheng-caier/
```

复制进去后会自动同步，新开一个会话即可生效。

---

## 设计取向

角色扮演技能最常见的失败不是设定写得不全，而是**语气跑偏**——模型会不自觉地
把角色写成一个话多、爱解释、情绪全写在脸上的解说员。

所以这里每个技能都在处理同一件事：**用范例和反例把语感钉住**。
反例往往比正例更有效——明确写出「不要这样写」比写十条「要这样写」管用。

---

## 目录结构

```
roleplay-ai-plugin/
├── README.md
├── LICENSE
└── skills/
    └── sheng-caier/
        ├── SKILL.md              角色规则 + 触发条件
        └── references/
            ├── lore.md           人物档案、关系网、世界观、时间线
            └── voice.md          语气范例与反例
```

---

## 贡献

欢迎 PR 补充其他角色。一个技能一个文件夹，放进 `skills/` 下，结构照 `sheng-caier` 来：

- `SKILL.md` 的 `description` 要写清楚**什么时候该触发**，并带上角色别名，
  否则模型不会主动加载它；
- 语气范例请同时给**正例和反例**；
- 拿不准的原著设定宁可留白，不要编。

---

## 版权声明

本仓库是**同人向的提示词作品，不包含任何原著正文**。
相关作品及其角色的版权归原作者及相关权利方所有。仅供个人学习与娱乐使用，请勿商用。

若二次分发，请保留本段说明。

## License

MIT，见 [LICENSE](LICENSE)。
