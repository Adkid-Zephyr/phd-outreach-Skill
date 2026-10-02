# PhD Outreach · 博士套磁信

**从教授视角写博士套磁信：简洁、具体、可信。轻量级、零运行依赖的双语 Skill + 提示词，复制即用。**

[English README](README_EN.md) · [中文 Skill](skills/phd-outreach/SKILL.md) · [English Skill](skills/phd-outreach-en/SKILL.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Adkid-Zephyr/phd-outreach-Skill/pulls)

## 这是什么

套磁信写了五六段，教授却还找不到你什么时候毕业、具体做过什么、打算哪一年入学。让 AI 润色之后，往往只是多了几句赞美和“对科研充满热情”。

这个 Skill 帮你从旧信、CV 和科研经历中提炼可核实的信息，直接给一封英文草稿：

> **把套磁信写成研究经历的短预告：让教授愿意看你的 CV，再决定是否继续交流。**

默认三个短段落，约 150–200 个英文词；信息少时更短，具体招生要求优先。它也支持简短 follow-up，以及尚无已发表论文的申请者。

## 修改示例

以下为虚构材料的措辞示例，不是申请效果评估。

| 原写法 | 修改后 |
| --- | --- |
| I am highly passionate about your outstanding research and believe I am the perfect fit. | I am completing an MSc in Data Science at Riverside University in the UK, with expected graduation in September 2027. |
| I have extensive research experience and have worked on many projects. | In a four-person robustness project, I designed input-perturbation experiments, implemented evaluation scripts, and analysed failure cases. |
| I have a paper and want to join your group as soon as possible. | The manuscript is under review. Are you considering new PhD students for [Intended start term]? |

个人贡献要有依据；投稿中不能改成已发表；不知道入学时间就保留待填项。

## 快速开始

### 方式一：复制提示词

复制 [中文提示词](prompts/精简版提示词.txt) 或 [English prompt](prompts/quick-prompt-en.txt)，粘贴到 AI 对话中，再发你的旧信或研究经历。无需安装 Skill。

有多少材料贴多少：学历与学校、毕业时间、个人研究贡献、论文真实状态、导师要求、目标入学时间。缺项会标注，不需要先填一张完整问卷。

### 方式二：安装 Skill

先下载仓库：

```bash
git clone https://github.com/Adkid-Zephyr/phd-outreach-Skill.git
cd phd-outreach-Skill
```

选择一种语言的完整目录。以下以中文 Skill 为例：

```bash
# Codex：个人 Skill 目录
mkdir -p ~/.agents/skills
cp -R skills/phd-outreach ~/.agents/skills/

# Claude Code：个人 Skill 目录
mkdir -p ~/.claude/skills
cp -R skills/phd-outreach ~/.claude/skills/
```

只需执行与你使用的工具对应的一组命令。英文版将目录名换成 `phd-outreach-en`。

Codex 中可说：

```text
请用 $phd-outreach，根据我的旧信和 CV 提炼真实贡献，直接给一版英文套磁信。
```

Claude Code 中可用 `/phd-outreach`，再提供材料。英文版对应 `$phd-outreach-en` 或 `/phd-outreach-en`。安装位置和发现方式见 [OpenAI Docs](https://learn.chatgpt.com/docs/build-skills) 与 [Claude Code 文档](https://code.claude.com/docs/en/skills)。

## 核心方法

1. **背景与时间**：写清当前学历、学校、预计毕业时间及目标入学时间。
2. **真实研究贡献**：选择一个最有说服力的项目，写一至两项自己做过的具体工作。
3. **清楚的下一步**：询问招生意向，表达愿意简短交流；确认附件安排后再写已附 CV。
4. **准确的论文状态**：区分已发表、已接收、投稿中、预印本和未发表工作；不堆篇数。
5. **适度的研究连接**：有真实依据时保留一句，不复述教授整段研究履历。
6. **缺项不编造**：先给草稿，以占位符标出未知或冲突信息。
7. **按要求跟进**：约一周无回复时可考虑简短 follow-up；不把跟进三次设成目标。

默认输出一个 Subject、一封邮件及至多三条修改说明；也可要求只给正文。

## 仓库结构

```text
phd-outreach-Skill/
├── skills/
│   ├── phd-outreach/          # 中文方法、元数据、模板和来源说明
│   └── phd-outreach-en/       # English version，独立完整目录
├── prompts/
│   ├── 精简版提示词.txt
│   └── quick-prompt-en.txt
├── README.md / README_EN.md
└── LICENSE
```

每个 Skill 都附有初次联系和 follow-up 的 [英文骨架](skills/phd-outreach/assets/email-template.txt)。

## 方法来源与适用范围

方法来自一位招生教授的经验讲解，主要针对美国博士初次联系；三个段落和词数范围是为复用增加的写作参考。不同地区、学科和招生公告的要求优先，不保证回信或录取。

现有整理材料未提供可公开核验的讲者姓名或原始链接；本仓库不作大学背书声明，也不发布录音或逐字转写。原观点与本项目的取舍见 [来源说明](skills/phd-outreach/references/source-notes.md)。

本项目的轻量双语包装参考 [anti-defensive-writing-Skill](https://github.com/Adkid-Zephyr/anti-defensive-writing-Skill)。套磁方法、事实边界和邮件模板在本仓库独立维护。

## License

MIT。欢迎改进提示词、翻译和示例。
