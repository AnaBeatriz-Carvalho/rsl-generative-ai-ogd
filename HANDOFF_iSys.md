# HANDOFF — Branch `isys`: manuscrito de RSL para a revista iSys

> Estado e instruções da branch `isys`, que contém **um segundo artigo** (uma
> Revisão Sistemática da Literatura) derivado do projeto da dissertação AgentAI.
> A dissertação e o artigo experimental permanecem em `main` e `results-chapter`
> e **não** são tocados por esta branch.

---

## 0. Avisos

- **`main` é a fonte de verdade** da dissertação e do artigo experimental. Não alterar.
- Trabalhar **somente na branch `isys`**.
- Todo conteúdo experimental foi removido desta branch, mas **preservado** em
  `main`/`results-chapter` (recuperável via git). Nada foi perdido.

---

## 1. Decisões consolidadas nesta linha de trabalho

- **Periódico:** iSys (Journal of Information Systems, SBC). Mantém-se o template
  oficial fornecido (classe `sbc2025`). As regras de submissão aplicadas vêm do
  checklist SBC/JBCS (comum à plataforma): **single-blind** e **XeLaTeX**.
- **Estratégia da RSL:** *estender* o Mapeamento Sistemático já conduzido na
  dissertação (`capitulos/estado_arte.tex`) — não conduzir uma RSL do zero.
- **Compilação:** **XeLaTeX** (exigência). `pdflatex` não é o alvo.
- **Revisão:** **single-blind** — autores identificados no PDF.
- **Autores:**
  - Ana Beatriz Carvalho Oliveira — ORCID 0009-0004-3454-6527 —
    anabeatrizcarvalho@academico.ufs.br (autora correspondente)
  - Gilton José Ferreira da Silva — ORCID 0000-0002-2281-9426 —
    gilton@dcomp.ufs.br
  - Afiliação: Universidade Federal de Sergipe (UFS).

---

## 2. Tema e protocolo da RSL

- **Título (EN):** *Generative AI for Open Government Data Access and Public
  Transparency: A Systematic Literature Review*.
- **Objetivo:** caracterizar como IA Generativa e LLMs são usados para ampliar o
  acesso a dados governamentais abertos (OGD) e promover transparência pública.
- **RQ1–RQ5:** aplicações; tipos de dados; LLMs; benefícios; desafios.
- **Bases (protocolo consolidado):** Scopus, Web of Science, ACM DL, IEEE Xplore
  (+ snowballing). O mapeamento original usou ainda a SOL/SBC.
- **Método completo** em `metodo_rsl.tex` (Kitchenham/Charters + PRISMA 2020;
  PICOC, critérios CI/CE, Kappa de Cohen, avaliação de qualidade, extração).

---

## 3. Estrutura de arquivos (branch `isys`)

| Arquivo | Papel |
|---|---|
| `isys_rsl.tex` | Manuscrito principal (frontmatter + seções + declarações + `\input`s) |
| `metodo_rsl.tex` | Seção **Método** (protocolo) |
| `resultados_rsl.tex` | Seção **Resultados** (migrada do mapeamento conduzido) |
| `referencias.bib` | Bibliografia (estilo `apalike-sol`) |
| `cover_letter.md` | Cover letter (esqueleto) |
| `CHECKLIST_iSys.md` | Checklist de submissão e pendências |
| `sbc2025.cls`, `aas_macros.sty`, `sectsty.sty`, `apalike-sol.bst` | Template iSys |
| `Template_LaTeX_iSys_2026_Preferred.zip` | Pacote oficial + exemplo `main-en.tex` |
| `capitulos/estado_arte.tex` | **Semente**: mapeamento conduzido (Kitchenham; 7 estudos; PRISMA-ScR) |
| `capitulos/introducao.tex`, `fundamentacao.tex` | Semente de enquadramento (OGD, transparência) |
| `imagens/` | Apenas imagens usadas pela RSL e pela semente |

---

## 4. Como compilar (XeLaTeX)

```
latexmk -xelatex isys_rsl.tex
```

A classe `sbc2025` exige pacotes/fontes que **já foram instalados nesta máquina**
na árvore de usuário (`~/Library/texmf`) e em `~/Library/Fonts`:
`orcidlink`, `fontawesome`, `abstract`, `environ`, `trimspaces`; fontes
`Roboto`, `TeX Gyre Termes`, `FontAwesome`. **Em outra máquina** (ou Overleaf),
instalar via `tlmgr`/MacTeX completo, ou usar o Overleaf (que já os traz).

Estado atual: compila com **exit 0**, **0 citações/refs indefinidas**, ~5 páginas.

---

## 5. O que já está pronto

- Manuscrito compilando em XeLaTeX, single-blind, autores completos (ORCID/e-mail).
- Frontmatter iSys (`\jid`, `\title` em inglês, resumos pt/en, palavras-chave).
- **Método** completo (`metodo_rsl.tex`).
- **Resultados** (`resultados_rsl.tex`): fluxo PRISMA + figura, tabela dos 7
  estudos, síntese por RQ1–RQ5 e lacunas — rotulados como **execução preliminar**.
- **Declarações obrigatórias**: Author's Contribution (CRediT), Funding,
  Acknowledgements, Competing Interests, Availability of Data, ética/uso de IA.
- DOIs nas referências do Método; demais referências a revisar.

---

## 6. Pendências (bloqueiam a submissão real)

### Conteúdo científico (principal)
1. **Discussão** e **Conclusão** (ainda `[TODO]` em `isys_rsl.tex`).
2. Atualizar o **resumo** (pt/en) com números e achados reais (hoje `[TODO]`).
3. **Estender a busca** (snowballing + reexecução nas 4 bases sob RQ1–RQ5) para
   resolver a inconsistência entre o protocolo consolidado e a execução
   preliminar (5 bases/Q1–Q4) e atingir o **mínimo de 15 páginas**.
4. Migrar o restante de `estado_arte.tex` que ainda for útil; revisar todas as
   entradas do `.bib` para incluir **DOI**.
5. Resolver os parâmetros `% CONFIRMAR` em `metodo_rsl.tex` (janela temporal
   — hoje 2019; artigos de controle; limiar de qualidade; string final).

### Itens de submissão (de Ana)
6. URL/DOI do repositório de dados (hoje `https://github.com/TODO` na seção
   *Availability of Data and Materials*).
7. Itens do **portal** (não vão no PDF): indicar a área do editor nos
   "Comments to the Editor"; indicar 1 revisor voluntário (nome, área, e-mail
   institucional, titulação); selecionar seção "Articles" e a categoria.
8. Revisar o `cover_letter.md`.

---

## 7. Resumo do estado

A branch `isys` entrega um **manuscrito de RSL compilável e conforme o template
iSys (single-blind, XeLaTeX)**, com Método e Resultados preenchidos a partir do
mapeamento já conduzido. O artigo **ainda não é submetível** porque a revisão
precisa ser **estendida e fechada** (Discussão, Conclusão, resumo, ≥15 páginas).

---

*Fim do handoff.*
