# 07 — Visual PDF Audit (Fase J)

> **Limitação do ambiente:** não há `poppler` / `pdftoppm` / `pdftotext` /
> `gs` / `mutool` instalados. **A renderização do PDF em imagem não foi possível.**
> A inspeção visual página a página **é uma AÇÃO HUMANA pendente** — o(a) autor(a)
> deve abrir `isys_rsl.pdf` e conferir os elementos abaixo. A auditoria **estrutural**
> (compilação, resolução de labels, contagens, overfull) foi feita integralmente e
> substitui parcialmente a inspeção visual.

## Verificação estrutural (feita)

| Elemento | Nº | Página | Status |
|---|---|---|---|
| Figura 1 — Web Semântica × IA (complementares) | Fig. 1 | 4 | label OK, TikZ compila |
| Fluxo PRISMA (29) | Fig. 3 | 8 | label OK |
| Caracterização do corpus | Tab. 6 | 9 | label OK |
| Distribuição geográfica | Tab. 7 | 10 | label OK, soma 29 |
| Taxonomia (definições/critérios) | Tab. 8 | 12 | label OK, Dim1 7/22, Dim2 8/11/5/4/1 |
| Taxonomia (figura relacional) | Fig. 4 | 13 | label OK, 2 posições + setas |
| QA dos 29 estudos | Tab. 9 | 16 | 29 linhas, somas corretas |
| Visão consolidada (29) | Tab. 10 | 18 | 29 linhas |

- **Compilação:** exit 0; **0** undefined references; **0** undefined citations; 21 páginas.
- **Overfull hboxes:** 2 × 66pt, ambos no bloco de *frontmatter* do template
  (linha de datas/afiliação), **pré-existentes** e sem relação com o conteúdo revisado.
  Nenhum overfull relevante em tabelas/figuras novas.

## Checklist para a inspeção humana

Abrir o PDF e confirmar visualmente:
- [ ] Título na capa = "Generative AI for Public-Sector Information Access…"; running header curto.
- [ ] Destaques amarelos (`\rev`) legíveis, sem quebrar linhas/citações.
- [ ] Tabela 8 e Tabela 10 sem corte de coluna à direita.
- [ ] Figura 1 e Figura 4 com setas e caixas alinhadas, texto não sobreposto.
- [ ] Ausência de `??` (nenhum previsto: 0 undefined).
