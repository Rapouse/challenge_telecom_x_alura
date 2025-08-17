# 📊 Análise de Evasão de Clientes (Churn) - Telecom X

## 1. Propósito da Análise

Este projeto realiza uma análise exploratória sobre uma base de dados da empresa fictícia Telecom X, que enfrenta uma alta taxa de evasão de clientes (churn). O objetivo principal é identificar, através de um processo de ETL (Extração, Transformação e Carga) e EDA (Análise Exploratória de Dados), os fatores e o perfil dos clientes com maior propensão a cancelar o serviço.

Os insights gerados servem como base para a tomada de decisões estratégicas e para o desenvolvimento de modelos preditivos focados em retenção.

## 2. Estrutura do Projeto

O repositório está organizado da seguinte forma:

- `TelecomX_Data.json`: Arquivo com os dados brutos dos clientes.
- `TelecomX_dicionario.md`: Dicionário que descreve cada coluna do dataset.
- `TelecomX_Churn_ETL_Analise.ipynb`: Notebook Jupyter contendo todo o processo de análise, desde a extração e limpeza dos dados até a visualização e conclusões.
- `README.md`: Este arquivo, com a documentação do projeto.

## 3. Principais Insights e Visualizações

A análise revelou uma taxa de churn de **26.5%**. O perfil do cliente com maior risco de evasão foi claramente identificado a partir dos seguintes padrões:

- **Contrato:** Clientes com contrato **mensal** são significativamente mais propensos a cancelar.
- **Tempo de Contrato:** A evasão é muito mais concentrada em **clientes novos**, com poucos meses de serviço.
- **Gasto Mensal:** Faturas com **valores mensais mais altos** apresentam maior risco de churn.

**Conclusão Central:** O cliente de maior risco é **recente, possui contrato mensal e um gasto mensal elevado**. Serviços como Fibra Ótica e métodos de pagamento como Cheque Eletrônico também são fatores de atenção.

## 4. Como Executar o Projeto

### Pré-requisitos

- As seguintes bibliotecas Python:
  - `pandas`
  - `seaborn`
  - `matplotlib`

### Como Executar o Notebook

- Abra [colab.research.google.com.](https://colab.google/)
- Clique em "Arquivo" → "Fazer upload do notebook".
- Carregue o arquivo TelecomX_Churn_ETL_Analise.ipynb.
- Carregue o arquivo TelecomX_Data.json.
- Execute as células na ordem apresentada.
