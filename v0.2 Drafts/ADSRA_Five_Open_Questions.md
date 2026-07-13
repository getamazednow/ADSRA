# ADSRA — Five Open Peer-Review Questions (v0.1 → v0.2)

**Artefact:** Working tracker · v0.2 workstream
**Owner:** Duane (author) · **Status:** Live — the active peer-review workstream
**Version cycle:** v0.1 (July 2026) → v0.2
**House style:** navy `142A4C` / gold `C8A24B`. Internal working document; plain formatting for versioning.

> Purpose: hold the five open questions from Technical Reference §14 (and Article 6) as a managed workstream. Each has a stable ID (`OQ-1…OQ-5`), the current author `[Position]`, what would resolve it, which sectors are wanted, its evidence dependencies, and a resolution target. Feedback lands via the [Response Log](ADSRA_Peer-Review_Response_Log.md) (`PRL-nnn`) and any resulting edit is tracked in the [Change Register](ADSRA_Change_Register.md) (`CR-nnn`).

**Status legend:** `Open` (no material input yet) · `Gathering` (feedback arriving) · `Converging` (a direction is forming) · `Resolved-v0.2` (decided, change applied) · `Carried` (deliberately left open in v0.2, stated as such).

---

## OQ-1 — Tier boundaries: is four tiers right?

**The question.** Is a four-tier classification (Low → Medium → High → Critical) correct, or should **Medium split into commercial-sensitive vs personal**? Classification is the engine of ADSRA — it prices every control — so the tier count is load-bearing.

**Why it matters.** Get tiers wrong in either direction and the cost logic breaks: too few and personal data hides inside a commercial Medium tier (under-protected, tort-exposed); too many and the scheme collapses into over-classification (a named anti-pattern, Tech Ref §11.4). Retail loyalty/behavioural data and super member data are the pressure points.

**Current author position.** `[Position]` Four tiers, held. Retail note already places loyalty behaviour at **High**, not Medium — the primary tort exposure after payment data. A Medium split is plausible but must earn its complexity.

**What good challenge looks like.** A worked estate where a single Medium tier demonstrably mis-prices either commercial-sensitive or personal data — with the control-cost consequence quantified.

**Sectors most wanted:** Retail · Financial services & superannuation.

**Evidence dependencies:** Privacy Act tiered-penalty / statutory-tort provisions [R3] — governs where personal data must sit. No date-sensitivity, but any tier claim tied to an obligation must trace to §12.

**Affected artefacts if changed:** Tech Ref §2.2, §6.1, §10.3; White Paper §6; Deck slides 7/9; Articles 2/5.

**Linked feedback:** _(PRL-…)_ · **Linked changes:** _(CR-…)_
**Resolution target:** v0.2 · **Status:** `Open`

---

## OQ-2 — HYOK guidance: surgical or broader?

**The question.** The draft says hold-your-own-key and client-side encryption are **"surgical, not universal."** Is that the right line? Bring the concrete workload where the feature-loss trade *was* — or *wasn't* — worth it.

**Why it matters.** HYOK/CSE is the strongest cryptographic-sovereignty control and the most expensive: it breaks real native cloud features (server-side search, some analytics, managed integrations). The "surgical" guidance is an explicit honest-ledger trade-off; it needs field evidence, not assertion.

**Current author position.** `[Position]` Apply CSE/HYOK only to assets whose threat model includes **lawful compulsion of the provider**; provider-managed keys for Low, CMK for Medium/High, HSM-backed CMK/HYOK for Critical. Universal application is self-harm.

**What good challenge looks like.** A named workload with the before/after feature loss and the risk it bought — either vindicating "surgical" or showing a class of workload where broader application paid off.

**Sectors most wanted:** Banking · Healthcare · Cross-industry / platform engineering.

**Evidence dependencies:** None regulatory — this is an engineering-economics `[Position]`. Keep it argued, not cited.

**Affected artefacts if changed:** Tech Ref §6.3; White Paper §4/§8; Deck slides 7/15; Article 5.

**Linked feedback:** _(PRL-…)_ · **Linked changes:** _(CR-…)_
**Resolution target:** v0.2 · **Status:** `Open`

---

## OQ-3 — Level 6 governance: who audits the auditor?

**The question.** At maturity Level 6 (Autonomous Sovereignty), AI agents assess and remediate the estate's own sovereignty posture. **What evidence would convince a regulator that agentic remediation is itself well-governed?** Named in §14 and Article 4 as the hardest open question in the pack.

**Why it matters.** Level 6 is the model's genuinely new contribution and its biggest exposure: the assurance system is itself an AI system, so it needs the same Pillar 5 treatment (registered models, scoped tool permissions, budget limits, evidence trails). Without a regulator-credible evidence answer, Level 6 stays a slide, not a control.

**Current author position.** `[Position]` Level 6 is **aspirational by design** — pilots, not production, are the realistic 36-month target. Agentic assurance must be governed as a Pillar 5 workload and is only reachable through Pillar 7 (observability) as its telemetry substrate.

**What good challenge looks like.** A concrete evidence package a regulator would accept for autonomous remediation — audit trail schema, human-oversight thresholds proportionate to blast radius, fail-safe behaviours, model/tool governance.

**Sectors most wanted:** Risk / regulatory practitioners · Banking.

**Evidence dependencies:** Existing-law posture — no standalone AI Act; obligation is to evidence control under current law (Privacy, CPS 230, SOCI). Anchor to [R3], [R1], [R5], AI-governance references [R10]/[R11]. Verify the "no standalone AI Act / AI Safety Institute" framing against [R10] before restating.

**Affected artefacts if changed:** Tech Ref §6.7, §9; White Paper §7; Deck slide 13; Article 4.

**Linked feedback:** _(PRL-…)_ · **Linked changes:** _(CR-…)_
**Resolution target:** v0.2 direction; likely **`Carried`** into v0.2 as an explicitly-open design question · **Status:** `Open`

---

## OQ-4 — Missing blueprints: utilities and education

**The question.** Utilities and education industry blueprints were **deliberately deferred** from v0.1. Who contributes them, and do they enter v0.2 or v0.3?

**Why it matters.** Both are on the author's primary vertical list; their absence is the most visible gap in the pack's industry coverage. Utilities sits inside SOCI (energy); education carries distinct student-data and research-data sovereignty profiles. Adding them materially widens the pack's addressable audience.

**Current author position.** `[Position]` Deferred, not dropped — explicitly inviting practitioner contributors who live those sectors.

**What good challenge looks like.** A contributor to co-author each blueprint on the existing template (anchor obligations, Critical-tier assets, signature patterns, worked example), matching the banking/FS/retail/healthcare structure in Tech Ref §10.

**Sectors most wanted:** Utilities (energy) · Education.

**Evidence dependencies:** Utilities → SOCI energy-sector obligations [R5]; verify sector coverage and CIRMP applicability before drafting. Education → Privacy Act [R3] plus any state/sector data-handling rules — check primary source, none currently in §12, so this needs new evidence-register entries.

**Affected artefacts if changed:** Tech Ref §10 (new §10.5/§10.6), §12 (new evidence rows); Deck slide 10 (extend lenses); White Paper §6.

**Linked feedback:** _(PRL-…)_ · **Linked changes:** _(CR-…)_
**Resolution target:** v0.2 if contributors secured, else `Carried` to v0.3 with deferral stated · **Status:** `Open`

---

## OQ-5 — Technology mappings: AU-region service capability

**The question.** The indicative AWS/Azure/GCP mappings evolve quarterly. Which need correction against **current AU-region service capability** before publication?

**Why it matters.** The mappings are labelled indicative, not endorsements — but stale mappings erode credibility with the engineering audience fastest. This is the lowest-controversy, highest-hygiene item: it's verification work, not a debate.

**Current author position.** `[Position]` Mappings are examples current at time of writing; validate service capabilities and regions before any design commitment. Not endorsements.

**What good challenge looks like.** Practitioner correction naming the service, the AU region, and the current capability (e.g., CMK/HSM, in-region model availability, policy-as-code primitives) versus what the draft states.

**Sectors most wanted:** Cross-industry · Cloud/platform engineering.

**Evidence dependencies:** Vendor primary sources (AWS/Azure/GCP AU-region service pages) — currency-sensitive; re-verify immediately before publication. In-region AI model availability is explicitly acknowledged to lag the frontier (honest-ledger point) — keep that caveat.

**Affected artefacts if changed:** Tech Ref §6.1–6.7 (indicative-mapping subsections), §7; Deck slides 7/8/11; Articles 2/3.

**Linked feedback:** _(PRL-…)_ · **Linked changes:** _(CR-…)_
**Resolution target:** v0.2 — final pre-publication verification pass · **Status:** `Open`

---

## Workstream dashboard

| OQ | Question | Type | Target | Status |
|----|----------|------|--------|--------|
| OQ-1 | Tier boundaries (four tiers vs Medium split) | Design decision | v0.2 | Open |
| OQ-2 | HYOK / CSE — surgical vs broader | Evidence-gather | v0.2 | Open |
| OQ-3 | Level 6 — regulator-credible governance evidence | Design / likely carried | v0.2 direction | Open |
| OQ-4 | Utilities + education blueprints | New content | v0.2 or v0.3 | Open |
| OQ-5 | Technology mappings currency | Verification | v0.2 pre-pub | Open |

---

*Cross-references: [ADSRA Peer-Review Response Log](ADSRA_Peer-Review_Response_Log.md) · [ADSRA Change Register](ADSRA_Change_Register.md). Source of truth for regulatory claims: Technical Reference §12 (Evidence Register). Author judgement marked `[Position]` throughout, per project instruction #2.*
