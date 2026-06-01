<div align="center">

<img src="https://raw.githubusercontent.com/greencalculus/.github/main/profile/assets/greencalculus-logo.png" width="72" height="72" alt="GreenCalculus" />

# GreenCalculus Methodology & Emission Factor Dataset

### The transparent, citable source for our carbon-accounting math.

[greencalculus.com](https://greencalculus.com) · [Standards](https://github.com/greencalculus/greencalculus-standards) · [Live demos](https://greencalculus.github.io/greencalculus-calculator-demo/) · [**Cite this repo**](https://github.com/greencalculus/greencalculus-methodology/blob/main/CITATION.cff)

![GHG Protocol](https://img.shields.io/badge/GHG_Protocol-Corporate_·_Scope_3_·_LSR_2026-04BF62?style=flat-square)
![IPCC AR6](https://img.shields.io/badge/IPCC_AR6-GWP--100-04BF62?style=flat-square)
![Dataset](https://img.shields.io/badge/Dataset-CalVer_2026.1-04BF62?style=flat-square)
![License: MIT](https://img.shields.io/badge/License-MIT-04BF62?style=flat-square)

</div>

---

**The formal methodology, emission factor datasets, and GHG Protocol
alignment documentation underpinning [GreenCalculus.com](https://greencalculus.com).**

Built for sustainability officers, CSRD compliance teams, ESG auditors,
and academic researchers who need a transparent, citable source for
carbon accounting methodology.

→ **[Cite this repository](https://github.com/greencalculus/greencalculus-methodology/blob/main/CITATION.cff)**
— GitHub renders a one-click BibTeX/APA export in the sidebar.

---

## What's in this repo

### 📄 Core documents
| File | Description |
|---|---|
| [`METHODOLOGY.md`](METHODOLOGY.md) | White-paper-style formal methodology — GWP basis, scope definitions, calculation architecture, data provenance |
| [`CITATION.cff`](CITATION.cff) | Cite this repository in BibTeX or APA with one click |
| [`CHANGELOG.md`](CHANGELOG.md) | Full record of methodology and factor changes by version |

### 📊 Data (`data/`)
| File | Description |
|---|---|
| [`data/gwp-values.json`](data/gwp-values.json) | IPCC AR6 GWP-100 values for 16 gases — machine-readable |
| [`data/emission-factors.json`](data/emission-factors.json) | Scope 1 (12 fuels) + Scope 2 (15 countries) — JSON |
| [`data/emission-factors.csv`](data/emission-factors.csv) | Same data — spreadsheet-friendly CSV |

### 📋 Standards alignment (`standards/`)
| File | Standard |
|---|---|
| [`standards/ghg-protocol-corporate.md`](standards/ghg-protocol-corporate.md) | GHG Protocol Corporate Standard |
| [`standards/ghg-protocol-scope3.md`](standards/ghg-protocol-scope3.md) | GHG Protocol Scope 3 Standard (15 categories) |
| [`standards/ghg-protocol-lsr-2026.md`](standards/ghg-protocol-lsr-2026.md) | GHG Protocol Land Sector & Removals Standard (2026) |
| [`standards/ipcc-ar6.md`](standards/ipcc-ar6.md) | IPCC AR6 GWP-100 basis |
| [`standards/iea-2026.md`](standards/iea-2026.md) | IEA Global Energy Review 2026 grid factors |

### 🔧 Schema templates (`schema-examples/`)
| File | Description |
|---|---|
| [`schema-examples/webapplication.json`](schema-examples/webapplication.json) | JSON-LD template for carbon calculator pages |
| [`schema-examples/dataset.json`](schema-examples/dataset.json) | JSON-LD template for emission factor data pages |
| [`schema-examples/howto.json`](schema-examples/howto.json) | JSON-LD template for reporting guide pages |

---

## Key methodology positions

| Topic | Position |
|---|---|
| GWP basis | IPCC AR6 GWP-100 |
| CH₄ (fossil) GWP | 29.8 (AR5 was 25 — +19.2%) |
| CH₄ (biogenic) GWP | 27.9 |
| N₂O GWP | 273 |
| Biogenic CO₂ | Excluded from Scope 1 per GHG Protocol |
| Org boundary default | Operational control approach |
| Land sector | GHG Protocol LSR 2026 (published 30 Jan 2026) |
| Dataset versioning | CalVer — `YYYY.N` |

---

## Governing standards hierarchy

1. GHG Protocol Corporate Standard (2026 revision)
2. GHG Protocol Scope 3 Standard (2011, current)
3. GHG Protocol Land Sector & Removals Standard (2026)
4. IPCC AR6 (scientific basis, GWP values)
5. IEA Global Energy Review 2026 (grid factors)

---

## How to use the data

**Direct download (JSON):**

https://raw.githubusercontent.com/greencalculus/greencalculus-methodology/main/data/emission-factors.json

**Direct download (CSV):**

https://raw.githubusercontent.com/greencalculus/greencalculus-methodology/main/data/emission-factors.csv

**GWP values:**

https://raw.githubusercontent.com/greencalculus/greencalculus-methodology/main/data/gwp-values.json

---

## Dataset version

**Current:** `2026.1` — published 2026-05-10  
**Next planned:** `2026.2` (Q3 2026) — Scope 3 Categories 6 & 7, expanded grid factors

---

## License

MIT License. See [LICENSE](LICENSE).  
If you use this methodology in research or reporting, please cite via
the [CITATION.cff](CITATION.cff) file.

---

## About GreenCalculus

[GreenCalculus.com](https://greencalculus.com) is the traceable reference layer for
corporate carbon accounting — high-precision calculators built for sustainability
officers, engineers, and corporate compliance teams, every result traceable to a
published factor and a named standard.

**Built and maintained by [Jeremiah Say](https://greencalculus.com/about/jeremiah-say/)**
— Lead Systems Architect · GHG Protocol · IPCC AR6 · CSRD/ESRS E1 · SBTi · PCAF
