# 01 — Data Reconciliation (Checkpoint 1)

Reconciliação programática das contagens do manuscrito contra os dados primários
(`resultado_extracao_rsl.txt`, `busca_registros.csv`). Recontagem, não leitura do `.tex`.

| Métrica | Manuscrito | Dados | Status | Fonte |
|---|---:|---:|---|---|
| Corpus incluído | 29 | 29 | ✅ CONFIRMADO | registro `incluido` |
| Reports not retrieved | 19 | 19 | ✅ CONFIRMADO | registro `nao_recuperado` |
| Excluídos | 8 | 8 | ✅ CONFIRMADO | registro `excluido` |
| Alucinação discutida | 18/29 | 18/29 | ✅ CONFIRMADO | extração (regex `alucina|hallucinat|phantom flaw` em 29 blocos) |
| Família GPT (principal) | 18 | 18 | ✅ CONFIRMADO | extração RQ3 + `tab:corpus_consolidado` (D1/modelo) |
| Pesos abertos (principal) | 6 | 6 | ✅ CONFIRMADO | extração RQ3 (Llama, Mistral, Gemma, DeepSeek, ChatGLM) |
| DialogFlow (não-generativo) | 2 | 2 | ✅ CONFIRMADO | extração (R037, R017) |
| Modelo não reportado | 3 | 3 | ✅ CONFIRMADO | extração (R038, R035, R039) |
| Empíricos | 23 | 23 | ✅ (codificação humana) | campo "Avaliação" da extração |
| Conceituais | 6 | 6 | ✅ (codificação humana) | campo "Avaliação" |
| Taxonomia Dim1 — Oferta | 7 | 7 | ✅ CONFIRMADO | `tab:corpus_consolidado` D1=O |
| Taxonomia Dim1 — Demanda | 22 | 22 | ✅ CONFIRMADO | `tab:corpus_consolidado` D1=D |
| Objeto — Legislativo/jurídico | 8 | 8 | ✅ CONFIRMADO | consolidado D2=LJ |
| Objeto — Portais OGD | 11 | 11 | ✅ CONFIRMADO | consolidado D2=OGD |
| Objeto — Serviços/procedim. | 5 | 5 | ✅ CONFIRMADO | consolidado D2=SP |
| Objeto — Políticas/setoriais | 4 | 4 | ✅ CONFIRMADO | consolidado D2=PS |
| Objeto — Conceitual | 1 | 1 | ✅ CONFIRMADO | consolidado D2=C |
| RQ1 tipos descritivos | 7 / 11 / 11 | 7 / 11 / 11 | ✅ CONFIRMADO | `tab:corpus` (RQ1) |
| Geografia — Europa | 13 | 13 | ✅ CONFIRMADO | contexto governamental (consolidado) |
| Geografia — Ásia | 5 | 5 | ✅ CONFIRMADO | idem |
| Geografia — Am. Norte | 5 | 5 | ✅ CONFIRMADO | idem |
| Geografia — Am. Sul | 4 | 4 | ✅ CONFIRMADO | idem |
| Geografia — Oceania | 1 | 1 | ✅ CONFIRMADO | idem |
| Geografia — África | 0 | 0 | ✅ CONFIRMADO | idem |
| Geografia — conceitual s/ contexto | 1 | 1 | ✅ CONFIRMADO | idem |
| QA — nº escores no Apêndice | 29 | 29 | ✅ CONFIRMADO | somas por linha recalculadas (29/29 corretas) |
| Desfecho cívico medido | 0/29 | 0/29 | ✅ (ver `06_transparency_traceability.md`) | extração campo "Avaliação" |

**Somas de consistência interna:** Dim1 7+22=29; Objeto 8+11+5+4+1=29; RQ1 7+11+11=29; Geografia 13+5+5+4+1+0+1=29; modelos 18+6+2+3=29; método 23+6=29.

**Observação (empírico/conceitual):** o split 23/6 vem da codificação humana do campo "Avaliação" na extração e não é reproduzível de forma exata por palavra-chave (termos como "prova de conceito" aparecem em estudos empíricos). Mantido conforme a extração — fonte de verdade de Nível 1.
