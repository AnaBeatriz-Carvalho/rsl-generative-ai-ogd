# Response to Reviewers — iSys (Major Revision)

**Manuscript:** *Generative AI for Public-Sector Information Access and Public Transparency: A Systematic Literature Review*

We thank the editor and the reviewers for the careful and constructive assessment. Below we respond to each
point, indicating whether we agree, what was changed, and exactly where. All changed passages are highlighted
in the revised PDF (via the `\rev{}` command); a few entirely new elements (new tables, two new figures, and
the new taxonomy subsection) are marked as new by their highlighted captions/headings and are listed here.
No data, counts, categories, citations, or methodological procedures were invented; every factual change is
traceable to the extraction spreadsheet and the study registry provided in the supplementary materials.

> **Note on integrity of the corpus and method.** In direct response to Reviewer A, we conducted an additional,
> documented full-text retrieval round for the 19 reports originally *not retrieved*; this recovered 9 full texts,
> **7 of which were included and 2 excluded after full-text assessment**, moving the synthesis corpus from
> **29 to 36 studies** (34 international + 2 SBC/SOL). This is the **only** change to the corpus, and every one
> of the 7 new studies was extracted, quality-assessed and classified from its full text with the **same**
> instrument used for the original 29; no data were invented (all traceable to `busca_registros.csv`,
> `resultado_extracao_rsl.txt` and the corpus `.bib`). We did **not** change the original search string, run a
> new search, perform snowballing, or alter the single-reviewer / no-double-coding procedures. Ten reports remain
> *not retrieved* and are still carried as an availability-bias limitation.

---

## Reviewer A

### A1 — "Taxonomy" is asserted but under-specified (also raised by Reviewer C)

**Comment.** The paper claims a supply/demand *taxonomy*, but the contribution reads as a three-box
description without a defined conceptual structure.

**Response.** We agree the previous version did not meet the bar for a taxonomy. Rather than downgrade the
term, we found that the extraction already sustains **three recoverable dimensions**, so we made the taxonomy
explicit and defensible: (1) position in the information chain (supply/preparation vs demand/access vs
demand/service mediation), (2) information object, and (3) GenAI function. Each category now has a definition,
an inclusion criterion, and a differentiation criterion; categories combine (each study is a coordinate across
the dimensions), and the relations between dimensions are shown in a figure. We did not invent categories: the
dimensions come directly from RQ1 (chain position), RQ2 (object), and the functions described in RQ1/RQ4.

**Changes in manuscript.** New subsection **4.6 "Taxonomia dos usos de IA Generativa no acesso à informação
pública"** (`resultados_rsl.tex`), with a new definitional **Table (`tab:taxonomia`)** and a new relational
**Figure (`fig:taxonomia`)**. Abstract/Resumo, Introduction (contribution ii), and Conclusion updated to
describe the taxonomy as three-dimensional.

### A2 — Unsupported inference: "shift from structured data to textual document"

**Comment.** The review is cross-sectional and cannot demonstrate a temporal *shift*.

**Response.** We agree. We removed the trend claim and now describe a cross-sectional *predominance* of textual
information in the corpus, explicitly noting the absence of a time series that would license a substitution
trend.

**Changes.** `resultados_rsl.tex`, RQ2 closing paragraph ("O quadro geral evidencia a predominância… e não uma
tendência histórica de substituição").

### A3 — Overgeneralized hallucination claims

**Comment.** "na maioria", "quase todos", "onipresença" are not quantified.

**Response.** We counted the corpus: hallucination was **explicitly discussed in 18 of the 29 studies** in the
original submission and, after the additional retrieval round, in **24 of the 36 studies** (as a risk to mitigate
or as an observed result). We replaced every vague quantifier with this verifiable count and removed
"onipresença"/"quase todos".

**Changes.** RQ5 opening (`resultados_rsl.tex`: "…vinte e quatro dos trinta e seis estudos…"); Discussion §3
(`isys_rsl.tex`), which also now reports "dezoito dos trinta e seis" for proprietary-model dependence and
"quatro" for unreported models (see the RQ3 model-family recoding section below).

### A4 — Rhetorical language

**Comment.** Expressions such as "ironia", "caixas-pretas", "criteriosa" weaken the scientific register.

**Response.** We agree and rewrote these passages analytically. The "irony" sentence became a statement about
the tension between component opacity and the auditability requirements of public transparency.

**Changes.** Discussion §3 (`isys_rsl.tex`, "…introduz uma tensão entre a opacidade de determinados componentes
tecnológicos e os requisitos de auditabilidade…"); Results selection paragraph ("aplicaram os critérios de
inclusão e exclusão" replacing "filtragem criteriosa").

### A5 — Additional effort to recover the 19 not-retrieved reports

**Comment.** Please attempt to recover the 19 reports not retrieved.

**Response.** We thank the reviewer for this recommendation. In response, we conducted an additional full-text
retrieval round for all 19 reports originally classified as *reports not retrieved*. The additional attempts
used, as applicable, publisher/DOI pages, institutional access, alternative versions indexed by scholarly search
engines, ResearchGate or repositories, and direct author requests. Nine full texts were recovered. We reapplied
the original eligibility criteria without modification: **seven studies were included and two were excluded after
full-text assessment**. Ten reports remained unavailable despite the additional retrieval effort. Accordingly, we
updated the PRISMA flow, the synthesis corpus (29 → 36), the quality assessment, the consolidated evidence
tables, and the availability-bias limitation. The two full-text exclusions were recorded with explicit reasons:

- **Baron (2025), "Using AI in providing greater access to the U.S. government's email"** — excluded because it
  does **not** constitute new, independent primary evidence for the Generative-AI phenomenon under review: its
  GenAI component synthesizes the already-included Baron et al. (2023) (same FOIA context, ChatGPT-3.5, Clinton
  collection; "No datasets were generated or analysed during the current study"). Including it alongside Baron
  et al. (2023) would double-count the same evidence. It is **not** treated as a duplicate (CE4) and **not** as a
  preliminary/extended version (CE5).
- **Tahtali et al. (2026), "Why public procurement professionals accept (or resist) generative AI"** — a
  peer-reviewed primary study, but its object is procurement professionals' *acceptance/resistance* of GenAI
  (TAM/TTF/TOE), not GenAI as a mechanism for the access, organization or mediation of public-sector information.
  It therefore fails **CI1**. It is **not** excluded for lack of peer review, nor under CE4/CE5.

**Changes.** Updated Threats item **"Viés de disponibilidade"** (`isys_rsl.tex`): the risk is **reduced** (9/19
recovered) but **not eliminated**, and the remaining 10 could still shift model/venue/geographic distributions.
Results §Seleção, PRISMA counts, Table 1, geography, taxonomy, QA appendix, and the consolidated table were
updated to N=36. Supplementary file `reports_not_retrieved_todo.md` now lists the **10** still-unretrieved studies
with DOIs and documents the 7 included and 2 excluded.

### A6 — SLR vs Systematic Mapping Study

**Comment.** Is this an SLR or a mapping study?

**Response.** The manuscript already adopts, and we retained, an explicit **hybrid design**: SLR rigor in
search and selection (Kitchenham & Charters; PRISMA 2020) with a mapping-style descriptive synthesis (Petersen
et al.). We did not retrofit a protocol that was not executed. We consider this framing defensible given the
characterization-oriented research questions and the presence of a quality assessment.

**Changes.** No change beyond confirming consistency of the wording in the Method (§3, ¶2) and abstract.

### A7 — Stronger Information Systems framing

**Comment.** The work reads as NLP/LLM rather than IS.

**Response.** We deepened the sociotechnical reading already introduced (transparency as a five-dimension
sociotechnical construct) by making explicit, in the Discussion, that the phenomenon emerges from the
interaction among the technological artifact, public-sector information, public organizations, institutional
practices, citizen capacity, and public outcomes — and that concentrating evaluation on the artifact alone is
what produces the identified gap. No new references were fabricated; if the editor wishes deeper theoretical
grounding, we list candidate literature in the final report for verified inclusion.

**Changes.** Discussion closing paragraph (`isys_rsl.tex`, "Lidos sob a leitura sociotécnica…").

---

## Reviewer C

### C1 — Make the taxonomy visible and defined

See **A1** — a definitional table and a relational figure were added, with inclusion/differentiation criteria
per category.

### C2 — Geographic synthesis is missing

**Comment.** Country is extracted but never synthesized.

**Response.** We agree. We first defined, in the Method, that the *country* field records the **empirical
government context** studied (not author affiliation), because this is more relevant to generalization. We then
added a geographic synthesis: 17 national contexts plus one supranational; USA 4, UK 3, China 3, Spain/Italy/
Brazil 2 each, twelve single-country contexts, one multinational, one conceptual. By region: Europe 13, Asia 5,
North America 5, South America 4, Oceania 1, **Africa 0**. We linked this concentration to external validity.

**Changes.** New Method sentence defining the *country* field (`metodo_rsl.tex`, §Extração); new Results
subsection **"Distribuição geográfica"** with **Table `tab:geografia`** (`resultados_rsl.tex`); new sentence in
Threats/External validity (`isys_rsl.tex`).

### C3 — Consolidated view of the corpus (now 36 studies)

**Comment.** Provide a consolidated corpus table.

**Response.** We agree. To avoid imposing contested per-study classifications, the consolidated table reports
the directly-extracted, verifiable fields (study, year, government context, main model reported),
cross-referenced to the quality scores (Appendix A) and to the taxonomy (§4.6). The full extraction spreadsheet
remains in the supplement.

**Changes.** New **Appendix B "Visão Consolidada do Corpus"** with a two-part **Table `tab:corpus_consolidado`**
(`isys_rsl.tex`).

### C4 — Figure 1 (Semantic Web "previous" vs GenAI "current") is too linear

**Comment.** The figure suggests technological substitution.

**Response.** We agree. We reframed the figure as **complementary approaches**: Linked Data/Knowledge Graphs
(structure, traceability) and GenAI/LLMs/RAG (natural-language access), converging in KG + RAG + LLM for
conversational access with greater traceability. We replaced the external image with a self-contained diagram
and updated the caption and the surrounding text (Background and Related Work) so the two are no longer
described as "previous"/"current".

**Changes.** Figure `fig:paradigmas` redrawn and re-captioned (`isys_rsl.tex`); related-work sentence changed
from "substituir" to "via complementar"; introductory sentence to the figure updated.

### C5 — Terminology and language consistency

**Comment.** Ensure acronyms are defined once; reduce PT/EN mixing; consider full English translation.

**Response.** We kept the manuscript in Portuguese with Portuguese section titles and treat full English
translation as an optional suggestion. We audited first-use definitions of LLMs and RAG and standardized
"informação do setor público" throughout. The taxonomy terminology is now used consistently (three-dimensional
taxonomy) across abstract, introduction, results, discussion, and conclusion.

**Changes.** Abstract/Resumo, Introduction, §4.6, Conclusion aligned; terminology audited (see final report §E
for one residual item flagged for author verification).

---

## Cross-cutting: transparency as an operational construct (A/B/C)

**Comment.** The claim "no study measures transparency as a civic outcome" needs a transparent procedure.

**Response.** We added an explicit **four-level determination rule** tied to the five transparency dimensions:
(i) mention, (ii) acting on a dimension, (iii) proxy measurement, (iv) civic-outcome measurement. We recorded,
per study, motivation → intended dimension → evaluated dimension → metric/proxy → civic outcome, in a matrix
placed in the supplement. This lets us state that many studies **act on** a dimension (e.g., legal-language
simplification acts on *comprehension*) and several measure **proxies**, while **none** reaches the
**civic-outcome** level — without conflating "does not measure social control" with "does not contribute to
transparency".

**Changes.** New Method paragraph (`metodo_rsl.tex`, §Síntese); reinforced nuance in Results characterization
(`resultados_rsl.tex`, "Contribuir para uma dimensão (nível ii) não equivale a demonstrar transparência como
resultado (nível iv)").

---

## Validation round — terminological/conceptual changes (corpus was 29 at that point)

> **Integrity note for that round.** At the time of the terminological/conceptual pass below, the corpus was
> **29 studies**; those changes did not add or remove any study. **A subsequent, separately documented full-text
> retrieval round then moved the corpus to 36** (see the top integrity note, the Reviewer A "19 reports" item,
> and the "Additional full-text retrieval round" section at the end). The changes in this subsection remain valid
> and are highlighted with `\rev{}`.

### Title and scope (Reviewers A & C — scope clarification)

**Comment.** The corpus is broader than Open Government Data in the strict sense; title and framing should match.

**Response.** The conceptual clarification requested by the reviewers showed that the corpus spans a broader
informational universe than OGD *stricto sensu*. OGD remains a **paradigmatic case** and an important component
(keyword, Background concept, search-string term, portal-related category), but legislation, official documents,
and service contents are also analyzed. We therefore updated the **title** to reflect the scope already retrieved
by the original protocol. **The corpus was not expanded — the terminology now better describes the original corpus.**

**Changes.** Title → *"Generative AI for Public-Sector Information Access and Public Transparency: A Systematic
Literature Review"* (full, short title, `pdftitle`); Abstract/Resumo opening reframed to public-sector information;
Introduction objective and Conclusion opening aligned; keywords already included "Public-Sector Information".

### Taxonomy made orthogonal (Reviewers A & C)

**Comment.** In Dimension 1, "Access" vs. "Service mediation" seemed distinguished mainly by the *object*,
overlapping with Dimension 2.

**Response.** We agree. We audited the axis (`03_taxonomy_validation.md`) and confirmed the overlap. We refactored
**Dimension 1** into two truly orthogonal positions — **Supply/preparation (7)** and **Demand/access mediation (22)**
— moving the dataset-vs-service distinction to **Dimension 2** (its proper axis). RQ1 still reports the three
descriptive application types (7/11/11); they are no longer presented as a taxonomy dimension. No individual study
was reclassified: the 7/22 counts come directly from the D1 column of the consolidated table.

**Changes.** `resultados_rsl.tex` §4.6 text, **Table 8** (`tab:taxonomia`, Dim1 now two rows), **Figure 4**
(`fig:taxonomia`, two positions + relations); Discussion distribution paragraph ("22 dos 29… sete"); Conclusion.

### Related work residual (Reviewer C)

**Comment.** The differentiation sentence still spoke of "oferta/demanda taxonomy" and "recorte legislativo".

**Response/Changes.** Rewritten to: sociotechnical operationalization of transparency + **multidimensional taxonomy**
+ broad public-sector-information scope as the differentiators (`isys_rsl.tex`, Related Work).

### CE1, RAG, grey literature, terminology

- **CE1** reworded to the two-axis intersection over *public-sector information / digital government* (no change to
  which studies were selected) — `metodo_rsl.tex`.
- **RAG** de-universalized: "…mechanisms of retrieval over updated repositories become particularly relevant; RAG is
  one of the main architectures identified" (was "RAG is a requirement") — `isys_rsl.tex` §2.
- **Grey literature**: new Threats item stating peer-reviewed-only synthesis and that the 0-civic-outcome finding is
  bounded to the 36 included studies — `isys_rsl.tex`.
- **Terminology/acronyms**: "Background" → "Fundamentação e Trabalhos Relacionados"; first-use definitions of
  Inteligência Artificial (IA), Sistemas de Informação (SI); LLMs/OGD/RAG/PICOC/PRISMA/RSL verified.

### Reports not retrieved (Reviewer A) — superseded

**RESOLVED in a subsequent round** (see below and the Reviewer A "19 reports" item). An additional full-text
retrieval round recovered 9 of the 19, of which 7 were included and 2 excluded after full-text assessment; the
corpus moved to 36. Ten reports remain *not retrieved* and are carried as availability bias in
`reports_not_retrieved_todo.md`.

---

## Additional full-text retrieval round (Reviewer A) — corpus 29 → 36

This round implements Reviewer A's recommendation on the 19 *reports not retrieved*.

**What was done.** An additional retrieval round was run for all 19 reports, using — as applicable — publisher/DOI
pages, institutional access, alternative versions indexed by scholarly search engines, ResearchGate/repositories,
and direct author requests. **Nine** full texts were recovered and reassessed under the **unchanged** CI1–CI5 /
CE1–CE5 criteria. **Seven were included** (Syahidi et al. 2025; Ryu et al. 2025; Kumar et al. 2024; Giarelis et
al. 2026; Fang & Xu 2023; Tsourma et al. 2025; García-Montero et al. 2025 — consolidated-table IDs 30–36) and
**two were excluded after full-text** (Baron 2025; Tahtali et al. 2026 — reasons above). **Ten** remain not
retrieved.

**PRISMA (international).** 46 sought → 10 not retrieved → 36 assessed → 2 excluded after full-text → 34 included.
With the 2 SBC/SOL studies, the final corpus is **36**. (Identification/deduplication/title-abstract screening
counts are unchanged, as the additional round acted only at the full-text-retrieval stage.)

**What was recomputed from data (not mechanically substituted).** Models — at this round GPT/proprietary 19,
open-weight 11, DialogFlow 2, not reported 4; **subsequently recoded** to proprietary 18 / open-weight 10 /
multiple-comparative 2 / DialogFlow 2 / not reported 4 (see the RQ3 model-family recoding section below); empirical 28 / conceptual 8; hallucination explicitly discussed 24/36; taxonomy D1 (supply 9 /
demand 27), D2 (LJ 9, OGD 12, services 9, sectoral 5, conceptual 1); geography (Europe 15, Asia 7, N. America 5,
S. America 5, Oceania 1, Africa 0, multi-region 1, no national context 2); QA (range 2.0–5.0, **median 4.5
unchanged**, twelve at 5.0, two below 2.5). The central finding is unchanged and re-verified: **none of the 36
studies** evaluates transparency as a civic outcome.

**Changes.** Abstract/Resumo, Results §Seleção + PRISMA narrative, Table 1, geography table, taxonomy Table 8 and
figure, RQ1–RQ5 narratives, QA appendix (rows 30–36), consolidated table (rows 30–36), Discussion, Threats
(availability bias), and Conclusion — all to N=36. Data files `busca_registros.csv`,
`resultado_extracao_rsl.txt`, `referencias_corpus.bib`, and `reports_not_retrieved_todo.md` updated accordingly.

**Status of prior human-action items (resolved in the pre-merge pass).** The PRISMA figure
`imagens/fluxograma_prisma.png` was **replaced manually** with the corrected flow (46 sought → 10 not retrieved →
36 assessed → 2 excluded → 34 included). The `[A CONFIRMAR]` bibliographic placeholders were resolved:
García-Montero et al. is now dated **2026** (Springer CCIS chapter; TICEC 2025 event; pp. 63–77) with key
`GarciaMontero2026`, and Giarelis et al. 2026 is now "Electronic Government (EGOV 2025), LNCS 15944, pp. 368–379".

---

## RQ3 model-family coding — explicit rule and terminology (Reviewers A & C)

**Comment (coding transparency / consistency).** The model-family variable was mutually exclusive but the "main
model" reduction was never operationally defined, the aggregate label "família GPT" absorbed proprietary non-GPT
systems (Gemini, Copilot), and several studies use more than one generative family.

**Response.** We did **not** change eligibility, the corpus (still 36), or any other analysis. We only made the
**descriptive RQ3 model-family coding explicit and reproducible**, operationalizing the previously implicit rule
across all 36 studies (not a rule invented for one study):

- A study is assigned to **one** category by the **generative** models central to its design. Auxiliary models
  (embedding, re-ranking, retrieval, classifiers, LLM-as-judge, synthetic-data or preprocessing) do not determine
  the category; a baseline that is a full experimental arm of a head-to-head comparison the conclusions depend on
  is treated as co-primary.
- Categories: **Proprietary · Open-weight · Multiple/comparative · DialogFlow · Not reported**. The aggregate
  label "família GPT" was renamed **"Proprietário/Proprietary"** (individual GPT-3.5/4/4o mentions are unchanged).
- **Multiple/comparative** is used **only** for symmetric cross-ownership-family designs (proprietary + open as
  co-primary experimental conditions, no focal model). Two studies qualify: Rakhimova et al. 2025 (GPT-4o-mini vs.
  seven open models on Kazakh legal QA) and García-Montero et al. 2026 (Gemini 2.5 Flash / GPT-4.1 Mini vs.
  DeepSeek V3 / Llama 4 Maverick on the same 16 datasets). Studies with a clear focal generator — including
  asymmetric pipelines (CLEAR: Llama interprets, GPT-4 generates → Proprietary) and same-family comparisons
  (three open models → Open-weight; three proprietary → Proprietary) — were **not** moved to Multiple/comparative.

**Recomputed distribution (from the 36 study-level decisions):** proprietary **18**, open-weight **10**,
multiple/comparative **2**, DialogFlow **2**, not reported **4** (= 36). Net change vs. the previous 19/11/2/4:
Rakhimova (was in the proprietary aggregate) and García-Montero/R022 (was open-weight) moved to
multiple/comparative; Gan (#19) remains open-weight; #12/#17 remain proprietary.

**Changes.** Documented rule added to Method (`metodo_rsl.tex`, §Extração); Table 1 relabelled with the new
category; RQ3 narrative rewritten (proprietary 18, open 10, new multiple/comparative paragraph); Abstract/Resumo,
Discussion §3 and reception paragraph, and Conclusion delabelled/recounted; extraction records for the two
comparative studies annotated. No inter-rater validation is claimed; the single-reviewer limitation is preserved.
This is an operational clarification of RQ3 coding, **not** a new taxonomy dimension.
