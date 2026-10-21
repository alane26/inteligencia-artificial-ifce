 <div align="center">

# 🧠 Rede de Funções de Base Radial (RBF)

### Questão 11 · Inteligência Artificial

**Implementação e avaliação de uma rede neural RBF para classificação não linear**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

**IFCE — Campus Aracati**  
Bacharelado em Ciência da Computação

</div>

---

## 📌 Sobre o projeto

Este projeto apresenta o desenvolvimento de uma **Rede Neural de Funções de Base Radial (RBF)** para solucionar um problema de classificação não linear.

O experimento utiliza um conjunto de dados sintético composto por duas classes distribuídas em círculos concêntricos: um disco interno e um anel externo.

A proposta é investigar a capacidade de aprendizado da rede RBF e comparar seus resultados com os de um modelo de **Regressão Logística**.

### 🎯 Objetivos

- Implementar uma rede RBF utilizando Python e NumPy.
- Aplicar o algoritmo *k-means* para determinar os centros das funções radiais.
- Investigar a influência da quantidade de centros e da largura das funções gaussianas.
- Avaliar a capacidade de generalização do modelo.
- Comparar o desempenho da RBF com a Regressão Logística.
- Visualizar as fronteiras de decisão obtidas.

---

## 🛠️ Tecnologias utilizadas

| Tecnologia | Aplicação |
|---|---|
| **Python** | Linguagem principal |
| **NumPy** | Operações matriciais e implementação da RBF |
| **Pandas** | Organização dos resultados |
| **Matplotlib** | Visualização dos dados e gráficos |
| **Scikit-learn** | Pré-processamento e modelo comparativo |
| **Jupyter Notebook** | Desenvolvimento e documentação |

---

## ⚙️ Metodologia

O desenvolvimento foi dividido em cinco etapas principais.

### 01 — Preparação dos dados

Foi gerado um conjunto de **200 amostras sintéticas**, distribuídas entre duas classes não linearmente separáveis.

Os dados foram divididos em:

- **70%** para treinamento;
- **30%** para teste.

Também foi aplicada a padronização das características de entrada.

### 02 — Implementação do K-Means

O algoritmo *k-means* foi implementado utilizando NumPy para identificar os centros das funções de base radial.

Foram testadas configurações com:

`5 centros` · `10 centros` · `20 centros` · `40 centros`

### 03 — Construção da rede RBF

A rede utiliza funções gaussianas para transformar os dados de entrada em uma representação não linear.

A função de ativação é definida por:

$$
\phi_j(x) = \exp\left(-\frac{\|x-c_j\|^2}{2\sigma^2}\right)
$$

Em que:

- **x:** vetor de entrada;
- **cⱼ:** centro da função radial;
- **σ:** parâmetro de largura da função gaussiana.

Os pesos da camada de saída são calculados por meio da pseudoinversa.

### 04 — Avaliação experimental

Foram realizados experimentos variando o número de centros e os parâmetros de largura das funções gaussianas.

A avaliação considera a acurácia de classificação no conjunto de teste.

### 05 — Comparação dos modelos

Foi utilizado um modelo de Regressão Logística como referência para comparar o desempenho em um problema não linear.

Também foram geradas visualizações das fronteiras de decisão.

---

## 📊 Resultados

Os experimentos demonstraram diferenças significativas no desempenho dos modelos.

| Modelo | Acurácia no teste |
|:---|:---:|
| Regressão Logística | **45,00%** |
| Rede RBF — 20 centros | **100,00%** |

**Configuração:** largura heurística e semente aleatória `42`.

### 🔎 Análise

A Regressão Logística apresentou dificuldades para distinguir as duas classes, devido à natureza não linear dos dados.

Por outro lado, a rede RBF conseguiu representar adequadamente a distribuição espacial das amostras, alcançando 100% de acurácia no conjunto de teste utilizado.

> **Observação:** os resultados correspondem à execução documentada no notebook e podem variar conforme as configurações experimentais.

---

## 🚀 Como executar

### 1. Abrir o notebook

Acesse o arquivo:

`Questao_11_RBF_Alane_Damasceno_Moreno.ipynb`

O projeto pode ser executado no **Google Colab** ou localmente utilizando Jupyter Notebook.

### 2. Instalar as dependências

```bash
pip install numpy pandas matplotlib scikit-learn notebook
```

### 3. Executar o experimento

Execute as células do notebook na ordem apresentada para reproduzir:

- A geração e preparação dos dados;
- O treinamento dos modelos;
- Os testes com diferentes configurações;
- A avaliação das métricas;
- Os gráficos e as fronteiras de decisão.

---

## 💡 Conclusão

A atividade demonstrou a eficiência das **Redes de Funções de Base Radial** na resolução de problemas de classificação não linear.

Os experimentos evidenciaram que a escolha dos centros e do parâmetro de largura das funções gaussianas influencia diretamente o comportamento da rede.

A comparação com a Regressão Logística também destacou a importância de representações não lineares para problemas em que as classes não podem ser separadas por uma fronteira linear.

---

<div align="center">

### 👩‍💻 Autoria

**Alane Damasceno Moreno**

Bacharelado em Ciência da Computação  
Instituto Federal de Educação, Ciência e Tecnologia do Ceará  
**IFCE — Campus Aracati**

*Disciplina de Inteligência Artificial · 2026*

</div>
