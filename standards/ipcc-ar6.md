# IPCC Sixth Assessment Report (AR6) — GreenCalculus Alignment

**Report:** IPCC Sixth Assessment Report  
**Published by:** Intergovernmental Panel on Climate Change (IPCC)  
**Working Groups:** WGI (2021), WGII (2022), WGIII (2022)  
**Report URL:** https://www.ipcc.ch/assessment-report/ar6/  
**GreenCalculus stack layer:** Layer 1 — Scientific Basis

---

## Role in GreenCalculus

The IPCC AR6 provides the scientific foundation for two critical
inputs to GreenCalculus calculations:

1. **GWP-100 values** — used to convert CH4, N2O, and F-gases to CO2e
2. **Climate science context** — used in "Why this matters" calculator copy

---

## GWP-100 values adopted from AR6

GreenCalculus uses AR6 GWP-100 values from **Table 7.SM.7**
(WGI Supplementary Material, Chapter 7).

Key values (see `data/gwp-values.json` for the full dataset):

| Gas | AR6 GWP-100 | Change from AR5 |
|---|---|---|
| CH4 (fossil) | 29.8 | +19.2% |
| CH4 (biogenic) | 27.9 | +11.6% |
| N2O | 273 | +3.0% |
| SF6 | 25,200 | +7.2% |

The increase in CH4 GWP from AR5 (25) to AR6 (29.8) is material.
Any organisation that has not updated to AR6 values is
underreporting methane-related emissions by approximately 19%.

---

## Adoption timeline

| Version | CH4 GWP-100 | Adopted by GreenCalculus |
|---|---|---|
| AR4 (2007) | 25 | Never |
| AR5 (2013) | 25 | Pre-2026 (legacy) |
| AR6 (2021) | 29.8 (fossil) | v2026.1 onwards |

---

## Key documents

| Document | URL |
|---|---|
| AR6 WGI Full Report | https://www.ipcc.ch/report/ar6/wg1/ |
| AR6 WGI Chapter 7 (GWPs) | https://www.ipcc.ch/report/ar6/wg1/chapter/chapter-7/ |
| AR6 WGIII (Mitigation) | https://www.ipcc.ch/report/ar6/wg3/ |

---

*GreenCalculus is not affiliated with the IPCC.*
