# Contributing to AI Rosetta Stone

Thanks for helping keep this reference accurate. AI platforms rename tiers, deprecate features, and ship new ones constantly — keeping this doc useful is mostly a maintenance job, and small PRs are very welcome.

## What kinds of changes are useful

**Highly useful:**
- A platform renamed a tier, feature, or menu path (e.g., "Connectors" → "Apps", "Saved Info" → "Personal context")
- A pricing number is wrong or outdated
- A feature was discontinued or merged into another (e.g., Copilot Pro → Microsoft 365 Premium)
- A new feature that doesn't fit the current taxonomy cleanly (worth discussing in an issue first)
- A new platform worth adding (would need its own column and section — open an issue first)

**Useful but lower priority:**
- Typo fixes
- Clearer wording for an existing concept
- Better example phrasings in the "Common Translation Scenarios" section

**Probably not useful:**
- Re-ranking the "Platform Strengths" table to favor one platform — the doc deliberately avoids absolute rankings. If a platform genuinely leads on a new task, add a new row rather than rewriting existing ones.
- Expanding into API/developer-platform concepts — this skill is scoped to end-user products (claude.ai, chatgpt.com, gemini.google.com, copilot.microsoft.com, github.com/copilot).

## How to verify before submitting

Every factual change should be cross-checked against an official source. Bookmark these:

- **Claude:** [docs.claude.com](https://docs.claude.com), [support.claude.com](https://support.claude.com), [claude.com/pricing](https://claude.com/pricing)
- **ChatGPT:** [help.openai.com](https://help.openai.com), [chatgpt.com/pricing](https://chatgpt.com/pricing)
- **Gemini:** [support.google.com/gemini](https://support.google.com/gemini), [one.google.com/about/google-ai-plans](https://one.google.com/about/google-ai-plans)
- **Microsoft Copilot:** [learn.microsoft.com](https://learn.microsoft.com), [microsoft.com/microsoft-365-copilot/pricing](https://www.microsoft.com/en-us/microsoft-365-copilot/pricing)
- **GitHub Copilot:** [docs.github.com/copilot](https://docs.github.com/en/copilot), [github.com/features/copilot/plans](https://github.com/features/copilot/plans)

When you submit a PR, please include the source URL you verified against in the PR description. This makes review fast and keeps the doc auditable.

## Style guide

A few conventions the existing content follows — please match them so the doc reads consistently.

1. **Concept-first.** Explain *why* a feature matters, not just where the button is. A new reader should understand the concept even if the UI moves.
2. **Neutrality.** Each platform has genuine strengths. The doc frames recommendations by task, not by overall ranking. Avoid "best AI" framing.
3. **Always ask "which Copilot?"** Any Copilot-related change should specify consumer, Microsoft 365, or GitHub. They're three different products that share a brand. Conflating them is the single biggest source of bad advice.
4. **Tier renames are a story worth keeping visible.** When you update a price or feature name, also update the **"Branding changes since early 2026"** callout in the pricing section so the rename history stays surfaced. Future readers searching for the old name need to find their way to the new one.
5. **Cite uncertainty.** If a fact isn't clearly documented, it's better to flag it as uncertain than to guess.

## Updating the "last verified" date (two places)

When you re-verify content against official docs, update the date in **both** places — they're kept in sync manually:

1. **`SKILL.md` footer** — the `*Last verified: [Month Year]...*` line at the bottom of the file.
2. **`README.md` badge URL** — the "Last verified" badge near the top of the README. Edit the `verified-[Month]%20[Year]` segment of the shields.io URL (`%20` is URL-encoded space). Example: `verified-May%202026-success` becomes `verified-November%202026-success`.

If you only update one, the README will lie to readers. Update both in the same PR.

## Updating the bundled .zip

`ai-rosetta-stone.zip` is checked in so people can upload it directly to claude.ai without cloning. After any change to SKILL.md, rebuild the zip:

```bash
rm -f ai-rosetta-stone.zip
zip ai-rosetta-stone.zip SKILL.md
```

Commit the rebuilt zip in the same PR as the SKILL.md change.

## Filing issues

Issues are the right place for:
- "I noticed [platform] renamed X to Y" reports if you don't want to open a PR yourself
- Discussion of new platforms or features that need a structural change (e.g., a new column in the main table)
- Bug reports — typos, broken links, broken tables

## License

By contributing, you agree your changes will be released under the project's MIT License (see [LICENSE](LICENSE)).
