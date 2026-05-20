# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AI Rosetta Stone is a Claude skill that translates Claude concepts and terminology to **ChatGPT, Gemini, and Microsoft Copilot** equivalents. Copilot coverage spans all three variants — consumer Copilot, Microsoft 365 Copilot, and GitHub Copilot — because they share a brand but diverge sharply on identity, memory, pricing, and feature set.

It's a pure markdown project — no code, no build system, no dependencies.

## Repository Structure

```
SKILL.md    # The skill itself (YAML frontmatter + markdown reference guide)
README.md   # Installation instructions and project overview
```

## Installation

**Claude Code (local):**
```bash
cp SKILL.md ~/.claude/skills/ai-rosetta-stone/SKILL.md
```

**claude.ai:** Upload the zip or SKILL.md via **Customize > Skills > + Create skill > Upload a skill**. Requires Pro/Max/Team/Enterprise and code execution enabled under Settings > Capabilities. (The older "Settings > Capabilities > Skills > + Add" path was replaced in 2026.)

## Working with This Repo

- There is no build, lint, or test process. Changes are purely editorial.
- `SKILL.md` must retain its YAML frontmatter (`name` and `description` fields) — this is required by both Claude Code and claude.ai's skill upload parser.
- The `.zip` format for claude.ai upload must contain `SKILL.md` at the root level (not nested in a subdirectory).

## Content Architecture

SKILL.md is organized as a reference guide with these sections:

1. **Quick Reference Table** — feature-by-feature mapping across four columns (Claude → ChatGPT → Gemini → Microsoft Copilot). GitHub Copilot is *not* in this table because it's a developer tool that doesn't map cleanly to consumer concepts.
2. **The Copilot Family** — dedicated comparison of consumer Copilot, Microsoft 365 Copilot, and GitHub Copilot, plus "biggest gotchas" for newcomers.
3. **Storage Locations** — where each platform stores skills/preferences/agents, with a critical distinction about Claude's local-file approach vs. server-side alternatives. Includes the updated `claude.ai` skill-upload path (Customize > Skills).
4. **Onboarding Guide** — 3-step walkthrough (identity → workspace → preferences) for each platform, with a Step 1 sub-block for M365 Copilot since the work-account path differs.
5. **Platform Strengths** — task-based recommendations, not universal rankings. Includes Microsoft-specific wins (Office automation, tenant grounding, Windows OS integration) and GitHub Copilot's multi-vendor model picker.
6. **Claude Code vs. the World** — dedicated coding-tool comparison table (Claude Code / Codex / Gemini Code Assist + Jules / GitHub Copilot). This is where GitHub Copilot belongs.
7. **Common Translation Scenarios** — real-world "I use X on Claude, what's the equivalent?" patterns. Each scenario now has four bullets (ChatGPT / Gemini / M365 Copilot / consumer Copilot).
8. **Pricing Quick Reference** — tier comparison across all four platforms, with a "Branding changes since early 2026" callout for the rename gotchas.

## Editing Guidelines

- The skill takes a concept-first approach: explain *why* features matter, not just where buttons are.
- Platform strengths are framed as task-specific, not absolute rankings. Maintain this neutrality.
- The footer contains a last-verified date and documentation links. Update the date when making changes.
- Pricing and feature details change frequently. When updating, verify against official docs: `docs.claude.com`, `support.claude.com`, `help.openai.com`, `support.google.com/gemini`, `learn.microsoft.com`, `docs.github.com/copilot`.
- **Always ask "which Copilot?"** Any new Copilot scenario should specify consumer, M365, or GitHub — they're three different products and conflating them is the #1 source of bad advice.
- When platforms rename tiers (which happens ~quarterly), update the price table AND the "Branding changes since early 2026" callout so the rename history stays visible.
