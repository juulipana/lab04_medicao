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

## Objetivo

O objetivo geral deste estudo é **realizar uma análise empírica em larga escala sobre Dívida Técnica Auto-Admitida (SATD)** em notebooks de competições do **Kaggle**, buscando entender suas **características, causas e impactos nas práticas de desenvolvimento de Machine Learning**.

Para isso, seguimos a definição de SATD proposta por **Potdar e Shihab (2014)** para identificar ocorrências de dívida técnica em comentários de código e aplicamos a **taxonomia de nove categorias de O’Brien et al. (2022)**, apresentada no estudo *“23 Shades of Self-Admitted Technical Debt: An Empirical Study on Machine Learning Software”*.

---

### Perguntas de Pesquisa (RQs)

| **ID**  | **Pergunta de Pesquisa**                                                                                                                                |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **RQ1** | Quais são as categorias mais frequentes e prevalentes de Dívida Técnica Auto-Admitida (SATD) em notebooks de competições de Machine Learning no Kaggle? |
| **RQ2** | Como a prevalência e o tipo de SATD se correlacionam com métricas de sucesso (medalhas) e visibilidade (upvotes) dos notebooks?                         |
| **RQ3** | Como a distribuição das categorias de SATD varia entre os diferentes domínios de competição (ex: Tabular, NLP e Visão Computacional)?                   |

---

### Métricas e Análise de Dados

| **RQ**  | **Métrica** | **Descrição**                                                                                               |
| ------- | ----------- | ----------------------------------------------------------------------------------------------------------- |
| **RQ1** | **M1.1**    | Distribuição relativa de cada categoria de SATD em todos os notebooks.                                      |
|         | **M1.2**    | Densidade geral de SATD por notebook (número de ocorrências de SATD normalizado pelo total de comentários). |
| **RQ2** | **M2.1**    | Correlação entre densidade/tipo de SATD e posição no *leaderboard*.                                         |
|         | **M2.2**    | Correlação entre densidade/tipo de SATD e obtenção de medalhas (Ouro, Prata, Bronze).                       |
|         | **M2.3**    | Correlação entre densidade/tipo de SATD e métricas de visibilidade (número de upvotes).                     |
| **RQ3** | **M3.1**    | Comparação da densidade média de SATD entre os domínios (Tabular, NLP e Visão Computacional).               |
|         | **M3.2**    | Distribuição percentual das categorias de SATD em cada domínio.                                             |
|         | **M3.3**    | Análise comparativa de padrões de SATD característicos de cada tipo de tarefa ou modalidade de dados.       |

---

## Tipos de Dívida Técnica Auto-Admitida (SATD)

Com base na taxonomia apresentada no estudo **“23 Shades of Self-Admitted Technical Debt: An Empirical Study on Machine Learning Software” (O’Brien et al., 2022)**, esta pesquisa adota uma classificação específica para sistemas de *Machine Learning*.
Os autores analisaram mais de **2.600 repositórios** e identificaram **23 tipos distintos de SATD**, organizados em **nove grandes categorias**, que representam as principais dimensões da dívida técnica em software de aprendizado de máquina.

Abaixo estão as nove categorias consideradas neste estudo:

| **Categoria**                     | **Descrição**                                                                   |
| --------------------------------- | ------------------------------------------------------------------------------- |
| **1. Data Dependency**            | Dívidas relacionadas ao processamento, armazenamento e configuração de dados.   |
| **2. Code Dependency**            | Dívidas causadas por dependências externas, como bibliotecas ou módulos.        |
| **3. Awareness**                  | Lacunas de conhecimento ou incertezas sobre algoritmos e decisões de design.    |
| **4. Modularity**                 | Falta de separação entre componentes ou ausência de abstrações no código de ML. |
| **5. Configurable Options**       | Configurações incompletas ou rígidas de hiperparâmetros e modelos.              |
| **6. Scalability**                | Dívidas associadas a código experimental, protótipos ou não otimizados.         |
| **7. Readability**                | Problemas de clareza e manutenção do código.                                    |
| **8. Performance**                | Implementações ineficientes que afetam o tempo de execução e o uso de recursos. |
| **9. Duplicate Code Elimination** | Códigos redundantes ou repetidos que precisam de refatoração.                   |

Essa taxonomia é um grande passo para **contextualizar a SATD no cenário do aprendizado de máquina**, permitindo analisar não só dívidas tradicionais de software, mas também **novos tipos de dívida** que emergem do uso de dados, modelos e experimentos.
Por sua relevância e estrutura hierárquica, ela serve como **base para a categorização adotada nesta pesquisa**.

---

## Metodologia 

<img width="688" height="230" alt="image" src="https://github.com/user-attachments/assets/f4bec7bd-3198-4cb7-a644-666ccd0e93a9" />

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

## Conclusão Parcial

Os dados coletados nos mostram que as dívidas técnicas mais comuns nos notebooks do Kaggle estão ligadas a **Data Dependency** e **Awareness**, ou seja, problemas com os dados e anotações de melhorias futuras. Também aparecem bastante **Readability** e **Performance**. Já itens como **Scalability** e **Duplicate Code Elimination** quase não aparecem, mostrando que esses pontos são menos lembrados pelos autores.

---
