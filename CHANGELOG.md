# Changelog — GreenCalculus Methodology Dataset

All methodology and dataset changes are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
Versioning follows CalVer: `YYYY.N` (e.g. `2026.1`).

A **breaking change** is any factor value change > 5%, or any
change to scope definitions, GWP basis, or calculation architecture.

---

## [2026.1] — 2026-05-10

### Added
- Initial public release of the GreenCalculus methodology dataset
- `METHODOLOGY.md` — formal white-paper-style methodology document
- `EMISSION-FACTORS.md` — human-readable factor catalogue
- `data/gwp-values.json` — IPCC AR6 GWP-100 values for 16 gases
- `data/emission-factors.json` — Scope 1 stationary combustion (12 fuels) and Scope 2 electricity (15 countries)
- `data/emission-factors.csv` — spreadsheet-friendly version of emission factors
- `standards/ghg-protocol-corporate.md` — GHG Protocol Corporate Standard alignment
- `standards/ghg-protocol-scope3.md` — GHG Protocol Scope 3 Standard alignment
- `standards/ghg-protocol-lsr-2026.md` — Land Sector and Removals Standard (2026) alignment
- `standards/ipcc-ar6.md` — IPCC AR6 GWP basis documentation
- `standards/iea-2026.md` — IEA 2026 grid factor source documentation
- `schema-examples/webapplication.json` — WebApplication JSON-LD template
- `schema-examples/dataset.json` — Dataset JSON-LD template
- `schema-examples/howto.json` — HowTo JSON-LD template
- `CITATION.cff` — BibTeX/APA citation file

### Methodology positions established
- GWP basis: IPCC AR6 GWP-100 (supersedes AR5)
- CH4 fossil GWP: 29.8 (was 25 under AR5 — +19.2%)
- CH4 biogenic GWP: 27.9 (was 25 under AR5 — +11.6%)
- Biogenic CO2 excluded from Scope 1 headline per GHG Protocol
- Organisational boundary default: operational control approach
- Land sector: GHG Protocol LSR 2026 adopted (published 30 Jan 2026)

---

## Future releases

Planned for 2026.2 (Q3 2026):
- Scope 3 Category 6 (business travel) factors — air, rail, hotel
- Scope 3 Category 7 (employee commuting) factors
- Additional grid emission factors (Middle East, Africa expansion)
- UK DESNZ 2025 factors when published
