Modelo Preditivo de vendas de sorvetes usando Machine Learning da Azure
# 🚀 Projeto de Previsão de Vendas de Sorvete (DIO e Microsoft)

Este projeto foi desenvolvido como parte do desafio "Construindo um Modelo Preditivo para Vendas de Sorvetes" da DIO. O objetivo é aplicar conceitos de Machine Learning para prever a quantidade de vendas de sorvetes com base na temperatura, utilizando Python e o ambiente do Azure Machine Learning Studio.

## 🍦 Cenário
A sorveteria fictícia "Gelato Mágico" precisa otimizar sua produção diária. A produção está fortemente correlacionada com a temperatura, e um modelo de previsão é necessário para evitar desperdícios e maximizar o lucro.

## 🛠️ Ferramentas Utilizadas
* **Linguagem:** Python
* **Bibliotecas Principais:** Scikit-learn, Pandas, Numpy, Matplotlib, Joblib
* **Ambiente:** Azure Machine Learning Studio (Notebooks)
* **(Opcional) MLOps:** MLflow (para registro de métricas)

## 📁 Estrutura do Repositório
* `/data/sorvetes.csv`: Base de dados fictícia gerada para o projeto (100 linhas).
* `/notebook/previsao_sorvetes.ipynb`: O notebook Jupyter contendo todo o processo (análise, treinamento e teste).
* `/model/model.pkl`: (Opcional) O artefato do modelo de Regressão Linear treinado.

## 📈 Processo e Resultados

O projeto foi dividido em três etapas principais executadas no Azure ML Notebook:

### 1. Geração e Análise de Dados
Foi criada uma base de dados fictícia (`sorvetes.csv`) simulando 100 dias de vendas. A análise exploratória confirmou uma forte correlação linear positiva entre a Temperatura e as Vendas.

![Gráfico de Dispersão](link_para_seu_print_do_grafico_da_celula_1.png)

### 2. Treinamento do Modelo
* Foi utilizado um **Pipeline** do Scikit-learn contendo um `LinearRegression()`.
* O modelo foi treinado e avaliado, alcançando os seguintes resultados:
    * **R² Score:** 0.XX (Coloque o R² da sua Célula 2 aqui)
    * **RMSE:** XX.XX (Coloque o RMSE da sua Célula 2 aqui)
* O modelo final foi salvo como `model.pkl` usando `joblib`.

### 3. Teste da Previsão
O modelo salvo foi carregado e testado com sucesso para simular uma previsão em tempo real, confirmando que está pronto para uso.

---
### ⚠️ Nota sobre o Deploy (Implantação)
O objetivo deste projeto era focar no treinamento e teste do modelo. A etapa de implantação (deploy) como um Ponto de Extremidade Online no Azure foi investigada, mas apresentou desafios de configuração de permissão na assinatura do Azure (`SubscriptionNotRegistered`), que são externos ao código do modelo. O foco foi mantido na entrega de um modelo funcional.
