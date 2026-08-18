# 03 — Taxonomy Validation (B4)

## Versão auditada (entrada)

Dimensão 1 (posição na cadeia) tinha **três** valores exclusivos:
Preparação 7 · Acesso 11 · Mediação de serviços 11.

## Problema testado

**A distinção entre "Acesso" e "Mediação de serviços" (Dim1) é conceitualmente
independente do objeto informacional (Dim2)?**

## Evidência

Os próprios critérios de diferenciação da versão anterior separavam "Acesso" de
"Mediação" **pelo objeto**:

- Acesso: "o objeto consultado é o *dataset*; distingue-se da mediação por operar
  sobre dados, não sobre serviços";
- Mediação: "o objeto é a informação de serviço/procedimento, não o *dataset*".

Ou seja, dentro do lado da demanda, a subdivisão dependia **essencialmente do
objeto** — exatamente o eixo da Dimensão 2. Isso torna Dim1 e Dim2 **parcialmente
redundantes** e reabre a crítica de validade de construto: "acesso" e "mediação"
seriam a mesma intervenção (mediar a demanda) aplicada a objetos diferentes.

## Decisão: **refatorar Dim1 para binária, ortogonal**

- **Dim1 (ONDE):** Oferta/preparação = **7** · Demanda/mediação do acesso = **22**.
- **Dim2 (SOBRE O QUÊ):** 8 / 11 / 5 / 4 / 1 (inalterada) — passa a ser o único
  eixo que distingue consulta a *datasets* de mediação de serviços.
- **Dim3 (O QUE FAZ):** funções inalteradas (não exclusiva).

A distinção dataset-vs-serviço **não se perde**: migra para a Dim2 (Portais OGD
vs. Serviços/procedimentos), que é ortogonal à posição.

## Justificativa

1. **Corpus inalterado (29).** Nenhuma reclassificação de estudo individual: as
   contagens O=7 / D=22 derivam diretamente da coluna D1 da `tab:corpus_consolidado`
   (7 estudos com O, 22 com D), que já usava o código binário O/D.
2. **RQ1 preservada.** RQ1 continua reportando os **três tipos descritivos**
   (estruturação/enriquecimento 7; acesso conversacional 11; serviços/informação 11)
   — eles não são mais apresentados como uma *dimensão* da taxonomia.
3. **Ortogonalidade.** A lógica final é limpa: ONDE (oferta/demanda) × SOBRE O QUÊ
   (objeto) × O QUE FAZ (função). Responde diretamente à crítica de Reviewer C/A.

## Consistência propagada

Atualizados: `tab:taxonomia` (2 linhas na Dim1), `fig:taxonomia` (2 caixas + setas),
texto de §4.6, parágrafo de distribuição na Discussão (22/7), e menção na Conclusão.
O Resumo/Abstract mantêm "taxonomia de três dimensões (posição na cadeia
informacional, objeto informacional e função)" — descrição que permanece exata.
A `tab:corpus_consolidado` já era consistente (D1 = O/D).
