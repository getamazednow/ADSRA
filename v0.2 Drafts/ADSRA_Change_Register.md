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
| CR-003 | | | | | | | | Proposed | |

*(CR-001 and CR-002 are seeded from the date-currency risks flagged during v0.1 review. Add rows as changes are raised.)*

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
| Position revision | 0 | |
| New content | 0 | |
| Mapping update | 0 | OQ-5 will feed this |
| Evidence-register update | 0 | |

---

*Cross-references: [ADSRA Peer-Review Response Log](ADSRA_Peer-Review_Response_Log.md) · [ADSRA Five Open Questions](ADSRA_Five_Open_Questions.md). Source of truth for regulatory claims: Technical Reference §12 (Evidence Register).*
