# Final Pre-Merge Validation — iSys Major Revision (corpus = 36)

**Scope:** verification pass over the completed 29→36 integration, plus a few authorized finalizations
(R022 year/key, R009 venue, PRISMA-comment updates). No recovery re-run, no re-extraction, no eligibility change,
no new taxonomy category, no new search. Nothing committed.

## 1. Files modified in this pass
| File | Change |
|---|---|
| `referencias_corpus.bib` | Key `GarciaMontero2025`→`GarciaMontero2026`; year 2025→2026; venue "Information and Communication Technologies (TICEC 2025)", CCIS, pp. 63–77. `Giarelis2026` venue → "Electronic Government (EGOV 2025)", LNCS 15944, pp. 368–379. Header comment key updated. |
| `resultados_rsl.tex` | 3 citation keys `GarciaMontero2025`→`GarciaMontero2026`; PRISMA source-comment updated (image now replaced, not "to regenerate"). |
| `busca_registros.csv` | R022 year 2025→2026; venue + note updated (validated 2026, pp. 63–77). |
| `isys_rsl.tex` | Consolidated table row 36 year 2025→2026; QA table row 36 "(2025)"→"(2026)". |
| `response_letter.md` | A3 hallucination "18/29 → 24/36"; C3 heading "36 studies"; grey-lit bound "36"; prior human-action item marked resolved (PRISMA replaced; year/venue fixed). |
| `revision_audit.md` | New §7 pre-merge addendum (items resolved; kept §6 as prior state). |
| `RECOVERY_INTEGRATION_REPORT.md` | Human-review items 1–3 marked resolved. |
| **NOT changed** | Corpus decisions, extraction, QA scores, taxonomy, search string, the 29 originals. |

## 2. Manually replaced PRISMA image — confirmation
- Referenced in `resultados_rsl.tex:31`: `\includegraphics[width=0.75\textwidth]{imagens/fluxograma_prisma.png}`.
- File `imagens/fluxograma_prisma.png` mtime **2026-08-22T11:40** (after my prior build 11:24); `git status` shows
  it **Modified** — i.e., you replaced it. It is embedded on compile (build ran after the replacement).
- **Limitation:** this environment has no poppler/pdftoppm/pdftotext, so I **cannot rasterize the page to read the
  figure's pixels**. I confirm the *reference*, the *fresh mtime*, and that it embeds; I did **not** visually read
  the numbers inside the raster. Visual confirmation of the figure content remains a human step.

## 3. Expected visible PRISMA counts (what the replaced figure must show)
International: Scopus 453 / ACM 445 / IEEE 224 / WoS 143 = **1,265** → 805 unique (460 removed) → **46 sought**,
759 excluded at title/abstract → **36 recovered / 10 not retrieved** → **36 assessed / 2 excluded / 34 included**.
SBC/SOL: 23 → 23 unique → 14 excluded by title → 9 full-text → 7 excluded / **2 included**. **Final = 34 + 2 = 36.**
Two full-text exclusions: **R010** (no independent primary GenAI evidence; already represented by Baron et al.
2023; not CE4/CE5) and **R033** (fails CI1; acceptance/resistance study). If the compiled PDF still shows 19 not
retrieved / 27 assessed / 27 international / 29 final, the old raster is cached — see §13 (it is not, per mtime).

## 4. R022 final metadata + temporal impact
García-Montero, Orellana, Zambrano-Martinez; DOI 10.1007/978-3-032-08366-1_5; **year 2026** (Springer CCIS chapter;
event TICEC 2025); "Information and Communication Technologies", CCIS, **pp. 63–77**; key **`GarciaMontero2026`**.
**Temporal recomputation (from `busca_registros.csv`):** included-study years = 2021×1, 2023×7, 2024×8, 2025×14,
2026×6 (= 36). **2024–2026 = 28/36**; none before 2021; range 2021–2026. Moving R022 from 2025 to 2026 shifts only
2025 (15→14) and 2026 (5→6); it does **not** change the manuscript's only year statement ("28 no triênio
2024–2026", "nenhum anterior a 2021"). No other statistic depends on year, so nothing else changed.

## 5. R009 final bibliographic metadata
Giarelis, Mastrokostas, Siachos, Karacapilidis; year **2026**; DOI 10.1007/978-3-032-01589-1_23;
**"Electronic Government (EGOV 2025)", LNCS vol. 15944, Springer, pp. 368–379**. Placeholder booktitle removed.
Eligibility/extraction/QA/taxonomy unchanged.

## 6. R001 geographic decision
**Kept "não especificado / no national context."** The full text names no government/country for its FAQ dataset;
inference from author affiliation (Thailand/Japan) was explicitly avoided. Counted under "sem contexto nacional
específico" (with Loukis), not in any region.

## 7. R006 geographic decision
**Kept "multi-region."** The full text explicitly analyzes government contexts in **Estonia, Singapore, and the
EU** (Europe + Asia + supranational). Not forced into Europe or Asia. The manuscript geography paragraph defines
it ("Um estudo transnacional analisa conjuntamente Estônia, Singapura e União Europeia, cobrindo mais de uma
região") and the table row is "Multinacional / multirregião = 1".

## 8. Aggregate-statistics verification (from data/tables, not prose)
| Quantity | Expected | Verified | Source |
|---|---|---|---|
| Corpus / intl / SOL | 36 / 34 / 2 | **36 / 34 / 2** | `busca_registros.csv` |
| Extraction blocks | 36 | **36** | `resultado_extracao_rsl.txt` |
| Not retrieved | 10 | **10** | CSV |
| New included / recovered-excluded | 7 / 2 | **7 / 2** | CSV |
| Models (family) | 19/11/2/4 at this pass — **SUPERSEDED** | later recoded to **proprietary 18 / open 10 / multiple-comparative 2 / DialogFlow 2 / not reported 4** (see `RQ3_MODEL_FAMILY_RECODING_REPORT.md`) | Table 1 + extraction |
| Empirical / conceptual | 28 / 8 | **28 / 8** (prose/Table 1) | Table 1 |
| Hallucination | 24/36 | **24/36** | RQ5 |
| D1 supply/demand | 9 / 27 | **9 / 27** | consolidated col D1 |
| D2 LJ/OGD/serv/sect/conc | 9/12/9/5/1 | **9/12/9/5/1** | consolidated col D2 |
| QA min/max/median | 2.0/5.0/4.5 | **2.0/5.0/4.5** | QA appendix |
| QA at 5.0 / below 2.5 | 12 / 2 | **12 / 2** (2.0×2,3.0,3.5×2,4.0×5,4.5×14,5.0×12) | QA appendix |
| Civic outcome | 0/36 | **0/36** | extraction + narrative |

Note: the consolidated **Aval** column (TECH 13 / USER 7 / MIX 5 / DEMO 5 / CONC 6) is a finer granularity than
the prose empirical(28)/conceptual(8) split — the same two-level design as the original 29-study baseline; not a
contradiction. **No discrepancy found**; no expected value was forced.

## 9. Geography consistency
Europe **15**, Asia **7**, North America **5**, South America **5**, Oceania **1**, Africa **0**, multi-region
**1**, no-context **2**. Assert 15+7+5+5+1+0+1+2 = **36** ✓ (matches `tab:geografia`). No forced correction.

## 10. Reviewer A response verification
Reviewer A "19 reports" item now states: an additional retrieval round was conducted for all 19; nine recovered;
original CI/CE reapplied unchanged; **7 included, 2 excluded after full-text**; 10 remained unavailable; PRISMA,
extraction, QA, synthesis and availability-bias updated. Route wording uses **"as applicable"** (no claim that
every route was used for every report). The old "no additional retrieval was performed" wording is gone.

## 11. Reviewer C response verification
Present and intact: taxonomy dimensions + definitions + exclusivity rules; geography table (updated); consolidated
study table (36 rows); QA appendix (36 rows); explicit coding process; SBC/SOL flow (unchanged); Semantic Web ↔
GenAI framed as **complementary** (fig:paradigmas); acronyms/terminology consistent. No prior reviewer revision
undone. Scope remains **Public-Sector Information** with OGD as paradigmatic subset; sociotechnical transparency +
four analytical levels preserved; central conclusion "none of the 36 evaluates a civic outcome" holds.

## 12–13. Compilation + LaTeX validation
Command: `latexmk -C isys_rsl.tex && latexmk -xelatex -interaction=nonstopmode -halt-on-error isys_rsl.tex`.
**Exit code 0.** **Undefined citations: 0. Undefined references: 0. Fatal errors: 0.** 23 pages. `GarciaMontero2025`
has 0 leftovers; `GarciaMontero2026` resolves. 3 overfull hboxes ≤66pt, all frontmatter (dates/abstract),
pre-existing; expanded QA and consolidated tables do not overflow.

## 14. Final assertions
29+7=36 ✓ · 46−10=36 ✓ · 36−2=34 ✓ · 34+2=36 ✓ · 10+9=19 ✓ · 7+2=9 ✓. R010 excluded ✓ · R033 excluded ✓ ·
R005 not retrieved ✓ · R036 not retrieved ✓. No corpus size 31/35/37 anywhere in visible text ✓. No visible
manuscript PRISMA state of 19 not retrieved / 27 assessed / 27 international / 29 final (source `.tex` clean;
raster is the freshly-replaced file) ✓.

## 15. Remaining human-review items
1. **Visual confirmation of the PRISMA raster** — I cannot render pages here (no poppler); please eyeball that
   `imagens/fluxograma_prisma.png` shows 1,265 → 805 → 46 → 36 recovered/10 not retrieved → 36 assessed/2 excluded/
   34 included (+ 2 SBC/SOL = 36), and that it is not cropped and reads clearly at 0.75\textwidth.
2. **R022 model-label convention** — recorded as open-weight (study emphasizes open-source viability; it also
   tests 2 proprietary models). Confirm the intended "main model" rule for comparison studies.
3. General visual pass of the two wide appendix tables and `\rev{}` highlights in the compiled PDF before merge.
