# 00 — Baseline Validation

**Data:** 2026-08-17 · **Modo:** auditoria do zero, corpus congelado em 29.

## Estado git (Checkpoint 0)

- Commit HEAD (base limpa): `8605fab` — "atualização artigo".
- Arquivos modificados no working tree (antes desta rodada): `isys_rsl.tex`, `metodo_rsl.tex`, `resultados_rsl.tex`, `isys_rsl.pdf` (revisão de 29 já validada) + `.md` de apoio não versionados.
- **Não** foi feito checkout/reset destrutivo automático. A base confiável de 29 já estava restaurada.

## Baseline (todas as verificações apontam para 29)

| Item | Valor | Fonte |
|---|---|---|
| Corpus incluído | **29** | `busca_registros.csv` (`decisao=incluido`) |
| Reports not retrieved | **19** | `busca_registros.csv` (`nao_recuperado`) |
| Excluídos | **8** | `busca_registros.csv` (`excluido`) |
| Total dos registros de controle | **56** | 29+19+8 |
| Estudos na extração | **29 blocos** `DOCUMENTO:` | `resultado_extracao_rsl.txt` |
| Estudos no Apêndice A (QA) | **29 linhas**, somas corretas | `isys_rsl.tex` `tab:qa_estudos` |
| Estudos na tabela consolidada (Apêndice B) | **29 linhas** | `isys_rsl.tex` `tab:corpus_consolidado` |
| PDF compila? | **Sim, exit 0** | `latexmk -xelatex` |
| Páginas | **21** | log |
| Undefined references | **0** | log |
| Undefined citations | **0** | log |

**Divergências:** nenhuma. Todas as contagens de controle convergem para 29.

## Nota sobre ferramentas

- Renderização de PDF em imagem (poppler/pdftoppm/pdftotext) **não está disponível** neste ambiente. A inspeção visual por imagem (Fase J) é registrada como ação humana em `07_visual_pdf_audit.md`; a verificação estrutural (compilação, resolução de labels, overfull) foi feita integralmente.
