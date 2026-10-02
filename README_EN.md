# PhD Outreach

**Write concise, specific and credible PhD inquiry emails from a professor's perspective. A lightweight bilingual Skill + prompt pack with no runtime dependencies.**

[中文 README](README.md) · [English Skill](skills/phd-outreach-en/SKILL.md) · [中文 Skill](skills/phd-outreach/SKILL.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Adkid-Zephyr/phd-outreach-Skill/pulls)

## What is this?

A long inquiry email can bury the information a professor needs: when you graduate, what you personally did in research and when you want to start a PhD. AI polishing can add praise without making those facts easier to find.

This Skill turns a draft, CV or research notes into a usable email:

> **Make the email a short preview of your research experience, giving the professor a reason to read your CV and continue the conversation.**

The default is three short paragraphs, roughly 150–200 English words. Use fewer when there is less information, and follow any specific recruitment requirements. Short follow-ups and applicants without published papers are supported.

## Editing examples

These are wording examples using fictional information, not an evaluation of admissions outcomes.

| Original wording | Revised wording |
| --- | --- |
| I am highly passionate about your outstanding research and believe I am the perfect fit. | I am completing an MSc in Data Science at Riverside University in the UK, with expected graduation in September 2027. |
| I have extensive research experience and have worked on many projects. | In a four-person robustness project, I designed input-perturbation experiments, implemented evaluation scripts, and analysed failure cases. |
| I have a paper and want to join your group as soon as possible. | The manuscript is under review. Are you considering new PhD students for [Intended start term]? |

Personal contributions need evidence. Under review must remain under review. An unknown start term remains a placeholder.

## Quick start

### Option 1: Copy the prompt

Copy the [English prompt](prompts/quick-prompt-en.txt) or [中文提示词](prompts/精简版提示词.txt) into your AI conversation, then paste your draft or research notes. No Skill installation is required.

Provide whatever you have: degree and institution, graduation date, personal contributions, manuscript status, professor requirements and intended start term. Missing facts are marked; a complete questionnaire is not required.

### Option 2: Install the Skill

Download the repository:

```bash
git clone https://github.com/Adkid-Zephyr/phd-outreach-Skill.git
cd phd-outreach-Skill
```

Choose the complete folder for one language. For the English Skill:

```bash
# Codex: personal Skill directory
mkdir -p ~/.agents/skills
cp -R skills/phd-outreach-en ~/.agents/skills/

# Claude Code: personal Skill directory
mkdir -p ~/.claude/skills
cp -R skills/phd-outreach-en ~/.claude/skills/
```

Run only the commands for your chosen tool. For Chinese instructions, use `phd-outreach` instead of `phd-outreach-en`.

In Codex, ask:

```text
Use $phd-outreach-en to turn my draft and CV into a concise PhD inquiry email, highlighting my actual research contributions.
```

In Claude Code, invoke `/phd-outreach-en` and provide your materials. The Chinese version uses `$phd-outreach` or `/phd-outreach`. See [OpenAI Docs](https://learn.chatgpt.com/docs/build-skills) and the [Claude Code documentation](https://code.claude.com/docs/en/skills) for discovery and installation locations.

## The method

1. **Background and timing:** make the degree, institution, graduation date and intended start term easy to find.
2. **Actual contributions:** select one convincing project and one or two specific things you personally did.
3. **A clear next step:** ask about recruitment and offer a brief conversation; mention an attached CV only when the attachment arrangement is confirmed.
4. **Accurate publication status:** distinguish published, accepted, under review, preprint and unpublished work. Paper counts do not replace contributions.
5. **A useful research connection:** retain one supported connection when it helps; avoid repeating the professor's research biography.
6. **Visible unknowns:** deliver a draft with clear placeholders for missing or conflicting facts.
7. **Contextual follow-ups:** a short follow-up may be considered after about a week without a reply. Three attempts are not a target.

The default output is one subject line, one email and up to three editing notes. You can request only the email.

## Repository structure

```text
phd-outreach-Skill/
├── skills/
│   ├── phd-outreach/          # Chinese instructions and resources
│   └── phd-outreach-en/       # Complete English instructions and resources
├── prompts/
│   ├── 精简版提示词.txt
│   └── quick-prompt-en.txt
├── README.md / README_EN.md
└── LICENSE
```

Each Skill includes an [English inquiry and follow-up template](skills/phd-outreach-en/assets/email-template.txt).

## Source and scope

The method was distilled from one recruiting professor's advice, mainly about initial contact for US PhD applications. The paragraph count and word ranges are practical defaults added for reuse. Specific programmes and recruitment instructions take priority; replies and admission are not guaranteed.

The supplied source notes did not include a publicly verifiable speaker name or original link. This repository makes no claim of university endorsement and distributes neither recordings nor verbatim transcripts. See the [source notes](skills/phd-outreach-en/references/source-notes.md) for which ideas were retained or adapted.

The lightweight bilingual packaging follows [anti-defensive-writing-Skill](https://github.com/Adkid-Zephyr/anti-defensive-writing-Skill). The outreach method, factual boundaries and templates are maintained independently here.

## License

MIT. Contributions to prompts, translations and examples are welcome.
