# ADSRA — Design System Localisation

Localises the portable **Getamazednow AI Design System v1.1** (see `Getamazednow AI Design System v1.1/LOCALISE.md`) for this project. The design-system folder stays generic and byte-identical to the master; ADSRA's project-specific values live **here**.

## 1. Artefact / product name

**ADSRA** — Australian Digital Sovereignty Reference Architecture.
Shown as: web topbar `Getamazednow AI · Digital Sovereignty Reference Architecture`; running headers `Getamazednow AI  ·  <artefact> · ADSRA v0.1`; covers as the ADSRA title beneath the logo lockup.

Artefacts in scope: Executive Briefing (deck), Technical Reference (docx), White Paper (docx), Article Series (md), Web summary (`index.html`).

## 2. Version + status

Current cycle: **v0.1 → v0.2**. Status line on every cover/footer: **DRAFT — FOR PEER REVIEW**. Version lives inside the document (cover + footer), not in file/folder names (see style guide §2).

## 3. Legacy colour remap (ADSRA-specific)

ADSRA's original artefacts were navy/gold. This is the remap actually applied to bring them onto the palette (uses `artefactApplication.colourRemap` as the template):

| Legacy (ADSRA) | → | Getamazednow AI |
|---|---|---|
| `142A4C`, `1A2433`, `1F3A63` | → | Ink `2A363B` |
| `C8A24B` (gold), `2E74B5`, `1F4D78`, `3D5A80` | → | signalDeep `2E7DA6` |
| `5B6B80` | → | neutral-500 `6B797E` |
| `F4F6F9` | → | neutral-50 `F6F7F7` |
| `D5DCE6`/`D9E4F0`/`E1E6EE` → `EBEDEE`; `AFC1DA` → `D5DADB`; `9FB0C8` → `B7BEC2` | → | neutral ramp |
| `8E2C2C`/`2E6B4F`/`8A6E2F` | → | error `A02E2E` / success `2C6644` / warning `A85A16` |

Fonts: Cambria → Poppins, Calibri → Inter.

## 4. Cover image (hybrid image strategy)

ADSRA uses the design system's **hybrid image strategy** (Artefact-Application-Spec §7/§8) to swap the generic `Getamazednow-AI-Hero-Lattice` / `Slide-BG-Ink` defaults for a **project-specific topic image**. The image is dark-toned (Ink field) so a reversed logo and title stay legible, and it is built only from brand tokens (Ink `2A363B`, Signal `5FA8CC`, signalDeep `2E7DA6`, signalCore `8FC3DE`, Stone `A8A17B`).

**Concept (current — Theme 3, selected 15 Jul 2026):** a **sovereign control room / operations centre** — a curved video wall carrying a node-lattice map of Australia, dashboards and a globe, over an operator desk. Reads as "Australian digital sovereignty, operated and governed". Sourced from `ADSRA_Option_3_*_TEXTLESS.png`; docs use the Whitepaper crop, the deck uses the 16:9 with a left Ink scrim for the title-safe zone.

*Prior concept (superseded):* a Tensor-style node-lattice map of Australia with a central sovereignty shield + keyhole and a Southern Cross accent.

Files (project-owned, in `brand-assets/`):

| File | Ratio | Used by |
|---|---|---|
| `ADSRA-Cover-Hero.png` / `.svg` | 1.6:1 | Document covers — framed lower-hero card (W2) |
| `ADSRA-Slide-BG.png` / `.svg` | 16:9 | Deck title slide — full-bleed behind an Ink scrim (map right, title-safe left) |

**Variant choices recorded:** White Paper & Technical Reference covers = **W2 (framed lower hero)**; Executive Briefing title slide = **P2 (corner lockup + topic image override)**. Content slides keep the quiet-footer treatment. The design-system `Logo Files/` defaults are untouched — this is a project swap only.

## 5. Reference implementation

The ADSRA **v0.2 pack** in `v0.2 Drafts/` (Executive Briefing, Technical Reference, White Paper) and the web summary `index.html`. These are the worked examples of the design system applied to ADSRA, now carrying the §4 topic image on their covers.

---

*Source of truth for brand + application rules: `Getamazednow AI Design System v1.1/` (`design-tokens.json`, `Artefact-Application-Spec.md`). This file localises it for ADSRA only.*
