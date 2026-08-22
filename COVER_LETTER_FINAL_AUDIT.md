# Cover Letter — Final Revision Audit (Major Revision)

Only `cover_letter.md` was edited; `COVER_LETTER_FINAL_AUDIT.md` was created. No other file was modified; nothing
committed. Structure, tone (acadêmico/cordial), section organization, numbered highlights, and the two-author
signature of the original were preserved.

## 1. Title: old → current
- **Old:** "Generative AI for **Open Government Data Access** and Public Transparency: A Systematic Literature Review"
- **New (used verbatim):** "Generative AI for **Public-Sector Information Access** and Public Transparency: A
  Systematic Literature Review" — matches `isys_rsl.tex` `\title`/`pdftitle`.

## 2. Opening paragraph
Reframed from an initial submission to a **resubmission after Major Revision**: states that the revised version is
submitted in response to the reviewers/editorial decision, thanks the reviewers, notes that substantial changes
were made, and points to the accompanying point-by-point **Response Letter**. Section *Surveys* retained. Subject
changed from "Submissão de manuscrito — Revisão Sistemática da Literatura" to **"Reapresentação de manuscrito
revisado — Major Revision"**.

## 3. Scope: OGD → Public-Sector Information
"Escopo e adequação ao iSys" rewritten: scope is now **informação do setor público** in the broad sense (OGD +
official documents + digital-government service content), with **OGD as paradigmatic but not exclusive** case;
sociotechnical transparency framing made explicit; IS framing preserved ("Understanding the IS nuances"). No
rhetorical inflation.

## 4. Corpus N=29 → N=36
Every corpus figure updated: **36 estudos (34 internacionais + 2 SBC/SOL)**. The stale "29 estudos / 27
internacionais" removed. Highlight 1 updated accordingly.

## 5. How the additional retrieval was summarized
"Background e cobertura da literatura": one concise sentence — the original search string was **not** re-run; in
response to Reviewer A, an additional full-text retrieval round was conducted; of the 19 previously unretrieved
reports, **nine were recovered and reassessed under the unchanged CI/CE, yielding 7 inclusions and 2 full-text
exclusions; ten remained unretrieved; final corpus = 36**. No study IDs (R001 etc.) listed; not turned into a
PRISMA walk-through.

## 6. Research Highlights: old → new
| # | Old | New |
|---|---|---|
| 1 | 29 estudos, convergência IA Generativa/LLMs × OGD | **36 estudos** (34+2), IA Generativa/LLMs no acesso, organização e mediação da **informação do setor público** (OGD → legislação, decisões, documentos oficiais) |
| 2 | Taxonomia oferta vs demanda (duas categorias) | **Taxonomia multidimensional**: posição na cadeia (oferta/preparação vs demanda/mediação), objeto informacional e funções dos sistemas |
| 3 | "predominância de modelos proprietários da família GPT (18/29)" | Predominância de modelos **proprietários**, adoção relevante de **pesos abertos** e um pequeno conjunto de estudos **comparativos entre famílias** (rótulo "família GPT" eliminado; sem os cinco números, todos consistentes com 18/10/2/2/4 se citados) |
| 4 | "Formula o **paradoxo da transparência**…" | "Identifica uma **lacuna** entre transparência como motivação e sua avaliação empírica: **nenhum dos 36 estudos** mensura transparência como desfecho cívico efetivo" (sem linguagem de causalidade, sem reivindicar conceito novo) |
| 5 | Agenda SI (cidadão/compreensão/confiança/uso efetivo/qualidade+confiabilidade) | Preservada e alinhada à discussão revisada; acrescido "para além de métricas puramente técnicas"; sem afirmar que esses elementos foram empiricamente avaliados |

Highlights descrevem o artigo, não o processo editorial (nenhum item vira changelog "respondemos ao Reviewer A…").

## 7. "família GPT" correction
The aggregate label "modelos proprietários da família GPT (18/29)" (Highlight 3) was replaced by **"modelos
proprietários"** plus mention of open-weight and comparative studies, consistent with the RQ3 recoding
(Proprietário 18 / Pesos abertos 10 / Múltiplos-comparativo 2 / DialogFlow 2 / Não reportado 4). No numeric family
values are asserted in the letter, so none can be wrong. Individual GPT technology names are not used in the
letter.

## 8. "paradoxo da transparência" correction
Removed as an authored conceptual contribution. The letter now states the empirically supported finding — a **gap
between transparency as motivation and its empirical evaluation; none of the 36 studies measures transparency as
an effective civic outcome** — using cautious, non-causal wording, consistent with the manuscript (which attributes
the "paradoxo da transparência" term to a single primary study, not to the authors).

## 9. Final state of the AI-use declaration
The letter now **truthfully** states that, in this revision, Generative-AI tools (Claude/Anthropic and
Gemini/Google — only the tools already declared in the manuscript) were used **as support** not only for writing,
material organization and textual-coherence checks, but also for **reading/auditing the recovered full texts,
organizing evidence, consistency checks, and updating the extraction sheet**; that **all inclusion/exclusion,
interpretation, classification and final-content decisions remained with the authors, who verified and validated
every AI-supported result**; and that scientific responsibility is entirely the authors'. No autonomous scientific
decision is attributed to the tools; no tool names invented.

## 10. Consistency with the Response Letter
Consistent: both use the current title, N=36 (34+2), the 9-recovered/7-included/2-excluded/10-not-retrieved
recovery summary, the RQ3 "proprietary / open-weight / comparative" framing, and the "0/36 civic outcome" finding.
The Response Letter's new "RQ3 model-family coding" section and the cover letter agree. The cover letter does not
reproduce point-by-point reviewer responses (it points to the Response Letter).

## 11. Obsolete values found/removed (sweep of cover_letter.md)
Searched and **absent** in the final letter: "29 estudos", "27 internacionais/bases", "18/29", "família GPT",
"GPT family", "paradoxo da transparência", "19 reports…", "Open Government Data Access", and the old blanket
"nenhuma ferramenta de IA foi utilizada na análise/extração". Numbers present are all current (36 / 34 / 2;
9 recovered; 7 included; 2 excluded; 10 not retrieved).

## 12. Points requiring human decision
1. **HUMAN REVIEW REQUIRED — manuscript AI declaration mismatch.** `isys_rsl.tex` (*Further relevant information*)
   still states: *"Nenhuma ferramenta de IA foi utilizada na análise dos estudos, na triagem, na extração de dados
   ou nas decisões metodológicas, que foram conduzidas exclusivamente pelos autores."* This was accurate for the
   original 29-study round, but the documented Major-Revision process (see `RECOVERY_INTEGRATION_REPORT.md`,
   `revision_audit.md`) used AI to support reading/auditing the recovered full texts and the extraction update. The
   cover letter was written truthfully and therefore is **broader** than the manuscript's current declaration. I
   was instructed **not** to edit the manuscript, so this is flagged, not masked: the authors should update the
   manuscript's *Further relevant information* block to match the truthful cover-letter wording (support role
   extended to reading/auditing/extraction-update; authors retain and validate all decisions). Until then, the
   cover letter's pointer "declaração completa em *Further relevant information*" points to a **narrower** text.
2. **Minor (not fixed here):** `isys_rsl.tex` line 5 has a stale internal **comment** "% Tema: Generative AI for
   Open Government Data Access and Transparency". It is a non-rendered comment (not the title, not visible output),
   so no manuscript edit was made; worth tidying in a future manuscript pass.
3. **`cover_letter.md` repository/Open-science wording** matches the manuscript's *Availability of Data and
   Materials* (anonymous mirror during double-anonymous review; identified repository at camera-ready) — kept as
   factually current; confirm the anonymous mirror URL is still live before resubmission.
4. The "verificamos exploratoriamente a inexistência de um estudo secundário com o mesmo recorte" claim was
   retained in hedged form (as in the original and consistent with §2, which discusses three nearby secondary
   reviews); confirm this hedging is acceptable to the editors.
