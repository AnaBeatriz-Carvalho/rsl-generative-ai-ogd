# Checklist de submissão — iSys (RSL)

Estado do manuscrito na branch `isys`. `[x]` = pronto; `[~]` = pronto com
TODO a confirmar; `[ ]` = pendente (depende de você ou da revisão conduzida).

## Compilação (XeLaTeX — exigência do periódico)
Classe oficial **`sbc2025`** (template iSys 2026). Compilar com **XeLaTeX**:

```
latexmk -xelatex isys_rsl.tex
```

Pacotes/fontes exigidos pela classe já foram instalados nesta máquina (árvore
de usuário `~/Library/texmf` + `~/Library/Fonts`): `orcidlink`, `fontawesome`,
`abstract`, `environ`, `trimspaces`, e as fontes `Roboto`, `TeX Gyre Termes` e
`FontAwesome`. Em outra máquina, instale-os (ou via `tlmgr`/MacTeX completo).
O documento compila e a bibliografia (`apalike-sol`) é resolvida.

## Itens obrigatórios (regras de submissão)
- [x] Enquadramento explícito em Sistemas de Informação — Introdução/Background
- [x] Template oficial (`sbc2025.cls`) integrado; compila em XeLaTeX
- [ ] Mínimo de 15 páginas — atualmente ~4 (faltam Resultados/Discussão)
- [x] **Single-blind** — autores identificados no PDF (nome, afiliação)
- [~] ORCID de cada autor (OBRIGATÓRIO) — placeholders `0000-0000-0000-0000`
- [~] E-mail de cada autor — placeholders `TODO@exemplo.br`
- [x] Cover Letter — `cover_letter.md` (revisar conteúdo)
- [x] Author's Contribution (CRediT) — bloco `contributions` (obrigatório)
- [x] Funding — bloco `funding` (obrigatório; revisar)
- [x] Acknowledgements — bloco `acknowledgements` (obrigatório; revisar)
- [x] Competing Interests — declarado (`interests`)
- [x] Availability of Data and Materials — bloco `materials` (inserir URL/DOI)
- [~] Declaração de uso de IA — em `furtherinformation` (preencher se aplicável)
- [x] Discussão ética — em `furtherinformation` (dados públicos, sem humanos)
- [~] Referências com DOI — DOIs adicionados às refs do Método; revisar o resto

## Itens do PORTAL de submissão (não vão no PDF)
- [ ] Indicar a área (especialidade do editor) nos "Comments to the Editor"
- [ ] Indicar 1 revisor voluntário (nome, área, e-mail institucional, titulação)
- [ ] Marcar a seção "Articles" e a categoria do artigo
- [ ] Survey demográfico (opcional)

## Conteúdo da RSL (BLOQUEIA a submissão — ainda não conduzido)
- [x] Método: protocolo completo (`metodo_rsl.tex`) — Kitchenham/Charters + PRISMA
- [ ] **Conduzir a revisão**: busca nas 4 bases, deduplicação, triagem em 2
      fases (revisora única; decisões rastreáveis no Rayyan), avaliação de
      qualidade, extração e síntese
- [ ] Resultados: diagrama PRISMA, caracterização do corpus, RQ1–RQ5
- [ ] Discussão e Conclusão
- [ ] Resumo (pt/en): substituir os `[TODO]` por números e achados reais
- [ ] Migrar o núcleo de `capitulos/estado_arte.tex` (mapeamento conduzido) para
      os Resultados, convertendo comandos ABNT (`\quadro`, `\citeonline`)
- [ ] Parâmetros marcados `% CONFIRMAR` em `metodo_rsl.tex` (janela temporal,
      artigos de controle, limiar de qualidade, string final)

## Arquivos
- `isys_rsl.tex` — manuscrito; `metodo_rsl.tex` — seção de Método (via `\input`)
- `referencias.bib`; template em `sbc2025.cls`, `aas_macros.sty`, `sectsty.sty`,
  `apalike-sol.bst` e pacote completo em `Template_LaTeX_iSys_2026_Preferred.zip`
- Semente: `capitulos/estado_arte.tex`, `introducao.tex`, `fundamentacao.tex`
