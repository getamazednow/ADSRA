# ADSRA Peer-Review Response Log

**Artefact:** Working tracker · v0.2 workstream
**Owner:** Duane (author) · **Status:** Live — updated as reviews arrive
**Version cycle:** v0.1 (July 2026) → v0.2
**House style:** navy `142A4C` / gold `C8A24B`. This is an internal working document; formatting is kept plain for versioning.

> Purpose: capture every piece of peer-review feedback on ADSRA v0.1, record the author's disposition, and link each item to a Change Register entry (`CR-nnn`) and, where relevant, one of the five Open Questions (`OQ-1…OQ-5`). Nothing changes in `artefacts/` until a linked `CR` item is verified and applied.

---

## How to use this log

Each inbound comment gets one row and a stable ID (`PRL-001`, `PRL-002`, …). Log the comment as received — do not pre-filter. Disposition and evidence handling happen in the columns, so the audit trail shows *why* a change was or wasn't made.

**Field definitions**

- **ID** — stable identifier, never reused.
- **Received** — date the comment arrived.
- **Reviewer / Sector** — name (or handle) and the vertical they speak from (banking, FS & super, retail, healthcare, utilities, education, cross-industry). Sector matters: §14 targets specific verticals for specific questions.
- **Channel** — LinkedIn, DM, CoP session, email, review workshop.
- **Artefact · Location** — which deliverable and section/slide/pillar the comment touches (e.g., *Tech Ref §6.3*, *Deck slide 10*, *Article 3*, *White Paper §6*).
- **Maps to OQ** — one of `OQ-1…OQ-5`, or `—` if it raises something new.
- **Comment (summary)** — the substance, in the reviewer's intent, one or two sentences.
- **Type** — `Challenge` (disputes a position/claim) · `Correction` (factual/date/mapping error) · `Addition` (new content, e.g. a blueprint) · `Clarification` (wording/ambiguity) · `Endorsement`.
- **Evidence needed?** — `Y/N`. If `Y`, the claim must be checked against the evidence register (Tech Ref §12) or the primary source before disposition — never from memory.
- **Author response** — the reply given to the reviewer, including `[Position]` where it is judgement.
- **Disposition** — `Accepted` · `Accepted-modified` · `Rejected` · `Deferred (v0.3)` · `Needs-evidence` · `Open`.
- **Change ID** — linked `CR-nnn` if the disposition creates a change; `—` otherwise.
- **Status** — `Open` · `In review` · `Responded` · `Closed`.

---

## Log

| ID | Received | Reviewer / Sector | Channel | Artefact · Location | Maps to OQ | Comment (summary) | Type | Evidence needed? | Author response | Disposition | Change ID | Status |
|----|----------|-------------------|---------|---------------------|-----------|-------------------|------|------------------|-----------------|-------------|-----------|--------|
| PRL-001 | | | | | | | | | | Open | | Open |
| PRL-002 | | | | | | | | | | Open | | Open |
| PRL-003 | | | | | | | | | | Open | | Open |

*(Add rows as feedback arrives. Keep IDs sequential and never reuse a retired ID.)*

---

## Standing review prompts (seeded from Tech Ref §14 / Article 6)

These are the challenges the author has *explicitly invited*. Expect inbound feedback to cluster here; pre-map it to the Open Question so the workstream stays organised.

| Prompt to reviewers | Maps to OQ | Sectors most wanted |
|---------------------|-----------|---------------------|
| Is a four-tier scheme right, or should Medium split into commercial-sensitive vs personal? | OQ-1 | Retail, FS & super |
| Bring a concrete workload where the HYOK / client-side-encryption feature-loss trade was — or wasn't — worth it. | OQ-2 | Banking, healthcare, cross-industry |
| What evidence would convince a regulator that agentic (Level 6) remediation is itself well-governed? | OQ-3 | Risk/regulatory, banking |
| Contribute a utilities or education industry blueprint. | OQ-4 | Utilities, education |
| Correct the indicative AWS/Azure/GCP mappings against current AU-region service capability. | OQ-5 | Cross-industry, platform engineering |

---

## Weekly triage note

Review cadence follows the article series (one article/week). After each publish, sweep the channel, log new comments, set dispositions, and roll anything actionable into the Change Register. Record the sweep date here.

- _[date]_ — sweep after Article _n_: _n_ new items logged (`PRL-…`), _n_ changes raised (`CR-…`).

---

*Cross-references: [ADSRA Change Register](ADSRA_Change_Register.md) · [ADSRA Five Open Questions](ADSRA_Five_Open_Questions.md). Source of truth for regulatory claims: Technical Reference §12 (Evidence Register).*
