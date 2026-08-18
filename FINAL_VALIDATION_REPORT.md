# FINAL VALIDATION REPORT — iSys Major Revision

**Data:** 2026-08-17 · **Modo:** validação do zero + correções seguras · **Corpus:** congelado em 29.

## 1. Estado da baseline

- Commit base: `8605fab`. PDF inicial compilava em 21 páginas, 29 estudos.
- Working tree partia da versão de 29 já restaurada (após reversão da adulteração para 31 feita por outra IA).

## 2. Integridade do corpus

**Esta rodada NÃO alterou o corpus de 29 estudos.** 19 reports not retrieved e 8 excluídos preservados.
`git diff` altera apenas `isys_rsl.tex`, `metodo_rsl.tex`, `resultados_rsl.tex`, `isys_rsl.pdf`.
Arquivos de dados (registro, extração, `.bib`, `.xlsx`) **intactos**. Fase N: **zero** resíduos de
`31 estudos / 19-31 / 18-31 / R005 / R036 / Ali2026 / Ferencek2023 / recovered_reports / ATUALIZAR APÓS EXTRAÇÃO`.

## 3. Contagens verificadas

Ver `01_data_reconciliation.md`. Todas ✅ rastreáveis: 29 · 18/29 alucinação · 18 GPT / 6 abertos / 2 DialogFlow /
3 n.r. · 23 empíricos / 6 conceituais · Dim1 7/22 · Objeto 8/11/5/4/1 · RQ1 7/11/11 · Geografia 13/5/5/4/1/0/1 ·
QA 29 linhas com somas corretas · desfecho cívico 0/29.

## 4. Mudanças científicas (por seção)

- **Resumo/Abstract:** abertura por informação do setor público; "nenhum dos 29 estudos incluídos".
- **§2 Fundamentação:** seção renomeada; RAG suavizado; Figura 1 (complementaridade — já vigente).
- **§3 Método:** CE1 alinhado ao escopo; regra de 4 níveis; campo "país" = contexto governamental.
- **§4 Resultados:** taxonomia (Dim1 ortogonal 7/22), geografia, RQ5 alucinação 18/29.
- **§5 Discussão:** distribuição 22/7 explícita; fecho sociotécnico; RAG/rastreabilidade.
- **Ameaças:** novo item "Literatura cinza"; "Viés de disponibilidade" (19).
- **Conclusão:** escopo de informação do setor público; taxonomia tridimensional.
- **Apêndices:** A (QA 29) e B (consolidado 29, D1/D2/D3/Aval./QA).

## 5. Mudanças conceituais

- **Título:** → "Public-Sector Information Access…" (terminológico, corpus inalterado).
- **Escopo:** informação do setor público; OGD como caso paradigmático, não exclusivo.
- **Transparência:** construto sociotécnico, 5 dimensões, 4 níveis; achado limitado ao corpus.
- **Taxonomia:** eixos ortogonais (ONDE × SOBRE O QUÊ × O QUE FAZ).
- **SI:** leitura sociotécnica explícita (artefato↔informação↔organização↔prática↔cidadão↔resultado).

## 6. Taxonomia final

Dim1 **Oferta 7 / Demanda 22**; Dim2 objeto **8/11/5/4/1**; Dim3 seis funções (não exclusiva).
Decisão e justificativa em `03_taxonomy_validation.md`; rastreabilidade em `05_taxonomy_traceability.md`.

## 7. Auditoria estudo a estudo

`05_taxonomy_traceability.md` (taxonomia) e `06_transparency_traceability.md` (transparência, 4 níveis).
Nenhuma classificação não rastreável; todas derivam da extração.

## 8. Revisores

Ver `02_reviewer_matrix.md`, `08_reviewer_A_simulation.md`, `09_reviewer_C_simulation.md`.
Todos os itens RESOLVIDOS, exceto a recuperação dos 19 (PARCIAL / ação humana).

## 9. Pontos NÃO executados (por integridade)

- **Recuperação dos 19 not-retrieved** — ação humana separada; corpus não alterado.
- **Segunda codificação / medida de concordância** — não realizada; declarada como limitação.
- **Snowballing** — não conduzido; declarado.
- **Literatura cinza** — excluída por CE3; reconhecida como limite, não pesquisada.
- **Pareceres originais dos revisores** — ausentes do repositório; matriz reconstruída do brief
  (conferir contra as cartas originais antes da ressubmissão).

## 10. Highlights

- Mecanismo do projeto: comando `\rev{}` (pacote `soul`/`\hl`), já existente. Nenhum segundo sistema introduzido.
- Todas as correções desta rodada estão em `\rev{}`.
- **Não destacáveis diretamente:** título (quebraria running header/bookmarks) e a **legenda da Figura 4**
  (o `soul` falha com `\ ` de controle e em-dash em legenda) — tratados como conteúdo revisado documentado aqui e
  na carta; a figura é visivelmente nova. Tabelas: legendas em `\rev`; a Figura 4 é nova por completo.

## 11. Compilação

- `latexmk -xelatex`: **exit 0**; **0** undefined references; **0** undefined citations; **21 páginas**.
- Warnings: 1 cosmético (FontAwesome italic shape); 2 overfull 66pt no *frontmatter* (pré-existentes, template).

## 12. Git diff

`isys_rsl.tex`, `metodo_rsl.tex`, `resultados_rsl.tex`, `isys_rsl.pdf` (esperado). Dados do corpus: inalterados.

## 13. Riscos remanescentes

- **ALTO/humano:** recuperação dos 19 (Reviewer A pediu esforço adicional) — recomendado antes da ressubmissão.
- **MÉDIO:** pareceres originais não conferidos (ausentes do repo) — conferir a matriz.
- **BAIXO:** inspeção visual do PDF por imagem pendente (sem poppler no ambiente) — abrir o PDF e checar `07_...md`.
- **BAIXO:** OGD definido duas vezes (intro parentético + §2 formal) — aceitável; opcional de-duplicar.

## 14. Recomendação

**PRONTO APÓS AÇÃO HUMANA ESPECÍFICA.** O manuscrito está cientificamente consistente, compila limpo e responde
aos revisores. Antes da ressubmissão, recomenda-se ao autor: (a) tentar a recuperação manual dos 19 estudos (ou
manter a resposta como está, transparentemente parcial); (b) conferir a matriz contra os pareceres originais;
(c) fazer a inspeção visual do PDF. Nenhuma dessas ações altera o corpus de 29.
