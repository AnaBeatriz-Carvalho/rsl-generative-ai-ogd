# Recovery Integration Report — corpus 29 → 36

**Round:** additional full-text retrieval + controlled integration (iSys major revision).
**Rule followed:** PDF recovered → eligibility → extraction → QA → classification → recomputation → synthesis →
manuscript. Every number below was **recomputed from the data files**, not mechanically substituted.
**Evidence base:** the 9 recovered PDFs (`recovered_fulltexts/` = 7 eligible; `recovered_fulltexts_excluded/` =
R010, R033), read in full before any edit.

> The earlier, reverted "29 → 31" migration was **not** reintroduced: R005 and R036 stay *not retrieved*; the
> corpus went to **36**, never 31/35/37.

---

## 1. Files changed

| File | Change |
|---|---|
| `busca_registros.csv` | 7 rows → `incluido` (CI1–CI5); R010/R033 → `excluido` (full-text, with reasons); venues/years filled from PDFs; R022 year 2026→2025. Tally now: 36 incluído, 10 não_recuperado, 10 excluído. |
| `resultado_extracao_rsl.txt` | +7 extraction blocks (RQ1–RQ5, AQ1–AQ5 w/ evidence, pages), same form as the 29. Now **36 blocks**. |
| `referencias_corpus.bib` | +7 entries (`Syahidi2025, Ryu2025, Kumar2024, Giarelis2026, Fang2023, Tsourma2025, GarciaMontero2025`); header 27→34. |
| `reports_not_retrieved_todo.md` | Rewritten: 10 still-unretrieved; 7 recovered+included; 2 recovered+excluded; integrity note updated. |
| `metodo_rsl.tex` | Extraction unit 29→36 (two places). |
| `resultados_rsl.tex` | PRISMA selection paragraph (retrieval round + 46/10/36/2/34), Table 1, geography paragraph+table, taxonomy Table 8 + figure, RQ1–RQ5 narratives, QA-stats paragraph. |
| `isys_rsl.tex` | Abstract PT/EN, Discussion, Threats (availability bias rewrite), Conclusion, QA appendix (+rows 30–36), consolidated table (+rows 30–36). |
| `response_letter.md` | Integrity note, Reviewer A "19 reports" item, new "Additional retrieval round" section, R010/R033 reasons; title header. |
| `revision_audit.md` | §6 addendum documenting this round. |
| **NOT changed** | Original search string, `busca_contagens.csv` (pre-retrieval counts), SBC/SOL flow, and all data of the original 29 studies. |

## 2. Seven studies added (consolidated-table IDs 30–36)

R001 Syahidi et al. 2025 · R006 Ryu et al. 2025 · R008 Kumar et al. 2024 · R009 Giarelis et al. 2026 ·
R011 Fang & Xu 2023 · R021 Tsourma et al. 2025 · R022 García-Montero et al. 2025.

## 3. Two recovered and excluded after full-text

- **R010 Baron (2025)** — no independent primary GenAI evidence: its GenAI part synthesizes the already-included
  Baron et al. 2023 (R012); "No datasets were generated or analysed during the current study." Double-counting.
  **Not** CE4/CE5.
- **R033 Tahtali et al. (2026)** — fails **CI1**: object is procurement professionals' acceptance/resistance of
  GenAI (TAM/TTF/TOE), not GenAI for access/organization/mediation of public-sector information. Not peer-review,
  not CE4/CE5.

## 4. Ten reports still not retrieved

R005, R014, R019, R020, R024, R028, R030, R031, R036, R043 (DOIs in `reports_not_retrieved_todo.md`).

## 5. New PRISMA counts (international) — source: `busca_registros.csv`

46 sought → **10** not retrieved → **36** assessed → **2** excluded after full-text → **34** included.
+ 2 SBC/SOL (flow unchanged) = **36**. Asserts: 46−10=36; 36−2=34; 34+2=36; 29+7=36; 10+9=19; 7+2=9. All hold.

## 6. Final corpus count

**36** (34 international + 2 SBC/SOL). Verified from `busca_registros.csv` and 36 blocks in
`resultado_extracao_rsl.txt`.

## 7. Quality assessment recomputed — source: extraction blocks + QA appendix (`tab:qa_estudos`)

New scores: R001 4.5 · R006 4.0 · R008 2.0 · R009 4.5 · R011 4.5 · R021 5.0 · R022 5.0.
Distribution over 36 (verified from the consolidated table QA column): 2.0×2, 3.0×1, 3.5×2, 4.0×5, 4.5×14, 5.0×12.
**Min 2.0 · Max 5.0 · Median 4.5 (unchanged) · 12 at 5.0 · 2 below 2.5** (Dineva & Atanasova 2025 = 2.0; TNGov-GPT
/ Kumar et al. 2024 = 2.0). The prior text ("median 4.5, ten at 5.0, one below threshold") was replaced, not
preserved.

## 8. Taxonomy recomputed — source: consolidated table (`tab:corpus_consolidado`) D1/D2/D3 columns

- **D1 (exclusive):** Supply/preparation **9**, Demand/access mediation **27**. (was 7 / 22)
- **D2 (exclusive):** Legislative-juridical **9**, OGD portals **12**, Services/procedures **9**, Policies/sectoral
  **5**, Conceptual **1**. (was 8 / 11 / 5 / 4 / 1)
- **D3 (non-exclusive):** all 7 fit existing functions (EX, EM, CT, GS, SI, OM). **No new category required.**
- **TAXONOMY REVIEW note:** R009's explainable-AI (XAI) layer was represented as generation (GS). It is a
  candidate for a dedicated "explanation/interpretability" function only if the pattern recurs (1 study does not
  justify a new category). No change made.

New-study placement: R011→(O, SP); R022→(O, OGD); R001→(D, SP); R006→(D, SP); R008→(D, SP); R009→(D, PS);
R021→(D, LJ). D1 aggregates verified (9 supply = 7 baseline + R011 + R022).

## 9. Geography recomputed — source: consolidated table country column + registry

Europe **15**, Asia **7**, North America **5**, South America **5**, Oceania **1**, Africa **0**,
Multi-region **1** (R006: Estonia/Singapore/EU), No national context **2** (Loukis conceptual + R001). Total 36.
Confident additions: Greece ×2 (R009, R021) and Ecuador (R022) → Europe/S.America; India (R008) and China (R011) →
Asia. **Flagged (human confirm):** R001 (no government named in the text — recorded "não especificado") and R006
(multi-region). Africa remains 0.

## 10. Models recomputed — source: extraction RQ3 + consolidated table

> **SUPERSEDED by the later RQ3 model-family recoding** (see `RQ3_MODEL_FAMILY_RECODING_REPORT.md`): the current
> distribution is proprietary 18 / open-weight 10 / multiple-comparative 2 / DialogFlow 2 / not reported 4. The
> 19/11/2/4 below reflects this earlier round before the coding rule was formalized.

GPT family (proprietary) **19** (+R001), open-weight **11** (+R008 GPT-2, R009 Llama-3.1, R011 Qwen, R021 Meltemi,
R022 open family), DialogFlow **2** (unchanged), not reported **4** (+R006, whose cross-national analysis
implements no single model; GPT-4 cited only as exemplar generator). Total 36. (was 18 / 6 / 2 / 3.)

## 11. Hallucination recomputed — source: extraction RQ5

Explicitly discussed in **24 of 36** (was 18/29): +R001, R006, R009, R011, R021, R022 (not R008).

## 12. Transparency / civic outcome recomputed

None of the 7 new studies measures a civic outcome (they report technical metrics, expert/usability assessment,
or secondary case metrics). The central finding holds and was re-verified: **none of the 36 studies** evaluates
transparency as an effective civic outcome. The four-level scheme (mention / acts-on-dimension / proxy / civic
outcome) still tops out at proxy for the new studies. "cerca de um terço" (HCI proxies) kept as an approximate
statement.

## 13. Abstract / Resumo sentences changed

PT & EN: "29 studies"→"36 studies"; "(18/29)"→"(19/36)"; "none of the 29 included studies"→"none of the 36
included studies". No number appears in the abstract that is not reproduced in Results.

## 14. Discussion changes

Demand/supply "22 of 29 / 7"→"27 of 36 / 9"; proprietary dependence "18 of 29"→"19 of 36" (two places);
model omission "three"→"four"; hallucination "18 of 29"→"24 of 36". New benefit evidence woven into RQ4
(R001 BLEU/human-eval; R006 63% hallucination reduction + operational gains). Central argument unchanged.

## 15. Threats to Validity changes

"Availability bias" rewritten: removed "no additional retrieval attempts were made"; now states the additional
round recovered 9/19 (7 included, 2 excluded), **risk reduced but not eliminated**, 10 remain and could still
shift distributions. Construct-validity and grey-literature bounds updated to "36".

## 16. Response Letter changes

Top integrity note; Reviewer A "19 reports" item rewritten (adapted from the provided template) with R010/R033
reasons; new "Additional full-text retrieval round" section; prior "frozen at 29" note reframed as superseded;
title header aligned.

## 17. Compilation result

`latexmk -xelatex` → **exit 0**; **0 undefined citations; 0 undefined references**; **23 pages** (was 21).
3 overfull hboxes ≤66pt, all in the frontmatter (dates/abstract), pre-existing — the expanded QA and consolidated
tables did **not** overflow. All 7 new bib keys resolve.

## 18. Points requiring human review

1. **PRISMA figure** `imagens/fluxograma_prisma.png` — **RESOLVED**: replaced manually (corrected flow
   46→10→36→2→34); verified as the referenced file in the pre-merge pass (see `FINAL_PREMERGE_VALIDATION.md`).
2. **R022 year** — **RESOLVED**: validated as **2026** (Springer CCIS chapter; TICEC 2025 event; pp. 63–77);
   BibTeX key renamed `GarciaMontero2025` → `GarciaMontero2026`. Within 2024–2026, so no count changed.
3. **Proceedings names** — **RESOLVED**: `GarciaMontero2026` = "Information and Communication Technologies
   (TICEC 2025)", CCIS, pp. 63–77; `Giarelis2026` = "Electronic Government (EGOV 2025)", LNCS 15944, pp. 368–379.
4. **R001 government context** (none named in the text — "não especificado") and **R006 multi-region**
   (explicitly analyzes Estonia/Singapore/EU) — reviewed and retained in the pre-merge pass.
5. **R022 model label**: recorded as open-weight (study's emphasis; it also compares 2 proprietary models) —
   confirm the intended "main model" convention for comparison studies.
6. **Visual PDF inspection** (page breaks, table layout, highlights, the new PRISMA raster) — not possible here
   (no poppler); recommended before resubmission, as in `07_visual_pdf_audit.md`.
