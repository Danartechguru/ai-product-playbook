---
name: ai-search-optimization
description: >-
  Write and optimize content so it gets surfaced and cited by AI search — Google AI
  Overviews, ChatGPT, Claude, Perplexity, and Gemini — covering AEO (answer engine
  optimization), GEO (generative engine optimization), and modern SEO, and finishing
  with a human-first pass that strips the "AI slop" tells so the text reads like a
  person wrote it. Built for product managers and marketers writing communications,
  newsletters, announcements, blog posts, or articles. Use this whenever someone wants
  their content to show up in AI answers, get cited by an AI assistant, rank in AI
  Overviews, "be found by ChatGPT", do AEO/GEO/SEO, make a newsletter or article more
  discoverable, or make AI-assisted writing sound human and less like a chatbot.
  Trigger on "optimize for AI search", "get cited by AI", "AEO", "GEO", "AI SEO",
  "appear in AI Overviews", "make this sound human", or "remove the AI tone".
---

# AI Search Optimization (AEO · GEO · SEO) + Human-First Writing

Search is splitting in two. Classic search returns a list of links and rewards pages
that rank. AI search — Google's AI Overviews, ChatGPT, Claude, Perplexity, Gemini —
reads many sources, synthesizes one answer, and *cites a handful*. The win is no longer
"rank #1"; it's "be the passage the model quotes." That changes how you write.

Your job with this skill is to make a piece of content maximally **citable by machines
and trusted by humans at the same time** — and those two goals reinforce each other.
Thin, keyword-stuffed, AI-slop content loses on both fronts: readers bounce and models
increasingly discount it. Substantive, well-structured, human-sounding content wins on
both.

This is for people writing real things — a product announcement, a newsletter, a
customer email, a thought-leadership article — not for spamming the web. The guardrails
below are not optional garnish; they're what keeps the work honest and effective.

## The three acronyms, briefly

- **SEO** (Search Engine Optimization): being findable and ranking in classic search.
  Still the foundation — AI engines retrieve from the indexed, ranking web.
- **AEO** (Answer Engine Optimization): structuring content so an answer engine can
  lift a clean, direct answer from it — question-shaped, answer-first, self-contained.
- **GEO** (Generative Engine Optimization): the content-level moves that make a
  generative model actually *pick and cite your passage* — quotations, statistics,
  cited sources, fluency, specificity.

You don't choose between them. SEO gets you into the candidate pool; AEO makes you
extractable; GEO makes you the one that gets cited. Do all three, then humanize.

## Operating principles

- **Write the answer, then the article.** AI engines extract passages, not whole
  pages. Lead with a direct, complete answer; make every section stand on its own.
- **Earn the citation with substance.** The research is clear: real quotations, real
  statistics, and real cited sources are what move the needle (see Appendix A).
  Keyword stuffing actively hurts. There is no structural trick that substitutes for
  having something worth citing.
- **Be the most specific source in the room.** Models favor concrete numbers, named
  examples, dates, and primary sources over vague generalities.
- **Trust is a ranking signal.** Author identity, credentials, freshness, and
  third-party reputation decide whether a model treats you as quotable.
- **Human-first is not in tension with AI-first.** Fluent, specific, human prose is
  both more citable and more trusted. Slop is the enemy of both. Always finish with
  the humanize pass (Appendix D).
- **Never fabricate to "optimize."** Inventing a statistic, a quote, or a source to
  trigger the GEO levers is misinformation, it is a classic AI-writing tell, and it
  gets caught. Every number and quote must be real, accurate, and attributed.

## How to run it

Work through these in order. Steps 0–4 make the content citable; Step 5 makes it
human; Step 6 tells you whether it worked.

### Step 0 — Pin the question and the asker

AI search is question-driven. Before writing, name:
- **Who is asking** (the PM, the buyer, the exec) and **what they'd type or say** to an
  AI assistant — in natural, conversational phrasing, not keywords.
- **The intent:** are they comparing options, looking for a how-to, checking a fact,
  deciding whether to trust a vendor? The intent dictates the answer shape.
- Pull real questions from Google's "People Also Ask", support tickets, sales calls,
  and the prompts your audience actually sends AI tools.

### Step 1 — Structure for machine extraction (AEO)

- **Answer-first.** Open with a direct, complete answer in the first ~60–80 words that
  makes sense on its own, before any background. This is the single highest-leverage
  AEO move.
- **Self-contained sections.** Each H2/H3 should answer one sub-question and be
  understandable if lifted out alone — engines cite passages, not pages.
- **Question-shaped headings.** Phrase headings the way a person would ask the AI
  ("How much does X cost?", not "Pricing").
- **Scannable structure.** Use short paragraphs, bulleted and numbered lists, and
  tables where they genuinely clarify — these are easy for models to parse and reuse.
- **Depth where it counts.** Very thin content is rarely cited; information-dense
  pages that actually answer the question do far better. Length is not the goal —
  answer density is.

### Step 2 — Earn the citation (GEO)

Apply the moves the GEO research found most effective (ranked table in Appendix A).
In plain terms, add **real** substance:
- **Quotations** — the strongest lever. Quote a named expert, a primary document, or a
  customer, with attribution.
- **Statistics & data** — cite concrete numbers with their source and date.
- **Cited sources** — link and name primary sources (studies, official data, docs).
- **Fluency** — clear, well-constructed sentences; models prefer readable prose.
- **Precise, authoritative-but-specific language** — confident and exact, never vague
  or inflated. "Reduced onboarding time from 9 days to 2" beats "dramatically improved
  onboarding."
- **Skip keyword stuffing** — it measurably *lowers* citation odds.

### Step 3 — Signal trust and freshness (E-E-A-T)

- Show **experience and expertise**: first-person insight, original data, a real
  byline with linked credentials.
- Add **author identity** a machine can read (named byline, bio, and — on web pages —
  `Person` schema with `sameAs` links).
- Keep it **fresh**: update stats and examples, show a visible "last updated" date, and
  on web pages set `datePublished` / `dateModified`. Recency is a repeatedly observed
  citation driver.

### Step 4 — Build entity and off-page presence

AI models weight what *other* trusted sources say about you, not just your own page.
- Earn mentions on high-trust places your audience and the models both read: reputable
  media, industry publications, Wikipedia (where genuinely warranted), relevant
  communities (e.g. Reddit, forums), and review sites.
- Keep your name, role, and company details **consistent** everywhere — models build an
  entity profile from the consensus.
- Contribute real expertise to podcasts, expert roundups, and Q&A communities.

### Step 5 — Humanize (strip the AI slop)

Run the full draft through **Appendix D — Anti-AI-slop field guide**. This is
non-negotiable for content that goes out under a person's or brand's name. Lead-with-
the-answer structure plus heavy lists is exactly the shape that reads as "AI wrote
this", so the humanize pass matters *more* here, not less. Fix the strongest tells
(negative parallelisms, bold-label bullets, em-dash overuse, inflated significance,
vague attribution), restore concrete detail and a real voice, and keep natural
variation.

### Step 6 — Measure

- **Test the prompts.** Ask the real questions in ChatGPT, Claude, Perplexity, and
  Google AI Overviews and see whether you're mentioned or cited.
- **Track AI share of voice** against competitors over time (how often each brand is
  named/cited for your key questions).
- **Watch branded impressions** in Google Search Console (now includes AI surfaces) and
  referral traffic from AI tools. Treat visibility and citation — not just clicks — as
  the metric.

## Platform quick notes

Tune emphasis by where you want to show up (full cheat-sheet in Appendix C):
- **Google AI Overviews** — answer-dense passages, schema, freshness, primary-source
  citations; sections compete individually, and pages far outside the top 10 still get
  cited if the passage is best.
- **ChatGPT (search)** — authoritative domains, clean structure, recency for
  time-sensitive queries; cites a few sources.
- **Perplexity** — recent, directly-answering content; cites many sources, so niche and
  specific pages have a real shot.
- **Claude** — favors recognized expertise and third-party consensus; names orgs,
  papers, and frameworks in prose. Being the acknowledged authority matters more than
  on-page tricks.
- **Gemini** — entity and Knowledge-Graph driven; structured data, clear entity
  associations, and press coverage matter most.

## Format playbooks

See Appendix E for ready structures. Quick version:
- **Newsletter:** one clear question/promise in the subject and first line; a direct
  takeaway up top; one real stat or quote; a human aside; a single clear CTA.
- **Article / blog:** answer-first intro, self-contained H2s phrased as questions, a
  data point or quote per section, author byline + date, primary-source links.
- **Product communication / announcement:** lead with what changed and why it matters
  in one sentence; concrete before/after numbers; a named quote (customer or exec);
  plain language, no hype.

## Honesty guardrails

- **Real data only.** Never invent or misattribute a statistic or quotation to trigger
  the GEO levers. If you don't have a real one, say what you'd need or leave it out.
- **This field moves fast and is partly observational.** The percentages in Appendix A
  come from published research; much platform guidance is pattern-based, not confirmed
  by the engines. Treat specifics as directional and re-check periodically.
- **Don't optimize into slop.** If a "GEO move" makes the text robotic, the humanize
  pass wins. A human who trusts the piece is the point; the citation is the byproduct.
- **No manipulation.** Building fake reviews, sock-puppet mentions, or spam to fake
  entity consensus is out of scope and off-limits.

## Output

Deliver (1) the optimized piece — answer-first, well-structured, substantiated with
real quotes/stats/sources, trust-signaled, and run through the humanize pass; and
(2) a short optimization note: the target question(s), which GEO levers were used,
the schema/freshness/author signals added, and the prompts to test it against.

---

# Appendix A — The GEO method ranking (research-backed)

From *GEO: Generative Engine Optimization* (Aggarwal et al., arXiv:2311.09735) — the
foundational study that tested content-level optimizations against generative engines
and measured the change in visibility (Position-Adjusted Word Count) and a subjective
quality score, versus an unoptimized baseline.

| Rank | Method | Visibility (PAWC) | Quality impression | Use it as |
|---|---|---|---|---|
| 1 | Add **quotations** | +41% | +28% | Named expert / primary-doc / customer quotes |
| 2 | Add **statistics** | +31% | +23% | Concrete sourced numbers and data |
| 3 | **Fluency** optimization | +28% | +13% | Clear, well-constructed sentences |
| 4 | **Cite sources** | +27% | +13% | Named, linked primary sources |
| 5 | **Technical terms** | +18% | +11% | Precise domain vocabulary (where real) |
| 6 | **Easy-to-understand** | +14% | +6% | Plain, accessible phrasing |
| 7 | **Authoritative** tone | +10% | +19% | Confident, exact (not inflated) |
| 8 | **Unique words** | +6% | +6% | Specific, non-generic language |
| 9 | **Keyword stuffing** | **−8%** | +5% | ❌ Avoid — it lowers visibility |

Key takeaways:
- **Quotes, stats, and citations are the top levers** — and all three require *real*
  material. This is why "earn the citation" beats "trick the citation."
- **Keyword stuffing backfires.** The classic SEO reflex hurts in generative search.
- **Lower-ranked sources gain the most** from these moves (the study saw a rank-5
  source's visibility rise ~115% after adding citations) — good news for challengers.
- **Effectiveness varies by query type:** citations help most on factual queries,
  quotations on people/society and history, statistics on law/government and opinion,
  authoritative tone on debate. Match the lever to the question.
- **Combine levers** — fluency + statistics beat any single method in the study.

*Figures are from one 2023 study on then-current engines; treat as directional and
re-validate as engines change.*

---

# Appendix B — AI-search content checklist (pre-publish)

**Structure (AEO)**
- [ ] Direct, complete answer in the first ~60–80 words, readable on its own
- [ ] Each H2/H3 answers one sub-question and stands alone
- [ ] Headings phrased as real questions / natural queries
- [ ] Lists and tables used where they clarify; short paragraphs
- [ ] Answer density high (genuinely answers the question, not padded)

**Substance (GEO)**
- [ ] At least one real, attributed quotation
- [ ] At least one real, sourced statistic or data point
- [ ] Primary sources named and linked
- [ ] Specific numbers/examples instead of vague claims
- [ ] No keyword stuffing

**Trust (E-E-A-T)**
- [ ] Named author with real, linked credentials
- [ ] First-person experience or original data present
- [ ] Visible "last updated" date; content actually current
- [ ] Schema added (see Appendix F): FAQPage, Article w/ author + dates, HowTo if steps

**Entity / off-page**
- [ ] Brand/author name, role, company consistent with everywhere else
- [ ] A path to earn a mention on a trusted third-party source

**Human (anti-slop)**
- [ ] Run through Appendix D; strongest tells removed; real voice restored

**Measure**
- [ ] Target prompts written down and tested in 2+ AI engines
- [ ] Baseline AI share-of-voice noted for re-check

---

# Appendix C — Platform cheat-sheet

Observed patterns (not official algorithms; re-check over time).

| Platform | How it cites | Typical # sources | Favors | Your emphasis |
|---|---|---|---|---|
| **Google AI Overviews** | Inline links; sections compete | ~6–14 | Answer-dense passages, schema, freshness, primary sources; ranking ≠ inclusion | Answer-first sections, schema, inline sourced stats |
| **ChatGPT (search)** | Inline numbered refs w/ browsing | ~3–8 | Authoritative domains, clean structure, recency for time-sensitive | Authority + tight structure + up-to-date facts |
| **Perplexity** | Numbered, always clickable, throughout | ~5–15 | Recent, directly-answering content; broad source range | Specific, current, directly-answering pages (niche wins) |
| **Claude** | Rarely inline; names orgs/papers in prose | ~0–3 | Recognized expertise, third-party consensus, frameworks | Be the acknowledged authority; get named elsewhere |
| **Gemini** | Names brands in prose; source cards | ~2–6 | Entities, Knowledge Graph, structured data, press | Entity consistency, schema, earned press |

---

# Appendix D — Anti-AI-slop field guide (humanize pass)

Adapted from the patterns in Wikipedia's "Signs of AI writing." Use it to edit a draft
so it reads as human. **Don't strip every pattern mechanically** — over-sanitized text
reads stiff and, ironically, more artificial. Fix the strongest tells, restore concrete
detail and voice, keep natural variation.

**The tells (fix the top ones first):**

1. **Negative parallelism ("not just X, but Y").** The #1 tell. "It's not just a
   feature; it's a philosophy." Cut it or rewrite as a plain statement.
2. **Bullet points with bold lead-in labels** that restate the label
   (**Scalable:** It scales well.). The classic chatbot list shape — vary it, or write
   prose.
3. **Overused em dashes** — many per paragraph where a human would use commas or
   parentheses. Thin them out.
4. **Inflated significance.** "Stands as a testament to", "plays a vital role",
   "leaves a lasting impact", "watershed moment". Delete or replace with the specific
   fact.
5. **Promotional / brochure tone.** "Rich history", "breathtaking", "must-visit",
   "enduring legacy". Neutralize to concrete description.
6. **Editorializing.** "It's important to note", "it's worth noting", "no discussion
   would be complete without". Usually deletable.
7. **Overused transitions.** "Moreover", "furthermore", "on the other hand", several in
   a short span. Prune.
8. **Superficial "-ing" analysis.** Empty trailing clauses: "...ensuring success",
   "...highlighting its importance", "...solidifying its role". Cut — they add nothing.
9. **Vague attribution (weasel wording).** "Industry reports suggest", "experts say",
   "studies show" with no name. Name the source or remove the claim. (Doubly important
   here — fake authority is both a tell and dishonest.)
10. **Excessive boldface** mid-paragraph where a human wouldn't bold.
11. **Rule of three.** Reflexive triplets ("innovative, transformative, and
    groundbreaking"). Break the pattern.
12. **Generic filler / section-summary padding.** "In conclusion", "Overall", recap
    paragraphs that add nothing; specifics smoothed into statements that fit any topic.

**Humanize moves (what to add back):**
- Concrete specifics: real numbers, names, dates, a particular example.
- A genuine point of view or a small, honest aside.
- Varied sentence length and rhythm; the occasional short sentence.
- Plain words over inflated ones; cut adverbs and hedges.
- One detail only you (the author) would know.

**Caveat:** a tell is not proof of AI authorship — humans write this way too, and
AI-detector scores are unreliable. The goal here is prose that reads well and sounds
like the author, not passing a detector.

---

# Appendix E — Format playbooks (structures to fill)

## Newsletter issue
```
Subject: [the one question or promise, in the reader's words]
Opening line: [the takeaway, stated directly — no "Hope you're well"]
Body:
  - The answer / the point, up top
  - One real stat or quote that proves it (attributed)
  - Why it matters to this reader, specifically
  - A human aside or opinion (voice)
One CTA: [a single clear next step]
```

## Article / blog post
```
# [Question or clear promise as the title]
[Answer-first intro: complete answer in ~60–80 words]

## [Sub-question as H2]
[Direct answer, then one data point or quote with source]

## [Sub-question as H2]
[Self-contained; specific example]

## [Sub-question as H2]
...
Byline: [name + linked credentials] · Last updated: [date]
Sources: [named, linked primary sources]
(Schema: FAQPage + Article; HowTo if there are steps)
```

## Product announcement / communication
```
[What changed and why it matters — one sentence]
[Concrete before → after numbers]
"[Named quote: customer or exec]"
[What to do / where to learn more — plain language, no hype]
```

---

# Appendix F — Schema & structured-data quick reference

For web content, structured data helps machines parse and trust the page. Add in this
priority order:

1. **FAQPage** — for Q&A sections; maps directly to how answer engines extract.
2. **Article** — with `author` (→ `Person` with `sameAs` links), `datePublished`,
   `dateModified`, `headline`.
3. **HowTo** — for step-by-step/procedural content.
4. **Organization / Person** — to anchor your entity (consistent `name`, `url`,
   `sameAs` to profiles).

Supporting signals: a visible last-updated date for human readers, a real author bio,
internal links within a topic cluster (a pillar page plus supporting posts, each with
its own standalone answer), and canonical, crawlable, fast pages (classic SEO hygiene
still gets you into the retrieval pool).

*Emerging: some sites publish an `llms.txt` file (a Markdown index of key pages for
LLMs). Adoption and effect are still unproven — treat as low-cost experiment, not a
requirement.*
