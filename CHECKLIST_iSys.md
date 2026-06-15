# Checklist de submissão — iSys (RSL)

Estado do esqueleto na branch `isys`. `[x]` = endereçado; `[ ]` = pendente
(depende de você ou da revisão conduzida).

## Compilação
O manuscrito usa a classe oficial **`sbc2025`** (template iSys 2026). Para
compilar localmente, instale os pacotes CTAN exigidos pela classe (este TeX
"basic" não os traz):

```
sudo tlmgr install fontawesome ifsym tabularray orcidlink
```

Depois: `latexmk -pdf isys_rsl.tex`.

## Itens obrigatórios iSys
- [x] Enquadramento explícito em Sistemas de Informação — Introdução/Background
- [x] Template oficial iSys (`sbc2025.cls`) integrado ao `isys_rsl.tex`
- [ ] Mínimo de 15 páginas — só verificável após preencher os resultados
- [x] Compatível com double-blind — autoria/ORCID/e-mail/agradecimentos omitidos
- [x] Cover Letter — `cover_letter.md` (esqueleto)
- [x] CRediT Taxonomy — bloco `contributions` (preencher na versão não-anônima)
- [x] Funding — bloco `funding` (TODO)
- [x] Competing Interests — declarado (`interests`)
- [x] Availability of Data and Materials — bloco `materials` (apontar GitHub/Zenodo)
- [x] Acknowledgments — bloco `acknowledgements` (omitido no double-blind)
- [x] Declaração de uso de IA — em `furtherinformation` (TODO)
- [x] Discussão ética — em `furtherinformation` (dados públicos, sem humanos)
- [ ] Referências com DOI — adicionar DOIs em `referencias.bib`

## Conteúdo da RSL (depende da revisão conduzida)
- [x] Protocolo (RQs, bases, string, critérios, seleção, extração) — preenchido a partir do mapeamento existente
- [ ] Decidir e executar a **extensão** do mapeamento (`capitulos/estado_arte.tex`): snowballing + reexecução de busca sob o escopo OGD/transparência
- [ ] Resultados: fluxograma PRISMA atualizado, caracterização, RQ1–RQ5
- [ ] Discussão e Conclusão
- [ ] Abstract/Cover Letter: atualizar com números e achados finais
- [ ] Migrar o conteúdo de `estado_arte.tex` para `isys_rsl.tex`, convertendo os
      comandos ABNT (`\quadro`, `\citeonline`, `\fonte`) e as citações
      (`\cite`→`\citep`, `\citeonline`→`\citet`) para o estilo `apalike-sol`

## Ativos reaproveitados (seed)
- `capitulos/estado_arte.tex` — Mapeamento Sistemático conduzido (Kitchenham; 7 incluídos; PRISMA-ScR) → núcleo de Método/Resultados
- `capitulos/introducao.tex`, `capitulos/fundamentacao.tex` — enquadramento (OGD, transparência)
- `referencias.bib`; `imagens/fase_rsl.png`, `imagens/fluxograma_execucao.png`

## Arquivos do template (raiz)
`sbc2025.cls`, `aas_macros.sty`, `sectsty.sty`, `apalike-sol.bst` e o pacote
oficial completo em `Template_LaTeX_iSys_2026_Preferred.zip` (inclui o exemplo
`main-en.tex` como referência).
