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

---

## 6. Adendo — rodada de recuperação de full-text e integração (corpus 29 -> 36)

Rodada **posterior** à validação final. Diferentemente do adendo §5 (mudanças apenas terminológicas, corpus
congelado em 29), esta rodada **altera o corpus** porque houve recuperação REAL e documentada de textos completos,
com os 9 PDFs correspondentes depositados em `recovered_fulltexts/` (7 elegíveis) e `recovered_fulltexts_excluded/`
(R010, R033). A migração 29 -> 31 vetada anteriormente **não** foi reintroduzida: R005 e R036 permanecem
*not retrieved*, e o corpus foi para 36 (não 31).

**Cadeia obrigatória cumprida por estudo** (PDF -> elegibilidade -> extração -> QA -> classificação -> cálculo ->
síntese -> manuscrito). Extração dos 7 novos feita do texto completo com o mesmo formulário (blocos adicionados a
`resultado_extracao_rsl.txt`, agora 36 blocos).

**Recuperados (9/19):** incluídos R001, R006, R008, R009, R011, R021, R022 (IDs 30–36 na tabela consolidada);
excluídos após full-text R010 (sem evidência primária independente; sintetiza Baron et al. 2023/R012) e R033
(não atende CI1). Permanecem *not retrieved* (10): R005, R014, R019, R020, R024, R028, R030, R031, R036, R043.

**Recomputações a partir dos dados** (não substituição mecânica): PRISMA internacional 46→10 not retrieved→36
avaliados→2 excluídos→34 incluídos; +2 SBC/SOL = 36. Modelos GPT 19 / abertos 11 / DialogFlow 2 / NR 4. Empíricos
28 / conceituais 8. Alucinação 24/36. D1 oferta 9 / demanda 27. D2 LJ 9, OGD 12, SP 9, PS 5, C 1. Geografia
Europa 15, Ásia 7, AmNorte 5, AmSul 5, Oceania 1, África 0, multirregião 1, sem contexto 2. QA min 2,0 / máx 5,0 /
mediana 4,5 (mantida) / 12 em 5,0 / 2 abaixo de 2,5 (Dineva 2,0; TNGov-GPT/R008 2,0). Achado central mantido e
reverificado: nenhum dos 36 mede desfecho cívico.

**TAXONOMY REVIEW:** nenhuma nova categoria foi necessária — os 7 estudos couberam em D1/D2/D3 existentes. A camada
de explicabilidade (XAI) de R009 foi representada como função de geração (GS); é candidata a uma função própria de
"explicação/interpretabilidade" apenas se o padrão recorrer (1 estudo não justifica).

**Compilação:** `latexmk -xelatex` exit 0; 0 undefined citations; 0 undefined references; 23 páginas; 3 overfull
hbox menores e pré-existentes (frontmatter datas/resumo), sem estouro das tabelas ampliadas.

**Ação humana pendente desta rodada:** (1) regenerar a imagem `imagens/fluxograma_prisma.png` (ainda mostra
19/27/29 → deve mostrar 10/36/2/34); (2) confirmar o ano definitivo de García-Montero et al. (fixado em 2025 pelo
prefixo de DOI 978-3-032; a tabela antiga trazia 2026) e os nomes exatos dos proceedings LNCS/CCIS
(`[A CONFIRMAR]` no `.bib`); (3) contexto governamental de R001 (não especificado no texto) e classificação
multirregião de R006 (Estônia/Singapura/UE) — confirmar; (4) inspeção visual do PDF (sem poppler no ambiente).

## 7. Adendo — passe de validação pré-merge (2026-08-22)

Itens (1)-(3) de §6 RESOLVIDOS: (1) PRISMA `imagens/fluxograma_prisma.png` substituída manualmente pela autora
(git: modificada; deve mostrar 46→10→36→2→34); apenas referência e embedding verificados aqui (sem poppler para
inspeção raster). (2) Ano de García-Montero validado como **2026** (capítulo Springer CCIS; evento TICEC 2025;
pp. 63-77); chave BibTeX renomeada `GarciaMontero2025`→`GarciaMontero2026` no `.bib` e nas 3 citações do
`resultados_rsl.tex`; ainda dentro de 2024-2026, sem alteração de contagem. Proceedings preenchidos: Giarelis =
"Electronic Government (EGOV 2025)", LNCS 15944, pp. 368-379. (3) R001 mantido "não especificado"; R006 mantido
"multirregião" (texto analisa explicitamente Estônia, Singapura e UE). Recompilação `latexmk -xelatex` exit 0,
0 undefined. Relatório: `FINAL_PREMERGE_VALIDATION.md`. Nada commitado.

## 8. Adendo — recodificação da família de modelo (RQ3), sem alterar corpus/eligibilidade

Correção do problema apontado em `MODEL_CODING_AUDIT.md`: a variável de família de modelo (RQ3) era mutuamente
exclusiva, mas a redução por "modelo principal" nunca fora definida; o rótulo agregado "família GPT" absorvia
proprietários não GPT (Gemini, Copilot); e há estudos com mais de uma família. **Nada além da RQ3 descritiva foi
tocado** — corpus 36, elegibilidade, PRISMA, QA, geografia, D1/D2/D3, alucinação e desfecho cívico inalterados.

- Regra formalizada e documentada no Método (§Extração), aplicada de forma uniforme aos 36 estudos: categoria pela
  família dos modelos **generativos centrais**; auxiliares (embedding, reordenação, recuperação, classificador,
  juiz, dados sintéticos, pré-processamento) não contam; baseline que é arm completo de comparação direta =
  coprimário. Categorias: Proprietário / Pesos abertos / Múltiplos-comparativo / DialogFlow / Não reportado.
- Rótulo agregado "família GPT" → **"Proprietário"** (menções às tecnologias GPT-3.5/4/4o preservadas).
- **"Múltiplos/comparativo"** só para desenhos simétricos entre famílias sem modelo focal: **#20 Rakhimova**
  (GPT-4o-mini vs. 7 abertos) e **#36 R022** (Gemini/GPT-4.1-mini vs. DeepSeek/Llama-4). #12 (pipeline assimétrico,
  GPT-4 focal) e #17 (comparação toda proprietária) permaneceram Proprietário; #19 permaneceu Pesos abertos.
- **Distribuição recomputada** dos 36: Proprietário 18 / Pesos abertos 10 / Múltiplos-comparativo 2 / DialogFlow 2
  / Não reportado 4 (= 36). Supersede o "GPT 19 / abertos 11 / DF 2 / NR 4" do §6/§7 (aquele número é estado
  anterior). Sem validação entre avaliadores; limitação de revisão única preservada. Não é nova dimensão de
  taxonomia — é clarificação operacional da RQ3. `latexmk -xelatex` exit 0, 0 undefined. Relatório:
  `RQ3_MODEL_FAMILY_RECODING_REPORT.md`. Nada commitado.
