# ADSRA Article Series — Sovereignty by Design

**Author:** Duane · **Status:** Draft v0.1 · **July 2026**
Six publication-ready articles (~700–1,100 words each) for LinkedIn / blog serialisation. Each article stands alone, references the white paper and Technical Reference as the deep-dive assets, and ends with a call to engage. Suggested cadence: one per week. Suggested series hashtags: #DigitalSovereignty #EnterpriseArchitecture #ADSRA #CloudGovernance #AIGovernance

**Editorial note on claims:** every regulatory fact in these articles is anchored in the ADSRA Technical Reference evidence register (Section 12) — dates are current as at July 2026. Positions and predictions are flagged in-line as the author's view.

---

## Article 1 — Your data is in Sydney. So why isn't it sovereign?

**Hook format:** myth-busting opener. **Target reader:** CIO/CTO/CISO, architecture leaders.

Ask most executives where their data is, and they'll answer with a city. "Sydney. Australia East. We're fine."

Residency was last decade's question. Here is this decade's: **who can be compelled to hand your data over — and what could they actually produce?**

Those are different questions with different answers. The US CLOUD Act (2018) allows US authorities to compel providers subject to US jurisdiction to produce data in their *possession, custody or control* — regardless of where it is stored. A Sydney region operated by a US-headquartered provider, encrypted with keys that provider manages, administered by that provider's global support teams, is *resident* in Australia. It is not *sovereign* in Australia.

Meanwhile, the Australian regulatory clock has been running hard:

- **APRA CPS 230** has been in force since 1 July 2025 — critical operations, board-approved tolerance levels, material service providers, and a 24-hour notification clock for tolerance-breaching disruptions. Pre-existing provider contracts were captured by the earlier of renewal or 1 July 2026. That deadline has now arrived.
- The **Privacy Act reforms** delivered a statutory tort for serious invasions of privacy (live since mid-2025), sitting on top of the 2022 penalty uplift — the greater of $50m, 3× the benefit, or 30% of adjusted turnover.
- From **10 December 2026**, privacy policies must disclose substantially automated decisions that significantly affect individuals — a direct constraint on how you architect AI.
- The **SOCI Act** now spans eleven critical-infrastructure sectors, including financial services, healthcare, energy and data storage.

No single instrument requires "sovereignty" by name. The obligation emerges from their intersection — and that is precisely why it keeps falling between organisational cracks. Compliance owns the instruments. Platform teams own the technology. **Nobody owns the architecture in between.** *(That's my position after three decades in enterprise architecture, and I'm happy to be argued with.)*

So I've spent recent months building what I couldn't find: a reference architecture that treats digital sovereignty as a first-class enterprise architecture domain — with named capabilities, control objectives, a maturity model, and measures a Risk Committee can actually govern. I've called it **ADSRA: the Australian Digital Sovereignty Reference Architecture**.

Over the next five articles I'll walk through it: the seven sovereignty pillars; why your AI model is the least interesting part of your AI architecture; the maturity model that ends in *autonomous* sovereignty; the honest business case (including what sovereignty costs you); and an invitation to tear the whole thing apart in peer review.

Because here's my bet: just as the industry evolved from "security" to **zero trust** as a first-class architectural principle, we are about to evolve from "data residency" to **digital sovereignty architecture** as a formal enterprise architecture domain. I'd rather Australian practitioners define that evolution than inherit it.

**Next week:** the seven questions every board should be able to answer — and mostly can't.

*The full white paper ("Sovereignty by Design") and the engineering-grade Technical Reference are available — comment or DM for the pack. All regulatory dates verified as at July 2026.*

---

## Article 2 — Seven questions your board can't answer (yet)

**Hook format:** diagnostic listicle. **Target reader:** board members, executives, architecture boards.

Frameworks fail when they start with technology. ADSRA starts with questions — seven of them, one per sovereignty pillar. Try them on your own organisation.

**1. Data — Who can legally compel access to our information?**
Not "where is it stored" — who can *compel* it. If the answer involves a foreign statute you haven't threat-modelled, you have a data sovereignty gap. The control set: classification with sovereignty tiers, residency and cross-border transfer controls, tokenisation, DLP, and privacy impact assessment embedded in delivery.

**2. Identity — Who is acting, from where, and with what privilege?**
Identity is now more valuable than infrastructure. Every request should answer: who, what, why, when, from where, at what risk score. Standing privilege on critical systems should be extinct — replaced by just-in-time elevation with session recording.

**3. Cryptographic — Who controls the keys that control trust?**
Encryption is the last defence against jurisdictional uncertainty — *if, and only if, you hold the keys*. Provider-managed keys mean the provider can be compelled to use them. Customer-managed keys, HSM-backed roots of trust, and (surgically) hold-your-own-key change that answer.

**4. Operational — Who administers production, and from which jurisdiction?**
This is the fastest-growing discipline in the domain, because regulators stopped asking where data lives and started asking who can act on it. Australian operations, an Australian SOC, provider-access approval workflows, jurisdiction-aware break-glass — and exit plans that have actually been tested, as CPS 230 expects.

**5. AI — Where do prompts, embeddings, inference and training occur?**
This pillar barely existed three years ago. Today, prompts and retrieval corpora are flowing through model supply chains most enterprises cannot map. If you cannot answer where inference happens for your top five AI use cases, you cannot sign the board paper that approves them.

**6. Governance — Is compliance enforced by the platform, or by a policy PDF?**
"Developers should..." is not a control. Policy-as-code, pipeline gates that fail closed for critical tiers, and guardrail exceptions that auto-expire — that is a control. Every deployment should *inherit* compliance.

**7. Observability — Can we prove, audit and continuously measure sovereignty?**
The underdeveloped pillar, and in my view the highest-leverage investment. A control without evidence should be treated as absent. If sovereignty isn't measured from telemetry — not attestation surveys — it isn't real.

Here's the pattern I see in Australian enterprises: strong on 2 and 6 (identity and cloud governance matured through the zero-trust and FinOps years), patchy on 1 and 3 (classification exists but doesn't *drive* anything; keys are provider-managed by default), and weakest on 4, 5 and 7 — exactly the pillars regulators are now probing. *(Position, not survey data — challenge me with yours.)*

Each pillar in ADSRA carries defined control objectives (with stable IDs engineering teams can build against), reference patterns, indicative AWS/Azure/GCP mappings, and key risk indicators. The point is not the taxonomy. The point is that a board can *fund, measure and govern* a pillar. It cannot fund a vibe.

**Next week:** why your AI model is the least interesting component in your AI architecture.

---

## Article 3 — The model is the least interesting part of your AI architecture

**Hook format:** contrarian technical. **Target reader:** CDOs, AI leads, solution architects.

Every AI strategy deck I see has a model in the middle. Big logo. GPT-something, Claude-something, Gemini-something.

The model is the least interesting component in the architecture. What matters is **everything you wrap around it** — because that wrapping is the difference between an AI use case your board can approve and one it can't.

Here is the ADSRA reference flow for AI sovereignty:

**User → Prompt Gateway → Policy Engine → PII Detection → Enterprise RAG → LLM Gateway + Model Registry → Approved Model (AU region) → Response Validation → User**
…with an **immutable audit rail** underneath capturing prompts, retrievals, model versions, decisions, tokens, cost, and — critically — the *jurisdiction of inference* for every single request.

Notice what this design asserts:

- **The LLM never talks directly to users.** Or to raw data stores. Direct application-to-model integration is the most consequential design error in enterprise AI today — every "temporary" pilot wired straight to a model API becomes permanent, invisible AI estate.
- **Prompt sovereignty:** nothing leaves the enterprise boundary unfiltered. PII detection redacts the customer identifiers your staff *will* paste into prompts.
- **Embedding and RAG sovereignty:** vector stores inherit the classification tier of their source data. An embedding of Critical data *is* Critical data. This one surprises people.
- **Inference and training sovereignty:** a model registry pins approved models, versions and regions. High/Critical inference executes in Australian regions. Enterprise data is excluded from provider training by contract *and* configuration.
- **Output governance:** responses are validated before delivery, and decisions that significantly affect individuals are flagged into the transparency register the Privacy Act requires from 10 December 2026.

Two vignettes from the ADSRA pack:

**A retailer's AI pricing assistant.** Merchandising asks for a price-elasticity recommendation. Gateway authenticates; policy engine confirms the use case is registered; PII detection scrubs; RAG retrieves only from the governed pricing corpus (Medium tier); inference runs on a registry-pinned model in an Australian region; the response filter checks for leakage; audit records the full trace. Overhead versus a raw model call: tens of milliseconds. Value: the use case is *approvable*.

**A bank's customer-service copilot.** Customer context — Critical tier — is tokenised before retrieval. The copilot's corpus is the governed knowledge base, not core-banking records. Outputs that could constitute significant automated decisions (hardship guidance, say) route through human review and into the ADM-transparency register ahead of the December 2026 obligation.

Australia's AI policy landscape reinforces this architecture-first posture. The Voluntary AI Safety Standard was superseded by the **Guidance for AI Adoption** (October 2025); the **National AI Plan** (December 2025) chose existing technology-neutral law plus an AI Safety Institute over a standalone AI Act. Translation: there will be no single statute to point compliance at. **The obligation is to evidence control under existing law** — privacy, prudential, consumer, critical infrastructure. Evidence is an architecture output, not a policy output.

My bet: *(position)* the enterprises that industrialise AI first will not be the ones with the best models. They will be the ones whose governance made the models approvable.

**Next week:** the six-level maturity model — and why Level 6 means AI agents auditing your sovereignty while you sleep.

---

## Article 4 — Level 6: when the platform audits itself

**Hook format:** future-state narrative. **Target reader:** strategy and architecture leaders, risk executives.

Maturity models are how architects turn ambition into a funding sequence. ADSRA's has six levels:

1. **Cloud Adoption** — workloads migrating; controls inherited ad hoc from providers.
2. **Cloud Security** — Essential Eight-aligned hardening; MFA; SIEM ingesting cloud logs.
3. **Cloud Governance** — landing zones, tagging, policy governance emerging.
4. **Digital Sovereignty** — classification *drives* residency, keys and Australian operations for critical tiers; obligations mapped to controls.
5. **AI Sovereignty** — all AI via gateway and registry; RAG governance; AI observability; ADM-transparency readiness.
6. **Autonomous Sovereignty** — the platform continuously assesses and remediates its own sovereignty posture.

Most Australian enterprises sit at Levels 2–3 today. *(Position, from practice; I'd welcome benchmarking data.)* ADSRA targets 4–5 within roughly 36 months. But Level 6 is the model's genuinely new contribution, so let me paint it.

Imagine assurance agents running continuously against your estate, asking:

- Is every workload still compliant with its tier's control set?
- Has any data crossed a jurisdiction in the last hour?
- Is an encryption key approaching expiry without a rotation scheduled?
- Has any model moved inference outside Australia — a region failover, a provider routing change, a developer "optimisation"?
- Is a privileged administrator operating from an unexpected location?

At Levels 1–5, these are audit questions answered quarterly, by humans, from samples. At Level 6 they are **computed properties of the platform**, evaluated continuously, with remediation initiated automatically — quarantine the workload, force the key rotation, fail inference back in-region, suspend the session — under human oversight proportionate to blast radius.

Three honest caveats:

**First, Level 6 is aspirational by design.** Pilots, not production, are the realistic 36-month target. A maturity model whose top level everyone already occupies isn't a model; it's a mirror.

**Second, agentic assurance is itself an AI system** — which means it needs the same Pillar 5 treatment as any other: registered models, scoped tool permissions, budget limits, evidence trails. "Who audits the auditor?" is a design requirement, not a gotcha. What evidence would convince a regulator that agentic remediation is well-governed? That is an open peer-review question in the ADSRA draft, and I genuinely want practitioner answers.

**Third, Level 6 is only reachable through Pillar 7.** Autonomous assurance is a consumer of telemetry. If your controls don't emit evidence, there is nothing for the agents to reason over. This is why I keep insisting observability is the highest-leverage sovereignty investment: it is the substrate for everything above it.

The strategic point: sovereignty at Level 6 stops being an *audit finding* and becomes a *continuously computed property* — the same shift monitoring made when it became observability, and deployment made when it became CI/CD. Every operational discipline eventually becomes software. Sovereignty assurance is next.

**Next week:** the business case — what sovereignty returns, and what it honestly costs.

---

## Article 5 — Sovereignty is not free. Here's the honest ledger.

**Hook format:** candid CFO-facing analysis. **Target reader:** CFOs, CROs, investment committees.

Architecture papers love benefits. Investment committees trust ledgers. Here is ADSRA's, both columns.

### The return side

**1. Penalty and tort exposure avoided.** Privacy penalties now reach the greater of $50m, 3× the benefit, or 30% of adjusted turnover for serious interferences. The statutory tort (live since mid-2025) adds per-incident, class-action-style exposure. This exposure concentrates in exactly the data estates most enterprises haven't classified — you cannot price what you haven't tiered.

**2. Regulatory speed.** Pre-approved sovereignty patterns collapse architecture and risk-approval cycle times. When the pattern is already endorsed — gateway, registry, CMK, AU-ops — a new AI use case is a configuration review, not a first-principles risk debate. In my experience the approval cycle, not engineering, is the binding constraint on enterprise AI velocity. *(Position.)*

**3. Concentration risk made visible.** CPS 230 requires material-service-provider registers and viable exit plans. Sovereignty KRIs quantify what Risk Committees previously accepted implicitly: how concentrated, how substitutable, how fast.

**4. The licence to deploy AI at all.** Evidenced control — gateway coverage, registry-pinned models, audit trails, ADM-transparency readiness — is becoming the precondition for board approval of customer-facing AI. This is the quiet return that dwarfs the others.

### The cost side — stated plainly

**Sovereign controls tax capability.** Hold-your-own-key and client-side encryption break real native cloud features (server-side search, some analytics, certain managed integrations). Apply them surgically to the assets whose threat model includes lawful compulsion of the provider — not universally.

**In-region AI lags the frontier.** Australian-region model availability trails global releases. Sometimes by weeks; occasionally by a capability generation. That is a real trade, and pretending otherwise erodes credibility with engineering teams.

**Over-classification is self-harm.** Default everything to Critical and you tax low-risk workloads, slow delivery, and teach the organisation to route around the scheme. The retailer example in the ADSRA pack runs its product catalogue on a *global public CDN, no sovereignty premium at all* — because classification said it could.

**Skills are scarce.** Policy-as-code, key-custody engineering, AI governance — thin markets, and getting thinner as CPS 230 remediation programs compete for the same people.

### The managed position

Not maximal sovereignty. **Tiered sovereignty, consciously priced.** Four tiers (Low → Critical); the premium spent only where obligations demand; residual risk measured and accepted in the open. And a handful of telemetry-derived KRIs on the Risk Committee dashboard quarterly:

- % of High/Critical data under customer-managed keys
- % of privileged sessions administered from Australia (and recorded)
- % of AI inference executed in-region via the gateway
- First-time pass rate through policy-as-code gates
- Mean time to detect a cross-jurisdiction data movement
- Recency of tested exit plans for material providers

None is an attestation. All are computable from telemetry. That is the difference between claiming sovereignty and measuring it.

**Next week (final):** the whole pack, released for peer review — and an invitation to break it.

---

## Article 6 — I built a sovereignty reference architecture. Please break it.

**Hook format:** open peer-review invitation. **Target reader:** the architecture community.

Over the past five articles I've argued that digital sovereignty is an enterprise architecture domain, not a compliance checkbox; walked the seven pillars; put the AI gateway pattern and the six-level maturity model on the table; and priced the trade-offs honestly.

Today I'm releasing the full pack as **v0.1 — deliberately a draft, deliberately for peer review**:

- **The Executive Briefing** (17 slides) — the board conversation: why now, the pillars, the industry lenses, the KRIs, three horizons, and the ask.
- **The Technical Reference** (~26 pages) — for engineering and architecture teams: control objectives with stable IDs (ADSRA-DS-01 through OB-05), indicative AWS/Azure/GCP mappings, the 20-capability model, maturity assessment evidence, industry blueprints for banking, financial services, retail and healthcare — and an **evidence register mapping every regulatory claim to its primary source**.
- **The White Paper** (*Sovereignty by Design*) — the narrative argument in ~4,500 words.

Why publish a draft? Because reference architectures earn authority through scar tissue, not polish. TOGAF, SABSA and the Essential Eight all got better by being argued with. And because the alternative — everyone rebuilding sovereignty thinking privately, client by client, program by program — wastes the profession's time at precisely the moment the regulatory clock is running.

**Where I most want to be challenged:**

1. **Tier boundaries.** Is four tiers right? Should Medium split into commercial-sensitive vs personal? Retail and super practitioners especially.
2. **HYOK guidance.** The draft says "surgical, not universal." Bring me the workload where the feature-loss trade was — or wasn't — worth it.
3. **Level 6 governance.** What evidence would convince a regulator that agentic remediation is itself well-governed? This is the hardest open question in the pack.
4. **Technology mappings.** AU-region service capabilities evolve quarterly; the mappings are indicative and need practitioner correction.
5. **Missing blueprints.** Utilities and education are explicitly deferred to v0.2 — I'm looking for contributors who live those sectors.

**What good challenge looks like:** cite the instrument, name the workload, bring the counter-example. The evidence register exists precisely so you can attack claims at their source. Where I've marked something *[Position]*, it's my professional judgement after 33 years across financial services, retail, healthcare, education and utilities in Australia, India, the US and Southeast Asia — argued, not cited, and fair game.

One prediction to close the series. *(Position, obviously.)* Within five years, "digital sovereignty architect" will be a role title, sovereignty KRIs will be a standing Risk Committee agenda item, and RFPs will ask for sovereignty maturity levels the way they ask for ISO certifications today. The organisations that built the capability deliberately — tiered, measured, priced — will treat that world as business as usual. The ones that didn't will be running remediation programs on regulator timelines instead of their own.

Comment, DM, or bring it to the next architecture community of practice. Version 0.2 will be better because of you.

*ADSRA — Australian Digital Sovereignty Reference Architecture. Draft v0.1, July 2026. All regulatory dates verified as at publication; evidence register in the Technical Reference, Section 12.*

---

## Series production notes

- **Cadence:** weekly; Article 1 sets the hook, Article 6 lands the CTA. Articles 2–5 can be reordered if engagement data suggests.
- **Visuals:** each article pairs with one diagram from the pack — A1: layered model; A2: seven pillars; A3: AI gateway flow; A4: maturity staircase; A5: KRI dashboard slide (deck slide 14); A6: title slide.
- **Cross-linking:** every article footer links the white paper; Articles 2–5 also link the Technical Reference for the engineering audience.
- **Compliance hygiene:** dates re-verified before each publish; if publication slips past a regulatory milestone (e.g., 10 Dec 2026), update tense accordingly.
