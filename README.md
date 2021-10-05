# Introduction

  Este projeto consiste em desenvolver uma solução para o problema de estimar tarifas para viagens de táxi em Nova Iorque, Estados Unidos, listado na plataforma Kaggle, sob o link   https://www.kaggle.com/c/new-york-city-taxi-fare-prediction/overview.
  
  This project consists in developing a solution for estimating cab fare prices in New York City. The link for the challenge can be found [here](https://www.kaggle.com/c/new-york-city-taxi-fare-prediction/overview).
  
  Our goal here is to create a model that can outperform the baseline solution already proposed by Kaggle (estimating the fare value based only on the distance between the pickup and dropoff locations)

# Project approach

There are 4 main topics within this project:
1. **Exploratory Data Analysis**, when we try to understand the nature of the data that we have and try to make sense of the possible paths to solve our problem
2. **Hypothesis creation/testing**, when we, using our previoulsy professional knowledge and also studying more about the problem and its specific characteristics, come up with insights about the data and then evaluate if those insights make sense and are sustaneid when looking into the data
3. **Model creation**, when we create our first model (our simplest model) to see how it behaves
4. **Model perfomance evaluation**, when we compare the perfomance of our simplest model with Kaggle's baseline solution to see how we have performed and check if further tuning of the model is needed
5. **Model fine tuning**


<details>
<summary>Exploratory Data Analysis</summary>
  
  _The first thing we notice is that the main file with our data has almost 6 GB of disk space. I'm using a notebook with 8 GB of RAM, so it's no feasible to open the whole dataset at once in memory. Para computarmos as estatísticas e visualizações necessárias em nossa EDA (Análise exploratória de dados), precisamos de uma ferramenta que possibilite trabalharmos com o nosso dataset de maneira eficiente e que não estoure a memória do notebook. Entra em cena então a biblioteca *Dask* para Python. 

  Através do *Dask*, podemos trabalhar com o nosso conjunto de dados de forma paralelizada e fazendo uso dos múltiplos processadores presentes no computador. Isso torna possível o processamento de datasets maiores do que a memória do notebook, processando-os em partes.
</details>


