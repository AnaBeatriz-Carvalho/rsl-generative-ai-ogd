# 04 — Reference Audit (Fase C)

## Resultado

- **Chaves de citação únicas no texto:** 57.
- **Undefined citations na compilação:** 0.
- **Undefined references:** 0.
- Todas as chaves `\citet/\citep/\cite` resolvem contra `referencias_rsl.bib` /
  `referencias_corpus.bib`.

## Resíduos da IA que adulterou o corpus (verificação dirigida)

| Entrada suspeita | No texto (`.tex`) | No `.bib` | Ação |
|---|---|---|---|
| `Ali2026TalkOpenData` (R005) | 0 | 0 | ✅ removido (bib revertido ao HEAD) |
| `Ferencek2023TopicModelling` (R036) | 0 | 0 | ✅ removido |
| `recovered_reports/` | n/a | n/a | ✅ diretório removido |

Ambas as entradas haviam sido inseridas indevidamente para sustentar o corpus=31.
Como R005 e R036 **não** fazem parte do corpus congelado de 29, suas entradas
BibTeX foram removidas junto com a reversão de `referencias_corpus.bib` ao commit.
Nenhuma referência conceitual legítima preexistente foi excluída.

## Integridade dos arquivos de dados (Fase H)

`git diff --stat` desta rodada altera **apenas**: `isys_rsl.tex`, `metodo_rsl.tex`,
`resultados_rsl.tex`, `isys_rsl.pdf`.

**Não** foram modificados: `busca_registros.csv`, `busca_contagens.csv`,
`referencias_corpus.bib`, `referencias_rsl.bib`, `resultado_extracao_rsl.txt`,
`AgentAI_RSL_formulario_extracao.xlsx`. Corpus de dados intacto, conforme exigido.
