---
name: ai-unit-economics
description: >-
  Model the unit economics and pricing of an AI/LLM product — cost per request, per
  active user, and per account — and find the levers (prompt caching, model routing,
  output limits, batching) and pricing structure (seat, usage, outcome-based, or
  hybrid) that protect gross margin. Use this whenever someone needs to understand or
  defend the cost and margin of an AI feature, set or sanity-check pricing, build a
  business case or board/investor model for an AI product, worry that token costs will
  eat their margin, or decide how to charge for an AI feature. Trigger on questions
  like "will this be profitable", "how much does each user cost us", "how should we
  price this AI feature", "what's our gross margin on the AI", or "our inference costs
  are too high".
---

# AI Unit Economics & Pricing

Traditional software has near-zero marginal cost, so product leaders rarely model it.
AI products break that assumption: every request has a real, variable cost in tokens,
and a heavy user can quietly cost more than they pay. The products that survive are the
ones whose leaders modeled unit economics *before* pricing, not after the margin alarm
went off. This skill does that modeling — honestly, with numbers — and turns it into a
pricing structure that holds up.

This is the leg of product thinking most teams skip: desirable and feasible, but not
**viable**. Treat it as first-class.

## How to run it

Gather the inputs, build the model, find the levers, then choose a pricing structure.
Show the arithmetic — a unit-economics claim no one can trace is worthless. Use
**Appendix A — Unit-economics model template** (end of this file) to structure the
numbers and **Appendix B — Pricing & cost-lever playbook** for the pricing patterns
and levers.

### Step 1 — Gather the cost drivers

For the core AI action(s), get real or estimated:

- **Tokens per request:** input (prompt + context + retrieved docs + history) and
  output. Context and chat history are the usual silent cost — measure them, don't
  guess.
- **Model & price:** which model, and its input/output token prices (they differ, often
  a lot; output is usually pricier). Confirm current prices from the provider.
- **Calls per task:** one call, or a chain/agent that makes several? Multiply.
- **Retries, tool calls, and failures** that still cost tokens.
- **Non-inference costs** that scale with usage: vector DB, embeddings, egress, human
  review.

### Step 2 — Build the unit-economics model

Roll costs up to the units that matter:

- **Cost per request** = (input tokens × input price) + (output tokens × output price),
  across all calls in the task.
- **Cost per active user** = cost per request × requests per user per period.
- **Cost per account** (for B2B) = sum across the account's users, including the
  heaviest users — model the *distribution*, not just the average, because usage is
  almost always long-tailed and the top few percent drive most of the cost.
- **Gross margin** = (price − AI cost − other variable cost) ÷ price. Compute it at the
  average *and* at the p90/p99 user, so you see where margin goes negative.

### Step 3 — Pull the cost levers

Before changing price, see how much margin you can engineer back. From
**Appendix B — Pricing & cost-lever playbook**:

- **Prompt caching** for stable context (system prompts, docs) — often a large,
  underused saving.
- **Model routing / cascade** — use a small cheap model for easy cases, escalate to a
  larger one only when needed.
- **Context & output discipline** — trim retrieved context, cap output length, avoid
  re-sending history.
- **Batching / async** where latency allows, for cheaper throughput.
- **Caching answers** to repeated queries.

Re-run the model after levers to get the realistic cost floor.

### Step 4 — Choose a pricing structure

Match how you charge to how cost is incurred, so margin is stable by design:

- **Per-seat** — simple and predictable for the buyer, but dangerous when usage varies
  wildly per seat; a few power users can break margin. Add fair-use limits.
- **Usage-based** — aligns revenue with cost; best when usage is spiky or unpredictable.
  Harder for buyers to forecast.
- **Outcome / value-based** — charge per resolved ticket, per document, per successful
  action. Strong story, best margin control, needs a clean definition of the outcome.
- **Hybrid** — a seat/platform base plus usage or outcome on top. Common for a reason:
  predictable floor, margin-safe ceiling.

Whatever the structure, build in guardrails: fair-use caps, rate limits, overage
pricing, and a plan for the abusive or runaway-cost user.

## Output

Produce (1) a filled unit-economics model showing cost per request / user / account and
gross margin at average and tail usage, (2) the lever analysis showing the realistic
cost floor, and (3) a pricing recommendation with the structure, the margin it
protects, and the guardrails. State assumptions explicitly and flag where real usage
data is needed to firm up the estimate — a model built on honest ranges beats a
precise-looking fiction.

## Honesty guardrails

- Always model the **tail**, not just the average user — that's where AI margin dies.
- Treat provider token prices as inputs to confirm, not memorized constants.
- If the honest answer is "at this price and usage, this loses money", say it. That
  finding *is* the value.

---

# Appendix A — Unit-economics model template

Copy this and fill every number or give an honest range.

# [Product / feature] — AI Unit Economics Model

> Fill every number or give an honest range. Show the arithmetic. Last updated: [date]

## Assumptions

- Model(s): [name] · Input price: [$ / 1M tokens] · Output price: [$ / 1M tokens]
  *(confirm current provider pricing)*
- Period for "active user": [day / month]

## 1. Cost per request

| Component | Tokens | Price / 1M | Cost |
|-----------|--------|-----------|------|
| Input (prompt + system) | | | |
| Input (retrieved context / RAG) | | | |
| Input (conversation history) | | | |
| Output | | | |
| Extra calls in the chain/agent (×N) | | | |
| **Total cost per request** | | | **$** |

Non-inference per-request cost (vector DB, embeddings, review): **$[ ]**

## 2. Cost per active user

| Input | Value |
|-------|-------|
| Requests per user per period | |
| Cost per request | $ |
| **Cost per active user / period** | **$** |

## 3. Cost distribution (model the tail)

| User segment | Requests / period | Cost / period |
|--------------|-------------------|---------------|
| Median (p50) | | $ |
| Heavy (p90) | | $ |
| Power (p99) | | $ |

## 4. Gross margin

| Scenario | Price to user | AI + variable cost | Gross margin % |
|----------|---------------|--------------------|----------------|
| Average user | $ | $ | % |
| p90 user | $ | $ | % |
| p99 user | $ | $ | % |

> If margin goes negative at p90/p99, that's the finding. Fix with levers (§5) or
> pricing structure/guardrails before launch.

## 5. After cost levers

| Lever | Applied? | Est. saving |
|-------|----------|-------------|
| Prompt caching (stable context) | | |
| Model routing / cascade | | |
| Context trimming / output cap | | |
| Answer caching | | |
| Batching / async | | |
| **Realistic cost floor per request** | | **$** |

## 6. Recommendation

- Pricing structure: [seat / usage / outcome / hybrid] — because…
- Margin it protects at the tail: [ ]
- Guardrails: [fair-use cap / rate limit / overage price / runaway-user plan]
- Where real usage data is still needed: [ ]

---

# Appendix B — Pricing & cost-lever playbook


## Part 1 — Cost levers (engineer margin back before touching price)

**Prompt caching.** If a large, stable block of context repeats across requests (system
prompt, policy docs, a knowledge base chunk), caching it can cut input cost
dramatically. Usually the single highest-ROI lever and the most overlooked. Identify
what's stable vs. per-request and cache the stable part.

**Model routing / cascade.** Not every request needs your biggest model. Route easy
cases to a small, cheap model and escalate to a larger one only when a confidence
check, classifier, or the task type demands it. Measure the quality impact with the
eval suite so routing doesn't silently degrade output.

**Context discipline.** Retrieval that dumps ten documents when two would do is pure
cost. Tune retrieval, rerank, and pass only what's needed. Cap conversation history;
summarize instead of re-sending it.

**Output limits.** Output tokens usually cost more than input. Cap max output, ask for
structured/terse responses where appropriate, and avoid "write me an essay" when a
sentence will do.

**Answer caching.** For repeated or near-duplicate queries, cache and reuse results.

**Batching / async.** Where latency allows, batch requests for cheaper throughput.

> After applying levers, re-run the unit-economics model to find the realistic cost
> floor. Only then reason about price.

## Part 2 — Pricing structures

| Structure | How it works | Best when | Margin risk | Guardrails |
|-----------|--------------|-----------|-------------|------------|
| **Per-seat** | Fixed price per user | Usage is uniform and predictable | A few power users break margin | Fair-use caps, tiered seats |
| **Usage-based** | Pay per token/request/action | Usage is spiky or unpredictable | Buyer hard to forecast; low floor | Minimums, prepaid credits |
| **Outcome / value** | Pay per resolved ticket, processed doc, successful action | The outcome is clean and attributable | Defining/attributing the outcome | Clear success definition, caps |
| **Hybrid** | Platform/seat base + usage or outcome on top | Most B2B AI products | Complexity for buyer | Predictable base + metered top |

## Part 3 — Principles

- **Price where value is felt, charge where cost is incurred.** The gap between those
  is your design problem; hybrid models exist to close it.
- **Protect the tail.** Margin that works on the average user and dies on the p99 user
  is a time bomb. Price and cap for the distribution.
- **Make cost a product decision, not just an infra one.** Caching, routing, and output
  limits are product/UX choices as much as engineering ones.
- **Re-check as models change.** Provider prices and model options shift; a model that
  was margin-negative can flip, and vice versa. Revisit the numbers on each major model
  or pricing change.
- **Instrument from day one.** You can't model the tail without per-user, per-request
  cost telemetry. Build it into the product early.
