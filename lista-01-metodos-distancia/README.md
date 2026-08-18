# 📏 Lista 01 — Métodos Baseados em Distância

Implementação prática dos métodos **k-Nearest Neighbors (k-NN)**, **k-Means** e **DBSCAN** utilizando **PyTorch** e a base de dados **Iris**.

A atividade tem como objetivo implementar os três métodos do zero, utilizando operações do PyTorch para compreender o funcionamento dos algoritmos e analisar seus comportamentos em problemas de classificação e agrupamento.

## 📊 Base de dados

Foi utilizada a base pública **Iris**, composta por:

* **150 amostras**;
* **4 atributos**;
* **3 espécies**: setosa, versicolor e virginica.

Para os experimentos foram utilizados apenas dois atributos:

* comprimento da pétala;
* largura da pétala.

Os dados foram padronizados utilizando **z-score** antes da aplicação dos métodos baseados em distância.

---

## 🔎 Exercício 1 — k-Nearest Neighbors (k-NN)

Implementação de um classificador **k-NN** utilizando PyTorch.

### Implementações

* divisão da base em **80% treino e 20% teste**;
* embaralhamento utilizando `torch.manual_seed(42)`;
* cálculo das distâncias euclidianas com `torch.cdist`;
* seleção dos vizinhos mais próximos com `torch.topk`;
* classificação pela classe mais frequente;
* cálculo da acurácia;
* comparação entre `k = 1, 3, 5, 7 e 9`.

### Desafio

Também foi construída uma **região de decisão em 2D**, permitindo visualizar as fronteiras criadas pelo k-NN entre as três espécies da Iris.

---

## 🎯 Exercício 2 — k-Means

Implementação do algoritmo de agrupamento **k-Means** utilizando somente os atributos das amostras, sem utilizar seus rótulos durante o processo.

### Implementações

* inicialização dos centroides com `torch.randperm`;
* cálculo das distâncias com `torch.cdist`;
* atribuição ao centroide mais próximo;
* atualização dos centroides pela média dos grupos;
* tratamento de clusters vazios;
* critério de convergência;
* máximo de **100 iterações**;
* cálculo da **inércia**.

### Desafios

Foram realizadas também:

* visualização da evolução da inércia;
* aplicação do **método do cotovelo** para `k = 1, 2, 3, 4 e 5`;
* associação posterior dos clusters às espécies;
* cálculo de uma acurácia ajustada para análise do agrupamento;
* comparação com o resultado obtido pelo k-NN.

---

## 🔵 Exercício 3 — DBSCAN

Implementação do algoritmo de agrupamento baseado em densidade **DBSCAN**.

### Implementações

* matriz de distâncias entre todas as amostras;
* construção da vizinhança a partir de `eps`;
* identificação dos **pontos núcleo**;
* expansão dos clusters;
* identificação de **pontos de borda**;
* identificação de **ruídos**.

A configuração principal utilizada foi:

```python
eps = 0.5
min_pts = 8
```

### Desafio

Para analisar a sensibilidade do algoritmo, o DBSCAN também foi executado com:

```python
eps = [0.2, 0.5, 0.8, 1.0]
```

mantendo:

```python
min_pts = 8
```

Os resultados permitem observar como o tamanho da vizinhança influencia a quantidade de clusters e de pontos classificados como ruído.

---

## 📈 Comparação final

Ao final da atividade, os três métodos são comparados considerando suas características e os resultados obtidos na base Iris.

| Método      | Tipo               | Principal característica                                  |
| ----------- | ------------------ | --------------------------------------------------------- |
| **k-NN**    | Supervisionado     | Classifica novas amostras a partir dos vizinhos rotulados |
| **k-Means** | Não supervisionado | Agrupa os dados em torno de centroides                    |
| **DBSCAN**  | Não supervisionado | Forma grupos por densidade e identifica ruídos            |

A análise final também discute:

* qual técnica apresentou melhor separação das três espécies;
* se o k-Means superou ou não o k-NN;
* em quais situações o DBSCAN pode ser mais adequado que o k-Means.

---

## 🛠️ Tecnologias utilizadas

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python\&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch\&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy\&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas\&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab\&logoColor=white)

## 📂 Arquivo

```text
lista-01-metodos-distancia/
│
├── README.md
├── lista_01_knn_kmeans_dbscan.ipynb
└── lista_exercicios_01.pdf
```

O notebook contém as implementações, execuções, tabelas, visualizações e análises desenvolvidas durante a atividade.

---

### 👩‍💻 Autoria

**Alane Damasceno Moreno**
Bacharelado em Ciência da Computação
IFCE — Campus Aracati
