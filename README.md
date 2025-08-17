# 📊 Análise e Predição de Evasão de Clientes (Churn) - Telecom X

## 1. Visão Geral do Projeto

Este repositório documenta um projeto completo de análise de dados e machine learning para a empresa fictícia Telecom X. O projeto foi dividido em duas fases principais:

1.  **Análise Exploratória (Parte 1):** Investigação dos dados para entender os fatores e o perfil dos clientes que cancelam seus serviços (churn).
2.  **Modelagem Preditiva (Parte 2):** Construção e avaliação de modelos de machine learning para prever quais clientes têm maior probabilidade de evadir.

O objetivo final é transformar dados brutos em insights acionáveis e em uma ferramenta preditiva para apoiar as estratégias de retenção de clientes da empresa.

## 2. Estrutura do Repositório

O repositório está organizado da seguinte forma:

- `TelecomX_Data.json`: Arquivo com os dados brutos dos clientes.
- `TelecomX_dicionario.md`: Dicionário que descreve cada coluna do dataset.
- `dados_tratados_telecom.csv`: Arquivo com os dados limpos, gerado pela Parte 1 e utilizado como entrada para a Parte 2.
- `TelecomX_Churn_ETL_Analise.ipynb`: (Parte 1) Notebook com o processo de Extração, Transformação, Carga (ETL) e Análise Exploratória de Dados (EDA).
- `TelecomX_Churn_ETL_Analise_2.ipynb`: (Parte 2) Notebook com o pipeline de pré-processamento, treinamento e avaliação dos modelos de machine learning.
- `README.md`: Este arquivo de documentação.

## 3. Metodologia e Principais Resultados

### Parte 1: Análise Exploratória (EDA)

A análise inicial revelou uma **taxa de churn de 26.5%**. A investigação dos dados identificou um perfil claro para o cliente com maior risco de evasão:

- **Contrato:** Clientes com contrato **mensal**.
- **Tempo de Serviço:** Clientes **novos**, com poucos meses de contrato.
- **Fatura Mensal:** Clientes com **gastos mensais mais elevados**.

### Parte 2: Modelagem Preditiva (Machine Learning)

Utilizando os dados tratados, foram treinados dois modelos de classificação para prever o churn: **Random Forest** e **Regressão Logística**.

- **Pré-processamento:** As etapas incluíram a remoção de colunas irrelevantes, *one-hot encoding* para variáveis categóricas e normalização dos dados para a Regressão Logística.
- **Performance:** A **Regressão Logística** apresentou um desempenho superior, com uma **Acurácia de 80%** e um **Recall de 54%**, sendo este último a métrica mais crítica para o problema (capacidade de identificar os clientes que realmente vão cancelar).

A análise de importância das variáveis nos modelos confirmou os achados da EDA, destacando `Meses_Contrato` e `Contrato_Month-to-month` como os fatores de maior impacto na previsão.

## 4. Como Executar o Projeto

### Pré-requisitos

- Python 3.x
- Bibliotecas: `pandas`, `seaborn`, `matplotlib`, `scikit-learn`

### Instruções

O projeto foi desenhado para ser executado em duas etapas sequenciais:

1.  **Executar a Parte 1:**
    - Abra o notebook `TelecomX_Churn_ETL_Analise.ipynb`.
    - Certifique-se de que o arquivo `TelecomX_Data.json` está na mesma pasta.
    - Execute todas as células. Ao final, o arquivo `dados_tratados_telecom.csv` será gerado.

2.  **Executar a Parte 2:**
    - Abra o notebook `TelecomX_Churn_ETL_Analise_2.ipynb`.
    - Ele irá carregar automaticamente o arquivo `dados_tratados_telecom.csv`.
    - Execute todas as células para treinar e avaliar os modelos.

**Instalação das dependências via pip:**
```bash
pip install pandas seaborn matplotlib scikit-learn jupyterlab
