---
name: ai-rosetta-stone
description: Translates Claude concepts and terminology to ChatGPT, Gemini, and Microsoft Copilot (consumer, Microsoft 365, and GitHub variants) equivalents. Use when helping friends or colleagues on other platforms get set up, or when someone asks "how do I do X on ChatGPT / Gemini / Copilot?"
---

# AI Rosetta Stone

You are a cross-platform AI guide. The user speaks in Claude terminology and wants to help friends and colleagues on ChatGPT, Gemini, or Microsoft Copilot accomplish equivalent things. Translate **concepts**, not just features — help people understand *why* these features matter, not just where buttons are.

> **Note on Copilot:** "Microsoft Copilot" is three distinct products that share a brand: the **consumer chatbot** at copilot.microsoft.com, **Microsoft 365 Copilot** (the workplace product wired into Word/Excel/Outlook/Teams), and **GitHub Copilot** (the developer product). They have **separate logins, separate memory stores, and meaningfully different feature sets.** When a colleague says "Copilot," ask which one — the answer changes everything. See the dedicated Copilot section below.

> **⚠️ New in mid-2026 — "Cowork" is now ambiguous too.** Two different vendors ship a product called Cowork: **Claude Cowork** (Anthropic's agentic file/task worker — desktop, plus web and mobile since July 2026) and **Microsoft Copilot Cowork** (an M365 Copilot capability, GA June 16, 2026, billed per Copilot Credit). They solve a similar problem — "give it an outcome, get a finished deliverable" — but they are different products on different accounts with different billing. **Always ask "whose Cowork?"** This is the fastest-moving category in the whole comparison: OpenAI's entry, **ChatGPT Work**, launched July 9, 2026.

## Quick Reference: The Big Translation Table

The main table compares Claude, ChatGPT, Gemini, and **Microsoft Copilot** (consumer + Microsoft 365, since they share most concepts). **GitHub Copilot** has its own section further down — it's a developer tool, not a chatbot replacement.

| Claude Concept | ChatGPT Equivalent | Gemini Equivalent | Microsoft Copilot Equivalent |
|---|---|---|---|
| **User Preferences** (Settings > Profile) | **Custom Instructions** (Personalization > Custom Instructions, 1,500 chars) | **Personal context** (gemini.google.com/personal-context) | **Personalization settings** (consumer: Profile > Personalization; M365: account-level memory) |
| **Styles** (Normal / Concise / Explanatory + custom from samples) | **Personality** (presets: Friendly, Efficient, Professional, Candid, Quirky, Cynical, Nerdy) + Characteristics sliders | No direct preset equivalent; encode tone in Saved Info or Gem instructions | No direct equivalent; encode tone in custom agent instructions |
| **Projects** (workspace + files + instructions) | **Projects** (sidebar > New Project) | **Notebooks** (Projects-like; Gems are the closest *agent-style* equivalent) | **Copilot Notebooks** (M365 Copilot); consumer Copilot has **Library** but no true Projects |
| **Project Knowledge** (uploaded files) | **Project Files** (5 on Free, up to 40 on Business/Enterprise) | **Notebook sources** (up to 600 depending on plan); Gem files: 10 per prompt, 100 MB each | M365: knowledge attached to Notebooks or Studio agents (up to 512 MB per file); consumer: per-chat uploads only. **Copilot Notebooks now reach Copilot Chat (Basic)** — no full add-on license required |
| **Project Instructions** (system prompt per project) | **Project Instructions** | **Notebook custom instructions** / Gem instructions | M365: Notebook + Pages instructions; consumer: no persistent per-workspace instructions |
| **Memory** (auto + manual; now individually categorized entries, plus **Monthly Recap** at Settings > Reflect, beta) | **Memory** (Saved Memories + Reference Chat History) | **Personal context** (Past chats + manually saved info) + **Personal Intelligence** (Pro/Ultra beta — draws on your Google account) | **Copilot Memory** (consumer GA; M365 Personalization separate) |
| **Memory User Edits** ("remember that I…") | **Saved Memories** ("Remember that…") | Tell Gemini in chat, or add manually at Personal context | "Remember that…" works on consumer Copilot; M365 has separate Personalization store |
| **Skills** (markdown files; also uploadable on claude.ai) | **Custom GPTs** (chatgpt.com/create) | **Custom Gems** (Gem Manager > New Gem) | **Copilot Studio agents** (M365); no consumer agent builder |
| **Artifacts** (rendered code/docs in side panel, now with publishing + persistent storage + AI apps) | **Canvas** (collaborative side-panel editor) | **Canvas** (docs, code, web apps, slides; exports to Google Docs) | **Copilot Pages** (collaborative canvas, content lands in Library) |
| **Claude Code** (terminal-based agentic coding; IDE extensions, desktop app with built-in sandboxed browser, claude.ai/code) | **Codex** — no longer a separate app: merged into the unified **ChatGPT desktop app** (July 9, 2026) as one of three modes (Chat / Work / Codex). CLI and IDE extensions continue. | **Jules** (async GitHub coding agent) / **Gemini Code Assist** (IDEs) | **GitHub Copilot** (see dedicated section below) |
| **Cowork** (agentic file/task worker — desktop, **plus web at claude.ai and iOS/Android since July 7, 2026**, beta, Max first; tasks run in the cloud) | **ChatGPT Work** (launched July 9, 2026) — give it an outcome, it works for hours and returns finished decks/sheets/docs/web apps. ⚠️ **ChatGPT Atlas is being retired Aug 9, 2026**; its browser-agent powers moved into the ChatGPT desktop app. | **Project Mariner** (AI Ultra); agentic browsing in AI Mode | **Copilot Cowork** (M365 Copilot; GA June 16, 2026; consumption-billed in Copilot Credits). Also **Copilot Vision** (sees your screen) |
| **Web Search** (built-in, all plans) | **Search / Browse** (built-in) | **Google Search grounding** (automatic) | Web grounding (built-in across all variants) |
| **Research** (paid plans) | **Deep Research** | **Deep Research** (Free basic) / **Deep Research Max** (Ultra, with charts/interactive simulators) | **Researcher agent** (M365 Copilot; 25 queries/mo combined with Analyst) |
| **MCP Connectors** (all plans incl. Free, via claude.ai/directory) | **Apps** (formerly "Connectors"; renamed Dec 2025) — Drive, GitHub, Linear, HubSpot, Teams, etc. | **Connected Apps** (formerly Extensions) — Workspace, Maps, YouTube, Flights, Hotels, Photos | Plugins / Copilot Studio connectors; **Microsoft Graph** grounding in M365 |
| **Incognito Mode** | **Temporary Chat** | **Temporary Chats** | "Don't save" / signed-out modes vary by surface; M365 follows tenant retention policy |
| **Conversation Search** | **Search** (bar over chat history) | **Search past chats** | Search history in consumer Copilot; M365 history follows compliance policy |
| **File Creation Skill** (.docx, .xlsx, .pptx, .pdf) | **ChatGPT Work** returns finished sheets/slides/docs; **Canvas + Python** for lighter cases | **Canvas** export to Docs; **Veo 3.1** for video; **Nano Banana 2 / 2 Lite** for images | **Native** in Word/Excel/PowerPoint/Outlook for M365 Copilot — this is its core advantage; **Agent Mode in PowerPoint** builds decks from your Work IQ context |

## The Copilot Family: Three Products, One Brand

This is the biggest source of confusion for newcomers. Microsoft uses "Copilot" as an umbrella, but the three products diverge sharply on identity, memory, pricing, and feature set.

| Aspect | Consumer Copilot | Microsoft 365 Copilot | GitHub Copilot |
|---|---|---|---|
| **URL / surface** | copilot.microsoft.com; Windows/Mac/iOS/Android apps; Edge sidebar | copilot.microsoft.com (work tab) + native Word/Excel/PowerPoint/Outlook/Teams | github.com/features/copilot; VS Code, JetBrains, Visual Studio, Xcode, Neovim, github.com itself |
| **Account** | Microsoft account (MSA) — personal | Entra ID — work/school account | GitHub account |
| **Underlying models** | OpenAI GPT family **+ Microsoft MAI-1, MAI-Voice-1, MAI-Vision-1** | OpenAI frontier + Microsoft MAI; "Frontier" multi-model intelligence in Researcher | **Multi-vendor pick list** (changes almost monthly — verify before quoting): GPT-5.6 Sol / Terra / Luna, Claude Opus 5, Grok 4.5, **Kimi K2.7 Code** (first open-weight option). ⚠️ **Gemini models were removed from Copilot Chat on the web in May 2026** — the multi-vendor promise is now weaker than it was |
| **Memory** | Long-term Memory & Personalization (GA, rolled out from 2025) | Separate Personalization store; voice chats can reference memory | **None** — no user memory layer; context lives in repos and Spaces |
| **Workspace concept** | **Library** (Pages, images, generated content) — not a full Projects equivalent | **Copilot Notebooks** (refs + Pages + chats in one view); since mid-2026 also available on Copilot Chat (Basic) | **Copilot Spaces** (bundle repos, PRs, issues, files as shareable context) + **Copilot Workspace** (agentic dev env) |
| **Agentic "do the whole job" mode** | None (Vision sees your screen, but doesn't produce deliverables) | **Copilot Cowork** — GA worldwide June 16, 2026. Long-running, multi-tool tasks across M365 apps/files; returns a finished deliverable, not a draft. Requires an M365 Copilot USL **plus** consumption billing. Powered by the **Work IQ API** (also GA June 16) | **Coding agent** (assign an issue, get a PR) |
| **Canvas / artifacts** | **Copilot Pages** (collaborative canvas) | **Copilot Pages with Work IQ** (interactive visuals/apps from tenant data) | None — output is code, PRs, and chat |
| **Custom agents** | None for consumers (just Copilot Appearance experiments) | **Copilot Studio** included; agents deploy to M365 Chat and Teams. External channels require standalone Studio plan ($200/mo for 25K credits) | **Coding agent** (autonomously opens PRs from issues, formerly "Project Padawan") + third-party agents (Claude, Codex) callable from GitHub |
| **Voice / multimodal** | **Copilot Voice**, **Mico** expressive avatar (Labs), **Copilot Vision** (sees your screen), **Designer** image gen (DALL-E lineage) | Real-time voice; unlimited image gen for licensed users | Images in Spaces; voice is not a headline feature |
| **Research mode** | Consumer Deep Research-like mode | **Researcher agent** (multi-step, web + tenant data, outputs PPT/PDF/audio); **Analyst agent** for data analysis; **Computer Use in Researcher** (Frontier) | Web search tool in Chat; no dedicated Deep Research product |
| **Pricing** | **Free.** ⚠️ **Standalone Copilot Pro at $20/mo was discontinued October 2025** — replaced by **Microsoft 365 Premium** (~$19.99/mo, 1–6 people, 6TB storage, full Copilot AI features) | **~$30/user/month** annual (M365 Copilot add-on). Bundled SKUs added July 1, 2026: Business Standard + Copilot ~$23.50, Business Premium + Copilot ~$32/user/mo. **Copilot Cowork is billed on top**, in Copilot Credits — **$0.01/credit** PAYG or a discounted prepaid commitment | **Base prices unchanged**: Pro $10, Pro+ $39, Business $19/user/mo, Enterprise $39/user/mo (a **Max** SKU also now appears in model-availability notes). **⚠️ Usage-based billing went live June 1, 2026** — see the billing note below |
| **What makes it unique** | Mico avatar; Windows OS integration (Copilot key, Click-to-Do, Recall); Edge sidebar | **Tenant-grounded data via Microsoft Graph** (knows your org's docs, emails, calendar); native Office app actions; Frontier program | Only AI that lets you pick **Claude, GPT, or Gemini** from a single dropdown; native repo/PR/issue grounding; autonomous PR-opening agent |

### The biggest "gotchas" for someone migrating from Claude

1. **Memory does not cross the three Copilots.** Tell your consumer Copilot you're vegetarian — your M365 Copilot at work won't know. Three accounts, three memory stores.
2. **Copilot Pro is gone.** If a colleague says "I have Copilot Pro," they either have a legacy subscription (renewing until expiry) or they actually have **Microsoft 365 Premium**. The standalone $20/mo Copilot Pro SKU was discontinued October 2025.
3. **Copilot Studio agents are work-only.** Agents you build in Studio surface in M365 Copilot Chat and Teams, but **not in consumer Copilot** unless you buy the standalone Studio plan to publish to external channels.
4. **GitHub Copilot is not a Claude chatbot replacement.** It's IDE-embedded and lives in PRs, repos, and codespaces. Compare it to Claude Code, not to claude.ai.
5. **⚠️ "Cowork" now means two different products.** Microsoft's **Copilot Cowork** is an M365 Copilot capability on a work account, billed per credit. Anthropic's **Cowork** is a Claude feature included in your existing paid plan. A colleague saying "Cowork saved me hours" could mean either. See the Cowork note at the top of this guide.
6. **⚠️ GitHub Copilot's flat rate is over.** As of **June 1, 2026**, premium request units were replaced by **GitHub AI Credits**, metered on token usage (input, output, *and* cached context) at each model's published API rates. **Base plan prices didn't change**, but each plan now converts to a credit allotment — so heavy chat, agentic sessions, and code review burn budget far faster than before. Inline code completions remain free on all plans. Annual subscribers keep premium-request pricing until their term expires. Expect sticker shock: this change was contentious enough that developers nicknamed it the "tokenpocalypse."
7. **M365 Copilot has its own metered layer.** Copilot Cowork usage bills in **Copilot Credits** on top of the per-user license, and usage-based Copilot Credits billing became mandatory across workflows **July 1, 2026**. "We have M365 Copilot licenses" no longer means "everything is covered."

## Where Things Live: File/Skill Storage Locations

| Platform | What It's Called | Where It Lives |
|---|---|---|
| **Claude** | Skills (local) | Markdown files at `~/.claude/skills/` — read by Claude Code, Cowork, and Claude Desktop |
| **Claude** | Skills (uploadable on claude.ai) | **Customize > Skills > + Create skill > Upload a skill** (Pro/Max/Team/Enterprise; requires code execution enabled in Settings > Capabilities) |
| **Claude** | User Profile / Styles | Settings > personalization hub (profile instructions are account-wide; styles set tone) |
| **Claude** | Project Instructions | Inside each Project on claude.ai sidebar |
| **Claude** | Memory | Settings > Capabilities > "View and edit memory". Memory is now a set of **individually categorized entries** Claude reads and updates as you chat (not one daily summary). **Monthly Recap** lives at Settings > Reflect (beta; requires memory on) |
| **Claude** | Cowork sessions | Desktop app, **claude.ai home screen** (web), or the sidebar of the iOS/Android app. Sessions and files save to your Claude account and run in the cloud |
| **ChatGPT** | Custom Instructions | Settings > Personalization > Custom Instructions (1,500 char limit per field) |
| **ChatGPT** | Personality | Settings > Personalization > Personality (preset + Characteristics sliders) |
| **ChatGPT** | Custom GPTs | chatgpt.com/create; published GPTs discoverable at chatgpt.com/gpts |
| **ChatGPT** | Project Instructions | Inside each Project (sidebar > Project > Add Instructions) |
| **Gemini** | Personal context | gemini.google.com/personal-context (was gemini.google.com/saved-info) |
| **Gemini** | Custom Gems | Gem Manager in sidebar |
| **Gemini** | Notebook context | Inside each Notebook (Projects-like workspace) |
| **Consumer Copilot** | Memory | Profile menu > Personalization; can also say "remember that…" in chat |
| **M365 Copilot** | Personalization | Account-level memory (separate from consumer); voice chat can reference memory |
| **M365 Copilot** | Custom agents | Copilot Studio (copilotstudio.microsoft.com) — included with M365 Copilot license for internal use |
| **M365 Copilot** | Copilot Cowork | Inside M365 Copilot (requires a Copilot USL); usage bills in Copilot Credits, so admin consumption controls matter here |
| **GitHub Copilot** | Spaces | github.com > Copilot > Spaces (bundle repos/PRs/issues/files as shareable context) |
| **GitHub Copilot** | Coding agent jobs | Assign GitHub issues to Copilot — the cloud agent works on them and opens PRs |

### Critical Distinction for Claude Users

Claude skills started life as **local markdown files** version-controllable via git. As of 2026, Claude has caught up on the cloud side too: skills now upload to claude.ai via **Customize > Skills**. The full landscape:

- **Claude:** Local files (`~/.claude/skills/`) OR uploaded `.zip` via Customize > Skills. Both work. Most powerful and version-controllable.
- **ChatGPT:** Custom GPTs (server-side, GUI builder, marketplace at chatgpt.com/gpts)
- **Gemini:** Custom Gems (server-side, GUI builder, files + Drive linking)
- **Microsoft 365 Copilot:** Copilot Studio agents (low-code builder, deploy to Teams/M365 Chat)
- **GitHub Copilot:** Copilot Spaces (context bundles for code work, shareable within an org)
- **Consumer Copilot:** No custom agent builder — your only persistence is Memory + Library

Claude skills remain the most version-controllable option. The GPT/Gem/Studio paths are more accessible for non-engineers.

## Onboarding Guide: First 15 Minutes on Each Platform

The goal: make the AI *theirs* immediately, not a generic chatbot.

### Step 1: Set Your Identity

**On ChatGPT:**
1. Settings > Personalization > Custom Instructions
2. Fill in "What would you like ChatGPT to know about you?" — name, role, expertise level, use cases
3. Fill in "How would you like ChatGPT to respond?" — tone, format, length
4. Optionally set Personality (Friendly / Efficient / Professional / Candid / Quirky / Cynical / Nerdy)
5. Limit: 1,500 chars per field

**On Gemini:**
1. gemini.google.com/personal-context (or Settings > Personal context)
2. Add entries: "My name is X. I work as Y. Explain things at [beginner / intermediate / expert] level."
3. Alternative: tell Gemini "Remember that I prefer concise answers and work as a data analyst"
4. Memory is **on by default** — toggle Temporary Chats when you want no-memory sessions

**On Microsoft Copilot (consumer):**
1. Profile menu > Personalization
2. Tell Copilot "Remember that I…" — it confirms and saves
3. View/edit saved facts under Personalization settings
4. ⚠️ Note: This memory is **separate** from any work Copilot (M365) memory

**On Microsoft 365 Copilot (work):**
1. Memory is managed in your work account's personalization settings
2. Your IT admin may have memory disabled or restricted by policy
3. Tenant data (your docs, emails, calendar) is automatically available via Microsoft Graph — no setup needed

**On Claude (reference):**
- Settings > Profile / personalization hub
- Or: "Please remember that I…"

### Step 2: Create Your First Workspace

**On ChatGPT:**
1. Sidebar > "+" next to Projects > name it
2. Upload files (5 on Free; 25 on Go; ~20 on Plus; 40 on Pro/Business/Enterprise)
3. Project menu > Add Instructions
4. Chats inside share project context

**On Gemini:**
1. Sidebar > Notebooks > New (requires AI Plus, Pro, or Ultra)
2. Add sources — up to 600 depending on tier
3. Set custom instructions
4. Alternative for an *agent-style* assistant: Gem Manager > New Gem (writes to a role; attach 10 files / 100 MB each)

**On Microsoft 365 Copilot:**
1. Copilot home > Notebooks > New notebook
2. Add references from SharePoint, OneDrive, Teams, or uploaded files
3. Add Pages for collaborative content; Copilot can generate Word/PowerPoint from notebook contents

**On Consumer Copilot:**
1. No formal Projects — but Library collects your Pages, images, and generated content
2. Use Copilot Pages for ongoing collaborative documents

**On Claude (reference):**
- Sidebar > New Project > add files, set instructions
- For Claude Code users: drop a `SKILL.md` in `~/.claude/skills/<name>/`
- For claude.ai users: Customize > Skills > Upload a skill

### Step 3: Teach It Your Preferences Over Time

All platforms learn from conversations. Explicit > implicit.

| Action | ChatGPT | Gemini | Microsoft Copilot | Claude |
|---|---|---|---|---|
| Save a fact | "Remember that I'm vegetarian" | "Remember my daughter's name is Mia" | "Remember that I prefer concise answers" (consumer) | "Please remember that I prefer R over Python" |
| View what it knows | Settings > Personalization > Manage Memories | Settings > Personal context | Profile > Personalization (consumer); account settings (M365) | Settings > Capabilities > View and edit memory |
| Delete a memory | Manage Memories > delete | Personal context > delete entry | Personalization > delete | Memory > delete |
| Chat without memory | Temporary Chat | Temporary Chats | Sign-out / private mode varies | Incognito chats |

## Current Frontier Model Lineup (July 2026)

Model names churn faster than anything else in this guide. Treat the **tiering pattern** as durable and the specific names as perishable — every vendor now ships a "top / balanced / cheap" ladder, and the useful question is which rung a colleague is actually on, not which brand they use.

| Vendor | Top tier | Everyday / balanced | Fast & cheap |
|---|---|---|---|
| **Anthropic** | **Claude Fable 5** (most capable widely released) | **Claude Opus 5** (released July 24, 2026 — near-Fable performance at half the price) · **Claude Sonnet 5** | **Claude Haiku 4.5** |
| **OpenAI** | **GPT-5.6 Sol** (and **Sol Pro** on Pro/Enterprise) | **GPT-5.6 Terra** · GPT-5.5 Instant remains the fast default in ChatGPT | **GPT-5.6 Luna** |
| **Google** | **Gemini 3.1 Pro** (still the flagship — Pro has not been refreshed since Feb 2026) | **Gemini 3.6 Flash** (July 21, 2026) | **Gemini 3.5 Flash-Lite** |
| **Microsoft** | Doesn't train its own frontier tier — resells OpenAI frontier models alongside its in-house **MAI** family | | |

**What actually matters for a newcomer:**

1. **Everyone has a 1M-token context window now.** Claude's 5 family, Gemini 3.1 Pro, and the GPT-5.6 line all reach ~1M. "Which one handles long documents" is no longer a differentiator; how the product *manages* that context (Projects, Notebooks, auto-RAG) is.
2. **The price ladder collapsed.** Opus 5 shipped at half of Fable 5's price with better scores on several benchmarks; OpenAI cut GPT-5.6 Luna by 80% and Terra by 20% on July 30. Cost-per-task assumptions from even three months ago are stale.
3. **Release cadence is now weeks, not quarters.** Opus 5 was Anthropic's fourth Claude 5 release in under two months. If a colleague's mental model is "big annual launches," recalibrate them.
4. **Google's flagship is the outlier.** Gemini 3.1 Pro dates to February 2026 and July's release was Flash-tier only; **Gemini 4 is confirmed in pre-training**. Expect the Google column of this guide to move next.
5. **Don't quote a model name to a non-technical colleague.** They interact with a *plan tier*, not a model ID. "Are you on Plus or Pro?" gets you further than "are you using Sol or Terra?"

## Platform Strengths: When to Recommend Which

Not "which is best" — which is best *for the task*.

| Task | Best Platform | Why |
|---|---|---|
| Long document analysis (100+ pages) | **Claude** | 1M context across the Claude 5 family (Opus 5, Sonnet 5, Fable 5); auto-RAG in Projects when knowledge exceeds context |
| Code generation and debugging | **Claude Code** or **GitHub Copilot** | Claude leads SWE-bench; GitHub Copilot wins if you live in PRs and want autonomous PR-opening |
| Image generation | **Gemini** (Nano Banana 2 / 2 Lite — strong text rendering in 10+ languages, semantic masking, infographics) or **ChatGPT** | Both excellent; Claude can't generate images |
| Video generation | **Gemini** (Veo 3.1, built-in; 4/6/8-sec clips up to 4K with synced audio) or **ChatGPT** (Sora) | Native to both; Claude and Copilot have no video gen |
| Video understanding | **Gemini** | Native video processing of uploaded clips |
| Microsoft Office automation | **Microsoft 365 Copilot** | Native Word/Excel/PowerPoint/Outlook actions; no comparison |
| Google Workspace integration | **Gemini** | Native Drive/Gmail/Calendar/Docs Connected Apps |
| Tenant-grounded enterprise data | **Microsoft 365 Copilot** | Microsoft Graph grounding across your org's content |
| Multi-model coding (pick GPT/Claude/Gemini per task) | **GitHub Copilot** | Only product with model picker across all three vendors |
| Creative writing | **Claude** | Less "AI-sounding" prose; pushes back on weak ideas |
| Research with citations | **All five** | All have web grounding + Deep Research modes |
| Multi-modal (image + audio + video + voice) | **ChatGPT** | Broadest multimodal generation including voice conversations |
| Privacy-first / no-train-by-default | **Claude** | Constitutional AI training stance |
| Live visual prototyping | **Claude Artifacts** | React/HTML/SVG render live in the interface; now publishable as apps |
| Spreadsheets/slides/docs as files | **Claude** (file creation skill) or **M365 Copilot** (native) | Claude makes real .xlsx/.pptx; M365 edits them inside Excel/PowerPoint |
| Math-heavy reasoning | **ChatGPT** (GPT-5.6 Sol / Sol Pro) or **Gemini 3.1 Pro** | Both strong on pure math benchmarks |
| Async coding agent that opens PRs | **GitHub Copilot coding agent** or **Jules** (Gemini) | Live in GitHub; Claude Code is interactive rather than autonomous-async |
| Hand off a whole multi-hour deliverable | **Claude Cowork**, **ChatGPT Work**, or **Copilot Cowork** | The newest and most contested category — all three take an outcome and return finished files. Pick by where your data already lives: Claude for local/connected files, ChatGPT for connected apps, Copilot Cowork for Microsoft 365 tenants |
| Windows desktop integration | **Consumer Copilot** | Copilot key, Click-to-Do, Recall, Edge sidebar — built into the OS |

## Claude Code vs the World: Coding Tool Comparison

If a colleague asks about coding assistants specifically, this table is the cleanest comparison.

| Capability | Claude Code | OpenAI Codex | Gemini Code Assist / Jules | GitHub Copilot |
|---|---|---|---|---|
| **Terminal CLI** | ✅ Yes (primary surface) | ✅ Codex CLI (open source) | Limited | ✅ GitHub Copilot CLI |
| **IDE extensions** | ✅ VS Code, Cursor, Windsurf, JetBrains | ✅ VS Code, Cursor, Windsurf | ✅ VS Code, IntelliJ | ✅ Broadest (VS Code, JetBrains, Visual Studio, Xcode, Neovim) |
| **Desktop app** | ✅ Redesigned 2026 (parallel sessions, diffs, scheduled tasks, **built-in sandboxed browser** for reading docs/designs and clicking through pages) | ✅ **Merged into the unified ChatGPT desktop app** (July 9, 2026) as the Codex mode, alongside Chat and Work | ❌ | ❌ |
| **Web (no local clone)** | ✅ claude.ai/code | ✅ Codex Cloud | Partial (Jules is cloud-based) | ✅ Spaces + Workspace on github.com |
| **Model choice** | Claude only (Opus 5 / Sonnet 5 / Haiku / Fable 5) | OpenAI only | Gemini only | **Multi-vendor**: Claude, GPT, Grok, Kimi — but **Gemini was dropped from Copilot Chat on web (May 2026)** |
| **Autonomous PR opening** | ❌ (interactive) | Codex Cloud (background tasks) | ✅ Jules (async GitHub agent, open beta) | ✅ Coding agent (assign issues, get PRs) |
| **Native repo grounding** | Via filesystem access | Via filesystem access | Via Jules | ✅ Native (PRs, issues, Actions, Codespaces) |
| **MCP support** | ✅ Local + remote MCP servers | Limited | Limited | Limited |
| **Pricing model** | Included with Pro/Max/Team/Enterprise | Included with Plus/Pro/Business (Pro now has a $100 and a $200 tier) | Free Code Assist tier; Jules generally available | **⚠️ Token-metered usage-based billing since June 1, 2026** — GitHub AI Credits replaced premium requests; base prices unchanged, inline completions still free, annual plans keep old pricing until expiry |
| **Best for** | Long agentic sessions, file-heavy work, custom skills | OpenAI-stack shops, Codex Cloud delegation | Google-stack shops, async PR work | Multi-language teams who live on GitHub |

## Common Translation Scenarios

### "I use Claude Projects to keep my work organized"
→ **ChatGPT**: "You want Projects — same name, same concept. Sidebar > New Project. Upload files, set instructions, chats share context."
→ **Gemini**: "Use **Notebooks** for the closest match (up to 600 sources, persistent instructions). For an agent-style assistant attached to a role, use a Gem instead."
→ **M365 Copilot**: "**Copilot Notebooks** — collect references, Pages, and chats in one workspace. Bonus: you can generate Word/PowerPoint from notebook contents."
→ **Consumer Copilot**: "No true Projects equivalent. Closest is **Library** (collects your Pages and generated content), plus saved memory."

### "I set up User Preferences so Claude knows my style"
→ **ChatGPT**: "Settings > Personalization > Custom Instructions (1,500 chars). Also try Personality presets (Friendly / Efficient / Candid / etc.)."
→ **Gemini**: "gemini.google.com/personal-context — add facts there, or just tell Gemini 'Remember that I prefer…' in chat."
→ **M365 Copilot**: "Memory is account-level — say 'Remember that…' or use your work account's personalization settings. Note: separate from any consumer Copilot memory."
→ **Consumer Copilot**: "Profile > Personalization, or say 'Remember that…' Copilot will confirm and save."

### "I have Claude skills that customize behavior for specific tasks"
→ **ChatGPT**: "Build a Custom GPT at chatgpt.com/create. Name, instructions, attach files, no coding needed. Publishable to the GPT Store."
→ **Gemini**: "Create a Gem. Gem Manager > New Gem. Detailed instructions, attach up to 10 files (100 MB each). The magic wand expands your instructions."
→ **M365 Copilot**: "Build a **Copilot Studio** agent. Low-code GUI. Included with your M365 Copilot license for internal use; deploys to Teams and M365 Chat. External publishing needs a standalone Studio plan."
→ **Consumer Copilot**: "No agent builder exists for consumer Copilot. Use saved Memory + Library for ongoing context instead."

### "I use Artifacts to preview code and docs"
→ **ChatGPT**: "Closest is **Canvas** — side panel for collaborative editing. Click the Canvas icon or ask 'open in Canvas.'"
→ **Gemini**: "Gemini has **Canvas** too — docs, code, web apps, slides. Exports to Google Docs. Can convert output to Audio Overviews or quizzes."
→ **M365 Copilot**: "**Copilot Pages** — collaborative canvas; with Work IQ it can render interactive visuals/apps grounded in tenant data."
→ **Consumer Copilot**: "**Copilot Pages** — same canvas idea, content lands in Library for later access."

### "I use Claude's memory to avoid re-explaining myself"
→ **ChatGPT**: "Two layers: Saved Memories (explicit) + Reference Chat History (learns from past chats since April 2025). Settings > Personalization > Manage Memories."
→ **Gemini**: "**Personal context** (memory ON by default) — manage at gemini.google.com/personal-context. Use Temporary Chats when you want no-memory. Pro/Ultra subscribers also get **Personal Intelligence** in beta, which draws on your wider Google account context."
→ **Claude note (2026 update)**: "Claude's memory is no longer one rolling daily summary — it's a set of individually categorized entries Claude reads and updates mid-conversation, so corrections stick better. There's also a **Monthly Recap** at Settings > Reflect (beta) summarizing what you worked on and how you work; it requires memory to be on."
→ **M365 / Consumer Copilot**: "Copilot has its own memory layer per identity. ⚠️ Consumer and M365 memories are separate — don't expect them to share."

### "I use Claude Code for agentic coding work"
→ **OpenAI**: "**Codex** is the equivalent, but it's no longer its own app — since July 9, 2026 it's a mode inside the unified **ChatGPT desktop app** (Chat / Work / Codex). The CLI and IDE extensions still work as before, and Codex Cloud still handles delegated background tasks."
→ **Gemini**: "**Jules** is an async GitHub agent — assign work and it opens PRs. **Gemini Code Assist** for in-IDE help."
→ **GitHub Copilot**: "Different model — GitHub Copilot lives in PRs and issues. Its **coding agent** opens PRs autonomously from assigned issues. It still offers the widest model picker (Claude Opus 5, GPT-5.6, Grok, Kimi), though Gemini was dropped from Copilot Chat on the web in May 2026. ⚠️ Warn them about the June 2026 switch to token-metered billing before they lean on it heavily."

### "I hand Claude Cowork a task and come back to a finished deliverable"
This is the newest and most confusing category — ask **whose** Cowork before answering.
→ **ChatGPT**: "**ChatGPT Work** (launched July 9, 2026) is the direct equivalent. You give it an outcome rather than message-by-message prompts; it pulls context from your connected apps and files, works independently for hours, and hands back finished decks, sheets, docs, or web apps. No separate price — it draws on your existing plan's allowance. Pro/Enterprise/Edu got it first; Free and Go don't include it."
→ **M365 Copilot**: "**Copilot Cowork** — GA June 16, 2026, same 'returns a completed result, not a draft' pitch, grounded in your tenant via the Work IQ API. ⚠️ It needs a Microsoft 365 Copilot license **and** consumption billing in Copilot Credits ($0.01/credit PAYG). Budget for it; the license alone doesn't cover it."
→ **Gemini**: "No direct equivalent yet. **Project Mariner** and agentic browsing in AI Mode are the closest, but they're browser-task-shaped rather than deliverable-shaped."
→ **Consumer Copilot**: "Nothing equivalent. Copilot Vision can see your screen, but it doesn't produce deliverables unattended."

### "I use MCP to connect Claude to my tools"
→ **ChatGPT**: "**Apps** (formerly Connectors, renamed Dec 2025) — Drive, GitHub, Linear, HubSpot, Outlook, Teams, etc. Connect via Settings > Apps."
→ **Gemini**: "**Connected Apps** (formerly Extensions) — Workspace (Drive/Gmail/Calendar/Docs), Maps, YouTube, Flights, Hotels, Photos."
→ **M365 Copilot**: "Built-in **Microsoft Graph** grounding gives access to your tenant's docs/emails/calendar. Plus Copilot Studio connectors for external systems."

## Pricing Quick Reference (verified July 2026)

| Tier | Claude | ChatGPT | Gemini | Microsoft Copilot |
|---|---|---|---|---|
| **Free** | Limited messages | Limited messages — **⚠️ now ad-supported.** OpenAI began testing ads Jan/Feb 2026 for logged-in adults on Free and Go; by July 2026 ads appeared in roughly half of US replies across six countries | Gemini Flash, basic features | Consumer Copilot free; M365 Copilot Chat free with eligible M365 plans |
| **Budget tier** | — | **Go $8/mo** (US) — also ad-supported | **Google AI Plus** — roughly $5–8/mo, varies by region; verify locally | — |
| **~$20/month entry** | **Pro $17/mo annual** ($20 monthly) — 5× usage, all models, unlimited Projects | **Plus $20/mo** | **Google AI Pro $19.99/mo** — YouTube Premium Lite bundled in some markets | **⚠️ Copilot Pro discontinued Oct 2025** → **Microsoft 365 Premium ~$19.99/mo** (1–6 people, 6TB storage, full Copilot AI) |
| **$100+ power user** | **Max $100/mo** (5×) or **$200/mo** (20×) | **Pro $100/mo** (5× Plus limits) **or $200/mo** (20×) — the $100 tier launched April 9, 2026, explicitly to match Claude Max. Both tiers get the same models, including GPT-5.6 Sol Pro | **Google AI Ultra $99.99/mo or $199.99/mo** — Project Mariner, Deep Research Max, YouTube Premium | — |
| **Team/business** | **Team $20/seat/mo annual** ($25 monthly); **Premium seat $100 annual** ($125 monthly) | **Business $20/seat annual ($25 monthly)** | Included in Google Workspace Business+ | **M365 Copilot ~$30/user/mo** annual; bundles from July 1, 2026 (Business Standard + Copilot ~$23.50, Business Premium + Copilot ~$32). **GitHub Copilot: Pro $10, Pro+ $39, Business $19/user/mo** |
| **Enterprise** | $20/seat + usage that scales with model and task | Contact sales | Workspace Enterprise plans | M365 Copilot enterprise; **GitHub Copilot Enterprise $39/user/mo** |
| **Metered on top** | — | ChatGPT Work draws on your plan's existing allowance (no separate SKU) | — | **⚠️ Two separate meters.** M365: Copilot Cowork bills in **Copilot Credits** ($0.01/credit PAYG), mandatory since July 1, 2026. GitHub: **AI Credits** metered on tokens since June 1, 2026 |

**Branding and packaging changes — the rename history:**
- ChatGPT "Team" → "Business" (Aug 2025)
- ChatGPT "Connectors" → "Apps" (Dec 2025)
- Google "Google One AI Premium" → "Google AI Pro / Ultra"
- Microsoft "Copilot Pro" (standalone) → discontinued; folded into Microsoft 365 Premium (Oct 2025)
- **ChatGPT Free/Go → ad-supported (rolled out from Feb 2026)**
- **ChatGPT Pro → split into $100 and $200 tiers (April 9, 2026)**
- **GitHub Copilot → token-metered usage-based billing; premium requests replaced by GitHub AI Credits (June 1, 2026)**
- **M365 Copilot → Copilot Credits consumption billing mandatory (July 1, 2026)**
- **ChatGPT Atlas (standalone browser) → discontinued; retiring Aug 9, 2026, folded into the ChatGPT desktop app**
- **Codex desktop app → merged into the unified ChatGPT desktop app as a mode (July 9, 2026)**

## Tips for Helping Friends and Colleagues

1. **Ask which Copilot.** If someone says "I use Copilot," your first question is always: *consumer, work (M365), or GitHub?* The answer changes everything — different account, different memory, different features.

2. **Ask whose Cowork.** As of mid-2026 this is the second disambiguation question. *Claude Cowork* (Anthropic, included in your paid plan) and *Copilot Cowork* (Microsoft 365, licensed **and** metered) are different products. *ChatGPT Work* is OpenAI's equivalent under a third name.

3. **Check whether they're on a meter.** The flat-rate era is ending. GitHub Copilot moved to token-metered AI Credits in June 2026, M365 Copilot Credits became mandatory in July, and ChatGPT's free and Go tiers now carry ads. Before recommending heavy agentic use, ask what happens to their bill.

4. **Start with identity, not features.** The single biggest unlock on every platform is telling the AI who you are. Everything else builds on that.

5. **One workspace, one purpose.** Whether it's a Project (Claude/ChatGPT), Notebook (Gemini/M365 Copilot), Gem (Gemini), or Space (GitHub Copilot), scoping the AI to a specific job makes it dramatically better.

6. **Explicit > implicit memory.** All platforms learn from conversations, but explicitly saved preferences are more reliable and persistent.

7. **Don't compare features 1:1.** Each platform has genuine strengths — Claude for long context and skills, ChatGPT for multimodal breadth, Gemini for Workspace integration and video, M365 Copilot for Office work, GitHub Copilot for code-in-context. Match the tool to the actual work.

8. **Memory does not roam.** On Microsoft, the three Copilots have separate memory stores. On other platforms, your account is the unit of memory — sign in with the same account everywhere or expect amnesia.

9. **Show, don't tell.** The best onboarding is sitting with someone for 15 minutes and setting up their identity + first workspace together.

10. **Watch the pricing-page rebrands.** Tier names change every few months on every platform. When the prices in this doc look stale, treat the *concepts* as durable and re-verify the dollar amounts.

---

*Last verified: July 2026. AI platforms change features frequently — the May→July 2026 window alone brought a new Anthropic flagship (Opus 5), a new OpenAI model family (GPT-5.6) plus a new product (ChatGPT Work), the retirement of ChatGPT Atlas, two separate shifts to metered billing (GitHub Copilot, M365 Copilot), and a brand collision on the word "Cowork." When in doubt, check official docs.*

*Sources: [docs.claude.com](https://docs.claude.com) · [support.claude.com](https://support.claude.com) · [help.openai.com](https://help.openai.com) · [support.google.com/gemini](https://support.google.com/gemini) · [learn.microsoft.com](https://learn.microsoft.com) · [docs.github.com/copilot](https://docs.github.com/en/copilot)*
