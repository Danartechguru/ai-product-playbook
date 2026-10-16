---
name: enterprise-ai-security
description: >-
  Act as the executive security and compliance brain for an AI company — decide which
  frameworks to pursue and in what order (SOC 2, ISO/IEC 27001, ISO/IEC 42001, NIST CSF
  2.0, NIST AI RMF, NIS2, DORA), run a gap and risk assessment, threat-model an AI/LLM
  product against the OWASP Top 10 for LLMs, and build the trust story that unblocks
  enterprise deals (board briefings, trust center, security questionnaires). This is a
  CTO/CISO-level decision and advisory tool, not control memorization. Use whenever
  someone asks about enterprise security, security compliance, which certification to
  get, SOC 2 vs ISO 27001 vs ISO 42001, AI governance, AI/LLM security, threat modeling
  an AI product, NIST, NIS2, DORA, OWASP for LLMs, answering a security questionnaire,
  briefing a board on security, or making their company "enterprise-ready" and trusted.
  Trigger on "security framework", "which cert", "SOC 2", "ISO 27001", "ISO 42001",
  "NIST", "NIS2", "AI security", "secure our LLM", "security questionnaire", or "get
  enterprise-ready".
---

# Enterprise AI Security & Compliance (executive playbook)

For a CTO, CISO, or founder, security is not a cost center — it is a **trust asset that
unlocks revenue**. Enterprise and public-sector buyers won't sign until they trust you;
regulators (EU especially) now hold the *board personally accountable*. The executive job
is not to memorize controls. It is to make the calls: which frameworks, in what order,
at what cost, and how to turn the whole posture into a story a board, a customer, and an
auditor all believe.

This skill makes those calls — AI-first, because an AI company's threat surface and
obligations go beyond classic infosec. Treat it as a decision and advisory tool.

> **Not legal, audit, or certification advice.** This structures the decisions and points
> to primary sources; it does not replace a qualified CISO, auditor, or counsel, and it
> cannot issue or guarantee a certification. Frameworks, versions, and regulatory dates
> move fast — verify specifics against the official sources in **Appendix G**.

## Operating principles

- **Security is a sales enabler.** The point of a framework is usually to close a deal or
  satisfy a regulator — pick it for the *buyer and the risk*, not for the badge.
- **Aligned ≠ certified.** Be precise. "SOC 2 Type II", "ISO 27001 certified", and "ISO
  42001 aligned" mean very different things to a buyer. Never imply more than is true.
- **AI changes the surface.** Classic frameworks (ISO 27001, SOC 2) secure the environment;
  AI needs its own layer — AI governance (ISO 42001, NIST AI RMF) and AI threat modeling
  (OWASP Top 10 for LLMs). Do both.
- **Governance is now a board matter.** Under EU NIS2, management bodies are *personally
  liable* for cyber risk management. Security belongs on the board agenda, not just in IT.
- **Secure the AI, not just the perimeter.** The new attack surface is prompts, training
  data, embeddings, model supply chain, and over-empowered agents — not only networks.
- **Frameworks are means, not ends.** A certificate with weak real controls is security
  theater, and worse than honest gaps. Build the control, then claim it.

## How to run it

Diagnose first, then give the few decisions that matter most for *this* company.

### Step 0 — Scope the company and the exposure

Get these before advising; they change every recommendation:
- **What are you?** An AI *vendor* selling to enterprises, a company *deploying* AI
  internally, or both?
- **What does the AI do?** Assistive with human review, or does it make/materially
  influence *consequential* decisions (hiring, credit, insurance, health, safety)? This
  sets the governance bar.
- **What data does it touch?** Public, internal, personal/PII, special-category, regulated
  (financial, health)?
- **Who are your buyers, and where?** US enterprise, EU, regulated industries, public
  sector? Buyer geography and sector decide which frameworks actually unblock revenue.
- **What's the trigger?** A stalled deal, a security questionnaire, a regulator, a board
  ask, an incident? Start where the pain is.

### Step 1 — Choose the frameworks, and the order

The highest-leverage executive decision. Don't pursue everything at once. Use
**Appendix A — Framework cheat-sheet** and **Appendix B — Which framework, when**. The
short logic:
- **Selling to US enterprise?** SOC 2 Type II is usually the ticket to entry.
- **Selling internationally / to regulated or public sector?** ISO/IEC 27001 (certifiable
  ISMS) carries weight.
- **Your AI makes consequential decisions, or you want to lead on AI trust?** ISO/IEC
  42001 (AI management system) is the differentiator, and early certification is a
  procurement advantage as buyers shift from "aligned" to "certified".
- **US risk language / internal program?** NIST CSF 2.0 (security) and NIST AI RMF (AI
  risk) are the common vocabularies.
- **In-scope for EU regulation?** NIS2 (essential/important entities) and DORA (financial
  entities) are obligations, not choices — map them early; they shape contracts and carry
  personal board liability.

Common sequence for an AI-native vendor: **SOC 2 → ISO 42001 → ISO 27001**, layering as
deals and regulation demand. "SOC 2 + ISO 42001" clears most 2026 procurement; "ISO 27001
+ ISO 42001" is the mature benchmark.

### Step 2 — Run a gap and risk assessment

Turn the chosen frameworks into a prioritized roadmap, not a 200-control spreadsheet. Use
**Appendix C**. For each domain: current state, target, gap, effort, and the risk if left
open — then sequence by *risk reduced per unit of effort*, front-loading what unblocks the
nearest deal or the hardest regulatory deadline.

### Step 3 — Threat-model the AI product itself

This is the part classic security programs miss. Walk the **OWASP Top 10 for LLM
Applications (2025)** against your product and add agentic risks — see **Appendix D**.
Cover prompt injection, sensitive-information disclosure, data/model poisoning, supply
chain, improper output handling, excessive agency, system-prompt leakage, vector/embedding
weaknesses, misinformation, and unbounded consumption/cost. Decide mitigations and who
owns each.

### Step 4 — Build the trust story (close the deals)

A strong posture that no buyer can see wins nothing. Use **Appendix E**:
- **Board briefing** — posture, top risks, roadmap, and the one decision you need.
- **Trust center / security page** — certifications, subprocessors, data handling, DPAs,
  so buyers self-serve.
- **Security questionnaire machine** — the thing that actually blocks deals. Build a reused
  answer library and evidence set so a questionnaire is a one-day job, not a two-week fire
  drill.

### Step 5 — Operate and prove it

Security is continuous, and auditors and regulators want evidence. Use **Appendix F**:
continuous monitoring, an incident-response plan that meets **NIS2 timelines (24-hour early
warning, 72-hour notification, one-month final report)**, ongoing evidence collection, and
the annual surveillance / renewal cadence (SOC 2 annually; ISO certs are three-year with
yearly surveillance).

## Talking to each audience

Same posture, different language:
- **Board:** risk, liability, revenue unblocked, and the decision you need. One page.
- **Customers / sales:** certifications held, data handling, and "yes we can answer your
  questionnaire" — trust, not jargon.
- **Auditors:** evidence, control ownership, and consistency over the observation period.
- **Engineers:** concrete controls, threat models, and guardrails they can build.

## Honesty guardrails

- **Never fabricate controls, evidence, or certification status.** A false "SOC 2
  compliant" claim is a misrepresentation that can sink a deal and worse.
- **Aligned, in progress, and certified are different words — use the true one.**
- **Don't design security theater.** A control that exists only on paper is a liability.
- **Regulatory specifics change and vary by country.** Treat obligations and dates as
  orientation; confirm against Appendix G and qualified counsel.

## Output

Deliver a short, prioritized **security & compliance plan**: the recommended frameworks and
sequence (with the reason), the gap/risk roadmap, the AI threat-model summary with owners,
and the trust narrative (board one-pager + questionnaire-ready control summary). Keep it to
decisions and next actions a board and a security reviewer can both act on.

---

# Appendix A — Framework cheat-sheet

Who requires it, what it certifies, and whether it's AI-specific. Verify current versions
in Appendix G.

| Framework | What it is | Certifiable? | AI-specific? | Who asks for it |
|---|---|---|---|---|
| **SOC 2 (Type II)** | Attestation that security controls *operated effectively* over 6–12 months (AICPA Trust Services Criteria: Security + optional Availability, Confidentiality, Processing Integrity, Privacy) | Attestation report (not a cert) | No | US enterprise buyers, SaaS procurement |
| **ISO/IEC 27001:2022** | Certifiable information security management system (ISMS); risk-based, Annex A controls | Yes (3-yr + annual surveillance) | No | International, regulated, public-sector buyers |
| **ISO/IEC 42001:2023** | Certifiable **AI management system** — AI policy, executive accountability, AI system inventory + risk classification, AI impact assessments, data governance, lifecycle controls | Yes (3-yr + annual surveillance) | **Yes** | Buyers whose AI makes consequential decisions; AI-trust leaders |
| **NIST CSF 2.0** (2024) | Voluntary cyber risk framework. Six functions: **Govern, Identify, Protect, Detect, Respond, Recover** (Govern added in 2.0) | No (framework) | No | US orgs, internal program backbone |
| **NIST AI RMF 1.0** (2023) | Voluntary AI risk framework. Functions: **Govern, Map, Measure, Manage** | No (framework) | **Yes** | US AI risk programs; pairs with CSF |
| **NIS2** (EU 2022/2555) | EU cybersecurity law for **essential / important entities** across critical sectors; risk mgmt, incident reporting, supply chain, **personal board liability** | Legal obligation | No | EU in-scope entities (not optional) |
| **DORA** (EU 2022/2554) | EU digital operational resilience for **financial entities**; ICT risk, third-party register, resilience testing, incident reporting | Legal obligation | No | EU financial sector (not optional) |
| **OWASP Top 10 for LLMs (2025)** | Community threat list for LLM/GenAI apps | No (threat model) | **Yes** | Security reviewers; your own threat modeling |

---

# Appendix B — Which framework, when (decision logic)

Ask in this order; stop pursuing more than the buyers and regulators require.

1. **Are you legally in scope for EU rules?** → NIS2 (essential/important entity in a
   covered sector) and/or DORA (financial entity) are *obligations*. Map them first — they
   carry board liability and shape contracts.
2. **Who must say yes to buy?** 
   - US enterprise security reviews → **SOC 2 Type II** first.
   - International / regulated / public sector → add **ISO/IEC 27001**.
3. **What does your AI do?**
   - Makes or materially influences consequential decisions, or you want to lead on AI
     trust → **ISO/IEC 42001** (and align to **EU AI Act** — see the companion
     `enterprise-ai-adoption-eu` skill).
   - Assistive with human review → 42001 can wait; prioritize SOC 2 / 27001.
4. **Need a shared internal risk language?** → **NIST CSF 2.0** (security) + **NIST AI
   RMF** (AI). They don't certify, but they structure the program and map to the above.
5. **Always, regardless of certs:** threat-model the product with **OWASP Top 10 for
   LLMs** (Appendix D). A cert proves process; the threat model proves the product is safe.

Sequencing heuristic: do the one that unblocks the **nearest revenue** or the **hardest
legal deadline** first; layer the rest as a roadmap.

---

# Appendix C — Gap assessment & roadmap template

```
Company: [ ] · Target frameworks: [ ] · Owner: [ ] · Date: [ ]

| Domain (map to chosen framework) | Current state | Target | Gap | Effort (S/M/L) | Risk if open | Priority |
|----------------------------------|---------------|--------|-----|----------------|--------------|----------|
| Governance & policy              |               |        |     |                |              |          |
| Access control & identity        |               |        |     |                |              |          |
| Data protection & encryption     |               |        |     |                |              |          |
| AI governance (inventory, impact)|               |        |     |                |              |          |
| AI/LLM product security (OWASP)  |               |        |     |                |              |          |
| Supply chain / third-party       |               |        |     |                |              |          |
| Logging, monitoring, detection   |               |        |     |                |              |          |
| Incident response & BCP/DR       |               |        |     |                |              |          |
| Vendor/subprocessor management   |               |        |     |                |              |          |

Sequenced roadmap: Now (unblocks nearest deal / deadline) → Next → Later
Each item: owner, effort, evidence it produces.
```

---

# Appendix D — AI/LLM threat model: OWASP Top 10 for LLMs (2025)

Walk each against your product; decide a mitigation and an owner. (Codes per the OWASP
GenAI Security Project 2025 list — confirm current wording in Appendix G.)

| Code | Risk | Typical mitigation |
|---|---|---|
| **LLM01** | Prompt Injection | Input/output boundaries, instruction hierarchy, allow-listing, treat retrieved/3rd-party content as untrusted |
| **LLM02** | Sensitive Information Disclosure | Data minimization, output filtering, no secrets in prompts, PII scrubbing |
| **LLM03** | Supply Chain | Vet models/datasets/plugins, pin & verify, SBOM for the AI stack |
| **LLM04** | Data & Model Poisoning | Source/validate training & fine-tune data, provenance, anomaly checks |
| **LLM05** | Improper Output Handling | Treat model output as untrusted; encode/validate before downstream use (stops XSS/SQLi/RCE) |
| **LLM06** | Excessive Agency | Least-privilege tools, human-in-the-loop for high-impact actions, scoped permissions |
| **LLM07** | System Prompt Leakage | Don't put secrets/authz logic in the system prompt; assume it can leak |
| **LLM08** | Vector & Embedding Weaknesses | Secure the RAG store, access-control embeddings, guard against injection via retrieved docs |
| **LLM09** | Misinformation | Grounding, citations, evals, human review where the cost of wrong is high |
| **LLM10** | Unbounded Consumption | Rate limits, quotas, cost caps, abuse detection (protects availability *and* margin) |

Agentic additions: constrain tool scope, sandbox actions, log and review agent decisions,
and define a kill switch.

---

# Appendix E — Trust-story toolkit

## Board security briefing (one page)
```
1. Posture in one line: where we stand vs. where buyers/regulators expect us.
2. Top 3 risks (likelihood × impact), in business terms.
3. The roadmap: Now / Next / Later, with cost and what each unblocks.
4. Liability & regulatory exposure (NIS2/DORA if in scope) — plainly.
5. The one decision I need from the board today.
```

## Trust center / security page checklist
- Certifications/attestations held (with precise status: certified vs. in progress)
- Data handling: residency, encryption, retention, subprocessors, DPA availability
- AI specifics: what data trains/doesn't train models, human oversight, AI governance
- Security contact / responsible disclosure; status page

## Security questionnaire machine (the deal-unblocker)
- Maintain a **reusable answer library** mapped to common frameworks (SOC 2, ISO, CAIQ/SIG).
- Keep an **evidence set** ready (policies, diagrams, pen-test summary, cert letters).
- Assign an owner; target a 1-day turnaround. Slow questionnaires lose deals.
- Never overstate — a questionnaire answer is a contractual representation.

---

# Appendix F — Incident response & reporting quick reference

- **Have a plan before you need it:** roles, severity levels, comms tree, evidence capture,
  and a decision log.
- **NIS2 reporting timeline (in-scope EU entities):** 24-hour early warning → 72-hour
  notification (with impact assessment) → interim report on request → **final report within
  one month**. (Confirm national transposition — it varies by country.)
- **DORA (financial entities):** major ICT-incident classification and reporting on its own
  timeline; maintain the register of information for ICT third parties.
- **Board accountability:** under NIS2 Article 20, management bodies are personally liable
  for cyber risk management — brief and involve them.
- **After resolution:** blameless postmortem, root cause, and feed fixes back into the
  roadmap and evidence set.

---

# Appendix G — Official sources (verify current versions here)

Frameworks, versions, and legal dates change — confirm before committing or claiming.
- **NIST CSF 2.0** & **AI RMF**: https://www.nist.gov/cyberframework and https://www.nist.gov/itl/ai-risk-management-framework
- **ISO/IEC 27001, 27002, 42001**: https://www.iso.org (search the standard number)
- **SOC 2 / Trust Services Criteria**: https://www.aicpa-cima.com (AICPA)
- **OWASP Top 10 for LLM Applications / GenAI Security Project**: https://genai.owasp.org
- **NIS2 (Directive (EU) 2022/2555)** & **DORA (Regulation (EU) 2022/2554)**: https://eur-lex.europa.eu; EU cyber agency guidance at https://www.enisa.europa.eu
- **EU AI Act** (overlaps governance): https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai

*This skill is orientation and decision support, not a substitute for a qualified CISO,
auditor, or legal counsel.*
