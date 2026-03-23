# Projeto BI - Análise IMDB Movies

Este repositório contém o desenvolvimento de um projeto de Business Intelligence focado no dataset de filmes do IMDB. O objetivo é demonstrar o fluxo completo de dados, desde a extração e tratamento (ETL) até a visualização final.

---

## Descrição do Projeto
O projeto utiliza dados do IMDB para realizar análises de performance cinematográfica, financeira e crítica. O fluxo de trabalho seguiu as seguintes etapas:
* **Extração:** Carga de arquivo CSV para o Power BI.
* **ETL (Power Query):** Limpeza de nulos, remoção de duplicatas por ID, tradução de cabeçalhos via linguagem M e normalização de textos.
* **Modelagem & DAX:** Criação de colunas calculadas e medidas de performance financeira e de crítica.
* **Versionamento:** Uso de formato `.pbip` para controle de versão via Git.

---

## Perguntas de Negócio
Para orientar a análise, foram definidas as seguintes perguntas:
1. **Pergunta 1:** Existe uma correlação direta entre o investimento (budget) e a margem de lucro nos títulos de maior arrecadação?
2. **Pergunta 2:** Quais são os diretores que conseguem manter o melhor desempenho de engajamento (votos/avaliações) no IMDB dentro do volume total de filmes?

---

## Transformações Relevantes (Linguagem M)
Algumas das transformações avançadas realizadas no Power Query incluíram:
* **Conversão de Duração:** Transformação de textos como "1h 38m" em minutos totais (inteiro).
* **Lógica de Metragem:** Classificação automática entre "Curta metragem" (<= 65 min) e "Longa metragem".
* **Tradução em Massa:** Renomeação de colunas em lote utilizando a barra de fórmulas M.

---

## Medidas DAX Principais
O relatório utiliza as seguintes métricas fundamentais:
* **Quantidade de Filmes:** `COUNTROWS` do dataset.
* **Média IMDB (Século XXI):** Média de notas para filmes lançados a partir do ano 2000
