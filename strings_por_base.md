# Strings de busca por base — RSL iSys

> String ampliada (5 dimensões PICOC) adaptada à sintaxe de cada base.
> **Janela temporal:** 2019–presente (CI3). **Idioma:** inglês ou português (CI4).
> Ajuste o filtro de ano na interface de cada base (não dentro da string), salvo onde indicado.
> Para cada base, registrar a contagem bruta **antes** de qualquer filtro manual (ver `PROTOCOLO` ao final).

---

## String de referência (conceitual — não colar em base)

```
(IA Generativa / LLMs / arquiteturas correlatas)
AND
(dados governamentais/legislativos/parlamentares · acesso à informação ·
 transparência · accountability · governo digital · dados abertos)
```

---

## 1. Scopus — campo `TITLE-ABS-KEY`

```
TITLE-ABS-KEY(
  ("generative artificial intelligence" OR "generative AI"
   OR "large language model*" OR "LLM*" OR "foundation model*"
   OR transformer* OR GPT* OR ChatGPT OR Llama OR Mistral OR Gemini
   OR "retrieval-augmented generation" OR RAG
   OR chatbot* OR "conversational agent*")
  AND
  ("open government data" OR "open data" OR "government data"
   OR "public sector data" OR "legislative data" OR "parliamentary data"
   OR "freedom of information" OR FOIA OR "access to information"
   OR transparency OR accountability
   OR "digital government" OR "e-government" OR "open government"
   OR "data portal*")
)
```
- Filtro de ano: aba **Limit to → Year ≥ 2019** (ou acrescente `AND PUBYEAR > 2018`).
- `*` = truncamento (multi-caractere). Aspas = frase aproximada.

---

## 2. Web of Science (Core Collection) — campo `TS=` (Topic)

```
TS=(
  ("generative artificial intelligence" OR "generative AI"
   OR "large language model*" OR "LLM*" OR "foundation model*"
   OR transformer* OR GPT* OR ChatGPT OR Llama OR Mistral OR Gemini
   OR "retrieval-augmented generation" OR RAG
   OR chatbot* OR "conversational agent*")
  AND
  ("open government data" OR "open data" OR "government data"
   OR "public sector data" OR "legislative data" OR "parliamentary data"
   OR "freedom of information" OR FOIA OR "access to information"
   OR transparency OR accountability
   OR "digital government" OR "e-government" OR "open government"
   OR "data portal*")
)
```
- `TS=` busca em título, resumo, palavras-chave de autor e Keywords Plus.
- Filtro de ano: refine por **Publication Years ≥ 2019**.
- `*` = truncamento. WoS aceita aspas para frases exatas.

---

## 3. IEEE Xplore — "Command Search" (campo `All Metadata`)

```
("All Metadata":"generative artificial intelligence" OR "All Metadata":"generative AI"
 OR "All Metadata":"large language model*" OR "All Metadata":"LLM"
 OR "All Metadata":"foundation model*" OR "All Metadata":transformer*
 OR "All Metadata":GPT* OR "All Metadata":ChatGPT OR "All Metadata":Llama
 OR "All Metadata":Mistral OR "All Metadata":Gemini
 OR "All Metadata":"retrieval-augmented generation" OR "All Metadata":RAG
 OR "All Metadata":chatbot* OR "All Metadata":"conversational agent*")
AND
("All Metadata":"open government data" OR "All Metadata":"open data"
 OR "All Metadata":"government data" OR "All Metadata":"public sector data"
 OR "All Metadata":"legislative data" OR "All Metadata":"parliamentary data"
 OR "All Metadata":"freedom of information" OR "All Metadata":FOIA
 OR "All Metadata":"access to information" OR "All Metadata":transparency
 OR "All Metadata":accountability OR "All Metadata":"digital government"
 OR "All Metadata":"e-government" OR "All Metadata":"open government"
 OR "All Metadata":"data portal*")
```
- IEEE exige **≥ 3 caracteres antes do `*`**: `GPT*`, `LLM`, `RAG` sem wildcard (ok). `transformer*`, `chatbot*` ok.
- Filtro de ano: **2019–presente** na barra lateral.
- Se a interface limitar o nº de cláusulas, quebre em 2 buscas (bloco de intervenção × cada subgrupo de contexto) e some, **removendo duplicatas**.

---

## 4. ACM Digital Library — Advanced Search (campo `[All: ...]`)

```
[[All: "generative artificial intelligence"] OR [All: "generative ai"]
 OR [All: "large language model"] OR [All: "llm"] OR [All: "foundation model"]
 OR [All: transformer] OR [All: gpt] OR [All: chatgpt] OR [All: llama]
 OR [All: mistral] OR [All: gemini] OR [All: "retrieval-augmented generation"]
 OR [All: rag] OR [All: chatbot] OR [All: "conversational agent"]]
AND
[[All: "open government data"] OR [All: "open data"] OR [All: "government data"]
 OR [All: "public sector data"] OR [All: "legislative data"]
 OR [All: "parliamentary data"] OR [All: "freedom of information"]
 OR [All: foia] OR [All: "access to information"] OR [All: transparency]
 OR [All: accountability] OR [All: "digital government"]
 OR [All: "e-government"] OR [All: "open government"] OR [All: "data portal"]]
```
- Restrinja a busca a **"The ACM Guide to Computing Literature"** ou **"ACM Full-Text Collection"** — anote qual usou.
- Filtro de ano: **E-Publication Date ≥ 2019** no painel lateral.
- ACM trunca por radical automaticamente; por isso os termos vão sem `*` (ex.: `transformer` cobre transformers).

---

## 5. SBC / SOL (Biblioteca Digital — Open Conference/Journal Systems) — PORTUGUÊS (CI4)

```
("inteligência artificial generativa" OR "IA generativa"
 OR "modelos de linguagem" OR "grandes modelos de linguagem"
 OR "modelo de linguagem de grande porte" OR LLM OR ChatGPT OR transformer)
AND
("dados abertos governamentais" OR "dados abertos" OR "dados governamentais"
 OR "dados legislativos" OR "dados parlamentares" OR "transparência pública"
 OR transparência OR "acesso à informação" OR "governo digital"
 OR "governo eletrônico" OR accountability OR "portal de dados")
```
- A busca da SOL é **simples** (suporte booleano limitado). Se o operador `AND/OR` não funcionar como esperado:
  1. Rode **sub-buscas** por par (1 termo de intervenção × 1 termo de contexto) e una os resultados manualmente, removendo duplicatas.
  2. Repita **sem acentos** (ex.: `transparencia`, `informacao`) — a indexação da SOL às vezes não normaliza diacríticos.
- Rode também a **string em inglês** (seção 1) na SOL, pois há trabalhos da SBC publicados em inglês.
- Registre a SOL na Figura PRISMA **mesmo com retorno 0** (a versão atual da figura a omite — corrigir).

---

## PROTOCOLO DE COLETA (ler antes de executar)

### O que registrar **por base**
| Campo | Exemplo |
|---|---|
| Base | Scopus |
| String exata colada (copy literal) | `TITLE-ABS-KEY(...)` |
| Campo/escopo de busca | TITLE-ABS-KEY / TS= / All Metadata / [All:] |
| Coleção (quando aplicável) | "ACM Guide to Computing Literature" |
| Filtro de ano aplicado | 2019–2026 |
| **Contagem bruta** (antes de qualquer triagem) | 6 |
| Data de execução | 2026-06-XX |
| Nº após dedup | (preencher na consolidação) |

> Registre a contagem **bruta**, antes de remover duplicatas ou aplicar CI/CE.
> Se quebrar a busca em sub-queries (IEEE/SOL), registre a contagem de cada sub-query e o total após união+dedup.

### Como trazer de volta (formato)
1. **Planilha-resumo por base** (`busca_contagens.csv`):
   `base, campo, colecao, filtro_ano, contagem_bruta, data_exec`
2. **Planilha de registros** (`busca_registros.csv`) — um registro por linha, com:
   `id, titulo, autores, ano, veiculo, tipo_veiculo, doi, base_origem,
    fase (titulo_resumo | texto_completo), decisao (incluido | excluido),
    criterio (CI/CE aplicado), generativo (S/N), observacao`
   - Exporte de cada base em **BibTeX/RIS** e importe no Zotero → deduplica → exporte para a planilha.
3. **Conjunto de controle** (calibração): liste 3–5 artigos que você *sabe* que são relevantes (ex.: Colombo 2025, Kim 2025) e confirme que a string os recupera em pelo menos uma base. Anote quais foram/ não foram recuperados (mede o *recall* da string).

### Com esses dois CSVs eu fecho:
- A **Figura PRISMA 2020** (identificação por base → dedup → triagem → incluídos, com n por motivo de exclusão e a SBC/SOL incluída).
- A **caracterização do corpus** e a síntese RQ1–RQ5 com os números reais.
- A exclusão formal dos não-generativos e do preprint (CI1/CI2/CE5).
- O fechamento do marcador `[TODO-transparência]` (se algum estudo medir transparência como desfecho).

> **Não prossigo com Resultados/Discussão/Conclusão até receber `busca_contagens.csv` + `busca_registros.csv`.**
