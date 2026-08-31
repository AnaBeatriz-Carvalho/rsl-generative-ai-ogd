# Carta-Resposta aos Revisores — iSys (Major Revision)

**Manuscrito:** *Generative AI for Public-Sector Information Access and Public Transparency: A Systematic Literature Review*

Agradecemos aos Editores e aos Revisores A e C pela leitura cuidadosa e pelos comentários construtivos. Abaixo respondemos a cada ponto, resumindo o comentário, indicando nossa resposta e apontando exatamente onde o manuscrito foi alterado. Todas as passagens modificadas estão destacadas em amarelo no PDF revisado (comando `\rev{}`); tabelas, figuras e a subseção de taxonomia inteiramente novas estão sinalizadas por seus títulos/legendas destacados.

**Nota sobre o corpus (29 → 36).** Na submissão original, a síntese reunia 29 estudos e 19 relatos haviam permanecido *não recuperados* (*reports not retrieved*). Atendendo à recomendação do Revisor A, conduzimos uma rodada adicional de recuperação de texto completo desses 19 relatos: nove foram recuperados e reavaliados sob os mesmos critérios, dos quais **sete foram incluídos e dois excluídos** após leitura integral; dez permanecem não recuperados. O corpus de síntese passou a **36 estudos** (34 internacionais + 2 da SBC/SOL). Todos os sete novos estudos foram extraídos, avaliados quanto à qualidade e classificados a partir do texto completo, com o mesmo instrumento aplicado aos demais. Não alteramos a string de busca, não realizamos nova busca nem *snowballing*, e mantivemos o procedimento de revisor único. Sempre que abaixo mencionamos "36 estudos", trata-se desse corpus atualizado.

---

## Revisor A

**A1 — O "paradoxo da transparência" é apresentado como contribuição original, mas deriva de Schelhorn et al.**
*Resposta.* Concordamos. O termo não é nosso: pertence ao estudo de Schelhorn et al. e refere-se ao efeito específico de sobrecarregar o usuário ao combinar interface conversacional com tabelas brutas. Reescrevemos o texto para atribuí-lo explicitamente àquele estudo e distingui-lo do nosso achado transversal, que passamos a nomear **"lacuna entre motivação e avaliação da transparência"**.
*Mudanças.* `resultados_rsl.tex` (RQ5, atribuição e desambiguação do termo a Schelhorn); Discussão (`isys_rsl.tex`), onde o achado central é consistentemente chamado de lacuna motivação–avaliação, nunca "paradoxo".

**A2 — "Transparência" nunca é definida; é um construto composto (compreensão, controle social, uso efetivo, acessibilidade, encontrabilidade…) que os estudos atendem parcialmente.**
*Resposta.* Concordamos e retornamos à literatura. Passamos a definir transparência como **construto sociotécnico de cinco dimensões** — encontrabilidade, acessibilidade, compreensão, uso efetivo e controle social — o que permite dizer que um estudo pode atuar sobre uma dimensão sem medir o desfecho cívico.
*Mudanças.* Nova conceituação na Fundamentação, §2.1 (`isys_rsl.tex`), com referências de SI/governo (Michener & Bersch; Meijer; Heald); operacionalização em quatro níveis na §Síntese do Método (ver A8/A13).

**A3 — A definição de OGD (Seção 2.1) não cobre o corpus real (legislação, memorandos, FAQs, saúde, imigração); ou limitar a OGD ou ampliar para informação do setor público.**
*Resposta.* Adotamos a segunda opção, recomendada pelo Revisor. Ampliamos o enquadramento para **informação do setor público**, mantendo OGD como caso paradigmático, mas não exclusivo, e alteramos o **título** de "Open Government Data" para "Public-Sector Information".
*Mudanças.* §2.1 (`isys_rsl.tex`, delimitação do escopo); título, resumo/abstract, Introdução, Conclusão e critério CI1 (`metodo_rsl.tex`) alinhados; string operacionaliza esse escopo (`metodo_rsl.tex`).

**A4 — "Tipo de dado" (RQ2) é polissêmico (formato? natureza? aplicação?); só o 2º dos quatro tipos é OGD; a discussão mistura tipos.**
*Resposta.* Concordamos. Renomeamos a RQ2 para **"Natureza e domínio da informação do setor público"**, eliminando a expressão ambígua "tipo de dado", e reorganizamos os agrupamentos por natureza/domínio (legislativo-jurídico; portais de dados abertos; serviços e procedimentos; políticas e dados setoriais; conceitual).
*Mudanças.* RQ2 renomeada na Tabela de RQs e no campo de extração (`metodo_rsl.tex`); §RQ2 reescrita (`resultados_rsl.tex`, "Natureza e Domínio da Informação do Setor Público").

**A5 — Se o desfecho é o impacto cívico, a fonte não são apenas artigos científicos; parte do estudo precisaria da literatura cinza.**
*Resposta.* Concordamos com o ponto de fundo. Assumimos, por decisão de protocolo, a síntese apenas de estudos primários revisados por pares (CI2/CE3), e explicitamos que a conclusão sobre a ausência de desfecho cívico refere-se **estritamente aos 36 estudos incluídos**, não à totalidade da prática do campo — implantações e evidências de impacto fora da literatura científica podem não ter sido captadas.
*Mudanças.* Novo item **"Literatura cinza"** nas Ameaças à Validade (`isys_rsl.tex`).

**A6 — A string (B1 AND (B2.1 OR B2.2)) retorna chatbots de e-gov/RAG fora do foco, gerando heterogeneidade; refinar os construtos e então a string.**
*Resposta.* A heterogeneidade decorre, em parte, do escopo agora explicitado (informação do setor público, não só OGD): estudos sobre serviços e documentos são legítimos sob esse recorte. Por isso não estreitamos a string após a execução — isso comprometeria a reprodutibilidade do protocolo já aplicado —, mas passamos a explicar que os termos operacionalizam o escopo ampliado e derivam da PICOC definida a priori.
*Mudanças.* Parágrafo explicativo após a figura da string (`metodo_rsl.tex`); a string permanece a executada, agora justificada pelo escopo de A3.

**A7 — A PICOC parece usada como justificativa a posteriori, não no planejamento.**
*Resposta.* Concordamos que a versão anterior não deixava isso claro. Reescrevemos a seção para mostrar que a PICOC **precede e orienta** a derivação dos termos, e que a tabela PICOC e a string dela decorrem, e não o inverso.
*Mudanças.* §Estratégia de Busca (`metodo_rsl.tex`), parágrafo que introduz a PICOC antes da Tabela e explicita "a PICOC precede e orienta a busca, em vez de justificá-la a posteriori".

**A8 — A codificação qualitativa precisa ser detalhada (indutiva/dedutiva? unidade? iterações? quem definiu/validou? categorias ambíguas?); um estudo poderia estar em mais de uma categoria.**
*Resposta.* Detalhamos o procedimento. A síntese temática foi **indutiva**, com o estudo primário como unidade; descrevemos como as categorias emergiram por comparação e agrupamento, como se tratou a classificação múltipla (a dimensão de função **acumula** valores; posição e objeto são exclusivos por estudo) e a regra de codificação de família de modelo. Registramos que a codificação foi feita por uma única pessoa (ver A15).
*Mudanças.* §Síntese e §Extração (`metodo_rsl.tex`): procedimento temático, regra de modelo principal, tratamento de funções combinadas; a taxonomia (§4.6) explicita exclusividade por dimensão e acúmulo na função.

**A9 — A taxonomia oferta/demanda é simplista; "acesso conversacional" e "mediação" parecem a mesma coisa variando o tipo de dado; é preciso maior fragmentação.**
*Resposta.* Concordamos e reconstruímos a taxonomia em **três dimensões ortogonais**: (1) posição na cadeia informacional (oferta × demanda), (2) objeto informacional, (3) função da IA Generativa. É a Dimensão 2 (objeto), e não a posição, que distingue consulta a dados de mediação de serviços — exatamente a sobreposição apontada. Cada categoria tem definição, critério de inclusão e critério de diferenciação.
*Mudanças.* Nova subseção **§4.6** com **Tabela `tab:taxonomia`** e **Figura `fig:taxonomia`** (`resultados_rsl.tex`); resumo, Introdução e Conclusão descrevem a taxonomia como tridimensional.

**A10 — Inferências na Discussão sem evidência: "deslocamento do dado estruturado para textual" (sem temporalidade); "alucinação em quase todos" (apontar quais).**
*Resposta.* Concordamos. Removemos a alegação de tendência temporal e passamos a descrever uma **predominância transversal** de informação textual no corpus, ressalvando a ausência de série histórica. Substituímos os quantificadores vagos por contagem verificável: a alucinação é discutida em **24 dos 36 estudos**.
*Mudanças.* Fecho da §RQ2 ("predominância… e não uma tendência histórica de substituição", `resultados_rsl.tex`); abertura da §RQ5 ("vinte e quatro dos trinta e seis"); Discussão §3 (`isys_rsl.tex`).

**A11 — Falta articulação com teorias de SI que descrevam a transparência como fenômeno sociotécnico.**
*Resposta.* Aprofundamos a leitura sociotécnica: além da definição de cinco dimensões (A2), a Discussão explicita que o fenômeno emerge da interação entre o artefato (LLM), a informação pública, as organizações, as práticas institucionais, a capacidade do cidadão e o resultado público — e que concentrar a avaliação no artefato é o que produz a lacuna identificada.
*Mudanças.* §2.1 (construto sociotécnico) e parágrafo de fecho da Discussão (`isys_rsl.tex`, "Lidos sob a leitura sociotécnica…").

**A12 — Muitas referências vêm de veículos de IA/IHC, distanciando o foco de SI/e-gov.**
*Resposta.* Reforçamos o enquadramento em SI e a seção de Trabalhos Relacionados, contrastando a revisão com sínteses de SI/governo digital (Bastos et al.; Widiyaningtyas et al.; Savveli et al.) e incorporando referências de SI para os construtos (OGD, *accountability*, transparência). Ressalvamos, com honestidade, que a composição do corpus reflete onde o campo efetivamente publica; não substituímos referências do corpus artificialmente.
*Mudanças.* §2.3 Trabalhos Relacionados reescrita; referências de SI adicionadas na Fundamentação (`isys_rsl.tex`).

**A13 — Não se detalha por que cada artigo retornado foi rejeitado, nem se apresenta a avaliação de qualidade.**
*Resposta.* Passamos a registrar os motivos de exclusão de forma rastreável e a apresentar os escores. As duas exclusões após leitura integral têm motivo e critério explícitos (ver A17); os motivos de triagem estão no material suplementar; e os escores de qualidade dos 36 estudos são agora apresentados.
*Mudanças.* §Seleção (`resultados_rsl.tex`, motivos + suplementar); novo **Apêndice A** com os escores AQ1–AQ5 estudo a estudo.

**A14 — Não se detalha como as categorizações foram criadas: houve análise temática ou outro método?**
*Resposta.* Explicitamos que foi **análise/síntese temática indutiva**, seguindo o procedimento de Cruzes & Dybå (2011), descrevendo o encadeamento comparação → agrupamento → categorias.
*Mudanças.* §Síntese (`metodo_rsl.tex`), com citação a Cruzes & Dybå (2011).

**A15 — A condução por um único autor deve constar como limitação (viés de julgamento), sobretudo dadas as fronteiras ambíguas de codificação.**
*Resposta.* Concordamos. Registramos explicitamente a condução por revisor único, sem medida de concordância, como ameaça à validade interna, descrevendo as salvaguardas adotadas (critérios a priori, registro rastreável), sem reivindicar concordância entre avaliadores.
*Mudanças.* Menção na Triagem, Extração e Codificação (`metodo_rsl.tex`) e item **Validade interna** nas Ameaças (`isys_rsl.tex`).

**A16 — Reavaliar se a metodologia é RSL ou Mapeamento Sistemático (mais provável, pois não compara resultados; protocolo PRISMA-ScR).**
*Resposta.* Adotamos um desenho híbrido explícito e **mantivemos a denominação "Systematic Literature Review"**: o rigor de busca e seleção segue o protocolo de RSL (Kitchenham & Charters; PRISMA 2020), com avaliação de qualidade dos estudos incluídos; a síntese, descritiva ao estilo de mapeamento (Petersen et al.), está agora explicitada no Método. Não retroajustamos um protocolo não executado, e a natureza de caracterização das questões de pesquisa sustenta essa denominação.
*Mudanças.* §Método, parágrafos iniciais (`metodo_rsl.tex`), que enunciam o desenho híbrido e a natureza de mapeamento da síntese. Título mantido.

**A17 — A exclusão de 19 de 29 é preocupante; buscar outras formas de recuperar (ResearchGate, contato com autores).**
*Resposta.* Seguimos a recomendação. Conduzimos rodada adicional de recuperação dos 19 relatos, usando páginas de editora/DOI, acesso institucional, versões indexadas por buscadores acadêmicos, ResearchGate/repositórios e contato direto com autores. Recuperamos nove; **sete foram incluídos e dois excluídos** após leitura integral (Baron 2025 — estudo secundário que sintetiza o Baron 2023 já incluído, **CE2**, evitando dupla contagem; Tahtali et al. 2026 — trata de aceitação organizacional de IA em compras, não do acesso/mediação de informação pública, **CI1**). Dez permanecem não recuperados e são tratados como viés de disponibilidade.
*Mudanças.* §Seleção e fluxo PRISMA atualizados para N=36 (`resultados_rsl.tex`); item **"Viés de disponibilidade"** nas Ameaças (`isys_rsl.tex`); lista dos dez remanescentes com DOIs no material suplementar.

**A18 — Linguagem ocasionalmente retórica ("ironia", "ferramentas opacas", "criteriosa", "rigorosa") e afirmações mais fortes que a evidência.**
*Resposta.* Concordamos e reescrevemos essas passagens em registro analítico. A frase da "ironia" tornou-se uma afirmação sobre a tensão entre a opacidade de componentes e os requisitos de auditabilidade; "filtragem criteriosa" foi substituída pela descrição do procedimento.
*Mudanças.* Discussão §3 e §Seleção (`isys_rsl.tex`, `resultados_rsl.tex`); os termos retóricos foram eliminados.

---

## Revisor C

**C1 — Os critérios usados para identificar e analisar a transparência nos estudos não são claros.**
*Resposta.* Passamos a classificar cada estudo por um procedimento explícito de **quatro níveis** ancorado nas cinco dimensões de transparência (menção; atuação sobre uma dimensão; uso de *proxy*; desfecho cívico), registrado em matriz no material suplementar.
*Mudanças.* Novo parágrafo na §Síntese (`metodo_rsl.tex`); ver também A2.

**C2 — Esclarecer como o conceito de transparência foi usado e como se diferencia de acesso, usabilidade, compreensão, confiança, participação, accountability.**
*Resposta.* Concordamos. Delimitamos transparência frente a esses construtos próximos: usabilidade e qualidade da informação podem favorecê-la sem demonstrá-la; confiança e participação podem decorrer dela sem serem sinônimos; *accountability* pressupõe mecanismos institucionais que ultrapassam o acesso.
*Mudanças.* §2.1 (`isys_rsl.tex`), parágrafo que separa transparência de construtos próximos.

**C3 — A taxonomia não é apresentada com estrutura (dimensões, categorias, relações, critérios); parece agrupamento descritivo; desenvolvê-la ou trocar "taxonomia" por "classificação".**
*Resposta.* Optamos por desenvolvê-la. Ver **A9**: taxonomia de três dimensões com tabela definicional (critérios de inclusão e de diferenciação por categoria) e figura de relações.
*Mudanças.* §4.6, `tab:taxonomia`, `fig:taxonomia` (`resultados_rsl.tex`). *(As referências de taxonomia sugeridas pelo Revisor foram consultadas como orientação sobre a forma de estruturar a contribuição.)*

**C4 — O procedimento de qualidade é descrito, mas os escores não são apresentados; informar e explicar se/como a qualidade influenciou a síntese.**
*Resposta.* Apresentamos os escores dos 36 estudos e explicamos seu papel: a avaliação de qualidade **pondera, não exclui** — foi aplicada após a seleção por CI/CE. Dois estudos ficaram abaixo do limiar de 2,5 (Dineva e Atanasova, #3; Kumar et al., #32; ambos 2,0) e, embora mantidos na caracterização, **não sustentam sozinhos** nenhuma categoria ou conclusão.
*Mudanças.* §Avaliação de Qualidade (`metodo_rsl.tex`); parágrafo de escores na Caracterização (`resultados_rsl.tex`); **Apêndice A** (escores AQ1–AQ5).

**C5 — Explicar como as categorias foram construídas, quais critérios, se um estudo pode ter mais de uma classificação e como híbridos foram tratados.**
*Resposta.* Detalhamos a construção (ver A8): posição e objeto são **exclusivos por estudo** (classificação pela aplicação principal); a função **acumula** valores; sistemas que combinam funções (p.ex. extração + consulta) são registrados na descrição sem gerar dupla contagem.
*Mudanças.* §Síntese e §Extração (`metodo_rsl.tex`); texto e nota da §4.6 com exemplo de estudo de função combinada (`resultados_rsl.tex`).

**C6 — A PICOC é usada sem explicação; apresentar seu significado, origem e papel na string, e defini-la antes da Tabela 2.**
*Resposta.* Passamos a explicar a PICOC (*Population, Intervention, Comparison, Outcome, Context*), sua origem (adaptação do PICO da medicina baseada em evidências, via Kitchenham & Charters) e seu papel na derivação dos termos, **antes** da tabela correspondente.
*Mudanças.* §Estratégia de Busca (`metodo_rsl.tex`), parágrafo que precede a Tabela PICOC; ver A7.

**C7 — Esclarecer como a busca na SBC/SOL foi feita (interface direta ou scripts; termos, filtros, tratamento manual).**
*Resposta.* Descrevemos a execução: consulta manual pela interface da própria plataforma (baseada em *Open Journal/Conference Systems*), sem script ou API, com string equivalente em português, triagem e deduplicação manuais e o mesmo recorte temporal e de idioma; por não haver exportação padronizada, a SBC/SOL aparece em fluxo separado no PRISMA.
*Mudanças.* §Estratégia de Busca (`metodo_rsl.tex`), parágrafo dedicado à execução na SBC/SOL.

**C8 — Apresentar a distribuição geográfica dos estudos (país já extraído, mas ausente dos resultados).**
*Resposta.* Concordamos. Definimos que o campo *país* registra o **contexto governamental empírico** (não a afiliação) e adicionamos uma síntese geográfica: **19 contextos nacionais** e um supranacional; EUA e China com 4 cada, Reino Unido 3; por região, **Europa 15, Ásia 7**, Américas do Norte e do Sul 5 cada, Oceania 1 e **nenhum contexto africano** — ligada às ameaças à validade externa.
*Mudanças.* Definição do campo *país* (`metodo_rsl.tex`); nova subseção **§Distribuição geográfica** com **Tabela `tab:geografia`** (`resultados_rsl.tex`).

**C9 — Ampliar a síntese quantitativa descritiva (países, tipos de dados, modelos, métodos de avaliação, métricas, categorias).**
*Resposta.* Ampliamos a síntese descritiva com a distribuição geográfica, os escores de qualidade, a tabela de caracterização do corpus e uma tabela consolidada estudo a estudo (país, modelo, três dimensões da taxonomia, tipo de avaliação e escore).
*Mudanças.* Tabela de caracterização (`resultados_rsl.tex`); **Apêndice B** consolidado (`isys_rsl.tex`); ver C8 e C15.

**C10 — Acrônimos: "IA" e "LLM" usados antes de definidos; LLM definido em PT na Introdução e em EN na §2.2; "RAG" definido duas vezes na §2; adotar sigla para SI.**
*Resposta.* Corrigimos. "Inteligência Artificial (IA)" e "Sistemas de Informação (SI)" passam a ser definidos na primeira ocorrência; LLMs é definido uma única vez; RAG é definido uma única vez na §2.
*Mudanças.* Resumo e Introdução (`isys_rsl.tex`); §2.2 (definição única de RAG).

**C11 — O manuscrito mistura PT e EN (título em EN, corpo em PT; título de seção "Background e Trabalhos Relacionados"); padronizar idioma; sugestão de redigir tudo em inglês.**
*Resposta.* Padronizamos a terminologia e corrigimos o título de seção para **"Fundamentação e Trabalhos Relacionados"**, eliminando a mistura de idiomas nos títulos e a dupla definição de LLM. Mantivemos o corpo em português, idioma do periódico e dos pareceres, e tratamos a redação integral em inglês como sugestão a ser considerada em versão futura.
*Mudanças.* Título da §2 (`isys_rsl.tex`); auditoria de terminologia no resumo, Introdução, §4.6 e Conclusão.

**C12 — "Objetivo e contribuições" e "Organização" poderiam ser incorporados ao texto corrido, sem negrito.**
*Resposta.* Concordamos. Removemos os rótulos em negrito e integramos ambos como parágrafos correntes da Introdução, preservando o conteúdo (objetivo, RQ1–RQ5, três contribuições e o mapa das seções).
*Mudanças.* Introdução (`isys_rsl.tex`): rótulos `\paragraph{}` removidos; os parágrafos fluem no corpo do texto.

**C13 — Incluir, na primeira ocorrência da SBC/SOL, nota de rodapé com o endereço e breve explicação de seu papel.**
*Resposta.* Adicionamos a nota de rodapé com o endereço (sol.sbc.org.br) e a explicação de que a SOL é a biblioteca digital da SBC, principal repositório da produção brasileira em Computação.
*Mudanças.* Nota de rodapé na §Estratégia de Busca (`metodo_rsl.tex`).

**C14 — A Figura 1 apresenta Web Semântica como paradigma anterior e IA Generativa como atual; a distinção é excessivamente linear; não seriam complementares?**
*Resposta.* Concordamos. Refizemos a figura como **abordagens complementares** (dados conectados/grafos de conhecimento e IA Generativa/RAG), convergindo em grafo + RAG + LLM, e ajustamos legenda e texto para não descrevê-las como "anterior/atual". A imagem externa foi substituída por diagrama autocontido.
*Mudanças.* **Figura `fig:paradigmas`** redesenhada e recaptionada; §2.2 e §2.3 ajustadas de "substituir" para "via complementar" (`isys_rsl.tex`).

**C15 — Tabela consolidada com os estudos (país, tipo de dado, modelo, categoria de aplicação, forma de avaliação, resultados).**
*Resposta.* Concordamos. Adicionamos uma tabela consolidada, auditável estudo a estudo, com contexto governamental, modelo principal, as três dimensões da taxonomia, o tipo de avaliação e o escore de qualidade, remetendo à planilha de extração no suplemento.
*Mudanças.* Novo **Apêndice B "Visão Consolidada do Corpus"**, Tabela `tab:corpus_consolidado` (`isys_rsl.tex`).

**C16 — Figuras que sintetizem a taxonomia, suas relações e a distribuição dos estudos; um diagrama de Sankey ou visualização compatível.**
*Resposta.* Adicionamos uma figura que representa as três dimensões da taxonomia e suas relações (`fig:taxonomia`), com as contagens por posição e objeto. Avaliamos um diagrama de Sankey e optamos por um diagrama relacional, por representar melhor a ortogonalidade das dimensões; a distribuição completa, estudo a estudo, é mantida na tabela consolidada e no material suplementar, onde uma visualização adicional pode ser disponibilizada.
*Mudanças.* **Figura `fig:taxonomia`** (`resultados_rsl.tex`); Apêndice B para a distribuição por estudo.

**C17 — A Discussão ficaria mais clara se os estudos fossem organizados pela taxonomia e discutidos a partir dela.**
*Resposta.* Acolhemos parcialmente. A Discussão permanece organizada pelos achados (a lacuna motivação–avaliação; o desequilíbrio oferta/demanda; a reprodutibilidade e a dependência de modelos proprietários; a recepção pelo cidadão), estrutura que sustenta a contribuição central; a **taxonomia estrutura os Resultados (§4.6) e é referenciada na Discussão** como ponto de partida da agenda de pesquisa.
*Mudanças.* Referência explícita à taxonomia no fecho da Discussão (`isys_rsl.tex`); vínculo com §4.6.

---

## Editores

**E1 — Clarificar construtos-chave, em especial transparência e OGD.**
*Resposta.* Feito: transparência como construto sociotécnico de cinco dimensões e distinção de construtos próximos; escopo ampliado para informação do setor público, com OGD como caso paradigmático. Ver **A2, A3, C1, C2**.

**E2 — Fortalecer o rigor e a transparência metodológica da revisão.**
*Resposta.* Feito: PICOC a priori, string justificada pelo escopo, execução da SBC/SOL descrita, rastreio de exclusões, revisor único declarado como limitação, e recuperação adicional dos 19 relatos. Ver **A6, A7, A13, A15, A17, C6, C7**.

**E3 — Explicar melhor os procedimentos de codificação e de avaliação de qualidade.**
*Resposta.* Feito: síntese temática indutiva (Cruzes & Dybå), regra de codificação de modelo, tratamento de classificação múltipla, e apresentação dos escores com seu papel de ponderação. Ver **A8, A14, C4, C5**.

**E4 — Reforçar a fundamentação teórica em SI.**
*Resposta.* Feito: leitura sociotécnica do fenômeno na Fundamentação e na Discussão, e reforço do enquadramento e das referências de SI. Ver **A11, A12**.

**E5 — Desenvolver mais claramente a taxonomia e suas evidências de apoio.**
*Resposta.* Feito: taxonomia de três dimensões com tabela definicional, figura de relações e tabela consolidada que evidencia a classificação estudo a estudo. Ver **A9, C3, C15, C16**.

**E6 — Submeter carta-resposta (comentário a comentário) e PDF revisado com mudanças destacadas.**
*Resposta.* Esta carta responde a cada comentário dos Revisores e dos Editores, indicando a alteração e sua localização. O PDF revisado acompanha todas as mudanças **destacadas em amarelo** (comando `\rev{}`), para comparação com a versão anterior. O protocolo, as strings por base, a lista de estudos e a planilha de extração permanecem no repositório de materiais suplementares.

---

Agradecemos novamente aos Revisores e Editores. As revisões, em conjunto, tornaram os construtos mais precisos, a metodologia mais rastreável e a taxonomia efetivamente uma contribuição estruturada.
