[README_Accumulator_Drawdown.md](https://github.com/user-attachments/files/35111325/README_Accumulator_Drawdown.md)
# Accumulator Drawdown Test Simulator — README

**J. Alvarado | S. Siddhu, SOGE | Central**
File: `Accumulator_Drawdown_v2.html` · Version: v2 · Updated: 2026-11-19

## Purpose
Single-file training tool for the Class III BOPE accumulator (closing unit) drawdown test with an HCR valve on the choke line. Calculations, test sequence and pass criteria follow CalGEM Publication M07.

## How to run
1. Open `Accumulator_Drawdown_v2.html` in Chrome or Edge. No install or internet needed.
2. **Bottle bank:** set the number of bottles, bottle capacity, manufacturer's and measured precharge, working pressure and starting pressure.
3. **Class III stack:** pick the annular, pipe rams and HCR by manufacturer, model, size and working pressure (or tick **Manual**).
4. **Drawdown test:** isolate pump power, then close pipe rams → close annular → open pipe rams → open HCR within two minutes.
5. Restore power, enter recovery times for the pump test, complete the **Test Record** and print / save as PDF or Word.

## What it calculates (M-07)
| Item | Method |
|---|---|
| Gas volume at start | P1V1 = P2V2 (Eq. 1) |
| Pressure after each function | P2 = P1(V1/V2)^1.4 (Eq. 3) |
| Minimum pressure | Greater of 1,000 psi or precharge + 200 psi |
| Usable fluid | Fluid withdrawn down to the minimum pressure |
| Pass criterion (5-2a4c) | ≥ 1,000 psi (750 psi precharge) · ≥ 1,200 psi (1,000 psi precharge) |
| Pump test (5-2a6) | Closing volume ÷ recovery minutes ≥ 80% of rated output |

Checked against M-07: sample problem P2 = 1,145 psi, usable fluid 13.44 gal, margin 4.94 gal; Figure 10 Examples 2 and 3 = 17.61 and 24.64 gal.

## Main features
- **Control unit diagram:** Koomey schematic with 53 clickable item numbers, or the **Interactive unit** toggle — electric triplex, air pumps, pressure switches, valves 16 / 49 / 23 / 25 / 3, regulators, four-way valves, air side and remote panel, with animated fluid and air flow.
- **Four-way valve panel:** CLOSE / NEUTRAL / OPEN routing and why neutral is dangerous (M-07 3-3c).
- **BOP volumes:** 190 entries from the Cudd Well Control Technical Data Book (pp. 61–66); questionable source entries are flagged.
- **Chart:** M-07 Appendix F-style fluid moved vs. accumulator pressure for the bank entered.
- **Test record:** fills in as you go; field gauge readings can be entered and are used for the result.

## Defaults and sources
- Pump ratings (editable): electric triplex 10 HP, 4.55 gpm @ 3,000 psi; air pumps 7.80 / 7.20 / 6.40 gpm @ 1,200 / 2,000 / 3,000 psi — Koomey S&S Operator's Manual.
- Pressure switches: electric 3,000 / 2,750 psi; air 2,900 / 2,700 psi. Relief valves: 3,500 psi accumulator, 5,500 psi manifold.

## Limitations
- Equation (3) results are theoretical; actual adequacy is confirmed by the field test (5-2a4).
- Interactive unit: gas warms back after discharge, so slow runs read slightly above Eq. (3). Stroke rates and reservoir size are illustrative; blind rams use pipe-ram volumes.
- HCR volumes are not in M-07 (from the Cudd tables or user entry).
- The test record does not replace Division Form OGD9 (M-07 5-1f).

## Version history
| Version | Change |
|---|---|
| v1 | Bottle bank, M-07 calculations, Class III stack volumes, drawdown sequence, four-way valve panel, chart, pump test, test record |
| v2 | Interactive accumulator unit (hydraulics, pumps, air side, remote panel) with reference-picture toggle; credits updated |

Full details: `Accumulator_Drawdown_Guide.docx`.
