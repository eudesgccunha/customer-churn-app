# Customer Churn App

Dataset da IBM com dados fictícios de uma companhia telefônica chamada [Telco](https://www.kaggle.com/datasets/blastchar/telco-customer-churn).

O case envolve seguir as etapas do processo CRISP-DM de mineração de dados para construir o modelo preditivo. Em seguida, o modelo será disponibilizado em um aplicativo Streamlit para prever novos clientes.

## Etapas do Case

As etapas propostas para resolução do case são:

1. Criar um arquivo requirements.txt com as bibliotecas Python necessárias
2. Criar um ambiente virtual para isolamento das dependências
3. Desenvolver o modelo seguindo as etapas do CRISP-DM
4. Criar um app Streamlit para prever novos clientes

## Desenvolvimento do Modelo

Nesta etapa vamos seguir o processo CRISP-DM para desenvolver nosso modelo preditivo de churn.

### Entendimento do Negócio

Primeiro, precisamos entender bem o problema de negócio que estamos tentando resolver. Neste caso, o objetivo é identificar clientes com maior probabilidade de cancelar o serviço, para que a companhia telefônica possa oferecer promoções e reter essas pessoas.

Isso pode gerar grande economia de custos para a empresa. Portanto, nosso modelo precisa ser preciso o suficiente para trazer valor real ao negócio.

### Entendimento dos Dados

O conjunto de dados fornecido contém 7043 linhas (clientes) e 21 colunas (variáveis ou atributos) sobre cada cliente.

As variáveis incluem informações demográficas (gênero, idade, região, etc), serviços utilizados (internet, segurança online, backups), dados de pagamentos e suporte.

A variável-alvo que queremos prever é a coluna “Churn”, que indica se o cliente cancelou (1) ou não (0) o serviço.

### Preparação dos Dados

Realizamos algumas transformações nos dados para prepará-los para o modelo de machine learning:

* Converter valores ausentes para NaN
* Substituir NaN por média, mediana ou valor mais frequente
* Codificar variáveis categóricas como valores numéricos
* Normalizar os dados para uma escala comum
* Dividir o conjunto entre treino (80%) e teste (20%)

Esse pré-processamento é essencial para garantir a qualidade dos dados que alimentam o modelo.



---
### Ambientes virtuais

#### Criar e ativar ambiente virtual do windows (venv)

```venv
python -m venv customer_churn
source customer_churn/bin/activate
pip install -r requirements.txt
```

#### Criar e ativar ambiente virtual conda

```bash
conda create -n customer_churn python==3.12.4
conda activate customer_churn
pip install -r requirements.txt
```