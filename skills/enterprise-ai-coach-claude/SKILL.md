---
name: enterprise-ai-coach-claude
description: >-
  Coach an EU-based organization through adopting Anthropic's Claude in production
  the compliant way — translating GDPR, Data Processing Agreements (DPA / SCCs), the
  EU AI Act, and (for financial entities) DORA into concrete, prioritized steps, and
  helping choose the right deployment path (Anthropic API, Amazon Bedrock, Google
  Vertex AI, or Microsoft Foundry on Azure) for data residency and risk. Use this
  whenever someone wants to roll out, pilot, procure, or get sign-off for Claude in a
  company — especially in the EU — or asks about GDPR, DPA, data residency, zero data
  retention, EU AI Act, DORA, Bedrock vs Vertex vs Azure/Foundry, security review, or
  how to get legal and security to approve Claude. Trigger even when they just say
  "we want to use Claude at work" or "how do we deploy Claude for the company".
---

# Enterprise AI Coach for Claude (EU focus)

Getting Claude into a European enterprise rarely fails on the technology. It fails on
the questions legal, security, and procurement ask *after* the pilot is already live:
Where is the data processed? Is there a signed DPA? Does this fall under the EU AI
Act? What happens to our prompts? Your job with this skill is to get ahead of those
questions — to help the organization adopt Claude deliberately, with the compliance
work sequenced *before* it becomes a blocker.

> **Important — not legal advice.** This skill structures the work and points to
> primary sources; it does not replace qualified legal or data-protection counsel.
> Compliance depends on the organization's role, data, and jurisdiction. Always
> verify specifics against the official sources in **Appendix D — Official sources**
> (end of this file) and have the organization's DPO or counsel sign off.

## How to run it

Start by understanding the situation, then work through the five workstreams below in
roughly this order. Don't lecture — diagnose first, then give the few next actions
that matter most for *this* organization.

### Step 0 — Scope the adoption

Get these before giving advice; they change almost every recommendation:

- **What will Claude actually do?** (internal productivity, a customer-facing feature,
  automated decisions, code, document processing?)
- **What data will it touch?** (public, internal, personal/PII, special-category,
  trade secrets?)
- **Who are the users, and what's the blast radius if it's wrong?**
- **Sector & regime:** general GDPR, financial services (DORA), health, public sector?
- **Where must data be processed/stored?** (EU-only? specific country?)
- **What's the buying surface?** (a Claude plan, or Claude via a cloud they already use?)

### The five workstreams

**1. Choose the deployment path.** The single most consequential decision for EU
compliance. The four paths — Anthropic API/first-party plans, Amazon Bedrock, Google
Vertex AI, and Microsoft Foundry (Azure) — differ on data residency, existing vendor
relationships, and procurement. Walk through the trade-offs with
**Appendix A — Deployment paths**. Rule of thumb: if the org already runs on AWS,
Google Cloud, or Azure and needs EU data processing, deploying Claude through that
same cloud's EU regions usually clears the fastest compliance path, because the
existing cloud DPA and security posture extend to it.

**2. Get the data-protection foundation in place.** This is what makes a pilot
legitimate rather than shadow IT. Work through **Appendix B — GDPR readiness checklist**:
controller/processor roles, a signed DPA with Standard Contractual Clauses, a
transfer impact assessment (the organization's own responsibility), data
minimization, retention and logging policy, and whether zero-data-retention is needed.
Confirm the provider's training policy in writing — Anthropic does not train its
models on commercial or API customer data by default, which is usually a key reassurance
for legal, but verify the current terms via the official sources.

**3. Classify under the EU AI Act.** Determine the risk tier of the *use case*
(prohibited / high-risk / limited / minimal) and what obligations follow — transparency,
human oversight, documentation. Most internal productivity uses are minimal/limited
risk; decisions affecting people's rights, employment, credit, or safety can be
high-risk and carry real obligations. Use **Appendix C — EU AI Act**.

**4. Add sector overlays.** For financial entities, DORA adds ICT third-party risk,
register-of-information, and exit-plan requirements on top of GDPR. Health, public
sector, and others have their own. Flag these early — they shape contracts.

**5. Plan the rollout & governance.** Pilot scope, an acceptable-use / AI policy for
employees, human-in-the-loop where it matters, logging and audit trail, an incident
path, and an owner. Adoption without a lightweight AI policy is how "shadow AI" starts.

## Output

Produce a short, prioritized **adoption plan**: the recommended deployment path with
the reason, the compliance gaps that must close before go-live (and who owns each),
the EU AI Act classification, any sector overlays, and the pilot plan. Keep it to the
decisions and the next actions — a document legal and security can actually act on,
not a wall of theory. End by pointing to the official sources and recommending DPO /
counsel sign-off on anything that constitutes a legal determination.

## Honesty guardrails

- Never state a compliance *conclusion* as settled fact ("this is GDPR-compliant").
  Frame it as "here's what's required and where you stand", and defer legal
  determinations to counsel.
- If the org wants Claude for a use that looks prohibited or high-risk under the AI
  Act, say so plainly and early.
- Keep provider facts (regions, training policy, retention) tied to the official
  sources, since these change — don't rely on memory for specifics.

---

# Appendix A — Deployment paths


Four ways to run Claude in production. They differ mostly on **where data is
processed**, **which vendor contract governs it**, and **how procurement and security
review go**. Verify current regions and terms against `official-sources.md` — these
change often.

## The four paths

### 1. Anthropic API / first-party plans (Team, Enterprise, API)
- Direct relationship with Anthropic; fastest to start; newest models first.
- Anthropic offers a **DPA with Standard Contractual Clauses** and, for API,
  **zero-data-retention** arrangements on request.
- Best when: you want the direct relationship, the latest capabilities, or you don't
  already standardize on one hyperscaler.
- Watch: confirm processing location and transfer mechanism for your data.

### 2. Amazon Bedrock (AWS)
- Claude runs inside your AWS account and chosen **AWS region**, including EU regions
  (e.g. Frankfurt / `eu-central-1`, Paris, Ireland — confirm current model/region
  availability).
- Governed by your existing **AWS DPA** and security posture.
- Best when: you're already on AWS and need EU data processing under a contract you
  already have.

### 3. Google Vertex AI (Google Cloud)
- Claude available through Vertex AI in Google Cloud, including **EU regions**
  (`europe-west*` — confirm current availability).
- Governed by your existing **Google Cloud DPA**.
- Best when: you're already on Google Cloud.

### 4. Microsoft Foundry on Azure
- Anthropic's Claude models became **generally available in Microsoft Foundry (Azure)
  in 2026**, so "the Azure route" is real — route Claude through Azure with EU region
  options and your existing **Microsoft DPA**.
- Best when: you're a Microsoft/Azure shop and want Claude under your existing Azure
  agreements and security review.

## Decision heuristic

1. **Do you have a hard EU-only data-processing requirement?** → Pick the path whose
   EU regions cover the models you need, and pin the region explicitly.
2. **Which cloud are you already on?** → Deploying Claude through that same cloud
   usually extends an already-approved DPA and security review — the fastest path to
   sign-off. If the org is on Azure, Microsoft Foundry is now a first-class option;
   if on AWS, Bedrock; if on GCP, Vertex.
3. **Do you want the newest models the day they ship, or the direct relationship?** →
   Anthropic first-party often leads on model availability.
4. **Do you need zero-data-retention or special contractual terms?** → Check which
   path offers it for your data and get it in writing.

## Comparison at a glance

| | Anthropic 1st-party | Bedrock (AWS) | Vertex (GCP) | Foundry (Azure) |
|---|---|---|---|---|
| Governing contract | Anthropic DPA + SCCs | AWS DPA | Google Cloud DPA | Microsoft DPA |
| EU regions | Verify | Yes (confirm model/region) | Yes (confirm model/region) | Yes (confirm model/region) |
| Fastest if you're on… | No cloud lock-in | AWS | Google Cloud | Azure |
| Newest models first | Usually | Follows | Follows | Follows |

*Regions, model availability, and contractual terms change — always confirm against
the official sources before committing.*

---

# Appendix B — GDPR readiness checklist


Work through these with the organization. This is a structuring aid, **not legal
advice** — the DPO or counsel owns the final determinations. Verify provider specifics
against `official-sources.md`.

## Roles & contracts

- [ ] **Determine controller / processor roles.** Usually the organization is the
      controller; the model provider (or cloud) is a processor. Get this right — it
      drives every obligation below.
- [ ] **Sign a DPA.** Anthropic publishes a Data Processing Addendum incorporating
      **Standard Contractual Clauses** for international transfers. If deploying via a
      cloud (Bedrock/Vertex/Foundry), the relevant cloud DPA typically governs.
- [ ] **Confirm the transfer mechanism** (SCCs and any supplementary measures) if data
      leaves the EEA.

## Data

- [ ] **Data minimization.** Send the model only what the task needs; strip or
      pseudonymize PII where possible.
- [ ] **Lawful basis** identified for any personal data processed.
- [ ] **Data residency / processing location** chosen and pinned (region selection on
      Bedrock/Vertex/Foundry; confirmed processing location on first-party).
- [ ] **Retention policy.** Decide how long prompts/outputs are kept; consider
      **zero-data-retention** (available for the Anthropic API on request) for
      sensitive workloads.
- [ ] **Training policy confirmed in writing.** Anthropic does not train its models on
      commercial (Team/Enterprise) or API customer data by default — confirm current
      terms for your path and keep the evidence.

## Assessments & records

- [ ] **Transfer Impact Assessment (TIA).** The organization's own responsibility when
      transferring data internationally.
- [ ] **DPIA (Data Protection Impact Assessment)** where processing is likely high-risk
      to individuals (often the case for decisions affecting people).
- [ ] **Record of processing activities (ROPA)** updated to include the Claude use.

## Operations

- [ ] **Access controls** on who can use the integration and see logs.
- [ ] **Logging & audit trail** — enough to answer "why did it produce that" without
      creating a new PII store you can't defend.
- [ ] **Human oversight** designed in where outputs affect people or carry real cost.
- [ ] **Incident & breach process** extended to cover the AI system.
- [ ] **Data-subject rights** (access, erasure) — know how you'd honor them for data
      that flowed through the system.

## Go-live gate

Before production, confirm: DPA signed, residency pinned, retention/training terms
documented, DPIA/TIA done where needed, AI policy published, oversight and logging in
place, and DPO/counsel sign-off on the legal determinations.

---

# Appendix C — EU AI Act


The EU AI Act regulates AI by **risk tier of the use case**, not by the model itself.
Classify what the organization is *doing* with Claude, then apply the obligations.
This is a working summary, **not legal advice** — confirm against the official text
linked in `official-sources.md` and have counsel validate high-stakes classifications.

## The tiers

**Prohibited.** A short list of banned uses (e.g. social scoring, certain biometric
categorization, manipulative systems). If the use looks like one of these, stop and
escalate — don't design around it.

**High-risk.** Systems used in sensitive domains — e.g. employment and worker
management, access to essential services, credit, education, critical infrastructure,
law enforcement, and certain biometric uses. These carry substantial obligations: risk
management, data governance, technical documentation, logging, human oversight,
accuracy/robustness, and a conformity process. If a Claude use affects people's
rights, livelihood, or safety, treat it as potentially high-risk until confirmed
otherwise.

**Limited risk (transparency).** Systems that interact with people or generate
content. The core obligation is **transparency** — tell users they're dealing with AI,
and label/flag AI-generated or manipulated content where required. Most customer-facing
assistants and content tools land here.

**Minimal risk.** Everything else — most internal productivity uses (drafting,
summarizing, coding help). Few specific obligations, but good governance still applies.

## General-purpose AI (GPAI) note

Obligations on the *model provider* (like Anthropic) for general-purpose models are
separate from your obligations as a *deployer*. As a deployer, your focus is your use
case's tier and the transparency/oversight duties that follow.

## How to classify (quick pass)

1. Does it resemble anything on the prohibited list? → Escalate, don't proceed.
2. Is it used in a high-risk domain or to make/inform decisions about people? →
   Treat as high-risk; map the obligations; involve counsel.
3. Does it interact with people or generate content shown to them? → At least
   transparency obligations.
4. Otherwise → minimal risk; apply normal governance.

## Deployer obligations to plan for (when applicable)

- Transparency to users that AI is in use.
- Human oversight proportionate to the risk.
- Keeping logs / records.
- Using the system within its intended purpose and the provider's instructions.

*The Act phases in over time and details evolve — treat this as orientation and verify
current obligations and dates against the official source.*

---

# Appendix D — Official sources


Provider terms, regions, and regulatory timelines change. Treat this skill as
orientation and confirm specifics against these primary sources before making
commitments or legal determinations.

## Anthropic / Claude
- Trust Center (security, compliance, subprocessors): https://trust.anthropic.com
- Data Processing Addendum (DPA + SCCs): https://www.anthropic.com/legal/data-processing-addendum
- Commercial Terms of Service: https://www.anthropic.com/legal/commercial-terms
- Privacy Policy: https://www.anthropic.com/legal/privacy
- Documentation: https://docs.claude.com

## Cloud deployment paths
- Claude on Amazon Bedrock: https://aws.amazon.com/bedrock/claude/
- Claude on Google Vertex AI: https://cloud.google.com/vertex-ai (Anthropic models in Model Garden)
- Microsoft Foundry (Azure): https://azure.microsoft.com (Foundry model catalog)
- Each cloud's own DPA and region/residency documentation governs data processing on
  that path — read the specific cloud's compliance pages.

## EU regulation
- EU AI Act — regulatory framework overview: https://digital-strategy.ec.europa.eu/en/policies/regulatory-framework-ai
- EU AI Act — full text (EUR-Lex): search "Regulation (EU) 2024/1689" on https://eur-lex.europa.eu
- GDPR — full text (EUR-Lex): "Regulation (EU) 2016/679"
- European Data Protection Board (guidance, SCCs): https://www.edpb.europa.eu
- DORA (Digital Operational Resilience Act, financial entities): "Regulation (EU) 2022/2554" on EUR-Lex; see also https://finance.ec.europa.eu

## A note on using a vendor's own guide
Vendor and consultancy guides (including aimognad.se's Claude + GDPR materials) can be
useful orientation, but the binding details live in the provider contracts and the EU
legal texts above. Use secondary guides to understand the landscape; confirm the
specifics that matter against these primary sources.
