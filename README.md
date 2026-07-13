# ADSRA — Australian Digital Sovereignty Reference Architecture

**Author:** Duane · Enterprise Architect · **Status:** Draft **v0.1** — released for peer review · July 2026

> Residency asks *where is the data stored?* Sovereignty asks *who can be compelled to hand it over — and what could they actually produce?* ADSRA treats digital sovereignty as a **first-class enterprise architecture domain**, not a compliance checkbox.

ADSRA gives Australian regulated enterprises a way to leverage global cloud and AI platforms while retaining control over data, identity, cryptography, operations and AI — expressed as control domains, capabilities, reference patterns, a maturity model and measurable KRIs a Risk Committee can govern.

## The idea in one line

Seven sovereignty pillars · twenty fundable capabilities · a six-level maturity model ending in **autonomous sovereignty** · a small set of telemetry-derived KRIs — anchored to Australian regulatory obligations (APRA CPS 230/234, Privacy Act, SOCI, ISM) and the US CLOUD Act as a design variable.

## The pack

| Artefact | Audience | File |
|---|---|---|
| **Executive Briefing** (17 slides) | Board, Risk Committee, exec technology leadership | [`artefacts/ADSRA_Executive_Briefing.pptx`](artefacts/ADSRA_Executive_Briefing.pptx) |
| **Technical Reference** (~26 pp) | Engineering, architecture, security, risk | [`artefacts/ADSRA_Technical_Reference_v0.1.docx`](artefacts/ADSRA_Technical_Reference_v0.1.docx) |
| **White Paper** — *Sovereignty by Design* (~4,500 words) | Strategy and architecture readers | [`artefacts/ADSRA_White_Paper.docx`](artefacts/ADSRA_White_Paper.docx) |
| **Article Series** (6 articles) | LinkedIn / blog serialisation | [`artefacts/ADSRA_Article_Series.md`](artefacts/ADSRA_Article_Series.md) |
| **Web summary** (this repo's landing page) | Portfolio / thought leadership | [`index.html`](index.html) |

## Web page (GitHub Pages)

`index.html` is a self-contained, brand-styled single-page summary of ADSRA. To publish it:
**Settings → Pages → Build and deployment → Source: *Deploy from a branch* → `main` / `root`.** The page then serves at `https://<user>.github.io/ADSRA/`.

## Repository structure

```
ADSRA/
├── index.html                 # Web summary (GitHub Pages landing page)
├── artefacts/                 # Published v0.1 pack — do not overwrite
├── v0.2 Drafts/               # Working drafts + peer-review trackers
│   ├── ADSRA_Peer-Review_Response_Log.md
│   ├── ADSRA_Change_Register.md
│   └── ADSRA_Five_Open_Questions.md
├── Evidence/  Peer-Review/  Articles/  diagrams/   # Workstream folders
└── README.md
```

## Peer review — where challenge is most wanted

1. **Tier boundaries** — is four tiers right, or should Medium split into commercial-sensitive vs personal?
2. **HYOK guidance** — "surgical, not universal": bring the workload where the feature-loss trade was, or wasn't, worth it.
3. **Level 6 governance** — what evidence would convince a regulator that agentic remediation is itself well-governed?
4. **Technology mappings** — AU-region service capabilities evolve quarterly; corrections welcome.
5. **Missing blueprints** — utilities and education, deferred to v0.2; contributors invited.

Progress is tracked in `v0.2 Drafts/` via the Response Log, Change Register and Open Questions trackers.

## Rigour

Every regulatory claim is anchored to a primary source in the Technical Reference evidence register (§12). Author judgement is marked **[Position]**. Regulatory dates verified against APRA and OAIC primary sources as at 13 July 2026.

## Licence

[![Licence: CC BY-NC 4.0](https://img.shields.io/badge/Licence-CC%20BY--NC%204.0-C8A24B.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

© 2026 Duane. Licensed under [Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](LICENSE). You may share and adapt this work for **non-commercial** purposes with attribution; **commercial use requires permission**. Please cite as *Duane (2026), ADSRA — Australian Digital Sovereignty Reference Architecture, v0.1, CC BY-NC 4.0.*
