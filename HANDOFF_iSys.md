# HANDOFF — Branch `isys`: manuscrito de RSL para a revista iSys

> Estado e instruções da branch `isys`, que contém **um segundo artigo** (uma
> Revisão Sistemática da Literatura) derivado do projeto da dissertação AgentAI.
> A dissertação e o artigo experimental permanecem em `main` e `results-chapter`
> e **não** são tocados por esta branch.

---

## Atualização — 19/06/2026 (sessão: reexecução da busca + Background)

Estado mais recente, por cima das seções 5–6 abaixo:

- **Busca reexecutada e contabilizada** (`busca_contagens.csv`):
  - 4 bases internacionais: Scopus 453, WoS 143, IEEE 224, ACM 445 = **1265 bruto → 805 pós-dedup** (Zotero).
  - **SBC/SOL** (fonte separada, fora do Rayyan): identificados **23** (busca booleana refeita em duas queries complementares, unidas/dedup à mão; substitui o 8 provisório).
  - **Triagem título/resumo (Rayyan)**: 805 triados → **137 incluídos**, 668 excluídos, 0 maybe.
  - **Triagem título (SOL, manual)**: 23 → 2 firmes, 3 a confirmar por texto completo, 18 excluídos; corpus SOL estimado 2–5.
  - O `TOTAL=1265/805` cobre só as 4 bases internacionais; a SOL é contabilizada à parte no PRISMA.
- **§2 Background e Trabalhos Relacionados ESCRITA** (`isys_rsl.tex`): 3 subseções
  (lacuna de acesso a OGD; LLMs/RAG; trabalhos relacionados/Linked Data + lacuna de
  estudo secundário). Sem citações fabricadas — só chaves já existentes no `.bib`.
  Há um `% TODO` para confirmar ausência de RSL correlata na busca.
- **Compila XeLaTeX exit 0**, 0 citações/refs indefinidas, **7 páginas**.
- **Reversão consciente do escopo do título (19/06/2026):** a autora **mantém o título
  amplo** ("...Public Transparency") e **rejeitou** o estreitamento para "...Legislative
  Data" antes registrado. Memória `decisao-escopo-isys`, índice `MEMORY.md` e este handoff
  foram realinhados; o título no `.tex` já estava amplo (o registro de "estreitado no
  `.tex`" era falso). A tensão título↔corpus passa a ser **limitação de validade de
  construto** (Ameaças à Validade), não estreitamento. Strings de busca, corpus e números
  não foram tocados.

**Ainda bloqueado pela triagem de texto completo (não fabricar):** Resultados ainda
com números antigos (47/7); Figura PRISMA final; QA; Discussão; Conclusão; e
os `[TODO]` de resultados nos resumos pt/en. Destravam ao fechar a leitura de texto
completo dos 137 (Rayyan) + confirmar os 3 da SOL.

**Decisão de escopo vigente** (memória `decisao-escopo-isys`): **título MANTIDO na forma
ampla** — "...Open Government Data Access and *Public Transparency*". O estreitamento para
"...Accessing Open Government and Legislative Data" foi **rejeitado conscientemente pela
autora (19/06/2026)** — NÃO voltar a estreitar. A tensão título↔corpus (corpus é
estruturação/acesso a dados legislativos e OGD, não medida de transparência como desfecho)
é tratada como **limitação de validade de construto** nas Ameaças à Validade, não por
estreitamento. Decisão de corpus separada e ainda válida: excluir formalmente os 3
não-generativos (Mendes2025, Bojars2019, PapadopoulosCharalabidis2020) e Colombo2024
(preprint → CI2) na consolidação final.

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
  PICOC, critérios CI/CE, avaliação de qualidade, extração). Revisora única —
  decisões rastreáveis no Rayyan, sem concordância interavaliadores (ver memória
  `revisora-unica-isys`).

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

Estado atual: compila com **exit 0**, **0 citações/refs indefinidas**, ~7 páginas
(ver bloco "Atualização — 19/06/2026" no topo).

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
1. **Fechar a triagem de texto completo** dos 137 incluídos (Rayyan) + confirmar os
   3 candidatos da SOL → consolidar o **corpus final** e o **n**. Isto destrava (3)–(6).
2. **Atualizar §Resultados** (`resultados_rsl.tex`): hoje com números antigos (47/7);
   reescrever seleção (PRISMA), corpus, RQ1–RQ5 e lacunas com o corpus consolidado.
   Refazer a **Figura PRISMA** com 805/137/.../n.
3. **Discussão** e **Conclusão** (ainda `[TODO]` em `isys_rsl.tex`).
4. Atualizar o **resumo** (pt/en) com números e achados reais (hoje `[TODO]` nos
   resultados).
5. **Snowballing** (Wohlin) sobre o corpus consolidado; reportar QA. Revisora
   única: não há concordância interavaliadores a reportar — declarar como
   limitação de validade interna (já feito nas Ameaças à Validade).
6. Atingir o **mínimo de 15 páginas** (hoje ~7).
7. Revisar todas as entradas do `.bib` para incluir **DOI**.
8. Resolver os parâmetros `% CONFIRMAR` em `metodo_rsl.tex` (janela temporal,
   artigos de controle, limiar de qualidade, string final).

> **FEITO nesta linha de trabalho (não retrabalhar):** §2 Background escrita;
> reexecução da busca + contabilização no `busca_contagens.csv`; string ampliada já no
> `.tex` (título **mantido na forma ampla**); ancoragem de refs SI agora disponível na §2.

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
