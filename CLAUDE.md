# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AI Rosetta Stone is a Claude skill that translates Claude concepts and terminology to **ChatGPT, Gemini, and Microsoft Copilot** equivalents. Copilot coverage spans all three variants — consumer Copilot, Microsoft 365 Copilot, and GitHub Copilot — because they share a brand but diverge sharply on identity, memory, pricing, and feature set.

The skill's core value is **disambiguation**: when one word means different products at different vendors, this doc is what untangles it. There are now two such words — **"Copilot"** (three Microsoft products) and, since mid-2026, **"Cowork"** (Anthropic's Claude Cowork vs Microsoft's Copilot Cowork, with OpenAI's ChatGPT Work as a third name for the same job).

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

0. **Two disambiguation notes at the top** — the "which Copilot?" note and the "whose Cowork?" note. These come before the first table on purpose: they are the questions that must be answered before any other advice is valid.
1. **Quick Reference Table** — feature-by-feature mapping across four columns (Claude → ChatGPT → Gemini → Microsoft Copilot). GitHub Copilot is *not* in this table because it's a developer tool that doesn't map cleanly to consumer concepts.
2. **The Copilot Family** — dedicated comparison of consumer Copilot, Microsoft 365 Copilot, and GitHub Copilot, plus "biggest gotchas" for newcomers. Includes an "agentic do-the-whole-job mode" row so Copilot Cowork sits in the family table, not just the main table.
3. **Storage Locations** — where each platform stores skills/preferences/agents, with a critical distinction about Claude's local-file approach vs. server-side alternatives. Includes the updated `claude.ai` skill-upload path (Customize > Skills).
4. **Onboarding Guide** — 3-step walkthrough (identity → workspace → preferences) for each platform, with a Step 1 sub-block for M365 Copilot since the work-account path differs.
5. **Current Frontier Model Lineup** — a top/balanced/cheap ladder per vendor, plus "what actually matters" notes. **Framed so the tiering pattern is the durable content and the model names are explicitly perishable** — this section will rot faster than any other, and it says so.
6. **Platform Strengths** — task-based recommendations, not universal rankings. Includes Microsoft-specific wins (Office automation, tenant grounding, Windows OS integration) and GitHub Copilot's multi-vendor model picker.
7. **Claude Code vs. the World** — dedicated coding-tool comparison table (Claude Code / Codex / Gemini Code Assist + Jules / GitHub Copilot). This is where GitHub Copilot belongs.
8. **Common Translation Scenarios** — real-world "I use X on Claude, what's the equivalent?" patterns. Each scenario has four bullets (ChatGPT / Gemini / M365 Copilot / consumer Copilot).
9. **Pricing Quick Reference** — tier comparison across all four platforms, including a "metered on top" row for the usage-based layers, with a rename-history callout for the branding gotchas.

## Editing Guidelines

- The skill takes a concept-first approach: explain *why* features matter, not just where buttons are.
- Platform strengths are framed as task-specific, not absolute rankings. Maintain this neutrality.
- The last-verified date lives in **three** places and they are kept in sync manually. Update all three or the doc lies to readers:
  1. the `SKILL.md` footer (`*Last verified: [Month Year]...*`)
  2. the README shields.io badge URL (`verified-July%202026-success`)
  3. the README "Keeping it current" prose, which names the month again
- Pricing and feature details change frequently. When updating, verify against official docs: `docs.claude.com`, `support.claude.com`, `claude.com/pricing`, `help.openai.com`, `support.google.com/gemini`, `learn.microsoft.com`, `github.blog`, `docs.github.com/copilot`.
- **Always ask "which Copilot?"** Any new Copilot scenario should specify consumer, M365, or GitHub — they're three different products and conflating them is a top source of bad advice.
- **Always ask "whose Cowork?"** Since mid-2026 this is the second required disambiguation. Claude Cowork (Anthropic, included in the plan), Copilot Cowork (M365, licensed *and* metered), and ChatGPT Work (OpenAI) are three products for one job. Never write "Cowork" unqualified.
- **Call out metered billing explicitly.** Flat-rate is no longer the default assumption: GitHub Copilot moved to token-metered AI Credits (June 1, 2026) and M365 Copilot Credits became mandatory (July 1, 2026). Any recommendation involving heavy agentic use should say what it does to the bill. This is now a first-class category of gotcha, alongside identity and memory.
- **Treat model names as perishable, tiers as durable.** The frontier lineup section is written so the top/balanced/cheap *pattern* survives even when every model name in it is wrong. Don't rewrite it into a flat list of current names — keep the framing that warns readers the names rot.
- When platforms rename tiers, retire products, or change billing (which happens ~quarterly), update the price table AND the rename-history callout so someone searching the old name can find their way to the new one. Retirements matter as much as renames — ChatGPT Atlas and the standalone Codex app both disappeared in July 2026.
- After editing `SKILL.md`, rebuild the release zip so the checked-in artifact matches: `rm -f ai-rosetta-stone.zip && zip ai-rosetta-stone.zip SKILL.md`.
