# Introduction

  Este projeto consiste em desenvolver uma solução para o problema de estimar tarifas para viagens de táxi em Nova Iorque, Estados Unidos, listado na plataforma Kaggle, sob o link   https://www.kaggle.com/c/new-york-city-taxi-fare-prediction/overview.
  
  
  This project consists in developing a solution for estimating cab fare prices in New York City. The link for the challenge can be found [here](https://www.kaggle.com/c/new-york-city-taxi-fare-prediction/overview).
  
  Our goal here is to create a model that can outperform the baseline solution proposed by Kaggle already (estimating the fare value based only on the distance between the pickup and dropoff locations)
  
  This project was made with Python, using *Pandas*, 

# Project approach

There are 4 main topics within this project:
1. **Análise exploratória de dados**, na qual buscamos entender a natureza dos dados presentes no dataset e tentamos traçar possíveis direções de análise para o nosso problema
2. **Formulação e validação de hipóteses**, nas quais, através do conhecimento advindo do cientista de dados ou de profissionais do ramo, junto com o conhecimento adquirido na exploração dos dados, geramos insights sobre o problema em questão e atestamos a veracidade/credibilidade de tais insights 
3. **Criação do modelo**, etapa na qual escolhemos o modelo que melhor se adequa às características dos dados e possua melhor balanço entre explicabilidade e performance, dentro das necessidades do problema
4. **Avaliação do modelo**, na qual comparamos o resultado obtido com o modelo base apresentado na introdução e avaliamos os resultados finais

## 1. Análise exploratória de dados

O primeiro ponto a ser notado ao observarmos o arquivo contendo o conjunto de dados é que o tamanho do mesmo é de aproximadamente 5.5 Gb. Este projeto está sendo realizado em um notebook que contém 8 Gb de memória RAM, o que torna inviável abrir os 5.5 Gb dados de uma só vez na memória do computador. Para computarmos as estatísticas e visualizações necessárias em nossa EDA (Análise exploratória de dados), precisamos de uma ferramenta que possibilite trabalharmos com o nosso dataset de maneira eficiente e que não estoure a memória do notebook. Entra em cena então a biblioteca *Dask* para Python. 

Através do *Dask*, podemos trabalhar com o nosso conjunto de dados de forma paralelizada e fazendo uso dos múltiplos processadores presentes no computador. Isso torna possível o processamento de datasets maiores do que a memória do notebook, processando-os em partes.
