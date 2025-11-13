# Visualização de Dados Utilizando uma Ferramenta de BI

Este laboratório é dedicado ao estudo e uso de **ferramentas de Business Intelligence (BI)** para apresentar os resultados obtidos em nossa pesquisa **“Self-Admitted Technical Debt Analysis in Competition Notebooks on Kaggle”**, que tem como objetivo realizar uma **análise empírica em larga escala sobre SATD** (*Self-Admitted Technical Debt* — Dívida Técnica Autoassumida) especificamente em **Notebooks de competições do Kaggle**.

---

## Índice 

1. [Introdução](#introdução)
2. [Objetivos](#objetivos)
   2.1. [Perguntas de Pesquisa (RQs)](#perguntas-de-pesquisa-rqs)
   2.2. [Métricas de Análise](#métricas-de-análise)
3. [Contexto do Kaggle](#contexto-do-kaggle)
4. [Metodologia](#metodologia)
   4.1. [Coleta de Dados](#1-coleta-de-dados)
   4.2. [Identificação de SATD](#2-identificação-de-satd)
   4.3. [Classificação de SATD](#3-classificação-de-satd)
   4.4. [Métricas e Análise de Dados](#4-métricas-e-análise-de-dados)
5. [Conclusões](#conclusões)

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

Realizar uma análise empírica sobre a Dívida Técnica Auto-Admitida (SATD) em sistemas de Machine Learning, através da classificação manual em larga escala de comentários de código de notebooks do Kaggle, a fim de criar uma taxonomia de seus tipos, localização e causas.

---

### Perguntas de Pesquisa (RQs)

| **ID** | **Pergunta de Pesquisa** |
|--------|---------------------------|
| **RQ1** | Quais são as categorias mais prevalentes de SATD em notebooks de competição de ML no Kaggle? |
| **RQ2** | Como a prevalência e o tipo de SATD se correlacionam com as métricas de sucesso (prêmios) e visibilidade (upvotes) de um notebook? |
| **RQ3** | Como a distribuição das categorias de SATD varia entre os diferentes domínios de competição (ex: Tabular, NLP, Visão Computacional)? |
| **RQ4** | Em que medida o domínio da competição modera a relação entre a SATD e o sucesso do notebook? |

---

###  Métricas de Análise

| **RQ** | **Métrica** | **Descrição** |
|--------|--------------|----------------|
| **RQ1** | **M1.1** | Distribuição percentual das categorias de SATD (ex: Dívida de Código, Dívida de Teste, Dívida de Modelo). |
|  | **M1.2** | Densidade de SATD por categoria (instâncias de SATD por notebook). |
| **RQ2** | **M2.1** | Densidade de SATD em relação à classificação na competição e quantidade de upvotes. |
|  | **M2.2** | Correlação entre quantidade/tipo de SATD e medalhas (Ouro, Prata, Bronze). |
|  | **M2.3** | Correlação entre quantidade/tipo de SATD e número de votos ("upvotes"). |
| **RQ3** | **M3.1** | Densidade média de SATD por domínio (Tabular, NLP, CV). |
|  | **M3.2** | Comparação percentual das categorias de SATD entre domínios. |
|  | **M3.3** | Densidade média de SATD por notebook dentro de cada domínio. |
| **RQ4** | **M4.1** | Análise de moderação do domínio na relação entre tipo/quantidade de SATD e medalhas. |
|  | **M4.2** | Análise de moderação do domínio na relação entre tipo/quantidade de SATD e número de votos. |

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

## Conclusões
<!-- TO-DO: Inserir observações, padrões encontrados e sugestões para trabalhos futuros -->

---
