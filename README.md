# Materiais Suplementares — RSL sobre IA Generativa e Dados Governamentais Abertos

Este repositório acompanha o artigo **"Generative AI for Open Government
Data Access and Public Transparency: A Systematic Literature Review"**,
submetido à *iSys — Brazilian Journal of Information Systems* (SBC/JBCS).

**Autoria:**

- Ana Beatriz Carvalho Oliveira — Universidade Federal de Sergipe (UFS)
- Gilton José Ferreira da Silva — Universidade Federal de Sergipe (UFS)

## Sobre a Revisão

Revisão Sistemática da Literatura conduzida segundo as diretrizes de
Kitchenham e Charters (2007) e relatada no formato PRISMA 2020, com foco
em IA Generativa e Modelos de Linguagem de Grande Porte (LLMs) aplicados
ao acesso a dados governamentais abertos e à transparência pública. O
corpus final reúne **29 estudos**, publicados entre 2021 e 2026.

## Funil PRISMA (resumo)

- **Identificados:** 1.288 registros (1.265 nas quatro bases
  internacionais + 23 na SBC/SOL).
- **Únicos após deduplicação (bases internacionais):** 805.
- **Avaliados em texto completo:** 46 (bases) + 9 (SOL).
- **Incluídos:** **29 estudos** (27 internacionais + 2 SBC/SOL).

O diagrama completo está em `prisma/fluxo_selecao.png`.

## Estrutura do Repositório

```
rsl-generative-ai-ogd/
├── README.md                    Esta porta de entrada
├── LICENSE                      Licença CC BY 4.0
├── protocolo/
│   └── protocolo_rsl.md         Protocolo: objetivo, RQs, PICOC, CI/CE,
│                                avaliação de qualidade, síntese, limitações
├── strings_busca/
│   ├── scopus.txt               String em TITLE-ABS-KEY
│   ├── web_of_science.txt       String em TS=
│   ├── acm.txt                  Bloco de intervenção + 3 passadas em [Abstract]
│   ├── ieee.txt                 String em "All Metadata"
│   └── sbc_sol.txt              String em português (CI4)
├── prisma/
│   └── fluxo_selecao.png        Diagrama PRISMA 2020 (Figura 2 do artigo)
├── estudos/
│   ├── estudos_incluidos.csv    Os 29 estudos (ID, autor/ano, veículo,
│   │                            país, modelo principal, escore QA, vertente)
│   └── busca_contagens.csv      Contagens brutas e pós-dedup por base,
│                                inclusive contagens parciais por passada na ACM
└── extracao/
    └── formulario_extracao.xlsx Formulário de extração com todos os
                                 estudos (RQ1–RQ5 + QA)
```

### Observações sobre os arquivos

- `estudos/estudos_incluidos.csv` usa `;` como separador (padrão pt-BR)
  e codificação UTF-8 com BOM, para abrir corretamente no Excel em
  ambientes em português.
- `estudos/busca_contagens.csv` registra a contagem bruta por base, a
  data de execução, e — para a ACM Digital Library — as três passadas em
  `[Abstract: ...]` somadas (com nota sobre necessidade de união +
  dedup posterior).
- O formulário `extracao/formulario_extracao.xlsx` contém uma linha por
  estudo com tipo de dado, vertente, método, escore de avaliação de
  qualidade e marcação de "Transparência como desfecho", além das
  evidências por RQ.
- **Os PDFs dos 29 estudos não estão incluídos por restrições de
  direito autoral.** O DOI de cada estudo está na seção de Referências
  do artigo e permite a recuperação direta na base de origem.
- Os arquivos brutos de exportação de cada base (`*.bib`, RIS) e os
  documentos internos de handoff usados durante a condução não são
  versionados, por não fazerem parte dos materiais prometidos na seção
  de Disponibilidade do artigo.

## Licença

Materiais distribuídos sob a Creative Commons Attribution 4.0
International License (CC BY 4.0). Consulte o arquivo `LICENSE`.

## Como citar

A citação completa será atualizada após a publicação do artigo. Até lá,
referencie este repositório como:

> Oliveira, A. B. C.; Silva, G. J. F. (2026). *Materiais suplementares
> da Revisão Sistemática "Generative AI for Open Government Data Access
> and Public Transparency".* Repositório no GitHub.
