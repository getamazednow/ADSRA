# ADSRA Change Register (v0.1 → v0.2)

**Artefact:** Working tracker · v0.2 workstream
**Owner:** Duane (author) · **Status:** Live — updated as changes are proposed and applied
**Version cycle:** v0.1 (July 2026) → v0.2
**House style:** navy `142A4C` / gold `C8A24B`. Internal working document; plain formatting for versioning.

> Purpose: record every change from v0.1 to v0.2 — what changed, why, which artefacts it touches, whether it required an evidence check, and its status. This is the controlled record behind the release. **Rule (project instruction #4): never overwrite `artefacts/`.** All edits are drafted in `v0.2 Drafts/`; the register tracks when a change moves from *proposed* to *applied* in the draft set.

---

## How to use this register

One row per discrete change, stable ID (`CR-001`, …). A change may serve several artefacts (the pack is deliberately consistent across deck, Tech Ref, white paper and articles) — list every affected location so nothing drifts out of sync.

**Field definitions**

- **ID** — stable identifier.
- **Raised** — date proposed.
- **Driver** — what prompted it: a Response Log item (`PRL-nnn`), an Open Question (`OQ-n`), an author-initiated edit (`Author`), or a date/evidence re-verification (`Evidence-check`).
- **Artefact(s) · Location** — every deliverable + section/slide/pillar affected. Flag when a change must propagate across the pack.
- **Change description** — what is changing, concisely.
- **Type** — `Factual/date correction` · `Position revision` · `New content` · `Wording/clarity` · `Structural` · `Mapping update` · `Evidence-register update`.
- **`[Position]` impact** — does this touch author judgement? `Y` (and note whether the `[Position]` marker is added, removed or reworded) / `N`.
- **Evidence check** — `N/A`, or the source verified against (evidence-register ref `Rn`, or primary-source URL) + date checked. Mandatory before any regulatory date/obligation is altered.
- **Status** — `Proposed` → `Drafted` (written into v0.2 draft) → `Verified` (evidence + peer sanity-checked) → `Applied` (in the v0.2 draft set) → `Published`. Or `Rejected` / `Deferred`.
- **Owner** — who is making the edit.

---

## Register

| ID | Raised | Driver | Artefact(s) · Location | Change description | Type | `[Position]` impact | Evidence check | Status | Owner |
|----|--------|--------|------------------------|--------------------|------|--------------------|----------------|--------|-------|
| CR-001 | 2026-07-13 | Evidence-check | White Paper §1; Deck slide 2; Article 1 | Update tense on the CPS 230 pre-existing-contract deadline — the date "earlier of renewal or 1 Jul 2026" is **correct** but now **past** as at 13 Jul 2026; move wording from future/imminent ("this month", "has now arrived") to completed framing. Date figure unchanged. | Factual/date correction (tense) | N | **Done 2026-07-13** — verified against [R1] / APRA primary source (apra.gov.au): CPS 230 in force **1 Jul 2025**; pre-existing provider contracts comply by **earlier of next renewal or 1 Jul 2026** (confirmed); targeted amendments finalised **30 Apr 2026**, effective **1 Jul 2026** (matches pack). Deadline has passed. | Verified — tense edit to apply in v0.2 artefact drafts | Duane |
| CR-002 | 2026-07-13 | Evidence-check | Tech Ref §3, §6.5, §7.2, §10; White Paper §5; Deck slides 2/10/14; Articles 1/3 | Confirm the 10 Dec 2026 ADM-transparency obligation is still **future** and consistently framed as forthcoming across the pack. | Factual/date confirmation | N | **Done 2026-07-13** — verified against [R3] / OAIC primary source (oaic.gov.au): from **10 Dec 2026**, APP entities must disclose in privacy policies where personal information is used in ADM that could significantly affect an individual's rights or interests (**APP 1.7, 1.8, 1.9**, Privacy and Other Legislation Amendment Act 2024). Date confirmed; still future as at 13 Jul 2026. OAIC guidance in consultation (submissions closed 15 Jun 2026). | Verified — no change required; forthcoming framing correct | Duane |
| CR-003 | 2026-07-16 | Source-review | Tech Ref §6.5 (Pillar 5, ref pattern + KRI); White Paper §4/§5; Deck slide 7 (AI), slide 10; index.html (Pillar 5 card, AI-flow note) | Extend Pillar 5 (AI) beyond residency of prompts/inference to **decision assurance** of AI-influenced decisions: algorithmic/impact assessment, explainability, contestability, human oversight, bias/fairness testing; add a matching KRI (% ADM-scope use cases with impact assessment + contestability path). | New content / Position revision | Y — assurance content added; ties author judgement to a named benchmark rather than asserting new obligation | **Done 2026-07-16** — verified against uploaded primary source [R13] *National framework for the assurance of AI in government* (v1.0, 21 Jun 2024) and its 8 AI Ethics Principles (DISR 2019); connects to existing [R3] ADM obligation (10 Dec 2026). No new regulatory date asserted. | Applied | Duane |
| CR-004 | 2026-07-16 | Source-review | Tech Ref §6.6 (Pillar 6) + §13 [R11]; White Paper §4; Deck slide 7 (Governance); index.html (Pillar 6 card) | Map Governance sovereignty to **AS ISO/IEC 42001:2023** (AI management system), 23894:2023 (AI risk) and 38507:2022 (governance of AI), and to the framework cornerstones (governance, data governance, risk-based approach, standards, procurement). | Mapping update / New content | N | **Done 2026-07-16** — standards named in [R13] cornerstones; [R11] extended to list AS ISO/IEC 23894 & 38507. | Applied | Duane |
| CR-005 | 2026-07-16 | Source-review | Tech Ref §12 (Evidence Register) + §13 (add [R13]); White Paper References; Deck slide 16; index.html (timeline "AI policy consolidates") | Add evidence-register entry and reference **[R13]** for the National AI assurance framework; note it is government-scoped and a private-sector benchmark. | Evidence-register update | N | **Done 2026-07-16** — anchored to uploaded primary source (v1.0, 21 Jun 2024). URL omitted rather than guessed; cited as published by the Australian Government (Data and Digital Ministers). | Applied | Duane |
| CR-006 | 2026-07-16 | Source-review / OQ-4 | Tech Ref §10.5 (Utilities), §10.6 (Education), §10 note, §14 (OQ-4); White Paper §6 vignettes; Deck slide 9 subtitle + **new dedicated slide 11 "Public-sector Lenses · Utilities & Education"** (2×2 obligations/AI-assurance grid; deck renumbered to 18 slides); index.html (scope chip, CTA) | Add Utilities and Education blueprints — the verticals where the government assurance framework binds most directly — anchored to SOCI [R5], Privacy [R3], NSW AIAF (2022) and [R13]. **Expanded 2026-07-16** to full blueprints (anchor obligations, critical-tier assets, tiering example, signature patterns, AI-assurance note, worked example) matching/exceeding the private-sector verticals; propagated to White Paper vignettes, deck and site. | New content | Y — blueprints carry author judgement; marked [Position], open for contributor input | **Done 2026-07-16** — obligations cross-checked to existing register refs [R5],[R3],[R6],[R8],[R11],[R13]. NSW AI Assurance Framework (2022) named in [R13]. Full blueprints still flagged [Position], not evidence-complete pending peer review. | Applied | Duane |
| CR-007 | 2026-07-16 | Source-review | Tech Ref §6.5, §12; White Paper §5/§6/§8; Deck slide 10/14; index.html (AI-flow note, ledger cost bullet) | Name **sovereign-model / onshore-compute supply** as a model-registry option and differentiate supply-side sovereign-AI initiatives (build) from ADSRA (govern/measure); **soften** the "in-region AI lags the frontier" cost line to note the gap is narrowing. | Position revision / Wording | Y — added [Position] markers | **N/A (market context)** — driven by review of sovereign-au.ai (vendor site). Per instruction #1, vendor capability claims are **deliberately excluded from the evidence register**; treated as market context to verify, marked [Position]. | Applied | Duane |
| CR-008 | | | | | | | | Proposed | |

*(CR-001–CR-002 seeded from v0.1 date-currency review. CR-003–CR-007 raised 2026-07-16 from review of two external sources: the uploaded* National framework for the assurance of AI in government *(2024) and the Sovereign Australia AI site (sovereign-au.ai). Add rows as changes are raised.)*

**Release note — 2026-07-16.** CR-003 to CR-007 promoted to `artefacts/` (v0.2 docx/pptx + regenerated PDFs) and committed. Web summary (`index.html`) bumped to Draft v0.2. Utilities and Education blueprints expanded to full depth (10.5–10.6) and reflected in the deck (new Public-sector Lenses slide), White Paper vignettes and site. Sovereign-AU vendor site remains excluded from the evidence register (market context only).

---

## Release gate checklist (v0.2)

Before v0.2 is declared ready, every item below must be true:

- All `CR` items are `Applied`, `Rejected` or explicitly `Deferred (v0.3)` — none left `Proposed` or `Drafted`.
- Every date-related change carries a completed **Evidence check** against §12 / primary source.
- Every `[Position]`-impacting change preserves the fact-vs-judgement distinction (instruction #2).
- The four artefacts remain mutually consistent (deck ↔ Tech Ref ↔ white paper ↔ articles) — no claim updated in one and stale in another.
- Open Questions `OQ-1…OQ-5` are each either resolved (with a linked `CR`) or consciously carried into v0.2 as still-open, stated as such.
- Utilities and education blueprints (OQ-4) added or their deferral to v0.3 stated in-text.
- `artefacts/` untouched; v0.2 lives in `v0.2 Drafts/`.

---

## Change-type summary (auto-tally as register grows)

| Type | Count | Notes |
|------|-------|-------|
| Factual/date correction | 2 | CR-001 (tense, verified), CR-002 (confirmed, no change) |
| Position revision | 2 | CR-003 (decision assurance), CR-007 (sovereign supply / cost softening) |
| New content | 3 | CR-003 (Pillar 5 KRI), CR-004 (ISO 42001 mapping), CR-006 (Utilities/Education stubs) |
| Mapping update | 1 | CR-004 (AS ISO/IEC 42001/23894/38507); OQ-5 still to feed |
| Evidence-register update | 1 | CR-005 ([R13] National AI assurance framework) |

*Note (instruction #1): the Sovereign Australia AI vendor site is **not** entered in the evidence register. Its claims are market context, verified independently before reliance, and marked [Position] where used (CR-007).*

---

*Cross-references: [ADSRA Peer-Review Response Log](ADSRA_Peer-Review_Response_Log.md) · [ADSRA Five Open Questions](ADSRA_Five_Open_Questions.md). Source of truth for regulatory claims: Technical Reference §12 (Evidence Register).*
