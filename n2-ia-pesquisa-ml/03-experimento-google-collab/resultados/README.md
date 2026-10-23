 <div align="center">

# 📊 Resultados Experimentais

### N2 — Inteligência Artificial

**Análise dos limiares de decisão na classificação de tumores mamários**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

**IFCE — Campus Aracati**  
Bacharelado em Ciência da Computação · Inteligência Artificial

</div>

---

## 📌 Sobre esta pasta

Esta pasta reúne os resultados gerados durante o experimento de classificação de tumores mamários utilizando **Regressão Logística e Multilayer Perceptron (MLP)**.

Os arquivos são produzidos a partir do notebook desenvolvido no Google Colab e permitem consultar as métricas, comparar o desempenho dos classificadores e analisar a influência dos diferentes limiares de decisão.

O objetivo é manter os dados organizados e garantir a rastreabilidade entre a implementação, os resultados apresentados e a discussão do artigo científico.

## 📂 Organização dos resultados

Os arquivos podem ser organizados em três categorias:

| Categoria | Conteúdo |
|---|---|
| **Tabelas CSV** | Métricas dos modelos, limiares avaliados e resultados da validação |

Os nomes e a quantidade de arquivos devem corresponder à exportação efetivamente realizada no notebook.

## 🔬 Modelos avaliados

| Característica | Configuração |
|---|---|
| Base de dados | Breast Cancer Wisconsin Diagnostic |
| Amostras | 569 |
| Atributos | 30 |
| Modelos | Regressão Logística e MLP |
| Treinamento e teste | 80% / 20% |
| Validação | 5 partições estratificadas |
| Limiar padrão | 0,5 |
| Limiares investigados | 0,1 a 0,9 |
| Classe positiva | Tumor maligno |

A Regressão Logística é utilizada como modelo de referência, enquanto a MLP permite investigar o comportamento de uma rede neural no mesmo problema de classificação.

---

## 📈 Métricas analisadas

**Acurácia:** proporção total de classificações corretas.

**Precisão:** proporção de casos classificados como malignos que realmente pertencem à classe maligna.

**Recall (sensibilidade):** capacidade do modelo de identificar corretamente os casos malignos.

**F1-score:** média harmônica entre precisão e recall.

**ROC-AUC:** capacidade de discriminação do modelo considerando diferentes limiares.

**Falsos negativos (FN):** casos malignos classificados incorretamente como benignos.

**Falsos positivos (FP):** casos benignos classificados incorretamente como malignos.

A análise prioriza os falsos negativos, mas também considera o aumento de falsos positivos e as mudanças nas demais métricas.

---

## ⚙️ Seleção dos limiares

Foram investigados valores de limiar entre **0,1 e 0,9**, comparando as decisões produzidas pelas probabilidades estimadas por cada modelo.

O procedimento utiliza previsões da validação cruzada no conjunto de treinamento para selecionar o limiar com maior F1-score da classe maligna.

O conjunto de teste permanece reservado para a avaliação final, evitando que a escolha do limiar seja influenciada diretamente pelos dados utilizados para medir o desempenho.

---


## 🔄 Reprodutibilidade

Os resultados podem ser reproduzidos executando o notebook disponível na pasta [03 — Experimento no Google Colab](../).

As etapas incluem preparação dos dados, treinamento, validação cruzada, seleção de limiares, avaliação dos modelos e exportação das métricas.

Pequenas diferenças podem ocorrer conforme as versões das bibliotecas e as condições de execução.

---

## ⚠️ Limitações

O experimento utiliza uma única base pública e um conjunto de teste relativamente pequeno. As diferenças observadas não representam necessariamente superioridade geral de um algoritmo.

A seleção do limiar pelo F1-score também não equivale à definição de um limiar clinicamente adequado.

**Os resultados possuem finalidade exclusivamente acadêmica e não devem ser utilizados para diagnóstico médico.**

---

<div align="center">

### 👩‍💻 Autoria

**Alane Damasceno Moreno**

Bacharelado em Ciência da Computação  
IFCE — Campus Aracati

*Inteligência Artificial · 2026.2*

</div>
