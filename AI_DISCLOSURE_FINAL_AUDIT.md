# AI-Disclosure Final Consistency Audit — iSys Major Revision

Narrow pass to reconcile the manuscript's AI-use disclosure with the (already truthful) cover letter and the
documented Major-Revision workflow. **Only `isys_rsl.tex` was edited** (the `furtherinformation` disclosure and one
non-rendered source comment). No change to corpus, eligibility, extraction data, QA, PRISMA, results, taxonomy,
RQ3, cover letter, or response letter. Nothing committed.

## 1. Old disclosure (manuscript, `furtherinformation`)
> "Os autores utilizaram ferramentas de IA Generativa (Claude, da Anthropic, e Gemini, do Google) como apoio à
> revisão de estilo, à organização de materiais e à verificação de coerência textual. **Nenhuma ferramenta de IA
> foi utilizada na análise dos estudos, na triagem, na extração de dados ou nas decisões metodológicas**, que foram
> conduzidas exclusivamente pelos autores. Todo o conteúdo final foi revisado e validado pelos autores, que assumem
> responsabilidade integral por ele."

The bolded blanket claim was accurate for the original 29-study round but no longer reflects the complete revised
workflow, in which AI supported reading/auditing the recovered full texts and the extraction update.

## 2. Final disclosure (manuscript, `furtherinformation`)
> "Os autores utilizaram ferramentas de IA Generativa (Claude, da Anthropic, e Gemini, do Google) como apoio à
> revisão textual e de estilo, à organização de materiais e à verificação de coerência e consistência. A busca
> automática e a triagem originais dos estudos foram conduzidas pelos autores. Durante a rodada de revisão maior,
> essas ferramentas também auxiliaram a leitura e a auditoria dos textos completos recuperados, a organização das
> evidências e a preparação e conferência da atualização dos registros de extração. As decisões de elegibilidade,
> codificação, interpretação e síntese foram tomadas e validadas pelos autores, com conferência das evidências nos
> textos completos. As ferramentas de IA não foram tratadas como fonte autônoma de evidência nem tomaram decisões
> metodológicas de forma independente. Todo o conteúdo final foi revisado e validado pelos autores, que assumem
> integral responsabilidade científica pelo trabalho."

It distinguishes (A) tool support — including the revision-round reading/auditing/organization/extraction-update —
from (B) author responsibility, and (C) clarifies the original search/screening was conducted by the authors. It
does **not** claim AI had no role in analysis/extraction across the revision. Wrapped in `\rev{}` so the change is
highlighted like other revision edits.

## 3. Files modified
- `isys_rsl.tex` only: (i) the `furtherinformation` AI-use disclosure (rewritten); (ii) line-5 non-rendered
  comment "% Tema: … Open Government Data Access …" → "… Public-Sector Information Access and Public Transparency".
No other file touched.

## 4. Tool names retained
**Claude (Anthropic)** and **Gemini (Google)** — exactly the two already declared in the manuscript and used in the
cover letter. No tool name was added or invented (ChatGPT etc. not introduced).

## 5. How author responsibility is stated
Explicitly: eligibility, coding, interpretation and synthesis decisions were **made and validated by the authors**;
evidence was **checked against the full texts**; AI was **not** an autonomous source of evidence and **did not** make
independent methodological decisions; final content **reviewed and validated by the authors**, who hold **integral
scientific responsibility**. Support verbs used: apoio, auxiliaram, organização, auditoria, conferência.

## 6. Consistency with `cover_letter.md`
Semantically consistent (wording differs, as allowed). Both agree that: AI was used in a **supporting** role; the
Major Revision included AI-assisted reading/auditing/organization/consistency-checking and extraction-update
support; the **authors retained all decision-making**; and evidence and final outputs were **human-validated**. The
cover letter's pointer "declaração completa em *Further relevant information*" now resolves to a **matching** (no
longer narrower) manuscript statement. `cover_letter.md` was read but **not** edited.

## 7. Response Letter AI-use statements
`response_letter.md` contains **no** AI-use process disclosure that could conflict; its only Claude/Gemini-adjacent
mentions are corpus model names in the RQ3 discussion (Gemini/Copilot as studied systems). **No contradiction; no
edit made.**

## 8. Stale internal title comment correction
`isys_rsl.tex` line 5 comment updated to "Public-Sector Information Access and Public Transparency". This is a
source-code comment only (never rendered); the rendered `\title` was already correct and was **not** altered. No
occurrence of "Open Government Data Access" remains anywhere in `isys_rsl.tex`.

## 9. Compilation command and result
`latexmk -xelatex -interaction=nonstopmode -halt-on-error isys_rsl.tex` → **exit 0**; converged; **23 pages**; the
disclosure renders in the declarations block with no layout problem.

## 10. Undefined citations / references
**0 undefined citations; 0 undefined references; 0 fatal errors.**

## 11. Anonymous-mirror manual-check reminder
**Anonymous mirror availability requires manual browser verification.** The manuscript's *Availability of Data and
Materials* and the cover letter reference `https://anonymous.4open.science/r/anon-supp-materials-2026-BD9F` as the
double-anonymous review mirror; its liveness was **not** and cannot be verified in this environment. No URL was
changed or invented.

## 12. Remaining human-review items
1. Confirm the final disclosure matches the authors' recollection of the actual tool usage (it was written to the
   documented workflow in `RECOVERY_INTEGRATION_REPORT.md` / `revision_audit.md`); adjust wording if any listed
   support activity did not occur.
2. Manually verify the anonymous-mirror URL is live before resubmission (§11).
3. `COVER_LETTER_FINAL_AUDIT.md` item 1 (manuscript-declaration mismatch) is now **resolved** by this pass; the
   two audits can be read together.
