# 02 — Reviewer Matrix

> **Alerta de fonte (Nível 4):** os **pareceres originais dos revisores não estão
> presentes no repositório** (busca por `parecer|review|revisor|decision|referee`
> não retornou arquivos). A matriz abaixo é **reconstruída do brief de revisão**.
> **REQUER AÇÃO HUMANA:** conferir cada item contra as cartas originais antes da
> ressubmissão. Nenhum relatório de IA tem precedência sobre os pareceres reais.

| Rev. | Comentário (reconstruído) | Pedido real | Estado atual | Evidência | Ação |
|---|---|---|---|---|---|
| A | "Taxonomia" é subespecificada | Estrutura conceitual definida | RESOLVIDO | `subsec:taxonomia`, `tab:taxonomia`, `fig:taxonomia`; Dim1 refatorada p/ ortogonal | Ver `03_taxonomy_validation.md` |
| A | Transparência não operacionalizada | Procedimento transparente p/ "0/29" | RESOLVIDO | regra de 4 níveis (`metodo` §Síntese) + `06_transparency_traceability.md` | — |
| A | Inferência "deslocamento" (tendência sem série) | Remover inferência temporal | RESOLVIDO | RQ2: "predominância… e não tendência histórica de substituição" | — |
| A | Alucinações "onipresentes/quase todos" | Contagem verificável | RESOLVIDO | "18 dos 29" (RQ5, Discussão) | — |
| A | Linguagem retórica (ironia, caixas-pretas) | Registro analítico | RESOLVIDO | "tensão entre opacidade e auditabilidade" | — |
| A | Recuperar os 19 not-retrieved | Esforço adicional de recuperação | **PARCIAL / REQUER AÇÃO HUMANA** | item "Viés de disponibilidade"; `reports_not_retrieved_todo.md` | Recuperação é ação humana separada; corpus não alterado |
| A | RSL vs. mapeamento | Coerência de desenho | RESOLVIDO (desenho híbrido) | `metodo` §1 | — |
| A | Enquadramento fraco em SI | Leitura sociotécnica | RESOLVIDO | fecho sociotécnico da Discussão | — |
| C | Tornar a taxonomia visível/definida | Tabela + figura + critérios | RESOLVIDO | `tab:taxonomia` (definição+critério), `fig:taxonomia` (relações) | — |
| C | Síntese geográfica ausente | Distribuição por país/contexto | RESOLVIDO | `subsec:geografia`, `tab:geografia` | — |
| C | Visão consolidada dos estudos | Tabela auditável estudo a estudo | RESOLVIDO | Apêndice B `tab:corpus_consolidado` (D1/D2/D3/Aval./QA) | — |
| C | Figura 1 linear (anterior/atual) | Complementaridade | RESOLVIDO | `fig:paradigmas` (Web Semântica ↔ IA; convergência) | — |
| C | Terminologia/idioma | Siglas definidas, consistência | RESOLVIDO | IA/SI/LLMs/OGD/RAG/PICOC/PRISMA/RSL; "Fundamentação e Trabalhos Relacionados" | — |
| A/C | Escopo OGD vs. maior | Título/escopo alinhados | RESOLVIDO nesta rodada | título → "Public-Sector Information"; abstract/conclusão/CE1 alinhados | — |

**Legenda:** RESOLVIDO · PARCIAL · PENDENTE · NÃO APLICÁVEL · REQUER AÇÃO HUMANA.
