# Model-Family Coding Audit (RQ3) — audit only, no files modified

**Question.** R022 (García-Montero et al.) is a genuinely **symmetric multi-model comparison** — proprietary
(Gemini 2.5 Flash, GPT-4.1 Mini) vs open-weight (DeepSeek V3, Llama 4 Maverick), **no single main model**. Does
the existing mutually-exclusive model-family variable have a rule that codes this consistently, and does the rest
of the corpus already show the same ambiguity?

**Method.** Read the `Modelo(s) (RQ3)` field of all 36 extraction blocks (`resultado_extracao_rsl.txt`), the
`Modelo principal` column of the consolidated table (`isys_rsl.tex`), Table 1 (`tab:corpus`), the RQ3 narrative,
and the method's extraction/synthesis sections. Nothing was edited; no count recomputed; R022 unchanged.

---

## 1. Is the model-family field governed by a documented rule?

**No.** The variable is presented as **mutually exclusive** — Table 1 (`Modelo principal (RQ3)`) partitions the
corpus into four buckets that sum to N: *Proprietário (família GPT)*, *Pesos abertos*, *Plataforma conversacional
(DialogFlow)*, *Não reportado* (19 / 11 / 2 / 4 = 36). But:

- The **extraction form** field is plural and descriptive: "**Modelo(s)** — LLM/IA Generativa, porte, licença"
  (`metodo_rsl.tex:171`); RQ3 itself is "**Quais LLMs são utilizados?**" (plural). Nothing there says "pick one".
- The term "**modelo principal**" appears only in the **Results/Table 1** (`resultados_rsl.tex:65`, `:219`,
  `:221`) and in the consolidated-table column header — and is **never defined**. There is no stated tie-break for
  studies that use or compare more than one model or family.
- Contrast with the taxonomy: the synthesis section **explicitly documents** the "**aplicação principal**" rule
  for RQ1 and for D1/D2 ("cada estudo foi classificado segundo sua aplicação principal, identificada a partir do
  objetivo e do caso de uso"; `metodo_rsl.tex:181`; `resultados_rsl.tex:141`). **No analogous rule exists for the
  model family.**
- The RQ3 narrative even **acknowledges multi-model use without a reduction rule**: "Modelos como Gemini e Copilot
  aparecem … como alternativas comparadas dentro de um mesmo estudo" and "Alguns estudos combinam modelos de
  naturezas distintas … como em CLEAR, que usa Llama para interpretar a consulta e GPT-4 para gerar o relatório"
  (`resultados_rsl.tex:219`, `:218` region). The manuscript knows families are mixed, yet Table 1 still forces one
  bucket per study, silently.

**Operative (implicit) rule, inferred from practice** (not written anywhere):
(a) the family = that of the **generative LLM that produces the output**; (b) **non-generative helpers do not
count** — sentence encoders / embedding models / re-rankers (BERT, `text-embedding-ada-002`, `text-embedding-3`,
`all-MiniLM`, `bge`, `simlm` reranker); (c) **baseline-only and judge/synthetic-data models do not count**;
(d) **same-family multi-version** use collapses to that family. There is **no rule for cross-family symmetric
comparisons** — which is exactly R022's case.

Also a **label-precision issue** (Reviewer C, terminology): the bucket is named "**família GPT**", but it absorbs
non-GPT proprietary models (Gemini/Google, Copilot/Microsoft in #17). It functions as "proprietary", so the label
is looser than literal.

## 2. Studies that use / compare more than one model or family

| # | Study | Models recorded (RQ3) | >1 model? | >1 **family**? | Clear focal/main? | Reduced to |
|---|---|---|---|---|---|---|
| 6 | Colombo et al. | Mistral-7B (gen) + BERT (classif.) | yes | no (open + encoder) | yes — Mistral | Open |
| 8 | Gao et al. | ChatGPT (gen) + BERT (embed.) | yes | no (GPT + encoder) | yes — ChatGPT | GPT |
| 10 | Mamalis et al. | gpt-3.5-turbo ×2 + ada-002 | yes | no (GPT + encoder) | yes — GPT-3.5 | GPT |
| 12 | Wu et al. (CLEAR) | **Llama-3.2-3B (interpret, open) + GPT-4 (generate, proprietary)** + embed-3 | yes | **YES (open+prop.)** | partial — GPT-4 does final gen | (proprietary, per narrative) |
| 13 | Schelhorn et al. | GPT-3.5-turbo + GPT-5-mini + ada-002 | yes | no (same family) | yes — GPT | GPT |
| 14 | Maslaris et al. | Llama-3.1 + Mistral-7B + Gemma (all open) + MiniLM | yes | no (all open) — **comparison** | no (3 compared) | Open |
| 17 | Farah & Sin | **ChatGPT + Gemini + Copilot (all proprietary, 3 vendors)** | yes | mixed-vendor proprietary — **comparison** | no (3 compared) | Proprietary ("família GPT") |
| 18 | Flores et al. | GPT-4o (gen) + embed-3-small | yes | no (GPT + encoder) | yes — GPT-4o | GPT |
| 19 | Gan et al. | **Gemini-2.5 (proprietary, synth. queries) + Gemma (open, main tool) + bge (embed)** | yes | **YES (prop.+open)** | ambiguous roles | see §3 |
| 20 | Rakhimova et al. | **GPT-4o-mini (proprietary) + Gemma/KazLLM/Llama/Phi/Qwen/Mistral (7 open), fine-tuned & compared** | yes | **YES (prop.+open)** — **symmetric-ish comparison** | no focal | see §3 |
| 21 | Papageorgiou et al. | GPT-4.1 + GPT-4.1-mini (+ reranker) | yes | no (same family) | yes — GPT | GPT |
| 24 | Colombo | Llama-3-70B (gen, open) + embed-3-small | yes | no (open + encoder) | yes — Llama | Open |
| 34 | Fang & Xu | Qwen (gen, open) + BERT; **GPT-3/BERT as baselines** | yes | no (open main; GPT baseline) | yes — Qwen | Open |
| 35 | Tsourma et al. | Meltemi-7B (gen, open); **GPT-4 only as judge / synthetic-data generator** | yes | no (open main; GPT auxiliary) | yes — Meltemi | Open |
| **36** | **García-Montero (R022)** | **Gemini 2.5 Flash + GPT-4.1 Mini (proprietary); DeepSeek V3 + Llama 4 Maverick (open) — symmetric comparison** | yes | **YES (2 prop. + 2 open)** | **NO focal model** | *(pending)* |

Single-model / single-family studies (1,2,3,4,5,7,9,11,15,16,22,23,25,26,27,28,29,30,31,32,33) are unaffected.

## 3. How each multi/mixed case was reduced to the exclusive category

- **Helper exclusion** (unambiguous, consistent): #6, #8, #10, #13, #18, #21, #24, #34, #35 — the encoder /
  embedding / re-ranker / baseline / judge model is dropped; the generative LLM's family is used. This is coherent
  and defensible, but the rule is **not written down**.
- **Same-family versions** (#13, #21, #23): collapse to GPT — trivial, consistent.
- **All-open comparison** (#14) → Open; **all-proprietary comparison** (#17) → Proprietary. Consistent *because the
  compared models share a family* — the exclusive bucket is unambiguous even without a rule.
- **Cross-family generative pipeline** (#12): both a Llama (open) and GPT-4 (proprietary) are integral; the
  narrative frames GPT-4 as the final generator, and the partition (below) places it in **Proprietary**. This is a
  judgement, not a stated rule.
- **Cross-family comparisons with no shared family** (#19, #20 — and now #36/R022): here the exclusive bucket is
  **not determinable** without an arbitrary choice.

**Partition arithmetic (verifiable, baseline 29 = 18 GPT / 6 open / 2 DialogFlow / 3 NR):** NR = {3,4,5};
DialogFlow = {2,25}; unambiguous Open = {6,7,14,24,29} (5); unambiguous/same-family GPT incl. all-proprietary #17
= 16. That leaves **{#12,#19,#20}: exactly two coded GPT and one coded Open** to reach 18/6. Given #12's GPT-4
final generation, the single "Open" among them is most plausibly **#19 (Gan) or #20 (Rakhimova)** — but **the
manuscript never states which study, or on what basis**. The RQ3 open-weight enumeration
(`resultados_rsl.tex:221`) names only the Llama/Mistral/DeepSeek/ChatGLM studies and does **not** name #17/#19/#20
in either the open or the explicit proprietary list. **→ their assignment is opaque from the manuscript.**

## 4. Can R022 be coded consistently under the same rule?

**No — because there is no documented rule, and the *implicit* rule cannot select a family for R022.**
- Helper-exclusion: N/A (all four are peer generative LLMs).
- Final-generator: N/A (no pipeline; parallel evaluation).
- Focal/deployed model: **none** (symmetric benchmark; no deployed system).
- Any single assignment would need an undocumented tiebreak — e.g., best performer (Llama-4 Maverick → Open) or
  the paper's rhetorical emphasis on open-source viability (→ Open). Both are *ad hoc* and used nowhere else.

So coding R022 into one exclusive family reproduces exactly the **opaque, rule-less** reduction already applied to
#19/#20 — it does not achieve consistency, it inherits the same inconsistency.

## 5. Do existing studies reveal the same ambiguity?

**Yes — R022 is not unique.** At least three pre-existing studies raise the identical issue **independently of
R022**:
- **#20 Rakhimova** — closest analog: a fine-tuning **comparison of GPT-4o-mini (proprietary) + 7 open models**,
  no deployed single model.
- **#19 Gan** — proprietary (Gemini) + open (Gemma) with mixed roles.
- **#17 Farah & Sin** — a 3-model **comparison** (only forced cleanly because all three happen to be proprietary,
  though two are non-GPT, exposing the label problem).
- **#12 Wu/CLEAR** — a cross-family generative pipeline (open + proprietary both integral).

The corpus therefore already contains the multi-family/comparison pattern, and at least one such study was placed
in an exclusive bucket **without a documented justification**. This is a **corpus-level coding-transparency gap**,
not a one-off caused by R022.

## 6. Recommendation

Grounded on the corpus (not on R022 being unusual): the exclusive variable already **lacks a documented rule** and
already **forced ≥3 multi-family studies (#17/#19/#20, plus the cross-family pipeline #12) into single buckets, at
least one opaquely**. Two things must happen regardless of which option is chosen: **(0) document the reduction
rule** (main *deployed generative* model; encoders/embedding/re-ranker/judge/baseline models and same-family
versions do not change the family), and **(0b) rename the bucket "família GPT" → "Proprietário"** so it does not
mislabel Gemini/Copilot (#17).

Given that, the ranked options:

- **Option A (keep exclusive + assign R022 by an existing documented rule) — insufficient alone.** There is no
  existing documented rule to invoke, and even the implicit practice yields **no** family for R022/#20 (no focal
  model). Forcing a choice perpetuates the #19/#20 opacity that Reviewers A/C flagged. A only works for the ~30
  studies that *do* have a single deployed generative model.

- **Option B (add an explicitly-defined mutually-exclusive value "Comparativo / múltiplas famílias") —
  RECOMMENDED as the primary path.** Justified by the pre-existing symmetric/cross-family comparisons
  (R022, #20, and arguably #17/#19), **not** by R022 alone. It (i) preserves mutual exclusivity and keeps Table 1
  a clean partition summing to N — the *consistency* Reviewer C asked for; (ii) turns the previously opaque forced
  choices into an **auditable, explicit** category — the *coding transparency* Reviewer A asked for; (iii) is the
  smallest conceptual change. It should be applied **only** to studies that are genuine symmetric comparisons with
  no deployed focal model (by the documented rule), so single-deployment studies keep their concrete family.

- **Option C (redesign RQ3 as non-exclusive family *presence*) — recommended alternative if maximum fidelity is
  preferred.** It removes *all* forced reductions (including the helper judgement calls), and it is **precedented
  in this very manuscript**: the taxonomy's Dimension 3 (function) is already non-exclusive with a documented
  rationale, so a non-exclusive "family present in the study" is internally coherent. Cost: Table 1 stops being a
  partition (counts become presence counts that can exceed N), and RQ3 must be re-tabulated.

**Bottom line.** Do **A's rule-documentation and the label fix in all cases**; for the handful of symmetric
comparisons adopt **B** (primary) or, if the authors want the most faithful representation and accept
re-tabulation, **C**. Implementing any of these requires editing extraction/Table 1 and recomputing RQ3 — **out
of scope for this audit** and left as an explicit decision for the authors.

## 7. Impact on Reviewer A / C concerns

- **Reviewer A (coding transparency, single reviewer).** The undocumented "modelo principal" reduction is a
  concrete instance of the transparency weakness Reviewer A raised. Documenting the rule (0) + making comparisons
  explicit (B) or presence-based (C) directly answers it and is auditable against `resultado_extracao_rsl.txt`.
- **Reviewer C (taxonomy consistency, terminology).** B preserves exclusivity/partition (consistent with how D1/D2
  are presented) and the "família GPT"→"Proprietário" rename fixes a terminology inaccuracy Reviewer C-type checks
  would catch. C is also consistent (mirrors the non-exclusive D3), at the cost of changing the counting basis.
- **Do NOT** frame any change as triggered by R022; frame it as resolving a **pre-existing** multi-family coding
  ambiguity (#12/#17/#19/#20) that R022 merely makes unavoidable.
