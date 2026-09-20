# Aviação e geopolítica: miniguia de estudo com NotebookLM

Projeto do desafio DIO **Acelere sua aprendizagem com IA: explore o poder do NotebookLM**.

## Contexto e objetivos

A aviação conecta países, mas depende de autoridades nacionais, acordos de tráfego e avaliação de riscos. O caderno investiga essa relação por três portas de entrada: a autoridade de aviação civil russa (Rosaviatsiya), a companhia norte-coreana Air Koryo e um alerta ucraniano sobre o espaço aéreo russo.

Objetivos de estudo:

1. Distinguir autoridade aeronáutica, companhia aérea e organização internacional.
2. Entender como soberania do espaço aéreo e direitos de tráfego condicionam rotas.
3. Analisar como um conflito gera pedidos de restrição e decisões de segurança.
4. Confrontar respostas da IA com suas citações, separando notícia, fonte de referência e regra oficial.

**[Caderno temático no NotebookLM](https://notebook.google.com/notebook/d87fcea4-3d0f-4c7d-ba40-f52cc3447844)**
## Curadoria: fontes inseridas no NotebookLM

| ID | Fonte aberta | Uso no estudo | Cuidado na leitura |
| --- | --- | --- | --- |
| N1 | [Agência Federal de Transporte Aéreo — Wikipédia](https://pt.wikipedia.org/wiki/Ag%C3%AAncia_Federal_de_Transporte_A%C3%A9reo) | Identificar a Rosaviatsiya como órgão da aviação civil russa. | Enciclopédia editável: conferir afirmações específicas e datas nas referências originais. |
| N2 | [Air Koryo — Wikipédia](https://en.wikipedia.org/wiki/Air_Koryo) | Examinar uma companhia aérea estatal como exemplo de conexão entre aviação e relações internacionais. | Rotas e frota mudam; evitar tomar dados atuais como permanentes. |
| N3 | [CNN Brasil/Reuters — Ucrânia alerta ONU sobre insegurança do espaço aéreo russo](https://www.cnnbrasil.com.br/internacional/aviacao-civil-ucrania-alerta-onu-sobre-inseguranca-do-espaco-aereo-russo/) | Estudar um pedido político ligado à segurança de voos civis em zona de conflito. | A reportagem descreve um **pedido** da Ucrânia, não uma proibição mundial já adotada. |

### Fontes oficiais que não foram adicionadas ao NotebookLM

| ID | Fonte | Uso |
| --- | --- | --- |
| C1 | [ICAO — soberania do espaço aéreo e avaliação de segurança](https://www.icao.int/news/icao-statement-state-sovereignty-over-airspace-and-safety-assessments) | Conferir a regra do Artigo 1º da Convenção de Chicago e as responsabilidades estatais. |
| C2 | [ICAO Data+ — liberdades do ar](https://dataplus.icao.int/Home/FAQ) | Conferir a distinção entre sobrevoo, escala técnica e transporte comercial. |

## Engenharia de prompts e cicatrizes

### Teste 1 — distinguir autoridade e companhia

**Prompt usado:** “Com base apenas nas fontes do caderno, explique a diferença entre a Agência Federal de Transporte Aéreo da Rússia (Rosaviatsiya) e a Air Koryo. Para cada uma, diga se é autoridade pública ou companhia aérea, qual função a fonte descreve e cite a fonte usada. Se alguma atribuição não estiver documentada, diga ‘não confirmado nas fontes’.”

**Resposta obtida, em resumo:** o NotebookLM classificou a Rosaviatsiya como autoridade pública de supervisão e gestão da aviação civil russa e a Air Koryo como companhia aérea estatal norte-coreana. Identificou funções de fiscalização e gestão do tráfego para a primeira e operações comerciais para a segunda. Também marcou como **não confirmado** o modo específico como a Rosaviatsiya autoriza ou fiscaliza voos da Air Koryo na Rússia e os detalhes de orçamento e pessoal. Os papéis gerais estão descritos em [N1](https://pt.wikipedia.org/wiki/Ag%C3%AAncia_Federal_de_Transporte_A%C3%A9reo) e [N2](https://en.wikipedia.org/wiki/Air_Koryo).

**Cicatriz:** a resposta acrescentou detalhes secundários, como atividades comerciais fora da aviação. Eles aparecem em N2, mas não ajudam a responder à distinção central. Uma revisão mais enxuta seria: “Compare somente natureza institucional e função aeronáutica de N1 e N2, em quatro linhas, e liste separadamente o que as fontes não demonstram.”

### Teste 2 — separar pedido, alerta e proibição

**Prompt usado:** “Na reportagem ‘Aviação civil: Ucrânia alerta ONU sobre insegurança do espaço aéreo russo’, separe em três tópicos: (1) o que a Ucrânia pediu, (2) o que a OACI pode fazer, segundo a reportagem, e (3) se o texto confirma que houve uma proibição global de voos. Cite os trechos usados. Não trate um pedido como decisão já implementada.”

**Resposta obtida, em resumo:** o NotebookLM distinguiu o pedido ucraniano para que a OACI incentivasse a proibição de operações civis no espaço aéreo russo, o alerta emitido pela organização e a ausência de uma proibição universal comprovada. A reportagem informa que transportadoras de alguns países ainda utilizavam esse espaço aéreo. Essa leitura é sustentada por [N3](https://www.cnnbrasil.com.br/internacional/aviacao-civil-ucrania-alerta-onu-sobre-inseguranca-do-espaco-aereo-russo/).

**Cicatriz:** a resposta chamou a OACI de “órgão regulador” e mencionou “decisões bilaterais/nacionais prévias” sem demonstrar, na reportagem, quais atos específicos produziram cada restrição. A formulação mais segura é: “A reportagem informa que a OACI influencia políticas nacionais, mas não impõe regras diretamente; ela não mapeia todas as decisões nacionais aplicáveis.”

### Teste 3 — síntese e lacunas

**Prompt usado:** “Usando as três fontes do caderno, explique em até 200 palavras como decisões de governos, atuação de companhias aéreas e riscos de conflito se relacionam na aviação civil. Identifique qual fonte sustenta cada afirmação e marque separadamente qualquer inferência. Termine com duas perguntas que as fontes não respondem.”

**Resposta obtida, em resumo:** o NotebookLM relacionou regulação estatal, operação de companhias aéreas e riscos de conflito. Apontou como inferência que a aviação pode funcionar como instrumento geopolítico. Terminou com duas lacunas úteis: como a Rosaviatsiya coordena especificamente os voos da Air Koryo na Rússia e qual o custo acumulado de desvios para as companhias. As bases documentais são [N1](https://pt.wikipedia.org/wiki/Ag%C3%AAncia_Federal_de_Transporte_A%C3%A9reo), [N2](https://en.wikipedia.org/wiki/Air_Koryo) e [N3](https://www.cnnbrasil.com.br/internacional/aviacao-civil-ucrania-alerta-onu-sobre-inseguranca-do-espaco-aereo-russo/).

**Cicatriz:** apesar do pedido de identificar a fonte de *cada* afirmação, o texto recebido não trouxe essa correspondência de forma verificável e generalizou sobre sanções e mudanças de rota.

**Lição do processo:** pedir fontes na resposta é útil, mas a conferência precisa ocorrer no documento original. As perguntas não respondidas orientam a próxima rodada de pesquisa, sem virar conclusões por repetição.

## Miniguia de estudo

### 1. Estado, agência e companhia aérea

O Estado exerce soberania sobre o espaço aéreo acima de seu território. Uma autoridade como a Rosaviatsiya integra a estrutura de supervisão da aviação civil russa; uma companhia como a Air Koryo opera transporte aéreo. Esses atores têm funções diferentes e uma resposta sobre “quem controla os voos” precisa nomear qual decisão está em análise. [N1](https://pt.wikipedia.org/wiki/Ag%C3%AAncia_Federal_de_Transporte_A%C3%A9reo), [N2](https://en.wikipedia.org/wiki/Air_Koryo), [C1](https://www.icao.int/news/icao-statement-state-sovereignty-over-airspace-and-safety-assessments).

### 2. Soberania e acesso a mercados

O princípio da soberania dá ao Estado autoridade para regular ou restringir o uso de seu espaço aéreo. As liberdades do ar descrevem direitos comerciais distintos: sobrevoar, fazer escala técnica e transportar passageiros ou carga. Operar uma rota internacional envolve, portanto, mais do que a capacidade técnica de uma aeronave. [C1](https://www.icao.int/news/icao-statement-state-sovereignty-over-airspace-and-safety-assessments), [C2](https://dataplus.icao.int/Home/FAQ).

### 3. Conflito e segurança

Em setembro de 2026, segundo a reportagem da CNN Brasil/Reuters, a Ucrânia pediu à OACI que incentivasse seus membros a proibir operações de aeronaves civis no espaço aéreo russo. A notícia também informa que a OACI não pode impor regras diretamente aos países membros. Portanto, **pedido diplomático**, **avaliação de risco** e **restrição implementada por um Estado** são etapas diferentes. A ICAO ressalta que Estados devem avaliar riscos e fornecer informações aeronáuticas oportunas aos operadores. [N3](https://www.cnnbrasil.com.br/internacional/aviacao-civil-ucrania-alerta-onu-sobre-inseguranca-do-espaco-aereo-russo/), [C1](https://www.icao.int/news/icao-statement-state-sovereignty-over-airspace-and-safety-assessments).

### Glossário

| Termo | Significado no estudo |
| --- | --- |
| Soberania do espaço aéreo | Autoridade completa e exclusiva de um Estado sobre o espaço aéreo acima de seu território. [C1](https://www.icao.int/news/icao-statement-state-sovereignty-over-airspace-and-safety-assessments) |
| Autoridade de aviação civil | Órgão público com funções de regulação ou supervisão do setor; a Rosaviatsiya é o caso observado. [N1](https://pt.wikipedia.org/wiki/Ag%C3%AAncia_Federal_de_Transporte_A%C3%A9reo) |
| Companhia aérea | Operadora de serviços de transporte aéreo; a Air Koryo é o caso observado. [N2](https://en.wikipedia.org/wiki/Air_Koryo) |
| OACI/ICAO | Organização da Aviação Civil Internacional, citada no pedido ucraniano e na explicação das regras internacionais. [N3](https://www.cnnbrasil.com.br/internacional/aviacao-civil-ucrania-alerta-onu-sobre-inseguranca-do-espaco-aereo-russo/), [C1](https://www.icao.int/news/icao-statement-state-sovereignty-over-airspace-and-safety-assessments) |
| Liberdades do ar | Direitos comerciais de sobrevoo, escala e transporte internacional. [C2](https://dataplus.icao.int/Home/FAQ) |
| Escala técnica | Parada sem embarque ou desembarque de tráfego comercial. [C2](https://dataplus.icao.int/Home/FAQ) |
| Restrição de espaço aéreo | Limitação de operações aéreas em área determinada por decisão da autoridade competente. [C1](https://www.icao.int/news/icao-statement-state-sovereignty-over-airspace-and-safety-assessments) |

### Prompts reutilizáveis para revisão

1. **Papéis:** “Classifique cada ator citado nas fontes como Estado, agência, companhia aérea ou organização internacional. Explique a função de cada um com citação.”
2. **Linha do tempo:** “Com N3, separe o que aconteceu, o que foi solicitado e o que ainda depende de decisão. Não transforme pedido em medida implementada.”
3. **Comparação:** “Compare N1 e N2: que tipo de decisão cabe a uma autoridade e que tipo de atividade cabe a uma companhia? Marque o que é inferência.”
4. **Revisão ativa:** “Faça uma pergunta por vez sobre soberania, liberdades do ar e segurança. Espere minha resposta; depois corrija com referência à fonte.”
5. **Auditoria da IA:** “Para cada afirmação factual da resposta anterior, indique documento e trecho. Se faltar apoio, escreva ‘não confirmado nas fontes’.”
