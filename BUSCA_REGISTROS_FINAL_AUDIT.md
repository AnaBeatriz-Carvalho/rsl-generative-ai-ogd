# busca_registros.csv — Final Audit (Major Revision, pre-commit)

Cleanup/reconciliation pass on the corpus-of-record spreadsheet only. **Only `busca_registros.csv` was
edited.** No manuscript, PRISMA, QA, taxonomy, RQ1–RQ5, Response Letter or cover-letter change; no new
studies fetched; corpus size, eligibility and decisions unchanged. Nothing committed.

Authoritative internal sources used, in priority order: recovered/full-text PDFs → `referencias_corpus.bib`
→ validated manuscript → `resultado_extracao_rsl.txt` → recovery/audit reports → original Rayyan export.
No web search. No metadata invented.

Delimiter note: `busca_registros.csv` is `;`-delimited. To keep it machine-parseable, none of the resolved
values introduce a literal `;`; the `base_origem` wording uses an em-dash instead. Every row now parses to
exactly 13 fields (quote-aware check), including the four legitimately quoted rows (SOL05/06/09, R047).

---

## 1–3. `[A CONFIRMAR]` rows — old value → final value → source

### 3a. `veiculo` / `tipo_veiculo` resolved from `referencias_corpus.bib` (priority 2)

| id | field(s) | old | final | source |
|---|---|---|---|---|
| R012 | veiculo/tipo | `[A CONFIRMAR]` | `CEUR Workshop Proceedings (LegalAIIA 2023), vol. 3423` / `workshop` | bib `Baron2023` |
| R015 | veiculo/tipo | `[A CONFIRMAR]` | `Proceedings of the 27th Pan-Hellenic Conference on Progress in Computing and Informatics (PCI)` / `conferencia` | bib `ScotlandChatGPT2024` |
| R027 | veiculo/tipo | `[A CONFIRMAR]` | `Proceedings of the 2023 International Conference on Big Data and Information Education (ICBDIE)` / `conferencia` | bib `Gao2023` — **see §7 HUMAN REVIEW** |
| R029 | veiculo/tipo | `[A CONFIRMAR]` | `2024 Fifth International Conference on Intelligent Data Science Technologies and Applications (IDSTA)` / `conferencia` | bib `TAGIFY2025` |
| R032 | veiculo/tipo | `[A CONFIRMAR]` | `Proceedings of the 2025 International Conference on Generative Artificial Intelligence for Business (GAIB)` / `conferencia` | bib `Gong2025` |
| R034 | veiculo/tipo | `[A CONFIRMAR]` | `Proceedings of the 6th ACM Conference on Conversational User Interfaces (CUI)` / `conferencia` | bib `ConversationalInterfaces2024` |
| R035 | veiculo/tipo | `[A CONFIRMAR]` | `2024 International Conference on Intelligent Cybernetics Technology and Applications (ICICyTA)` / `conferencia` | bib `Ingole2024` |
| R037 | veiculo/tipo | `[A CONFIRMAR]` | `Proceedings of the 22nd Annual International Conference on Digital Government Research (DG.O)` / `conferencia` | bib `ChatbotMadrid2021` |
| R038 | veiculo/tipo | `[A CONFIRMAR]` | `International Multidisciplinary Scientific GeoConference SGEM` / `conferencia` | bib `Dineva2025` |
| R039 | veiculo/tipo | `[A CONFIRMAR]` | `2025 IEEE International Conference on Emerging Trends in Computing and Communication (ETCOM)` / `conferencia` | bib `Nagesh2025` |
| R040 | veiculo/tipo | `[A CONFIRMAR]` | `Proceedings of the 2025 Conference on Conversational User Interfaces (CUI)` / `conferencia` | bib `HeyGoogleTaxes2025` |
| R041 | veiculo/tipo | `[A CONFIRMAR]` | `Proceedings of the 28th Pan-Hellenic Conference on Progress in Computing and Informatics (PCI)` / `conferencia` | bib `EvaluatingLLMsOGD2025` (see note) |
| R044 | veiculo/tipo | `[A CONFIRMAR]` | `Companion Proceedings of the 21st ACM/IEEE International Conference on Human-Robot Interaction (HRI Companion)` / `conferencia` | bib `RobotStorytelling2025` |
| R045 | veiculo/tipo | `[A CONFIRMAR]` | `Proceedings of the 33rd ACM International Conference on Information and Knowledge Management (CIKM)` / `conferencia` | bib `Colombo2024` |
| R046 | veiculo/tipo | `[A CONFIRMAR]` | `Companion Proceedings of the ACM Web Conference (WWW Companion)` / `conferencia` | bib `CLEAR2025` |

Note R041: the old free-text note said "PCI 2024"; the validated bib gives the **28th** Pan-Hellenic
Conference and year **2025** (kept). No manuscript year conflict (manuscript/bib both 2025).

### 3b. `[A CONFIRMAR]` that could **not** be resolved → explicit missing-data status

| id | field | old | final (truthful status) | why unavailable |
|---|---|---|---|---|
| R012 | doi | `[A CONFIRMAR]` | `não disponível no registro consolidado (CEUR-WS vol. 3423, sem DOI)` | CEUR-WS proceedings have no DOI; bib carries none |
| R014 | veiculo/tipo | `[A CONFIRMAR]` | `não disponível no registro consolidado (relato não recuperado)` / `não disponível` | not-retrieved; no bib entry, no full text |
| R019 | veiculo/tipo | `[A CONFIRMAR]` | `não disponível no registro consolidado (relato não recuperado)` / `não disponível` | not-retrieved; no bib entry, no full text |
| R036 | veiculo/tipo/doi | `[A CONFIRMAR]` (all three) | `não disponível no registro consolidado (relato não recuperado)` / `não disponível` / `não identificado` | not-retrieved; DOI never found (old note: "não achei em lugar nenhum") |

Not inferred from DOI publisher (per instruction). R014/R019 keep their existing DOIs (10.1109/…); only the
conference *name* — absent from any validated source — is marked missing.

### 3c. `base_origem` — the shared placeholder (§4)

- **Old (all R001–R046):** `Rayyan (Scopus/WoS/IEEE/ACM — distribuicao por base [A CONFIRMAR])`
- **Final:** `Rayyan (multi-base internacional — base específica não preservada no registro consolidado)`
- **Source / justification:** `busca_contagens.csv` records the 805 unique records as an **aggregate** set
  across the four international bases ("Zotero, conjunto agregado das 4 bases internacionais; **não rastreado
  por base**"). The per-record source database is therefore **not preserved** in the consolidated export, so
  the honest statement is "base específica não preservada". Source DB was **not** guessed from DOI publisher.
- R047 already read `Rayyan (multi-base internacional)` (an exclusion row) and was left as-is.

### 3d. R001 governmental-context note (§5)

- **Old (observação):** "Contexto governamental não especificado no texto **[A CONFIRMAR país]**"
- **Final:** "Contexto governamental não especificado no texto **completo**." (`[A CONFIRMAR país]` removed)
- Country was **not** inferred from affiliation/institution/conference/dataset language. The full text does
  not name the governmental country; the truthful statement is that it is unspecified.

---

## 4. Included studies with metadata placeholders (§6)

All of R012, R015, R027, R029, R032, R034, R035, R037, R038, R039, R040, R041, R044, R045, R046 were
reconciled against `referencias_corpus.bib` and the validated manuscript references (year / venue / type /
DOI / title / authors). Venues/types resolved as in §3a; years, DOIs, titles and authors already matched the
bib and were left unchanged (except the R015 year correction, §8). **Eligibility unchanged** for every row.

---

## 5. Unresolved values → explicit missing-data status

See §3b. Four fields across R012 (doi), R014, R019, R036 (venue/type, plus R036 doi) now carry explicit
"não disponível / não identificado" wording instead of a placeholder. No uncertainty was converted into a
guessed value.

---

## 6. Stale workflow notes removed (§8–§13)

Removed from the observação field wherever present, as obsolete working/notebook residue:
`Handoff #NN` / `Handoff só-Rayyan` (all rows), `SÓ NO RAYYAN — recuperar (...)`, `Sem PDF declarado`,
`REVERSÃO Ana`, `PDF obtido — corpus de síntese`, and the `PROVÁVEL match / CONFIRMAR / alternativa` note on
R031. Post-cleanup marker counts in the file: `[A CONFIRMAR]`=0, `SÓ NO RAYYAN`=0, `Sem PDF declarado`=0,
`REVERSÃO Ana`=0, `Handoff`=0, `PROVÁVEL`=0.

**Preserved** (per §13 — not over-cleaned): inclusion/exclusion rationale, borderline-case rationale
(rewritten from "REVERSÃO Ana — incluído apesar de borda X" to "Caso-limite…"), recovered-in-Major-Revision
provenance for the 7 new inclusions + 2 full-text exclusions, the full-text exclusion reasons for R010/R033,
the "reports not retrieved (PRISMA 2020)" status for the 10 not-retrieved, and methodological notes (model
family, domain, region, evaluation, consolidated-table study number).

---

## 7. Factual inconsistency — R027 venue (**RESOLVED**)

Two internal sources had disagreed on R027's venue name (same paper, same DOI `10.1145/3605801.3605806`,
same pages 24–27, ACM ICPS 2023): the bib entry read **ICBDIE**, while the old CSV note and a cross-reference
in the R011 full text read **CNCIT**.

**Resolution (external bibliographic verification):** DOI `10.1145/3605801.3605806` corresponds to
*Proceedings of the 2023 2nd International Conference on Networks, Communications and Information Technology
(**CNCIT 2023**)*, ACM, pp. 24–27, 2023 — i.e. the **CNCIT** reading is correct and the bib's **ICBDIE** was
wrong. The venue metadata was corrected to CNCIT 2023 in **both** `referencias_corpus.bib` (`Gao2023`
booktitle) and `busca_registros.csv` (R027 `veiculo` + observação). **Only the venue string changed** —
title, authors, year (2023), DOI, eligibility, corpus size, extraction, QA, RQ classifications, PRISMA and
taxonomy are untouched. The manuscript prose does not name the conference, so no prose edit was needed. The
bibliography now renders "Networks, Communications and Information Technology (CNCIT)"; `latexmk -xelatex`
exits 0 with **0 undefined citations / 0 undefined references**. No `ICBDIE` string remains in the bib, CSV,
or manuscript.

---

## 8. R015 year verification (explicit)

- **busca_registros.csv (old):** year **2023**.
- **Validated bibliography (`referencias_corpus.bib`, `ScotlandChatGPT2024`):** year **2024**, booktitle
  "Proceedings of the 27th Pan-Hellenic Conference on Progress in Computing and Informatics", pages 53–59,
  DOI `10.1145/3635059.3635068`.
- **Manuscript:** cites **Mamalis et al. (2024)** with the same DOI.
- **Resolution:** authoritative evidence (bib + manuscript + DOI) agrees on **2024**. `busca_registros.csv`
  corrected **2023 → 2024**; observação records the correction. **No manuscript/bib disagreement** — the CSV
  was the sole outlier, so no STOP condition. Manuscript data **not** altered (already 2024).

---

## 9. Final list of the 10 not-retrieved reports

`decisao = nao_recuperado` (reports not retrieved, PRISMA 2020 — **not** content exclusions), exactly:

**R005, R014, R019, R020, R024, R028, R030, R031, R036, R043.**

Legacy "recuperar / CONFIRMAR / PROVÁVEL / SÓ NO RAYYAN / Sem PDF declarado" wording removed from all ten;
each now states the final factual retrieval status. R031's identity is **confirmed** by title + authors +
DOI, so the speculative "PROVÁVEL match #92 / alternativa R039" note was dropped and the confirmed record
retained (no HUMAN REVIEW needed for R031).

---

## 10. Corpus assertion (§11) — confirmed

Quote-aware parse of the final file:

- **Included corpus = 36** — 34 international (R…) + 2 SBC/SOL (SOL01, SOL02). ✔
- **Recovered/full-text excluded:** R010, R033 (both `excluido`, full-text reasons intact). ✔
- **Not retrieved (exactly 10):** R005, R014, R019, R020, R024, R028, R030, R031, R036, R043. ✔
- **Total `excluido` = 10:** SOL03–SOL09 (7) + R010 + R033 + R047 (CI2). ✔
- No row in the included corpus is marked `nao_recuperado`; no not-retrieved row is in the included corpus.
- Every row parses to 13 fields; header intact.

---

## 11. HUMAN REVIEW REQUIRED — summary

**None outstanding.** The single item previously flagged — the **R027 venue name** (ICBDIE vs CNCIT) — is now
**resolved**: external verification confirmed **CNCIT 2023**, and the bib + CSV were corrected accordingly
(§7). *Venue string only — no effect on corpus, eligibility, or any RQ.*

All other `[A CONFIRMAR]` values were either resolved from validated evidence or converted to explicit,
truthful missing-data status; no value was guessed.
