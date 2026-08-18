# Response to Reviewers — iSys (Major Revision)

**Manuscript:** *Generative AI for Open Government Data Access and Public Transparency: A Systematic Literature Review*

We thank the editor and the reviewers for the careful and constructive assessment. Below we respond to each
point, indicating whether we agree, what was changed, and exactly where. All changed passages are highlighted
in the revised PDF (via the `\rev{}` command); a few entirely new elements (new tables, two new figures, and
the new taxonomy subsection) are marked as new by their highlighted captions/headings and are listed here.
No data, counts, categories, citations, or methodological procedures were invented; every factual change is
traceable to the extraction spreadsheet and the study registry provided in the supplementary materials.

> **Note on integrity of the corpus and method.** We did **not** alter the corpus (29 studies), the
> single-reviewer procedure, the absence of double coding, the absence of snowballing/grey literature, or the
> 19 reports not retrieved. Where a reviewer suggestion would have required re-running the protocol or
> fabricating data, we instead strengthened the corresponding limitation and, where possible, added verifiable
> synthesis from the data already collected.

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

**Response.** We counted the corpus: hallucination is **explicitly discussed in 18 of the 29 studies** (as a
risk to mitigate or as an observed result). We replaced every vague quantifier with this verifiable count and
removed "onipresença"/"quase todos".

**Changes.** RQ5 opening (`resultados_rsl.tex`: "…dezoito dos vinte e nove estudos…"); Discussion §3
(`isys_rsl.tex`), which also now reports "dezoito dos vinte e nove" for proprietary-model dependence and "três"
for unreported models.

### A4 — Rhetorical language

**Comment.** Expressions such as "ironia", "caixas-pretas", "criteriosa" weaken the scientific register.

**Response.** We agree and rewrote these passages analytically. The "irony" sentence became a statement about
the tension between component opacity and the auditability requirements of public transparency.

**Changes.** Discussion §3 (`isys_rsl.tex`, "…introduz uma tensão entre a opacidade de determinados componentes
tecnológicos e os requisitos de auditabilidade…"); Results selection paragraph ("aplicaram os critérios de
inclusão e exclusão" replacing "filtragem criteriosa").

### A5 — Additional effort to recover the 19 not-retrieved reports

**Comment.** Please attempt to recover the 19 reports not retrieved.

**Response.** We did **not** perform (or claim) additional retrieval beyond the original protocol, to avoid
misrepresenting the method. We instead (i) strengthened the availability-bias limitation and (ii) compiled the
19 studies with their DOIs so they can be attempted before any future extension. Recovering them would require
re-applying the full-text criteria and re-running extraction/quality assessment; until then the corpus remains
29 studies.

**Changes.** New Threats item **"Viés de disponibilidade"** (`isys_rsl.tex`), explaining that non-retrieval
concentrates in paywalled venues and may bias the corpus toward open-access work. Supplementary file
`reports_not_retrieved_todo.md` lists the 19 studies with DOIs.

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

### C3 — Consolidated view of the 29 studies

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

## Final validation round — additional changes (corpus frozen at 29)

> **Integrity note for this round.** The corpus remains **29 studies** (19 reports not retrieved, 8 excluded).
> No study was recovered or added; `busca_registros.csv`, the extraction file, and the corpus `.bib` were **not**
> modified. All changes below are terminological/conceptual and are highlighted with `\rev{}` in the revised PDF.

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
  bounded to the 29 included studies — `isys_rsl.tex`.
- **Terminology/acronyms**: "Background" → "Fundamentação e Trabalhos Relacionados"; first-use definitions of
  Inteligência Artificial (IA), Sistemas de Informação (SI); LLMs/OGD/RAG/PICOC/PRISMA/RSL verified.

### Reports not retrieved (Reviewer A) — status this round

**PARTIALLY RESOLVED / REQUIRES HUMAN ACTION.** The 19 remain *reports not retrieved*. No additional retrieval was
performed or claimed; the availability-bias limitation is reinforced and the list with DOIs is in
`reports_not_retrieved_todo.md`. Recovery is a separate human action for a future round; the corpus stays at 29.
