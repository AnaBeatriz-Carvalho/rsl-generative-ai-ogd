# Revision Audit — iSys Major Revision

**Manuscript:** *Generative AI for Open Government Data Access and Public Transparency: A Systematic Literature Review*
**Decision:** Major Revision
**Audit date:** 2026-08-16
**Auditor role:** scientific auditor / methodological reviewer / academic editor (pre-change diagnosis)

---

## 0. Scope note and sources consulted

This audit was produced **before** any manuscript change, per the revision protocol. It classifies each
reviewer concern as **RESOLVIDO / PARCIAL / PENDENTE / REQUER AÇÃO DOS AUTORES**, citing the current
manuscript location as evidence.

Materials read in full:

- `isys_rsl.tex` (frontmatter, Introduction, Background/Related Work, Discussion, Threats, Conclusion, QA appendix)
- `metodo_rsl.tex` (Method), `resultados_rsl.tex` (Results, RQ1–RQ5)
- `resultado_extracao_rsl.txt` (full extraction for the 29-study corpus)
- `busca_registros.csv` (complete study registry: 29 included + 19 not-retrieved + exclusions, **with DOIs**)
- `busca_contagens.csv`, `strings_por_base.md` (search execution), `HANDOFF_iSys.md`, `CHECKLIST_iSys.md`

**Important limitation of this audit:** the *verbatim* reviewer reports (Reviewer A / B / C letters) are **not
present as files** in the repository. The concerns below are reconstructed from the structured revision brief.
They are treated as faithful, but the editor should cross-check each item ID against the original letters.

---

## 1. Verified data (baseline for every factual change)

All numbers below are traceable to `busca_registros.csv` and `resultado_extracao_rsl.txt`.

| Quantity | Value | Source |
|---|---|---|
| Final corpus | **29** (27 international + SOL01, SOL02) | registry `decisao=incluido` |
| Reports not retrieved | **19** (R001,005,006,008,009,010,011,014,019,020,021,022,024,028,030,031,033,036,043) | registry `decisao=nao_recuperado` |
| Main model = GPT family (proprietary) | **18/29** | extraction RQ3 |
| Open-weight main model | **6/29** (Llama, Mistral, Gemma, DeepSeek, ChatGLM) | extraction RQ3 |
| DialogFlow (non-generative) | **2/29** | extraction RQ3 |
| Model not reported | **3/29** | extraction RQ3 |
| Empirical studies | **23/29**; conceptual **6/29** | extraction "Avaliação" |
| Hallucination **explicitly** discussed | **≈18/29** (see §Priority 3) | extraction RQ5 count |
| Studies measuring transparency as a **civic outcome** | **0/29** | extraction "Avaliação" |
| QA scores | range 2.0–5.0, median 4.5, ten at 5.0, one below threshold (Dineva & Atanasova 2025 = 2.0) | Appendix A |

**Geographic distribution (by empirical/government context studied), verified from extraction:**

USA 4 · UK 3 · China 3 · Spain 2 · Italy 2 · Brazil 2 · Germany 1 · Bulgaria 1 · India 1 · Australia 1 ·
Colombia 1 · Canada 1 · Peru 1 · Kazakhstan 1 · Netherlands 1 · Estonia 1 · EU/supranational 1 ·
multinational (Spain+Luxembourg) 1 · not reported/conceptual 1 = **29**.
By region: **Europe 13, Asia 5, North America 5, South America 4, Oceania 1, n/r 1. Africa = 0.**

---

## 2. Audit table (reviewer concern → status → evidence → action)

| ID | Reviewer | Concern (reconstructed) | Current status | Evidence in manuscript | Action needed | Priority |
|---|---|---|---|---|---|---|
| C-01 | C | "Taxonomy" is only a 3-box supply/demand description; no defined structure | **PARCIAL** | `resultados_rsl.tex` RQ1 (3 categories); `isys_rsl.tex` abstract/intro/concl. use "taxonomia" | Build a real multi-axis taxonomy (definitions, inclusion/differentiation criteria, relational figure) OR rename to "classificação". **Decision: Alternative A** (data support 3 axes) | P1 · ALTO |
| A-01 | A | Transparency named but never operationalized; "no study measures it" needs a transparent procedure | **PARCIAL** | Def. added in `bg_ogd` (5 dimensions); claim "0/29" in Results/Discussion/Threats, but *how* it was determined is not stated | Add explicit 4-level determination rule (mentions / acts-on-a-dimension / proxy / civic outcome); place conceptual matrix in supplement | P2 · ALTO |
| A-02 | A | Unsupported inference: "deslocamento do dado estruturado para o documento textual" (implies a temporal trend without longitudinal evidence) | **PENDENTE** | `resultados_rsl.tex` RQ2 last paragraph ("confirma o deslocamento…") | Replace with cross-sectional wording ("predominância de informação textual no corpus") | P3 · ALTO |
| A-03 | A | Overgeneralized hallucination claims ("na maioria", "quase todos", "onipresença") | **PENDENTE** | Discussion ("onipresença…relatadas em quase todos"); RQ5 ("aparece na maioria dos estudos") | Replace with verifiable count "≈18/29" or cautious quantifier | P3 · ALTO |
| A-04 | A | Rhetorical language ("ironia", "caixas-pretas", "criteriosa/rigorosa") | **PENDENTE** | Discussion ¶3 ("Há aqui uma ironia…", "caixas-pretas comerciais"); Results ("filtragem criteriosa") | Rewrite in analytical register | P4 · MÉDIO |
| C-02 | C | Country is extracted but never synthesized geographically | **PENDENTE** | `metodo_rsl.tex` extraction form lists "país" as metadata; no geographic result | Add geographic synthesis (table + text) + link to external validity; define what "país" means (→ government context) | P5 · ALTO |
| C-03 | C | No consolidated view of the 29 studies | **PARCIAL** | Only QA scores appendix (Table `tab:qa_estudos`) | Add consolidated corpus table (ID, study, year, country, info type, category, model, evaluation) in appendix/supplement | P6 · MÉDIO |
| A/C-04 | A,C | Figure 1 (Semantic Web = "previous" vs GenAI = "current") is linear/substitutive | **PENDENTE** | `fig:paradigmas` caption "paradigma anterior … paradigma atual" | Reframe as complementary approaches (Linked Data ↔ RAG/LLM, convergence KG+RAG); update caption + discussion | P7 · MÉDIO |
| A-05 | A | Effort to recover the 19 not-retrieved reports | **REQUER AÇÃO DOS AUTORES** | Results §Seleção; Threats (Cobertura da busca) | Do **not** claim new attempts. Strengthen availability-bias limitation; produce `reports_not_retrieved_todo.md` (19 studies + DOIs) | P8 · ALTO |
| A-06 | A | Is this an SLR or a Systematic Mapping Study? | **RESOLVIDO** (defensible) | `metodo_rsl.tex` ¶2 "desenho híbrido: rigor de RSL na busca/seleção, síntese de mapeamento" | Keep hybrid framing; align abstract/keywords wording; audit only | P9 · BAIXO |
| A-07 | A | Weak Information-Systems framing (reads as NLP/LLM) | **PARCIAL** | Sociotechnical transparency in `bg_ogd`; IS closing ¶ in Discussion | Deepen sociotechnical reading (artifact ↔ information ↔ org ↔ citizen ↔ outcome) without new theory; no fabricated citations | P10 · MÉDIO |
| C-05 | C | Terminology/language consistency (IA/LLM/RAG defined once; PT/EN mix) | **PARCIAL** | RAG defined in `bg_genai`; "informação do setor público" used | Audit acronym first-use; keep PT section titles; full EN translation = optional, not required | P11 · BAIXO |
| — | — | Abstract/Resumo must match final scope, method, counts, terminology | **PENDENTE** (depends on C-01) | `abstract-pt`, `abstract-en` | Update after taxonomy decision + count fixes | P12 · ALTO |
| — | ints. | Construct-validity tension title (OGD) vs broader corpus | **RESOLVIDO** (author decision) | Title kept broad by explicit author decision (HANDOFF `decisao-escopo-isys`); tension carried in Threats (Validade de construto) | Keep title; ensure no remaining "all corpus = strict OGD" claims | P (title) · BAIXO |

---

## 3. Decisions taken for this revision round

1. **Taxonomy (P1): Alternative A — build a real taxonomy.** The extraction sustains three recoverable
   dimensions (chain position; information object; GenAI function), so the honest and stronger response is to
   define them (with inclusion/differentiation criteria and a relational figure), rather than to downgrade to
   "classificação". Rationale detailed in the final report.
2. **Title:** kept in its broad form by explicit prior author decision; the OGD-vs-broader-corpus tension
   remains a construct-validity limitation. No title change.
3. **19 not-retrieved reports:** no new retrieval attempted or claimed; limitation strengthened; DOIs handed
   off in `reports_not_retrieved_todo.md` for the authors to attempt before resubmission.
4. **Language:** manuscript stays in Portuguese with PT section titles; full EN translation treated as optional.

---

## 4. Items that REQUIRE human (author) action

- **Recover the 19 not-retrieved reports** (`reports_not_retrieved_todo.md`) — needs paid-database / author-contact access not available here. Changing the corpus requires re-running the protocol.
- **Decide on full English translation** (Reviewer C suggestion; optional).
- **New theoretical IS references**, if the editor wants deeper grounding — must be verified, never fabricated.
- **Confirm** the reconstructed reviewer-comment IDs against the original letters.

---

## 5. Adendo — rodada de validação final (2026-08-17)

Corpus **congelado em 29** (adulteração para 31 por outra IA foi revertida; ver `FINAL_VALIDATION_REPORT.md`).
Correções seguras implementadas nesta rodada, todas terminológicas/conceituais e destacadas em `\rev{}`:

- **Título** → "Public-Sector Information Access…" (P1/B1); OGD mantido como caso paradigmático.
- **Taxonomia** — Dim1 refatorada para ortogonal **Oferta 7 / Demanda 22** (B4); distinção dataset/serviço movida à Dim2. Ver `03_taxonomy_validation.md`.
- **Resumo/Abstract/Conclusão** — abertura por informação do setor público; "nenhum dos 29 estudos incluídos" (B2/B3).
- **CE1** alinhado ao escopo; **RAG** suavizado; item **Literatura cinza** nas Ameaças; **Background → Fundamentação**; siglas IA/SI definidas (B8/B11/B13/B14).
- **Resíduo B6** ("taxonomia oferta/demanda… recorte legislativo") corrigido no Trabalhos Relacionados.

Deliverables desta rodada: `00_baseline_validation.md` … `09_reviewer_C_simulation.md`, `FINAL_VALIDATION_REPORT.md`, `response_letter.md` (atualizado).

**Ação humana pendente:** recuperação dos 19 not-retrieved; conferência contra pareceres originais (ausentes do repo); inspeção visual do PDF (sem poppler no ambiente).
