# AI Rosetta Stone

[![Latest release](https://img.shields.io/github/v/release/pem725/ai-rosetta-stone?label=release&color=blue)](https://github.com/pem725/ai-rosetta-stone/releases/latest)
[![License: MIT](https://img.shields.io/github/license/pem725/ai-rosetta-stone?color=brightgreen)](LICENSE)
[![Downloads](https://img.shields.io/github/downloads/pem725/ai-rosetta-stone/total?color=informational)](https://github.com/pem725/ai-rosetta-stone/releases)
[![Last verified](https://img.shields.io/badge/verified-May%202026-success)](SKILL.md)
[![Claude Skill](https://img.shields.io/badge/Claude-Skill-D97757)](https://docs.claude.com)

A Claude skill that translates Claude concepts and terminology to **ChatGPT, Gemini, and Microsoft Copilot** equivalents. Built for Claude users who want to help friends and colleagues on other platforms get set up fast.

## What This Does

When you invoke this skill, Claude becomes a cross-platform translation guide. Speak in Claude terms ("Projects", "Skills", "Artifacts", "User Preferences", "MCP") and get concrete instructions for doing the equivalent on **ChatGPT, Gemini, or Microsoft Copilot** (consumer, Microsoft 365, or GitHub Copilot variants).

## Installation

**Claude Code (local):**
```bash
cp SKILL.md ~/.claude/skills/ai-rosetta-stone/SKILL.md
```

**claude.ai:** Upload `SKILL.md` (or the bundled `.zip`) via **Customize > Skills > + Create skill > Upload a skill**. Requires Pro, Max, Team, or Enterprise, with code execution enabled under Settings > Capabilities.

Or if sharing with others, they can clone and copy.

## Usage

Just reference the skill when helping someone:

- "My friend uses ChatGPT — how do they set up something like my Claude Projects?"
- "Translate my Claude workflow to Gemini for a colleague"
- "What's the Gemini equivalent of Artifacts?"
- "How do I do Claude Code stuff on GitHub Copilot?"
- "My colleague says they use 'Copilot' — what does that even mean?"

## What's Covered

- **Feature-to-feature translation table** (Claude → ChatGPT → Gemini → Microsoft Copilot)
- **The three Copilots explained** — consumer Copilot vs. Microsoft 365 Copilot vs. GitHub Copilot
- Where each platform stores its skills / agents / custom behavior
- **First-15-minutes onboarding guide** for each platform
- **Claude Code vs. Codex vs. Gemini Code Assist vs. GitHub Copilot** — coding-tool comparison
- **Platform strength comparison** (which tool for which job)
- **Common scenario translations** (Projects, Skills, Artifacts, Memory, MCP, coding agents)
- **Pricing quick reference** with the recent rebrand gotchas (Copilot Pro discontinued, ChatGPT Team→Business, Google AI Premium retired, GitHub Copilot billing transition)

## Maintenance

AI platforms change features constantly. The `SKILL.md` footer notes the last-verified date (currently **May 2026**). Update the skill when platforms ship major feature changes or rename tiers — the latter happens roughly quarterly across all four vendors.

When updating, verify against official docs:
- Claude: [docs.claude.com](https://docs.claude.com), [support.claude.com](https://support.claude.com)
- ChatGPT: [help.openai.com](https://help.openai.com)
- Gemini: [support.google.com/gemini](https://support.google.com/gemini)
- Microsoft Copilot: [learn.microsoft.com](https://learn.microsoft.com), [copilot.microsoft.com](https://copilot.microsoft.com)
- GitHub Copilot: [docs.github.com/copilot](https://docs.github.com/en/copilot)

## License

Share freely. Help your friends and colleagues use AI better.
