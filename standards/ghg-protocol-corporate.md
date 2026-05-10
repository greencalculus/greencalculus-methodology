# GHG Protocol Corporate Standard — GreenCalculus Alignment

**Standard:** GHG Protocol Corporate Accounting and Reporting Standard  
**Administered by:** World Resources Institute (WRI) & World Business Council for Sustainable Development (WBCSD)  
**Version in use:** 2026 revision  
**Standard URL:** https://ghgprotocol.org/corporate-standard  
**GreenCalculus stack layer:** Layer 1 — Core Accounting Framework

---

## What this standard defines

The GHG Protocol Corporate Standard is the world's most widely used
greenhouse gas accounting framework. It establishes:

- Definitions of Scope 1, Scope 2, and Scope 3 emissions
- Organisational boundary rules (equity share vs. control approaches)
- Operational boundary rules (what must vs. may be included)
- Reporting principles: relevance, completeness, consistency, transparency, accuracy

---

## How GreenCalculus applies it

### Scope definitions
Every GreenCalculus calculator is tagged to a GHG Protocol scope:

- **Scope 1** — Direct emissions from owned/controlled sources (stationary combustion, mobile combustion, process emissions, fugitive emissions)
- **Scope 2** — Indirect emissions from purchased electricity, steam, heat, or cooling
- **Scope 3** — All other indirect value chain emissions (15 categories)

### Organisational boundary
GreenCalculus calculators assume the **operational control** approach
unless the calculator explicitly states otherwise. Users applying the
equity share approach must adjust outputs accordingly.

### Biogenic CO2
Following GHG Protocol guidance, biogenic CO2 from biomass combustion
is reported separately and excluded from the Scope 1 total.
GreenCalculus fuel factors for biomass fuels reflect CH4 and N2O only
in their headline CO2e figure, with biogenic CO2 shown separately.

### GWP basis
GreenCalculus uses **IPCC AR6 GWP-100** values. The GHG Protocol
Corporate Standard permits AR5 or AR6; we use AR6 as the more current
basis. See `data/gwp-values.json`.

---

## Key documents

| Document | URL |
|---|---|
| Corporate Standard (full text) | https://ghgprotocol.org/corporate-standard |
| Scope 2 Guidance (2015) | https://ghgprotocol.org/scope_2_guidance |
| Corporate Value Chain (Scope 3) Standard | https://ghgprotocol.org/scope-3-standard |
| GHG Protocol website | https://ghgprotocol.org |

---

*This page documents GreenCalculus's alignment position. It is not
an official publication of WRI or WBCSD.*
