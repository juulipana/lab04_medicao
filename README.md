# Visualização de Dados Utilizando uma Ferramenta de BI

Este laboratório é dedicado ao estudo e uso de **ferramentas de Business Intelligence (BI)** para apresentar os resultados obtidos em nossa pesquisa **“Self-Admitted Technical Debt Analysis in Competition Notebooks on Kaggle”**, que tem como objetivo realizar uma **análise empírica em larga escala sobre SATD** (*Self-Admitted Technical Debt* — Dívida Técnica Autoassumida) especificamente em **Notebooks de competições do Kaggle**.

---

## Índice
1. [Introdução](#introdução)
2. [Objetivos](#objetivos)
3. [Contexto do Kaggle](#contexto-do-kaggle)
4. [Metodologia](#metodologia)
5. [Visualizações e Resultados](#visualizações-e-resultados)
6. [Conclusões](#conclusões)

---

## Introdução

**Dívida técnica** é o custo implícito associado à adoção de soluções rápidas, porém menos ideais, no desenvolvimento de software — em detrimento de abordagens mais robustas e sustentáveis a longo prazo.  
Esse conceito está intimamente ligado à manutenção, evolução e qualidade do código em projetos de software.

No contexto do **aprendizado de máquina (Machine Learning)**, a dívida técnica pode se manifestar em forma de:
- Código não documentado ou de difícil reuso;
- Modelos treinados com dados inconsistentes;
- Falta de padronização em pipelines;
- Comentários que admitem limitações ou soluções temporárias (*Self-Admitted Technical Debt* — SATD).

---

## Contexto do Kaggle

O **Kaggle** é uma comunidade online voltada para **cientistas de dados e engenheiros de aprendizado de máquina**.  
Ele oferece um ambiente colaborativo com diversas ferramentas, tais como:

- **Conjuntos de Dados (Datasets):** uma vasta coleção de dados públicos para uso em projetos e pesquisas;
- **Competições:** desafios organizados por empresas ou instituições, nos quais participantes competem para criar os melhores modelos de predição;
- **Notebooks (Kernels):** um ambiente interativo onde os usuários podem desenvolver, documentar e compartilhar suas análises e modelos;
- **Modelos (Models):** um repositório de modelos pré-treinados voltados para *machine learning* e *IA generativa*.

---

## Objetivos

- Realizar uma **análise empírica em larga escala** sobre a Dívida Técnica Autoassumida (SATD) em notebooks de competições do Kaggle.  
- Compreender **suas características, causas e impactos** nas práticas de desenvolvimento em Machine Learning.

---

## Metodologia 

### 1. Coleta de Dados
- Seleção de **3.600 notebooks de competições do Kaggle**.  
- Três domínios de Machine Learning:
  - **Tabular:** *Titanic*, *Santander Customer Transaction Prediction*  
  - **Computer Vision (CV):** *Digit Recognizer*, *Cassava Leaf Disease*, *HuBMAP – Kidney Segmentation*  
  - **NLP (Processamento de Linguagem Natural):** *Disaster Tweets*, *Jigsaw Toxicity*, *CommonLit Readability*  
- Amostra equilibrada com diferentes níveis de dificuldade e estilos de código.

---

### 2. Identificação de SATD
- Baseada na definição de **Potdar e Shihab (2014):** comentários que admitem soluções temporárias (ex: TODO, FIXME, HACK).  
- Processo híbrido:
  - **Extração automática** de comentários de código.  
  - **Filtragem por palavras-chave** e análise contextual com modelo de linguagem.  
  - **Validação manual** para remover falsos positivos.

---

### 3. Classificação de SATD
- Utilização de um **agente de IA (ChatGPT-4.0 mini)** para interpretar e classificar os comentários.  
- Divisão em **4 lotes JSON** (TODO, HACK, WORKAROUND, FIXME).  
- Classificação segundo as **9 categorias de SATD** definidas por **Bhatia et al. (2023)**.  
- Resultados registrados em **Google Sheets** para revisão e validação manual.

---

### 4. Métricas e Análise de Dados
Análise guiada por **3 Questões de Pesquisa (RQs):**

#### RQ1 — Frequência e Distribuição
- Percentual de cada categoria de SATD.  
- Densidade de SATD por notebook.

#### RQ2 — Correlação com Sucesso e Visibilidade
- Relação entre densidade de SATD e:
  - Posição no *leaderboard*  
  - Medalhas (Ouro, Prata, Bronze)  
  - Upvotes dos notebooks

#### RQ3 — Variação por Domínio
- Densidade média de SATD em Tabular, NLP e CV.  
- Comparação de categorias entre domínios.

---

## Visualizações e Resultados
<!-- TO-DO: Inserir gráficos, dashboards e análises visuais obtidas através da ferramenta de BI -->

---

## Conclusões
<!-- TO-DO: Inserir observações, padrões encontrados e sugestões para trabalhos futuros -->

---
