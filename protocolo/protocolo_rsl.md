# Protocolo da Revisão Sistemática da Literatura

Este protocolo foi definido a priori, antes do início da triagem, para
assegurar a reprodutibilidade da revisão e reduzir o viés do pesquisador.
Segue as diretrizes de Kitchenham e Charters (2007), as orientações de
mapeamento sistemático de Petersen et al. (2015) e o relato no formato
PRISMA 2020 (Page et al., 2021).

## 1. Objetivo

Identificar como a IA Generativa e os Modelos de Linguagem de Grande Porte
(LLMs) vêm sendo utilizados para ampliar o acesso a dados governamentais
abertos (Open Government Data, OGD) e promover a transparência pública,
com recorte em Sistemas de Informação na interseção entre governo digital,
dados abertos e apoio à decisão.

## 2. Questões de Pesquisa

| ID  | Questão de pesquisa                                                                                          | Foco da extração                          |
| --- | ------------------------------------------------------------------------------------------------------------ | ----------------------------------------- |
| RQ1 | Quais aplicações de IA Generativa são utilizadas no acesso a dados governamentais abertos e na transparência? | Tipo de aplicação / caso de uso           |
| RQ2 | Quais tipos de dados governamentais são analisados?                                                          | Natureza e domínio dos dados              |
| RQ3 | Quais LLMs são utilizados?                                                                                   | Modelo(s), porte, aberto/proprietário     |
| RQ4 | Quais benefícios são reportados?                                                                             | Ganhos de acesso e transparência          |
| RQ5 | Quais desafios e limitações são reportados?                                                                  | Barreiras técnicas, éticas e de adoção    |

## 3. Estrutura PICOC

| Elemento     | Termos                                                                            |
| ------------ | --------------------------------------------------------------------------------- |
| População    | Setor público; portais e dados governamentais                                     |
| Intervenção  | IA Generativa; LLMs; modelos de linguagem (incluindo arquiteturas correlatas)     |
| Comparação   | Não aplicável (revisão de caracterização)                                         |
| Desfecho     | Acesso à informação; transparência; benefícios e desafios                         |
| Contexto     | Governo digital; e-government; OGD                                                |

## 4. Bases e Janela Temporal

- **Bases internacionais:** Scopus, Web of Science, ACM Digital Library, IEEE Xplore.
- **Fonte adicional:** Biblioteca Digital da SBC/SOL (string em português, CI4).
- **Janela temporal:** janeiro de 2019 até a data da busca (junho de 2026),
  recorte justificado pela consolidação dos LLMs a partir desse período.
- **Idiomas:** inglês ou português (CI4).
- Strings exatas por base estão em `strings_busca/` deste repositório.

## 5. Critérios de Seleção

Um estudo é incluído apenas se atende a **todos** os critérios de inclusão
e a **nenhum** dos critérios de exclusão.

### Inclusão

| ID  | Critério                                                                                          |
| --- | ------------------------------------------------------------------------------------------------- |
| CI1 | Aplica ou investiga IA Generativa/LLMs em contexto de dados abertos, transparência ou governo digital |
| CI2 | Estudo primário revisado por pares (conferência ou periódico)                                     |
| CI3 | Publicado na janela temporal definida (2019–2026)                                                 |
| CI4 | Texto em inglês ou português                                                                      |
| CI5 | Texto completo acessível                                                                          |

### Exclusão

| ID  | Critério                                                                                                 |
| --- | -------------------------------------------------------------------------------------------------------- |
| CE1 | Aborda apenas um dos eixos (somente IA *ou* somente governo aberto), sem a interseção                    |
| CE2 | Estudo secundário (outra revisão, mapeamento ou *survey*) — usado apenas como referência para trabalhos relacionados |
| CE3 | Literatura cinza, editorial, resumo estendido, pôster, *keynote* ou tutorial                             |
| CE4 | Duplicata                                                                                                |
| CE5 | Versão preliminar de estudo posteriormente estendido (mantém-se a versão mais completa)                  |

## 6. Avaliação de Qualidade

Cada estudo aprovado na leitura de texto completo é pontuado em cinco
critérios, valores em {0; 0,5; 1} (não atende; atende parcialmente; atende),
totalizando um escore entre 0 e 5.

| ID  | Critério                                                                                                       |
| --- | -------------------------------------------------------------------------------------------------------------- |
| AQ1 | Os objetivos do estudo estão claramente declarados?                                                            |
| AQ2 | O contexto (domínio governamental e dados) está adequadamente descrito?                                        |
| AQ3 | A abordagem de IA Generativa/LLM está descrita com detalhe suficiente para ser compreendida e replicada?       |
| AQ4 | Os resultados e benefícios são reportados e sustentados por evidências?                                        |
| AQ5 | As limitações e ameaças à validade são discutidas?                                                             |

**Limiar de corte:** 2,5. Estudos com escore ≥ 2,5 integram a síntese em
condições regulares; os de escore inferior são reportados à parte e
ponderados com cautela na discussão, em vez de descartados. A avaliação
de qualidade também serve para ponderar estudos publicados em veículos
de menor rigor editorial (p. ex., periódicos de iniciação científica),
registrando essa condição nos itens AQ4 e AQ5 sem alterar o critério CI2.

## 7. Extração de Dados

Formulário padronizado, definido antes da leitura integral, com campos
mapeando diretamente as questões de pesquisa.

| Campo                    | Descrição                                       | RQ  |
| ------------------------ | ----------------------------------------------- | --- |
| Aplicação / caso de uso  | Como a IA Generativa é empregada                | RQ1 |
| Dados governamentais     | Tipo e domínio dos dados analisados             | RQ2 |
| Modelo(s)                | LLM/IA Generativa, porte, licença               | RQ3 |
| Benefícios               | Ganhos de acesso/transparência relatados        | RQ4 |
| Desafios                 | Limitações técnicas, éticas e de adoção         | RQ5 |
| Avaliação                | Método de validação do estudo                   | —   |

Foram registrados, ainda, metadados bibliográficos (autores, ano,
veículo, tipo de veículo, país).

## 8. Síntese

- **Síntese quantitativa descritiva**: caracteriza o corpus por meio de
  distribuições (evolução temporal das publicações, veículos, modelos
  empregados e tipos de dados).
- **Síntese temática (qualitativa)**: codifica e agrupa em categorias as
  aplicações (RQ1), os benefícios (RQ4) e os desafios (RQ5).

## 9. Limitações Declaradas

- **Anotadora única**: a revisão foi conduzida por uma única revisora,
  sem medida de concordância entre avaliadores. Mitigação: critérios
  definidos a priori, aplicados uniformemente, com cada decisão de
  triagem registrada de forma rastreável no Rayyan.
- **Idiomas**: o recorte a inglês e português pode sub-representar a
  produção em espanhol.
- **Cobertura da busca**: a revisão apoiou-se exclusivamente em busca
  automática; *snowballing* (Wohlin, 2014) não foi conduzido nesta versão.

## 10. Ferramentas

- **Zotero**: gerenciamento de referências e deduplicação inicial.
- **Rayyan**: triagem de títulos/resumos e registro auditável das decisões.

## Referências

- Kitchenham, B.; Charters, S. (2007). *Guidelines for performing
  Systematic Literature Reviews in Software Engineering.* EBSE-2007-01.
- Petersen, K.; Vakkalanka, S.; Kuzniarz, L. (2015). Guidelines for
  conducting systematic mapping studies in software engineering: An
  update. *Information and Software Technology*, 64, 1–18.
- Page, M. J. et al. (2021). The PRISMA 2020 statement: an updated
  guideline for reporting systematic reviews. *BMJ*, 372: n71.
- Wohlin, C. (2014). Guidelines for snowballing in systematic literature
  studies and a replication in software engineering. *EASE '14*.
