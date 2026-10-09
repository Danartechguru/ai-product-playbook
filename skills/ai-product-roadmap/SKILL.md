---
name: ai-product-roadmap
description: >-
  Turn a raw AI product idea into a phased, agile roadmap by running a tough-love
  interview that pressure-tests assumptions across product, users, technical
  architecture, infrastructure, and AI evaluation — then breaks the idea into thin,
  shippable phases with a measurable eval plan. Use this whenever someone wants to
  plan, scope, sequence, de-risk, or sanity-check an AI or LLM product or feature:
  when they have an idea but no plan, when they ask for a roadmap, phasing, a
  discovery or validation plan, an AI eval strategy, or a roadmap template, or when
  they say things like "help me plan my AI product", "what should my roadmap look
  like", or "how do I take this from idea to launch". Trigger even if they don't use
  the word "roadmap".
---

# AI Product Roadmap

Most AI roadmaps fail the same way: they are a wish-list of features with dates
attached, built on untested assumptions, with no plan for whether the AI is
actually good enough to ship. Your job with this skill is **not** to fill in a
pretty template. It is to be the sharp, slightly uncomfortable thinking partner a
good Chief Product Officer would be — the one who asks the question everyone in the
room is avoiding, *then* turns the answers into a roadmap that survives contact with
reality.

Work through this as a conversation, not a form. Ask, listen, push back, and only
produce the artifact once the thinking is sound.

## Operating principles

- **Interrogate before you organize.** A roadmap is a *consequence* of good
  decisions, not a substitute for them. Spend most of the effort on the interview.
- **Separate desirability, viability, and feasibility.** A feature can be loved,
  buildable, and still lose money on every call. Hold all three lenses at once.
- **Thin vertical slices beat big phases.** Each phase should ship something a real
  user touches end-to-end, not "the backend" followed later by "the UI".
- **The model is a dependency, not a given.** Treat "the AI is good enough" as a
  hypothesis that must be *evaluated*, with a number, before it anchors a launch.
- **Name the non-goals.** What you refuse to build this quarter is as much a part of
  the roadmap as what you commit to.
- **Challenge with care.** Push hard on ideas, stay warm with the person. The goal
  is a better product, not to win the argument.

## How to run it

Move through the phases below in order. Don't dump every question at once — ask a
few, react to the answers, and follow the thread where it's weakest. If the person
is vague or hand-waves a hard question, that is exactly the spot to slow down and
dig in. Summarize what you heard before moving on, so gaps become visible.

### Phase 0 — Frame the bet

Before anything else, get crisp answers to these. If any are fuzzy, the roadmap is
premature.

- What specific problem does this solve, for whom, and how do they solve it today?
- Why is an AI/LLM the right tool here — what makes a deterministic solution
  insufficient?
- Why now? What changed (model capability, cost, regulation, distribution)?
- What does "this worked" look like in one sentence and one metric?
- If this fails, what is the most likely reason? (Write it down — you'll test it.)

### Phase 1 — Interrogate across five lenses

Pressure-test the idea through each lens. The sample questions are starting points;
the real skill is following the weakest answer. See **Appendix A — Interview bank** (end of this file) for the
full question bank organized by lens and by product maturity.

**1. Problem & product**
- Who feels this pain most acutely, and would they pay (in money or attention)?
- What is the smallest version that still delivers the core value?
- What are you *not* building, and who will be upset about that?

**2. Users & adoption**
- What does the user have to stop doing to adopt this? What's the switching cost?
- How will they build trust in an output that is sometimes wrong?
- What's the "aha" moment, and how many steps until they reach it?

**3. Technical & architecture**
- Single model call, a chain, or agentic? What forces that choice?
- Build on an API, fine-tune, or RAG — and what evidence supports that, not vibes?
- Where does latency live, and what's the acceptable ceiling for this use case?
- What is the fallback when the model fails, times out, or returns garbage?

**4. Infrastructure, data & compliance**
- Where does the data live, where is it processed, and who can see it?
- What are the data-residency, privacy, or regulatory constraints (e.g. EU/GDPR)?
- How will you handle logging, evals data, and PII without creating a liability?
- What's the plan for versioning prompts, models, and datasets?

**5. AI evaluation & risk**
- How will you *measure* whether the AI is good enough — before users do?
- What's the cost of a wrong answer here: annoying, expensive, or dangerous?
- What are the failure modes (hallucination, bias, jailbreak, drift) and which
  actually matter for this product?

### Phase 2 — Shape into bets

Convert the interview into a short list of **bets**: outcome-oriented statements of
what you believe and what you'll do about it. For each bet, capture the hypothesis,
the riskiest assumption, and how a phase will test it. Explicitly list **non-goals**.

### Phase 3 — Phase it (crawl → walk → run)

Sequence the bets into phases by *risk retired per unit of effort*. Put the scariest
assumption in the earliest phase a thin slice can test it. Use a Now / Next / Later
structure. Each phase states: the goal, the thin slice that ships, the assumption it
de-risks, and the exit criteria (including the AI eval bar) to move on.

### Phase 4 — Build the AI eval plan

This is the part most roadmaps skip and most products die without. For each phase,
define what "good enough" means as a number and how you'll measure it. Use
**Appendix C — AI eval plan template**. At minimum: the task, the eval method
(golden set, LLM-as-judge, human review, A/B), the metric and threshold, and what
happens if it's missed.

### Phase 5 — Produce the roadmap artifact

Only now, assemble the roadmap using **Appendix B — Roadmap template**. Fill it from
the interview — never with generic filler. If a section has no real content yet, say
so and note what's needed to fill it, rather than inventing it.

## Red flags to call out

When you hear these, name them kindly but clearly — they're where AI products go to
die:

- "The model will figure it out" with no eval plan.
- A roadmap that ships infrastructure for months before any user sees value.
- No answer for what happens when the AI is wrong.
- Success measured only by usage, never by whether the output was *correct*.
- Compliance treated as a final-phase checkbox rather than a Phase 0 constraint.
- Unit economics unexamined — see the companion `ai-unit-economics` skill.

## Output

The deliverables are (1) a filled roadmap from the template and (2) an AI eval plan.
Keep them tight and specific to this product. A roadmap a recruiter or exec reads
should make the *thinking* visible: the bets, the risks, and how each phase buys down
uncertainty — not just boxes on a timeline.

---

# Appendix A — Interview bank


A deeper set of questions to draw from during the interview. Pick the ones that
target the weakest part of the current idea — don't ask all of them. Questions are
grouped by lens and tagged by product maturity: `[0→1]` for brand-new ideas, `[scale]`
for existing products being extended.

## 1. Problem & product

- What is the job the user is hiring this product to do? `[0→1]`
- Describe the last time someone actually hit this problem. What did they do? `[0→1]`
- If you could only ship one capability, which one justifies the product's existence?
- What's the cheapest possible test that this problem is worth solving? `[0→1]`
- Who is this explicitly *not* for?
- What would make a user churn in week one? `[scale]`
- Which existing workflow does this replace, and is it 10x better or 10% better?

## 2. Users & adoption

- What does the user have to believe to trust this output?
- How many of your users can tolerate a wrong answer, and how many can't?
- What's the onboarding moment where they first see value, and how long to get there?
- Who in the org has to say yes for this to be adopted (user, manager, security, legal)?
- What's the manual fallback when the user doesn't trust the AI yet?
- How will you teach users what the AI is good and bad at? `[scale]`

## 3. Technical & architecture

- Is this one model call, a prompt chain, retrieval-augmented, or an agent? Why?
- What evidence do you have that fine-tuning beats prompting + RAG for this? `[scale]`
- What context does the model need, and how does it get there reliably?
- What's your p95 latency budget, and what breaks if you exceed it?
- How do you handle partial failure, timeouts, and rate limits gracefully?
- What's your strategy for prompt/version management as the product evolves?
- Where's the human in the loop, and can they realistically keep up at scale?
- What happens to quality when the input is adversarial or out of distribution?

## 4. Infrastructure, data & compliance

- Where is data stored and processed, and does that satisfy your users' constraints?
- What are the residency, privacy, and retention requirements (e.g. EU/GDPR)?
- Do you need zero-data-retention or a signed DPA with your model provider?
- How do you collect eval and training data without creating PII liabilities?
- What's your plan for model/prompt/dataset versioning and reproducibility?
- What's the audit trail when a regulator or customer asks "why did it say that"?
- See the companion `enterprise-ai-coach-claude` skill for EU deployment specifics.

## 5. AI evaluation & risk

- How do you know the AI is good enough *before* a user tells you it isn't?
- What's your golden set, and who curates it?
- Is LLM-as-judge appropriate here, or do you need human review / ground truth?
- What's the cost asymmetry of false positives vs. false negatives?
- Which failure modes actually matter: hallucination, bias, jailbreak, drift, leakage?
- How will you detect quality regression when you change a prompt or model version?
- What's your red-team plan, and who owns it?

## Follow-the-weakest-answer heuristic

When an answer is confident and specific, move on. When it's vague ("we'll figure
that out", "the model handles it", "it should be fine"), stop and dig — that vagueness
is usually hiding the risk that will sink the project. Name it, then help the person
turn it into either a real answer or an explicit assumption to test in an early phase.

---

# Appendix B — Roadmap template

Copy this and fill it from the interview. Don't use generic filler.

# [Product name] — AI Product Roadmap

> One-line description of what this is and for whom.
> Owner: [name] · Last updated: [date] · Status: [draft / in review / committed]

## 1. The bet in one paragraph

What we believe, who it's for, why now, and what success looks like — in plain
language, no jargon. If you can't write this clearly, the roadmap isn't ready.

## 2. Success metric

The single number that tells us this worked, plus its current baseline and target.

| Metric | Baseline | Target | By when |
|--------|----------|--------|---------|
|        |          |        |         |

## 3. Bets & assumptions

For each bet: what we believe, the riskiest assumption, and the phase that tests it.

| Bet | Riskiest assumption | Tested in |
|-----|---------------------|-----------|
|     |                     |           |

## 4. Non-goals (this cycle)

- What we are deliberately not building, and why.

## 5. Phases

### Now — [phase name]
- **Goal:**
- **Thin slice that ships:** (a real, end-to-end thing a user touches)
- **Assumption it de-risks:**
- **AI eval bar to exit:** (see eval plan)
- **Exit criteria:**

### Next — [phase name]
- **Goal:**
- **Thin slice that ships:**
- **Assumption it de-risks:**
- **AI eval bar to exit:**
- **Exit criteria:**

### Later — [phase name]
- **Goal:**
- **What has to be true to start:**

## 6. Technical & infrastructure track

Run alongside the phases, not before them.

- **Architecture:** (single call / chain / RAG / agentic — and why)
- **Model & provider strategy:** (API, fine-tune, routing; EU/residency constraints)
- **Data & compliance:** (storage, processing location, DPA/retention, audit trail)
- **Observability:** (logging, eval data capture, versioning of prompts/models)
- **Fallbacks:** (what happens when the AI fails)

## 7. Key risks & how we're buying them down

| Risk | Likelihood | Impact | Mitigation / phase |
|------|-----------|--------|--------------------|

## 8. Open questions

- Questions that must be answered before the relevant phase starts.

---

# Appendix C — AI eval plan template

# [Product name] — AI Evaluation Plan

> The point of this document: define what "good enough" means as a number, for each
> phase, *before* users do it for us. An AI feature without an eval bar is a guess.

## Eval philosophy for this product

- **Cost of a wrong answer:** [annoying / expensive / dangerous] — this determines
  how strict the bar is and whether a human must stay in the loop.
- **Ground truth availability:** [have labeled data / can create golden set / subjective]
- **Primary eval method:** [golden set + exact/semantic match / LLM-as-judge / human
  review / online A/B] — and why it fits this task.

## Eval suite

| # | Task / capability | Method | Metric | Threshold | On miss |
|---|-------------------|--------|--------|-----------|---------|
| 1 |                   |        |        |           |         |
| 2 |                   |        |        |           |         |

*Method examples: golden-set accuracy, LLM-as-judge with rubric, human spot-check at
N%, pairwise preference, groundedness/citation check, refusal-rate on red-team set.*

## Per-phase eval bars

| Phase | Must hit before exit |
|-------|----------------------|
| Now   |                      |
| Next  |                      |

## Regression & drift

- **When we change a prompt or model version:** rerun the golden set; block release
  if any threshold drops by more than [X].
- **In production:** sample [N%] of outputs for ongoing human/LLM review; alert on
  [metric] moving beyond [band].

## Red-team / safety set

- Adversarial inputs we test against (jailbreaks, PII probes, out-of-scope requests):
- Who owns it and how often it runs:

## Golden set

- **Size & source:**
- **Who curates it and how it grows:**
- **How we avoid it going stale:**
