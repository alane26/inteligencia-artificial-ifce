# 🤖 Inteligência Artificial

Repositório destinado à organização das **atividades, listas de exercícios, trabalhos e projetos** desenvolvidos durante a disciplina de **Inteligência Artificial** do curso de **Bacharelado em Ciência da Computação — IFCE Campus Aracati**.

## 📚 Sobre a disciplina

Ao longo da disciplina, este repositório será utilizado para registrar implementações práticas, experimentos e estudos relacionados aos principais conceitos e técnicas de Inteligência Artificial.

Os códigos são desenvolvidos principalmente em **Python**, utilizando ferramentas como **NumPy**, **PyTorch**, **Pandas**, **Matplotlib**, **scikit-learn**, **Jupyter Notebook** e **Google Colab**.

---

## 🗂️ Atividades

| Atividade | Conteúdo | Status |
| --- | --- | :---: |
| [Lista 01](./lista-01-metodos-distancia/) | Métodos baseados em distância — k-NN, k-Means e DBSCAN | ✅ |
| [Lista 02](./lista-02-regressao/) | Regressão Linear — Equação Normal, MSE e RMSE | ✅ |
| [Lista 03](./lista-03-perceptron/) | Perceptron de Rosenblatt — OR, AND, XOR e Iris | ✅ |
| [Lista 04](./lista-04/) | Próxima atividade | ⏳ |

---

## 📌 Lista 01 — Métodos Baseados em Distância

A primeira lista aborda a implementação e análise de três algoritmos baseados em distância utilizando a base de dados **Iris**.

### 🔎 k-Nearest Neighbors (k-NN)

- cálculo da distância euclidiana;
- classificação pelos vizinhos mais próximos;
- comparação de diferentes valores de `k`;
- cálculo de acurácia;
- visualização da região de decisão.

### 🎯 k-Means

- inicialização e atualização dos centroides;
- atribuição dos clusters;
- análise da convergência;
- cálculo da inércia;
- método do cotovelo;
- comparação com as classes reais.

### 🔵 DBSCAN

- construção da vizinhança;
- identificação de pontos núcleo, borda e ruído;
- expansão dos clusters;
- análise da influência do parâmetro `eps`.

📂 **[Acessar Lista 01](./lista-01-metodos-distancia/)**

---

## 📌 Lista 02 — Regressão Linear com NumPy e PyTorch

A segunda lista aborda a implementação de uma **Regressão Linear utilizando a Equação Normal**, além da implementação e análise das métricas **MSE** e **RMSE**.

Para os experimentos foi utilizada a base pública **Auto MPG**, com o objetivo de prever o consumo de combustível dos automóveis.

### 🧮 Equação Normal

- divisão dos dados em treino e teste;
- tratamento dos valores ausentes;
- padronização das features utilizando z-score;
- criação da matriz de design;
- inclusão do intercepto;
- implementação da Equação Normal com NumPy;
- utilização de `np.linalg.solve`;
- comparação com a solução utilizando a matriz inversa;
- análise dos pesos da regressão.

### 📐 MSE e RMSE

- implementação manual do MSE;
- implementação manual do RMSE;
- avaliação nos conjuntos de treino e teste;
- reprodução dos cálculos utilizando tensores do PyTorch;
- comparação entre NumPy e PyTorch;
- conferência dos resultados utilizando scikit-learn.

### 🔬 Experimentos

- regressão com e sem padronização;
- comparação dos pesos encontrados;
- identificação da feature mais influente;
- previsão de uma amostra concreta;
- comparação do erro individual com o RMSE;
- análise do efeito de aumentar uma feature em um desvio-padrão.

📂 **[Acessar Lista 02](./lista-02-regressao/)**

---

## 📌 Lista 03 — Implementando o Perceptron

A terceira lista aborda a implementação **do zero, em NumPy**, do **Perceptron de Rosenblatt**, explorando sua regra de aprendizado e sua relação com problemas linearmente separáveis.

### 🟠 OR e AND

- implementação manual do algoritmo;
- função de ativação degrau;
- atualização dos pesos e do bias;
- registro dos erros por época;
- análise da convergência;
- construção das fronteiras de decisão;
- comparação entre OR e AND.

### ❌ XOR

- treinamento durante 50 épocas;
- experimento com 1000 épocas;
- análise da acurácia;
- observação da oscilação dos erros;
- estudo da não separabilidade linear;
- relação com o Teorema de Convergência do Perceptron.

### 🌸 Iris

- classificação entre setosa e versicolor;
- utilização do comprimento e largura da pétala;
- visualização das classes;
- treinamento com o Perceptron implementado manualmente;
- análise dos pesos e bias;
- acurácia final;
- construção da fronteira de decisão.

A atividade também relaciona as limitações de um único Perceptron à necessidade de modelos mais complexos, como **Redes Neurais Multicamadas (MLP)**.

📂 **[Acessar Lista 03](./lista-03-perceptron/)**

---

## 📌 Lista 04 — Próxima atividade

A pasta da próxima atividade já está preparada e será atualizada conforme o desenvolvimento da disciplina.

📂 **[Acessar Lista 04](./lista-04/)**

---

## 🛠️ Tecnologias

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

---

## 📁 Estrutura do repositório

```text
inteligencia-artificial-ifce/
│
├── lista-01-metodos-distancia/
│   ├── README.md
│   ├── Lista_Exercicios_01_IA_Alane_Damasceno.ipynb
│   └── lista_exercicios_01.pdf
│
├── lista-02-regressao/
│   ├── README.md
│   ├── Lista_Exercicios_02_IA_Alane_Damasceno.ipynb
│   └── lista02_regressao_numpy_torch.pdf
│
├── lista-03-perceptron/
│   ├── README.md
│   ├── Lista_Perceptron_IA_Alane_Damasceno.ipynb
│   └── lista_perceptron.pdf
│
├── lista-04/
│   └── README.md
│
├── trabalhos/
│
├── projetos/
│
└── README.md
```

A estrutura será atualizada ao longo da disciplina conforme novas listas, trabalhos e projetos forem desenvolvidos.

---

## 📈 Progresso

- [x] Lista 01 — Métodos Baseados em Distância
- [x] Lista 02 — Regressão Linear com NumPy e PyTorch
- [x] Lista 03 — Implementando o Perceptron
- [ ] Lista 04 — Próxima atividade
- [ ] Próximas atividades
- [ ] Trabalhos
- [ ] Projetos

---

### 👩‍💻 Autoria

**Alane Damasceno Moreno**  
Bacharelado em Ciência da Computação  
**IFCE — Campus Aracati**