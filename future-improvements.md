# CEA Tool — Future Improvements

## Completed

| # | Issue | Category | Date Fixed |
|---|-------|----------|------------|
| 1 | XSS in streaming output / error messages | Security | 2026-04-10 |
| 2 | SRI hashes on CDN scripts | Security | 2026-04-10 |
| 3 | `esc()` missing quote escaping | Security | 2026-04-10 |
| 4 | Retry with backoff on pipeline API calls | Robustness | 2026-04-10 |
| 5 | Greedy JSON regex replaced with tag-based extraction | Robustness | 2026-04-10 |
| 6 | Lenient JSON fallback for malformed `<cea-results>` | Robustness | 2026-04-10 |
| 7 | Proper two-ended tornado chart + Excel string fix | Methodology | 2026-04-11 |
| 8 | WHO-CHOICE thresholds updated to current supply-side methodology | Methodology | 2026-04-11 |
| 9 | GBD 2021 life expectancy table hardcoded in CEA prompt | Methodology | 2026-04-11 |
| 10 | Monitoring adjustment factor defined with methodology | Methodology | 2026-04-11 |
| 11 | Mixed intervention calculation path added | Methodology | 2026-04-11 |
| 12 | Parameter editing and re-run | UX | 2026-04-11 |
| 13 | Multi-intervention comparison view | UX | 2026-04-11 |
| 14 | Mobile sidebar hamburger menu | UX | 2026-04-11 |
| 15 | Conversation context restored on loaded analyses | UX | 2026-04-11 |
| 16 | Loading states on export buttons | UX | 2026-04-11 |
| 17 | History export/import + limit raised to 50 | UX | 2026-04-11 |
| 18 | Welcome textarea auto-resize | UX | 2026-04-11 |
| 19 | Word export now renders markdown tables | Export | 2026-04-11 |
| 20 | Word export Firefox/Safari download fix | Export | 2026-04-11 |
| 22 | PDF export via @media print + window.print() | Export | 2026-04-11 |
| 23 | Paper evaluator now has web search | Prompt Engineering | 2026-04-11 |
| 24 | Report agent respects output_format (cash vs DALY) | Prompt Engineering | 2026-04-11 |
| 25 | Counterfactual agent receives user-provided data | Prompt Engineering | 2026-04-11 |
| 26 | Casual "analyze" no longer triggers pipeline | Prompt Engineering | 2026-04-11 |
| 27 | GBD weights lazy-loaded from separate JSON file | Performance | 2026-04-11 |
| 28 | Multiple Chart.js instances supported | Performance | 2026-04-11 |
| 29 | Sub-agent model respects sidebar selection | Architecture | 2026-04-11 |

---

## Remaining

### Export Quality

**21. Excel formulas linking Parameters to Calculations**
Currently the Excel sheets contain disconnected static values. Linking them with formulas would make the Excel genuinely useful for scenario modeling. This is hard to automate because the parameter-to-calculation relationship is dynamic (the AI model determines which parameters exist and how they combine, varying by intervention type). Would require hardcoded formula templates per intervention type.
