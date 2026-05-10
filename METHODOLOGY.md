# GreenCalculus Methodology — Formal Reference

**Version:** 2026.1  
**Published:** 2026-05-10  
**Author:** Jeremiah Say, Lead Systems Architect, GreenCalculus  
**License:** See LICENSE  
**Canonical URL:** https://greencalculus.com/methodology/

---

## 1. Scope and Purpose

This document defines the calculation methodology underpinning all
GreenCalculus carbon and environmental calculators. It is intended
as a citable reference for sustainability officers, CSRD compliance
teams, academic researchers, and ESG auditors who require transparency
into the mathematical and scientific basis of GreenCalculus outputs.

All calculators on GreenCalculus.com produce results in tonnes of
CO₂ equivalent (tCO₂e) unless explicitly stated otherwise.

---

## 2. Governing Standards

GreenCalculus methodology is grounded in the following authoritative
standards. Where standards conflict, we apply the hierarchy listed.

| Priority | Standard | Body | Version |
|---|---|---|---|
| 1 | GHG Protocol Corporate Accounting and Reporting Standard | WRI / WBCSD | 2026 revision |
| 2 | GHG Protocol Scope 3 Standard | WRI / WBCSD | 2011 (current) |
| 3 | GHG Protocol Land Sector and Removals Standard | WRI / WBCSD | 2026 (published 30 Jan 2026) |
| 4 | IPCC Sixth Assessment Report (AR6) | IPCC | 2021–2022 |
| 5 | IEA Global Energy Review | IEA | 2026 |

---

## 3. Global Warming Potential (GWP) Values

All GreenCalculus calculators use **IPCC AR6 GWP-100** values for
converting non-CO₂ gases to CO₂ equivalent. These supersede the
AR5 values previously used across the industry.

| Gas | AR6 GWP-100 | AR5 GWP-100 | Change |
|---|---|---|---|
| CO₂ | 1 | 1 | — |
| CH₄ (fossil) | 29.8 | 25 | +19.2% |
| CH₄ (biogenic) | 27.9 | 25 | +11.6% |
| N₂O | 273 | 265 | +3.0% |
| HFC-134a | 1526 | 1430 | +6.7% |
| SF₆ | 25,200 | 23,500 | +7.2% |

Source: IPCC AR6 WGI Table 7.SM.7  
Machine-readable values: `data/gwp-values.json`

---

## 4. Emission Factor Sources

### 4.1 Stationary Combustion (Scope 1)

Fuel emission factors are sourced from:
- UK DESNZ/DBET Conversion Factors (2024, updated annually)
- US EPA Emission Factors for Greenhouse Gas Inventories (2024)
- IPCC 2006 Guidelines for National Greenhouse Gas Inventories

Factors are expressed as kg CO₂e per unit of fuel consumed (litre,
tonne, MWh, or m³ depending on fuel type). Both gross calorific
value (GCV) and net calorific value (NCV) variants are provided
where the source distinguishes them.

### 4.2 Electricity (Scope 2)

Grid emission factors follow the **market-based** and
**location-based** dual-reporting approach mandated by the GHG
Protocol Scope 2 Guidance (2015).

Location-based factors are sourced from:
- IEA Global Energy Review 2026 (international grids)
- US EPA eGRID 2023 (US sub-regional grids)
- UK DESNZ (UK national and regional)

### 4.3 Scope 3 Categories

Scope 3 emission factors follow GHG Protocol Scope 3 Standard
category definitions (Categories 1–15). Spend-based factors are
sourced from the UK DESNZ environmentally extended input-output
(EEIO) tables and the US EPA Supply Chain GHG Emission Factors.

---

## 5. Calculation Architecture

### 5.1 Core Formula

All GreenCalculus calculators apply the following base formula:

Emissions (tCO₂e) = Activity Data × Emission Factor × GWP

Where:
- **Activity Data** = measured quantity (litres, kWh, km, £, etc.)
- **Emission Factor** = kg CO₂e per unit of activity (sourced per §4)
- **GWP** = 1 for factors already expressed in CO₂e; otherwise AR6 value

### 5.2 Unit Handling

All internal calculations are performed in SI base units before
display conversion. Currency-based factors use the year of the
source dataset; calculators display the base year prominently.

### 5.3 Precision and Rounding

Raw outputs are computed to full floating-point precision.
Display rounding is applied at the final output step only:
- Results ≥ 1 tCO₂e: 2 decimal places
- Results < 1 tCO₂e: 4 decimal places
- Never round intermediate values

---

## 6. Scope Definitions

Following GHG Protocol Corporate Standard:

**Scope 1** — Direct emissions from owned or controlled sources
(combustion, process emissions, fugitive emissions, company vehicles).

**Scope 2** — Indirect emissions from purchased electricity, steam,
heat, or cooling.

**Scope 3** — All other indirect emissions in the value chain,
upstream and downstream (15 categories per GHG Protocol Scope 3 Standard).

---

## 7. Land Sector and Carbon Removals

Calculations involving land use change, forestry, or carbon removal
follow the **GHG Protocol Land Sector and Removals Standard (2026)**.
This standard was published 30 January 2026 and supersedes previous
guidance on agricultural land management and biological carbon removal.

Key methodological positions:
- Permanence risk adjustments applied to all biological removal claims
- Additionality assessed against national baseline scenarios
- No netting of removals against Scope 1/2/3 emissions without
  explicit disclosure

---

## 8. Data Provenance and Versioning

Every emission factor in the GreenCalculus dataset carries:
- Source document name and URL
- Source publication year
- GreenCalculus dataset version it entered
- SHA-256 hash of the source workbook where available

Full machine-readable provenance: `data/emission-factors.json`

Dataset versioning follows **CalVer**: `YYYY.N` (e.g. `2026.1`).
Breaking changes (factor value changes > 5%) trigger a major version bump.

---

## 9. Changelog

See `CHANGELOG.md` for a full record of methodology changes,
including which calculators were affected by each update.

---

## 10. Citation

If you use this methodology in research or reporting, please cite
using the `CITATION.cff` file in this repository. GitHub renders
a "Cite this repository" button in the sidebar for one-click
BibTeX and APA export.

---

*GreenCalculus is an independent platform. It is not affiliated with
WRI, WBCSD, IPCC, or IEA. Standard citations reference the original
authoritative sources; GreenCalculus applies those standards in its
calculation engine.*
