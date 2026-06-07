# Handoff — Ajustes do Artigo (proposta de dissertação AgentAI)

> Resumo de sessão para retomar depois com contexto completo. Companion do handoff da apresentação SAS 1.

## Objetivo da sessão
Continuar os **ajustes no texto do artigo** (proposta de dissertação de mestrado da Bia) — os arquivos LaTeX deste repositório, **não** a apresentação. O foco é garantir que o texto reflita o mesmo **enquadramento honesto** consolidado no handoff da apresentação SAS 1.

## Repositório
- Caminho: `C:\Users\Nitro 5\Documents\GitHub\democracia_legislativa_artigo`
- Branch atual: `developer` (branch principal: `main`)
- Estrutura: `main.tex` + `capitulos/` (`introducao`, `fundamentacao`, `metodologia`, `desenvolvimento`, `estado_arte`, `consideracoes`)
- Último commit relevante: `81ffec5 "ajustes artigo"` (07/06/2026, 00:36) — mexeu pesado em `metodologia.tex`.
- Commit anterior importante: `9ce4e98` — "Corrige erros factuais: substitui SQLite por cache em memória e atualiza status PROPOR/ERBASE".

## Estado do artigo (auditado)
`metodologia.tex` relido por completo. **Já está alinhado** com o enquadramento honesto. Confirmado no texto:
- **Mistral 7B local** (não Gemini); justificativa (replicabilidade/soberania/custo) remetida à fundamentação (`subsec:escolha_modelo`).
- **Cache em memória** (não SQLite).
- **Linguagem de capacidades, não percentuais** ("cita por identificador estável", "preserva rastreabilidade").
- **Instrumentação pronta / medição em curso** explícito (fase 5, avaliação de rastreabilidade).
- **Limiares como metas-alvo**, não resultados; **suporte semântico** introduzido como métrica que torna a cláusula (c) da hipótese testável.
- **Ameaças à validade** tratam cobertura de recuperação ~100% por construção como "verificação de funcionamento, não qualidade".
- Cronograma: **PROPOR 2026** (retorno negativo fev/2026), **ERBASE 2026** (submetido).

## Decisões / princípios herdados (do handoff SAS 1)
- Falar em **CAPACIDADES**, nunca em **PERCENTUAIS** como se fossem resultados.
- Hipótese tem 3 limiares = **METAS**, não achados: classificação > baseline; factual >= 70%; rastreabilidade >= 80%.
- Rastreabilidade **já implementada** (no projeto de código, branch `developer-v2` — repo separado deste de artigo); o que está em curso é a **medição** com amostra significativa.
- Limitações honestas das métricas atuais: amostra minúscula (~4 perguntas), cobertura de recuperação ~100% por construção, precisão de citação só checa existência do id (não suporte semântico).
- Defesa prevista: **janeiro de 2027**.

## O que foi feito nesta sessão
1. Levantamento do estado do repo (git log, status, estrutura).
2. Auditoria do `metodologia.tex` contra o enquadramento honesto -> **conforme**.
3. Memória persistente do Claude Code criada: `projeto-agentai.md` (visão geral) + ponteiro no `MEMORY.md`.

## Pendências / próximos passos (a decidir)
1. **Revisar os demais capítulos** com o mesmo enquadramento honesto — prioridade para `fundamentacao.tex` (seção de escolha do modelo, que a metodologia referencia) e `desenvolvimento.tex` (reporta a "verificação funcional preliminar").
2. Incorporar **feedback específico da banca / da apresentação**, se houver.
3. **Compilar o PDF** e conferir referências/figuras/quadros fechando.
4. Outro item da lista que não esteja registrado aqui.

## Observações de ambiente
- Windows / PowerShell. LaTeX no repo (latexmk — há `main.fdb_latexmk`, `main.fls`).
