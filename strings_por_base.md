# Strings de busca por base — RSL iSys

> String ampliada (5 dimensões PICOC) adaptada à sintaxe de cada base.
> **Janela temporal:** 2019–presente (CI3). **Idioma:** inglês ou português (CI4).
> Ajuste o filtro de ano na interface de cada base (não dentro da string), salvo onde indicado.
> Para cada base, registrar a contagem bruta **antes** de qualquer filtro manual (ver `PROTOCOLO` ao final).

> **Refinamento (calibração para reduzir falsos positivos — decisão declarada):**
> A versão anterior, com os termos ambíguos `transparency`, `accountability`, `access to information`, `open data` e `data portal*` soltos no bloco de contexto, trouxe ruído de fora do domínio governamental — p. ex. trabalhos de **contabilidade** (`accountability` → *accounting*), **criptografia** (LLM/RAG sem vínculo com governo) e **transparência de algoritmo/modelo**. Para corrigir, a string foi reestruturada em **três blocos**: os termos ambíguos passam a contar **apenas quando qualificados por um termo governamental** (ex.: `"government transparency"`, `"government accountability"`, `"access to public information"`), nunca soltos. Não foram usados operadores de proximidade (`NEAR`/`W/n`) — variam por base e quebram; usam-se frases qualificadas diretamente. Esta calibração deve ser registrada no protocolo como decisão metodológica.

---

## String de referência (conceitual — não colar em base)

```
Bloco 1 — Intervenção (IA): IA Generativa / LLMs / arquiteturas correlatas
AND
(
  Bloco 2 — Contexto governamental inequívoco (podem aparecer sozinhos):
            dados governamentais / legislativos / parlamentares · setor público ·
            governo digital / eletrônico / aberto · liberdade de informação / FOIA
  OR
  Bloco 3 — Termos ambíguos SÓ como frases qualificadas (nunca soltos):
            transparência governamental/pública · accountability governamental/pública ·
            acesso à informação pública · portal de dados governamental/aberto
)
```
> Estrutura final: **Bloco1 AND (Bloco2 OR Bloco3)**. O Bloco 3 já contém apenas frases qualificadas.

### Campo de busca correto por base

> A string deve restringir a busca a **título + resumo + palavras-chave**. O campo exato muda por base:

| Base | Campo correto (restringe a título-resumo-keywords) |
|---|---|
| Scopus | `TITLE-ABS-KEY(...)` |
| Web of Science | `TS=(...)` (Topic) |
| IEEE Xplore | `All Metadata` (ok — **não** é texto completo) |
| ACM Digital Library | `[Abstract: ...]` |
| SBC / SOL | busca simples |

> **Aviso geral:** nunca usar **"All Fields" / "texto completo" / "Full Text" / "[All:]"**. Buscar em texto completo infla a contagem em ordens de magnitude ao capturar menções incidentais no corpo do artigo; restringir sempre ao campo indicado para cada base.

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
  (
    ("open government data" OR "government data" OR "public sector data"
     OR "legislative data" OR "parliamentary data"
     OR "digital government" OR "e-government" OR "open government"
     OR "freedom of information" OR FOIA)
    OR
    ("government transparency" OR "public transparency"
     OR "government accountability" OR "public accountability"
     OR "access to public information"
     OR "government data portal*" OR "open data portal*")
  )
)
```
- Bloco 1 = intervenção (IA); bloco interno = **(Bloco 2 governamental inequívoco) OR (Bloco 3 ambíguos qualificados)**. Sem comentários na string — Scopus não os suporta.
- **A string deve ser colada DENTRO do parêntese do `TITLE-ABS-KEY(...)` no Advanced Search — nunca na barra de busca simples.** A barra simples equivale a *All Fields* e infla o resultado em ordens de magnitude. Conferida assim, a contagem cai drasticamente.
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
  (
    ("open government data" OR "government data" OR "public sector data"
     OR "legislative data" OR "parliamentary data"
     OR "digital government" OR "e-government" OR "open government"
     OR "freedom of information" OR FOIA)
    OR
    ("government transparency" OR "public transparency"
     OR "government accountability" OR "public accountability"
     OR "access to public information"
     OR "government data portal*" OR "open data portal*")
  )
)
```
- `TS=` busca em título, resumo, palavras-chave de autor e Keywords Plus.
- **Se a contagem vier alta demais**, isso sugere que a string longa foi cortada (cláusulas truncadas ao colar) ou que o filtro de ano não foi aplicado. Antes de exportar, conferir que: (a) o filtro **Publication Years ≥ 2019** foi efetivamente aplicado na interface; (b) a string inteira entrou **sem truncamento de cláusulas** (todos os `OR` e os dois blocos `AND` presentes). Recolar e reexecutar se houver dúvida.
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
(
 ("All Metadata":"open government data" OR "All Metadata":"government data"
  OR "All Metadata":"public sector data" OR "All Metadata":"legislative data"
  OR "All Metadata":"parliamentary data" OR "All Metadata":"digital government"
  OR "All Metadata":"e-government" OR "All Metadata":"open government"
  OR "All Metadata":"freedom of information" OR "All Metadata":FOIA)
 OR
 ("All Metadata":"government transparency" OR "All Metadata":"public transparency"
  OR "All Metadata":"government accountability" OR "All Metadata":"public accountability"
  OR "All Metadata":"access to public information"
  OR "All Metadata":"government data portal*" OR "All Metadata":"open data portal*")
)
```
- IEEE exige **≥ 3 caracteres antes do `*`**: `GPT*`, `LLM`, `RAG` sem wildcard (ok). `transformer*`, `chatbot*` ok.
- Filtro de ano: **2019–presente** na barra lateral.
- Se a interface limitar o nº de cláusulas, quebre em 2 buscas (bloco de intervenção × cada subgrupo de contexto) e some, **removendo duplicatas**.
- **Se a base estiver indisponível ("site fora", erro de acesso), registrar como "não executado — base indisponível em [data]", nunca como contagem 0.** Zero é uma afirmação sobre a literatura (não há trabalhos); indisponibilidade é uma afirmação sobre a base (não foi possível consultar). Reexecutar quando voltar.

---

## 4. ACM Digital Library — Advanced Search (campo `[Abstract: ...]`, em **3 passadas**)

> **NÃO usar o campo `All` / texto completo (`[All:]`) — o campo `[All:]` busca o texto inteiro do artigo e infla a contagem em ordens de magnitude, capturando menções incidentais. Restringir a `Abstract`.**

> **Coleção:** usar **"The ACM Guide to Computing Literature"** (~4M, padrão para RSL), **não** a "ACM Full-Text Collection" (~848k). Registrar qual coleção foi usada na contagem.

> **Por que 3 passadas:** ao colar a query longa inteira, a interface da ACM injeta cláusulas `[All: ]` **vazias** unidas por `AND` (ex.: `[[All: []] AND [Abstract: "..."] AND [All: ]]`), o que exige um campo vazio e **zera** a busca. Quebrar em 3 passadas curtas — bloco de intervenção **fixo** + um bloco de contexto por vez — mantém cada query curta o bastante para a interface aceitar sem injetar `[All: ]` vazios.

> **Como montar (obrigatório):** montar a query pelo **construtor do Advanced Search**, escolhendo o campo **`Abstract`** no dropdown de cada cláusula — **NÃO** colar a string inteira na barra de busca simples (é a colagem que injeta os `[All: ]` vazios). Se ainda aparecerem cláusulas `[All: ]` vazias unidas por `AND`, **removê-las manualmente** antes de executar.

**Bloco de intervenção (fixo — repetir idêntico nas três passadas):**
```
[Abstract: "generative artificial intelligence"] OR [Abstract: "generative ai"]
OR [Abstract: "large language model"] OR [Abstract: "llm"] OR [Abstract: "foundation model"]
OR [Abstract: transformer] OR [Abstract: gpt] OR [Abstract: chatgpt] OR [Abstract: llama]
OR [Abstract: mistral] OR [Abstract: gemini] OR [Abstract: "retrieval-augmented generation"]
OR [Abstract: rag] OR [Abstract: chatbot] OR [Abstract: "conversational agent"]
```

Cada passada = **(bloco de intervenção) AND (bloco de contexto da passada)**.

**Passada A — contexto governamental inequívoco:**
```
(bloco de intervenção)
AND
([Abstract: "open government data"] OR [Abstract: "government data"]
 OR [Abstract: "public sector data"] OR [Abstract: "legislative data"]
 OR [Abstract: "parliamentary data"])
```

**Passada B — governo digital / FOI:**
```
(bloco de intervenção)
AND
([Abstract: "digital government"] OR [Abstract: "e-government"]
 OR [Abstract: "open government"] OR [Abstract: "freedom of information"]
 OR [Abstract: foia])
```

**Passada C — termos qualificados:**
```
(bloco de intervenção)
AND
([Abstract: "government transparency"] OR [Abstract: "public transparency"]
 OR [Abstract: "government accountability"] OR [Abstract: "public accountability"]
 OR [Abstract: "access to public information"]
 OR [Abstract: "government data portal"] OR [Abstract: "open data portal"])
```

- Filtro de ano: **E-Publication Date ≥ 2019** no painel lateral (aplicar nas três passadas).
- ACM trunca por radical automaticamente; por isso os termos vão sem `*` (ex.: `transformer` cobre transformers).
- **Consolidação:** registrar a contagem **bruta de cada passada (A, B, C) separadamente** em `busca_contagens.csv` (ou numa nota). Exportar as três em **BibTeX/RIS**, importar no Zotero, **deduplicar a união** e usar o número **pós-dedup** como contagem final da ACM. Anotar **tanto as três contagens brutas quanto o total após união+dedup** (as passadas se sobrepõem — não somar as brutas diretamente).
- **Validação do controle:** confirmar que **Kim et al. (2025)** (*LegisFlow*, ACM UIST) aparece em **alguma** das três passadas — é o controle esperado na ACM. Se não aparecer em nenhuma, **sinalizar antes de prosseguir** (a string pode estar restrita demais ou na coleção errada).

---

## 5. SBC / SOL (Biblioteca Digital — Open Conference/Journal Systems) — PORTUGUÊS (CI4)

```
("inteligência artificial generativa" OR "IA generativa"
 OR "modelos de linguagem" OR "grandes modelos de linguagem"
 OR "modelo de linguagem de grande porte" OR LLM OR ChatGPT OR transformer)
AND
(
  ("dados abertos governamentais" OR "dados governamentais"
   OR "dados do setor público" OR "dados legislativos" OR "dados parlamentares"
   OR "governo digital" OR "governo eletrônico" OR "governo aberto"
   OR "liberdade de informação")
  OR
  ("transparência governamental" OR "transparência pública"
   OR "accountability governamental" OR "accountability pública"
   OR "responsabilização pública" OR "acesso à informação pública"
   OR "portal de dados governamentais" OR "portal de dados abertos")
)
```
- A busca da SOL é **simples** (suporte booleano limitado). Se o operador `AND/OR` não funcionar como esperado:
  1. Rode **sub-buscas** por par (1 termo de intervenção × 1 termo de contexto) e una os resultados manualmente, removendo duplicatas.
  2. Repita **sem acentos** (ex.: `transparencia`, `informacao`) — a indexação da SOL às vezes não normaliza diacríticos.
- Rode também a **string em inglês** (seção 1) na SOL, pois há trabalhos da SBC publicados em inglês.
- **Se houver bloqueio de acesso/login, não abandonar a base.** Buscar caminho institucional (biblioteca da UFS / orientador) para destravar o acesso. Só declarar como limitação — *"SOL não consultada por indisponibilidade de acesso no período"* — se o acesso **não** for resolvido a tempo.
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

### Validação obrigatória **antes de exportar** (calibração de recall)
> Depois de rodar cada string e **antes** de exportar os resultados, confirmar que o **conjunto de controle** aparece nos resultados: **Colombo et al. (2025)** e **Kim et al. (2025)**.
>
> - Se os controles **aparecem** → a string tem recall aceitável; pode exportar.
> - Se **não aparecem** → a string está **restrita demais** (campo errado, cláusula faltando, filtro de ano cortando) e precisa de ajuste **antes** de prosseguir. Não exportar uma string que não recupera os controles conhecidos.
>
> Registrar, **por base**, quais controles foram / não foram recuperados (mede o *recall* da string). Um controle pode legitimamente não estar indexado em uma base específica — o que importa é que cada controle seja recuperado em **pelo menos uma** base.
>
> **Especialmente após o refinamento de três blocos:** confirmar que **Colombo et al. (2025)** e **Kim et al. (2025)** continuam aparecendo. Se algum sumiu depois de qualificar os termos ambíguos, a string **apertou demais** — reavaliar quais frases qualificadas do Bloco 3 precisam ser ampliadas antes de exportar.

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
