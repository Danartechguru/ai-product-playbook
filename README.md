<h1 align="center">AI Product Playbook</h1>

<p align="center">
  <strong>Battle-tested Claude Skills and frameworks for building AI products that ship, scale, and stay compliant.</strong><br/>
  By <a href="https://danarmustafa.com">Danar Mustafa</a> — AI Product Leader · CPO / AI Product Manager / AI Tech Lead
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude-Skills-6b4fbb?style=for-the-badge" alt="Claude Skills"/>
  <img src="https://img.shields.io/badge/Focus-AI%20Product%20%26%20Strategy-2563eb?style=for-the-badge" alt="Focus"/>
  <img src="https://img.shields.io/badge/Region-EU%20%2F%20GDPR--aware-10b981?style=for-the-badge" alt="EU/GDPR"/>
</p>

<p align="center">
  <a href="#install--use"><strong>⬇️ Install in ~2 minutes</strong></a> ·
  <a href="#the-skills">See the skills</a> ·
  <a href="#try-one-now">Try one now</a>
</p>

---

## What this is

This is my working playbook for AI product leadership, packaged as **Claude Skills** —
reusable, installable capabilities that encode how I take AI products from a raw idea to
a compliant, margin-positive launch.

These aren't templates to fill in passively. Each skill is an opinionated thinking
partner: it asks the hard questions, pressure-tests assumptions, and produces artifacts
that make the *reasoning* visible — the way a good CPO works with a team.

## The skills

### 🧭 [`ai-product-roadmap`](skills/ai-product-roadmap)
Turns a raw AI idea into a phased, agile roadmap by running a tough-love interview that
pressure-tests the idea across product, users, technical architecture, infrastructure,
and AI evaluation — then breaks it into thin, shippable phases with a measurable eval
plan. The opposite of a feature wish-list with dates attached.

### 🇪🇺 [`enterprise-ai-coach-claude`](skills/enterprise-ai-coach-claude)
Coaches an EU organization through adopting Claude the compliant way — translating GDPR,
DPAs/SCCs, the EU AI Act, and DORA into prioritized steps, and helping choose the right
deployment path (Anthropic API, Amazon Bedrock, Google Vertex AI, or Microsoft Foundry
on Azure) for data residency and risk. *Structuring aid, not legal advice.*

### 💰 [`ai-unit-economics`](skills/ai-unit-economics)
Models the unit economics and pricing of an AI product — cost per request, per user, and
per account — and finds the levers (prompt caching, model routing, output limits) and
pricing structure (seat / usage / outcome / hybrid) that protect gross margin. The
viability leg most product teams skip.

### 🔎 [`ai-search-optimization`](skills/ai-search-optimization)
Writes and optimizes content so it gets surfaced and cited by AI search — Google AI
Overviews, ChatGPT, Claude, Perplexity, Gemini — covering AEO, GEO, and modern SEO, then
finishes with a human-first pass that strips the "AI slop" tells. Research-backed (the
GEO study's ranked levers) and built for product managers and marketers writing
newsletters, announcements, and articles.

### 🛡️ [`enterprise-ai-security`](skills/enterprise-ai-security)
The executive security and compliance brain for an AI company: decide which frameworks to
pursue and in what order (SOC 2, ISO 27001, ISO/IEC 42001, NIST CSF 2.0 + AI RMF, NIS2,
DORA), run a gap/risk assessment, threat-model an LLM product against the OWASP Top 10 for
LLMs, and build the trust story that unblocks enterprise deals (board briefings, trust
center, security questionnaires). AI-first, CTO/CISO-level — decisions and trade-offs, not
control memorization.

The first three cover the questions every AI product has to answer —
**is it desirable, is it viable, and can it actually be adopted?** The fourth makes sure
the story gets found, and the fifth makes it **trusted and enterprise-ready**.

## Install & use

Pick the path that matches how you use Claude. New to skills? Start with **Option A** —
it takes about two minutes and needs no command line.

### Option A — Upload into the Claude app (easiest, ~2 min)

A skill is just a small `.zip` you upload once. After that, Claude uses it automatically
whenever your request matches.

1. **Download** the skill you want from the [`dist/`](dist) folder (one `.zip` each), or
   grab [all five in one file](dist/ai-product-playbook-all-skills.zip).
2. In Claude, open **Settings → Capabilities → Skills** (on
   [claude.ai](https://claude.ai) or the desktop app).
3. Click **Upload skill** and choose the `.zip` you downloaded. Repeat for each skill.
4. That's it. Just describe your situation — *"help me plan my AI product"*, *"how should
   we price this feature"* — and the matching skill kicks in.

> Download links: [ai-product-roadmap](dist/ai-product-roadmap.zip) ·
> [ai-unit-economics](dist/ai-unit-economics.zip) ·
> [enterprise-ai-coach-claude](dist/enterprise-ai-coach-claude.zip) ·
> [ai-search-optimization](dist/ai-search-optimization.zip) ·
> [enterprise-ai-security](dist/enterprise-ai-security.zip)

### Option B — One command in Claude Code

This repo is also a Claude Code **plugin marketplace**, so you can install all five skills
with two commands:

```bash
/plugin marketplace add Danartechguru/ai-product-playbook
/plugin install ai-product-playbook@danar-ai-skills
```

Then run `/reload-plugins` (or restart). All five skills load at once and stay updated
when you re-run the marketplace add.

### Option C — Read them as frameworks (no Claude needed)

Each `skills/<name>/SKILL.md` is a self-contained playbook you can read straight through.
Scroll to the appendices for the interview banks, checklists, model templates, and
framework cheat-sheets.

### Try one now

These buttons open a new Claude chat with a ready-to-go prompt (they start a conversation;
they don't install the skill — do that with Option A or B first):

[![ai-product-roadmap](https://img.shields.io/badge/Try-ai--product--roadmap-6b4fbb?style=flat-square)](https://claude.ai/new?q=I%20want%20to%20build%20an%20AI%20product.%20Use%20the%20ai-product-roadmap%20skill%3A%20interview%20me%20with%20the%20tough%20questions%2C%20then%20turn%20it%20into%20a%20phased%2C%20agile%20roadmap%20with%20an%20evaluation%20plan.)
[![ai-unit-economics](https://img.shields.io/badge/Try-ai--unit--economics-2563eb?style=flat-square)](https://claude.ai/new?q=Help%20me%20model%20the%20unit%20economics%20and%20pricing%20of%20my%20AI%20feature%20using%20the%20ai-unit-economics%20skill%20%E2%80%94%20cost%20per%20request%2C%20per%20user%2C%20margin%20at%20the%20tail%2C%20and%20the%20right%20pricing%20structure.)
[![enterprise-ai-coach-claude](https://img.shields.io/badge/Try-enterprise--ai--coach-10b981?style=flat-square)](https://claude.ai/new?q=We%20want%20to%20roll%20out%20Claude%20in%20our%20EU%20organization%20the%20compliant%20way.%20Use%20the%20enterprise%20AI%20adoption%20skill%20to%20walk%20me%20through%20GDPR%2C%20DPAs%2C%20the%20EU%20AI%20Act%2C%20and%20the%20right%20deployment%20path.)
[![ai-search-optimization](https://img.shields.io/badge/Try-ai--search--optimization-f59e0b?style=flat-square)](https://claude.ai/new?q=Help%20me%20write%20content%20that%20gets%20cited%20by%20AI%20search%20%28Google%20AI%20Overviews%2C%20ChatGPT%2C%20Claude%29.%20Use%20the%20ai-search-optimization%20skill%20and%20finish%20with%20a%20human-first%20pass%20that%20removes%20AI-slop%20tells.)
[![enterprise-ai-security](https://img.shields.io/badge/Try-enterprise--ai--security-ef4444?style=flat-square)](https://claude.ai/new?q=Act%20as%20our%20executive%20AI%20security%20brain%20using%20the%20enterprise-ai-security%20skill%3A%20which%20frameworks%20should%20we%20pursue%20and%20in%20what%20order%20%28SOC%202%2C%20ISO%2027001%2C%20ISO%2042001%2C%20NIST%2C%20NIS2%29%2C%20and%20threat-model%20our%20LLM%20product.)

## Why I built this

I lead AI products at the intersection of strategy, applied AI, and business value. I
kept reaching for the same hard questions and frameworks across projects, so I encoded
them. Publishing them is partly to be useful, and partly to show how I think — rigor
over hype, evaluation over vibes, and viability treated as seriously as the demo.

## About

**Danar Mustafa** — AI Product Leader (CPO / AI Product Manager / AI Tech Lead), based in
Stockholm. I also build [aimognad.se](https://portal.aimognad.se/), an AI maturity
assessment platform for leadership teams.

🌐 [danarmustafa.com](https://danarmustafa.com) · 💼 [LinkedIn](https://www.linkedin.com/in/danarmustafa/) · 🧠 [digitalstrategy-ai.com](https://digitalstrategy-ai.com)

## Disclaimer

The `enterprise-ai-coach-claude` skill structures compliance work and points to primary
sources; it is **not legal advice** and does not replace qualified legal or
data-protection counsel. Provider terms, regions, and regulations change — always verify
against the official sources cited in the skill.

## License

[MIT](LICENSE) — use these freely, attribution appreciated.
