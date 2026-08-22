# RQ3 Model-Family Recoding Report

Controlled recoding of the **descriptive RQ3 model-family variable only**. Corpus stays **36**; eligibility,
PRISMA, QA, geography, D1/D2/D3, hallucination and civic-outcome findings **unchanged**. Nothing committed.

## 1. Final operational coding rule

A study is assigned to **one** mutually-exclusive category by the **generative** model(s) central to its study
design:

1. **Proprietary** — focal generative model(s) proprietary, all co-primary generative models proprietary
   (GPT family, Gemini, Copilot, …). *(Label is "Proprietary", not "GPT".)*
2. **Open-weight** — focal generative model(s) open-weight, all co-primary generative models open-weight.
   Several open models in one study still = Open-weight (not Multiple/comparative).
3. **Multiple/comparative** — **only** when generative models of **different ownership families** (proprietary +
   open) are **co-primary experimental conditions/components**, the design/conclusions depend on comparing or
   jointly using them, **and no single generative model is defensibly focal**.
4. **DialogFlow** — preserved for the studies already on that technology.
5. **Not reported** — family not determinable.

**Auxiliary models do not determine the category**: embedding, encoders, re-rankers, retrieval, classifiers,
judges/evaluators (LLM-as-judge), synthetic-data generation, preprocessing. **Exception:** a nominal baseline that
is a *full experimental arm* of a head-to-head generative comparison on which the conclusions depend is treated as
co-primary. This operationalizes the previously implicit "main model" rule uniformly across all 36 studies. Coding
by a single reviewer (limitation preserved; no inter-rater validation claimed).

## 2. Study-level classifications (all 36)

Legend families: P=proprietary, O=open-weight. Old = previous 36-pass bucket ("GPT/proprietary aggregate" or
open). New per the rule above.

| # | Study | Generative model(s) | Families | Focal? | Co-primary cross-family? | Old | New |
|---|---|---|---|---|---|---|---|
| 1 | Korpan | GPT-5 | P | yes | no | Prop | **Proprietary** |
| 2 | Cantador | DialogFlow | — | — | no | DF | **DialogFlow** |
| 3 | Dineva | unnamed LLM | ? | — | no | NR | **Not reported** |
| 4 | Ingole | unnamed (BERT/Rasa/DialogFlow generically) | ? | no | no | NR | **Not reported** |
| 5 | Nagesh | unnamed LLM (AWS Bedrock RAG) | ? | no | no | NR | **Not reported** |
| 6 | Colombo et al. | Mistral-7B (gen) + BERT (classif., aux) | O | yes—Mistral | no | Open | **Open-weight** |
| 7 | Gong | DeepSeek-v3 (gen) + RoBERTa (encoder baseline, aux) | O | yes—DeepSeek | no | Open | **Open-weight** |
| 8 | Gao | ChatGPT (gen) + BERT (embed, aux) | P | yes—ChatGPT | no | Prop | **Proprietary** |
| 9 | Gomez-Vazquez | GPT-4 | P | yes | no | Prop | **Proprietary** |
| 10 | Mamalis | gpt-3.5-turbo ×2 + ada-002 (aux) | P | yes—GPT | no | Prop | **Proprietary** |
| 11 | Loukis | ChatGPT (conceptual) | P | yes | no | Prop | **Proprietary** |
| 12 | Wu (CLEAR) | Llama-3.2-3B (interpret) + GPT-4 (**generate output**) + embed (aux) | O+P | **focal = GPT-4** (asymmetric pipeline) | no (not a comparison; focal exists) | Prop | **Proprietary** |
| 13 | Schelhorn | GPT-3.5-turbo + GPT-5-mini + ada-002 | P (same family) | yes—GPT | no | Prop | **Proprietary** |
| 14 | Maslaris | Llama-3.1 + Mistral-7B + Gemma (**all open**) + MiniLM | O (same family) | no (3 open compared) | no (same family) | Open | **Open-weight** |
| 15 | Schelhorn | GPT-3.5-turbo | P | yes | no | Prop | **Proprietary** |
| 16 | Monsalvo | GPT via Azure OpenAI | P | yes | no | Prop | **Proprietary** |
| 17 | Farah & Sin | ChatGPT + Gemini + Copilot (**all proprietary**, 3 vendors) | P (same family) | no (3 proprietary compared) | **no** (no open arm) | Prop | **Proprietary** |
| 18 | Flores | GPT-4o (gen) + embed (aux) | P | yes—GPT-4o | no | Prop | **Proprietary** |
| 19 | Gan | Gemini-2.5 (**synthetic-query gen, aux**) + Gemma (**main gen, open**) + bge (aux) | O (focal) | yes—Gemma | no (Gemini auxiliary) | Open | **Open-weight** |
| 20 | **Rakhimova** | **GPT-4o-mini (P) + 7 open models (Gemma/KazLLM/Llama/Phi/Qwen/Mistral), fine-tuned & compared** | O+P | **no focal** | **YES** | Prop (aggregate) | **Multiple/comparative** |
| 21 | Papageorgiou | GPT-4.1 + GPT-4.1-mini + reranker (aux) | P (same family) | yes—GPT | no | Prop | **Proprietary** |
| 22 | van Heusden | gpt-3.5-turbo | P | yes | no | Prop | **Proprietary** |
| 23 | Kliimask | GPT-3.5-turbo + GPT-4 | P (same family) | yes—GPT | no | Prop | **Proprietary** |
| 24 | Colombo | Llama-3-70B (gen, open) + embed (aux) | O | yes—Llama | no | Open | **Open-weight** |
| 25 | Cortes-Cediel | DialogFlow | — | — | no | DF | **DialogFlow** |
| 26 | Baron | ChatGPT (GPT-3.5) | P | yes | no | Prop | **Proprietary** |
| 27 | Silva et al. | GPT-4 | P | yes | no | Prop | **Proprietary** |
| 28 | Freitas e Silva | ChatGPT | P | yes | no | Prop | **Proprietary** |
| 29 | Han | ChatGLM-6B | O | yes | no | Open | **Open-weight** |
| 30 | Syahidi | GPT-4 (fine-tuned) | P | yes | no | Prop | **Proprietary** |
| 31 | Ryu | no model implemented; cross-national analysis (RASA/BERT-EU/GPT-4 exemplar) | ? | no | no | NR | **Not reported** |
| 32 | Kumar | GPT-2 (open-weight) | O | yes | no | Open | **Open-weight** |
| 33 | Giarelis | Llama-3.1 8B (gen, open) + KG + XAI | O | yes—Llama | no | Open | **Open-weight** |
| 34 | Fang & Xu | Qwen (**proposed focal**, open) + BERT (aux); GPT-3/BERT baselines | O (focal) | yes—Qwen | no (proposed-vs-baseline; focal exists) | Open | **Open-weight** |
| 35 | Tsourma | Meltemi-7B (focal, open); GPT-4 **only as judge/synthetic-data** (aux) | O (focal) | yes—Meltemi | no | Open | **Open-weight** |
| 36 | **García-Montero (R022)** | **Gemini 2.5 Flash + GPT-4.1 Mini (P) vs DeepSeek V3 + Llama 4 Maverick (O), same 16 datasets** | O+P | **no focal** | **YES** | Open | **Multiple/comparative** |

## 3. Cross-family cases found

Studies where generative models of different ownership families appear: **#12, #19, #20, #36**. Of these, only
**#20 and #36** meet all Multiple/comparative criteria (symmetric, co-primary, no focal). **#12** is an asymmetric
pipeline with GPT-4 as the output generator (focal → Proprietary); **#19** uses Gemini only for auxiliary
synthetic-query generation, leaving Gemma as the focal generator (→ Open-weight). #17 is cross-*vendor* but
all-proprietary (no open arm) → Proprietary, not Multiple/comparative.

## 4. Decisions for #12, #19, #20, R022

- **#12 Wu/CLEAR → Proprietary.** Asymmetric pipeline: Llama-3.2-3B interprets the query, **GPT-4 generates the
  delivered report**. A single focal generator is defensible; not a comparison. (Rule §C fails "no focal".)
- **#19 Gan → Open-weight.** Gemini-2.5 generates the synthetic evaluation queries (auxiliary data-generation,
  §D); the focal generative tool is the open Gemma; bge is embeddings. Not a cross-family co-primary comparison.
- **#20 Rakhimova → Multiple/comparative.** GPT-4o-mini (proprietary) and seven open models are fine-tuned and
  compared as equal experimental conditions on Kazakh legal QA; no focal model. Not decided by best score,
  rhetoric, order, or which model is open.
- **R022/#36 García-Montero → Multiple/comparative.** Gemini 2.5 Flash + GPT-4.1 Mini (proprietary) and DeepSeek
  V3 + Llama 4 Maverick (open) evaluated on the same 16 datasets / same framework; explicitly compares proprietary
  vs open; no methodologically dominant model. (Consistent with the full-text audit.)

## 5. Old vs new for every changed study

| # | Study | Old | New | Why changed |
|---|---|---|---|---|
| 20 | Rakhimova | Proprietary (in the "família GPT" aggregate) | **Multiple/comparative** | symmetric cross-family benchmark, no focal |
| 36 | García-Montero (R022) | Open-weight | **Multiple/comparative** | symmetric cross-family benchmark, no focal |
| all proprietary studies | — | *label* "família GPT" → **"Proprietário/Proprietary"** | terminology fix (absorbed Gemini/Copilot) |

No other study changed category. #12, #17, #19 were audited and **retained** (Proprietary, Proprietary,
Open-weight respectively).

## 6. Previous distribution

Proprietary (labelled "família GPT") **19** · Open-weight **11** · DialogFlow **2** · Not reported **4** = 36.

## 7. New distribution (recomputed from the 36 study-level decisions)

**Proprietary 18 · Open-weight 10 · Multiple/comparative 2 · DialogFlow 2 · Not reported 4 = 36.**
Net: −1 proprietary (#20 out), −1 open-weight (#36 out), +2 multiple/comparative.

## 8. Files modified

- `resultados_rsl.tex` — Table 1 model block (relabelled header "Família do modelo generativo (RQ3)"; rows
  Proprietário 18 / Pesos abertos 10 / Múltiplos-comparativo 2 / DialogFlow 2 / Não reportado 4); §Caracterização
  RQ3 sentence; §RQ3 proprietary sentence (18), open paragraph (10, R022 removed), new Multiple/comparative
  paragraph (#20, #36).
- `metodo_rsl.tex` — new documented RQ3 coding rule in §Extração.
- `isys_rsl.tex` — Abstract PT/EN (proprietary 18/36, label fixed); Discussion §3 (18) and reception paragraph
  (18, label dropped); Conclusion (label dropped).
- `resultado_extracao_rsl.txt` — family-classification notes added to #20 and #36 (R022 old "pesos abertos" label
  corrected to Multiple/comparative).
- `response_letter.md` — A3 count (18), retrieval-round model line, new "RQ3 model-family coding" subsection.
- `revision_audit.md` — §8 addendum.
- `RECOVERY_INTEGRATION_REPORT.md`, `FINAL_PREMERGE_VALIDATION.md` — superseding notes on the old 19/11/2/4.
- **Not modified:** consolidated table model column (holds model *names*, still accurate), QA appendix, geography,
  taxonomy, PRISMA, CSV decisions, `.bib`.

## 9. Manuscript sentences changed

Abstract PT ("Predominam modelos proprietários (18/36)"); Abstract EN ("Proprietary models prevail (18/36)");
Results §Caracterização (RQ3 sentence → 18 proprietary / 10 open / 2 comparative); Results §RQ3 (three
paragraphs); Discussion §3 ("dezoito dos trinta e seis"); Discussion reception ("dezoito dos trinta e seis",
label dropped); Conclusion ("modelos proprietários" without "família GPT"); Method §Extração (new rule paragraph).

## 10. Tables / figures changed

Table 1 (`tab:corpus`) model block only — header relabelled, one new row (Múltiplos/comparativo), counts 19→18 /
11→10 / +2. No figure changed. Taxonomy Table 8, geography table, QA appendix, consolidated table: **unchanged**.

## 11. Terminology changes

Aggregate bucket "família GPT" / "GPT family" → **"Proprietário" / "Proprietary"** (Table 1, abstract, discussion,
conclusion). Individual technology names GPT-3.5/GPT-4/GPT-4o and the descriptor "predominantly of the GPT family"
(within proprietary) are preserved. Legitimate non-aggregate mentions kept: Bastos2025's reported "predominância
da família GPT" (their finding); line 220's "predominantemente da família GPT" (actual technology).

## 12. N=36 and non-RQ3 analyses unchanged (verified)

Corpus **36** (34+2); not-retrieved 10; extraction 36 blocks. D1 supply 9 / demand 27; D2 LJ 9 / OGD 12 / SP 9 /
PS 5 / C 1; QA min 2.0 / max 5.0 / **median 4.5** / 12 at 5.0 / 2 below 2.5; geography sum 36 (Europe 15 / Asia 7 /
N.Am 5 / S.Am 5 / Oceania 1 / Africa 0 / multi-region 1 / no-context 2); hallucination 24/36; civic outcome 0/36 —
all **unchanged**. RQ3 categories sum to **36** (18+10+2+2+4).

## 13. Compile result

`latexmk -xelatex -interaction=nonstopmode -halt-on-error isys_rsl.tex` → **exit 0**; **0 undefined citations; 0
undefined references; 0 fatal errors**; converged (no rerun needed); **23 pages**.

## 14. Remaining human-review issues

1. **`cover_letter.md`** (line 51) still reads "modelos proprietários da família GPT (18/29)" — it predates the
   whole 29→36 migration and carries N=29 throughout. It needs a **separate full N=36 + RQ3 pass**; it was left
   untouched here to avoid creating false internal consistency (out of this task's listed scope).
2. **#19 Gan (Open-weight)** rests on reading Gemini's role as auxiliary synthetic-query generation and Gemma as
   the focal generator; the extraction wording ("Gemma among the main tools") is slightly terse — worth an author
   confirmation.
3. **#12 CLEAR (Proprietary)** treats GPT-4 as the focal output generator over the open interpreter Llama — a
   defensible but reviewable pipeline judgement.
4. Visual PDF pass (Table 1's new row, `\rev{}` highlights) — not rasterizable here (no poppler).
