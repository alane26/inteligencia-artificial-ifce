# 📈 Lista 02 — Regressão Linear com NumPy e PyTorch

Implementação prática de **Regressão Linear** utilizando **NumPy** e **PyTorch**, com foco na aplicação da **Equação Normal** e na avaliação do modelo por meio das métricas **MSE** e **RMSE**.

A atividade tem como objetivo compreender, na prática, o funcionamento da regressão linear e comparar diferentes formas de realizar os cálculos, implementando as principais etapas manualmente.

---

## 📊 Base de dados

Foi utilizada a base pública **Auto MPG**, disponibilizada pelo **UCI Machine Learning Repository**.

O objetivo do problema é prever o consumo de combustível dos automóveis, representado pela variável:

- `mpg` — *miles per gallon*.

### Features utilizadas

Foram selecionadas seis características numéricas:

- `cylinders`;
- `displacement`;
- `horsepower`;
- `weight`;
- `acceleration`;
- `model_year`.

Antes do treinamento, os valores ausentes foram removidos e os dados foram preparados para utilização no modelo.

---

## 🧮 Exercício 1 — Equação Normal com NumPy

A primeira etapa consiste na implementação de uma regressão linear utilizando a solução fechada da **Equação Normal**:

\[
w^* = (X^TX)^{-1}X^Ty
\]

### Implementações

- separação das features `X` e do alvo `y`;
- divisão dos dados em **80% treino e 20% teste**;
- padronização das features utilizando **z-score**;
- cálculo da média e do desvio-padrão somente no conjunto de treino;
- construção da matriz de design;
- inclusão de uma coluna de `1`s para representar o intercepto;
- implementação manual da Equação Normal;
- comparação entre `np.linalg.inv` e `np.linalg.solve`;
- cálculo dos pesos da regressão;
- geração das previsões de treino e teste;
- comparação entre valores reais e previstos.

### 🔎 Análise dos pesos

Os coeficientes encontrados pelo modelo também foram analisados para identificar a **feature com maior peso em módulo**.

Como as características foram padronizadas, os coeficientes podem ser utilizados para analisar a influência relativa de cada variável sobre o consumo previsto.

---

## 📐 Exercício 2 — MSE e RMSE

Nesta etapa foram implementadas manualmente duas métricas utilizadas na avaliação de problemas de regressão.

### MSE — Mean Squared Error

\[
MSE = \frac{1}{n}\sum_{i=1}^{n}(y_i-\hat{y}_i)^2
\]

O MSE calcula a média dos erros elevados ao quadrado.

### RMSE — Root Mean Squared Error

\[
RMSE = \sqrt{MSE}
\]

O RMSE retorna o erro para a mesma unidade da variável alvo, tornando sua interpretação mais intuitiva.

### Implementações

- MSE manual com NumPy;
- RMSE manual com NumPy;
- avaliação no conjunto de treino;
- avaliação no conjunto de teste;
- conversão dos dados para tensores;
- reprodução das previsões utilizando PyTorch;
- cálculo manual do MSE com PyTorch;
- cálculo manual do RMSE com PyTorch;
- comparação entre NumPy e PyTorch.

---

## 🔍 Conferência com scikit-learn

Após a implementação manual, o modelo também foi comparado com o `LinearRegression` do **scikit-learn**.

O scikit-learn foi utilizado somente como forma de **conferência dos resultados**, não para realizar a implementação principal da atividade.

Foram comparados os resultados obtidos com:

- NumPy;
- PyTorch;
- scikit-learn.

As diferenças numéricas entre as implementações também foram analisadas.

---

## 🔬 Experimento com e sem padronização

Como parte dos desafios da atividade, a regressão também foi executada utilizando as features **sem padronização**.

Foram comparados:

- MSE de treino;
- RMSE de treino;
- MSE de teste;
- RMSE de teste;
- pesos encontrados pelo modelo.

O experimento permite observar principalmente o impacto da escala das variáveis sobre a magnitude e a interpretação dos coeficientes da regressão.

---

## 🚗 Exercício 3 — Previsão concreta

Uma amostra do conjunto de teste foi utilizada para realizar uma previsão completa.

O processo inclui:

- recuperação dos valores originais da amostra;
- aplicação da mesma padronização utilizada no treinamento;
- adição do intercepto;
- cálculo da previsão;
- comparação entre o valor real e o valor previsto;
- cálculo do erro absoluto;
- comparação do erro individual com o RMSE do conjunto de teste.

### 📈 Influência das features

Também foi realizado um experimento com a feature de maior peso.

A variável foi aumentada em **um desvio-padrão**, mantendo as demais características constantes, permitindo observar diretamente o impacto do coeficiente sobre a previsão realizada pelo modelo.

---

## 📊 Comparativo final

Ao final da atividade são discutidas três questões principais:

1. **MSE e RMSE apresentaram resultados semelhantes entre NumPy, PyTorch e scikit-learn?**
2. **Qual é a relação entre MSE e RMSE e como interpretar suas unidades?**
3. **Qual feature apresentou maior influência sobre o alvo e o sinal do seu peso faz sentido?**

Essas análises permitem relacionar os resultados numéricos obtidos com o funcionamento matemático da regressão linear.

---

## 🛠️ Tecnologias utilizadas

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

---

## 📂 Estrutura

```text
lista-02-regressao/
│
├── Lista_Exercicios_02_IA_Alane_Damasceno.ipynb
└── README.md
```

O notebook contém os códigos, execuções, resultados, comparações e análises desenvolvidas durante a atividade.

---

### 👩‍💻 Autoria

**Alane Damasceno Moreno**  
Bacharelado em Ciência da Computação  
IFCE — Campus Aracati
