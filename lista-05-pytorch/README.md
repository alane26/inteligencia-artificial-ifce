 <div align="center">

# 🧠 Minha Primeira Rede Neural com PyTorch

### Lista de Exercícios · Inteligência Artificial

**Implementação, treinamento e avaliação de uma rede neural MLP para classificação multiclasse**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)

**IFCE — Campus Aracati**  
Bacharelado em Ciência da Computação

</div>

---

## 📌 Sobre o projeto

Esta atividade propõe a implementação de uma **Rede Neural Artificial do tipo Multilayer Perceptron (MLP)** utilizando o framework PyTorch.

O objetivo é construir, treinar e avaliar um modelo de classificação multiclasse utilizando a base de dados **Iris**, composta por características de três espécies de flores.

O projeto explora conceitos fundamentais de aprendizado de máquina, como propagação direta (*forward propagation*), retropropagação (*backpropagation*), otimização e avaliação de modelos.

### 🎯 Objetivos

- Implementar uma rede neural MLP com PyTorch.
- Compreender a organização das camadas e funções de ativação.
- Aplicar o processo de treinamento com cálculo automático de gradientes.
- Monitorar a evolução da função de perda.
- Avaliar o desempenho do classificador.
- Interpretar a matriz de confusão e as probabilidades de saída.
- Investigar o impacto de diferentes hiperparâmetros.

---

## 🌸 Base de dados — Iris

O conjunto de dados Iris é utilizado para problemas de classificação supervisionada.

| Característica | Descrição |
|---|---|
| **Amostras** | 150 |
| **Variáveis de entrada** | 4 |
| **Classes** | 3 espécies |
| **Treinamento** | 120 amostras (80%) |
| **Teste** | 30 amostras (20%) |
| **Semente aleatória** | 42 |

### Classes utilizadas

- Iris setosa
- Iris versicolor
- Iris virginica

As variáveis representam o comprimento e a largura das sépalas e pétalas.

Os dados são padronizados utilizando exclusivamente as estatísticas do conjunto de treinamento, evitando vazamento de informações do conjunto de teste.

---

## 🏗️ Arquitetura da rede neural

A arquitetura proposta utiliza uma MLP com duas camadas ocultas e função de ativação ReLU.

<div align="center">

**Entrada → Camada Oculta 1 → Camada Oculta 2 → Saída**

`4 neurônios → 16 neurônios → 16 neurônios → 3 neurônios`

</div>

| Camada | Neurônios | Ativação |
|---|---:|---|
| Entrada | 4 | — |
| Oculta 1 | 16 | ReLU |
| Oculta 2 | 16 | ReLU |
| Saída | 3 | Logits |

**Total esperado: 403 parâmetros treináveis.**

A camada final não utiliza Softmax diretamente, pois a função `CrossEntropyLoss` já incorpora a operação necessária para o cálculo da perda.

---

## ⚙️ Etapas de desenvolvimento

### 01 — Construção da MLP

Definição de uma classe `MLP` herdando de `nn.Module`, utilizando `nn.Sequential` para organizar as camadas da rede.

A implementação inclui o método `forward()`, responsável pela propagação das entradas até a saída.

### 02 — Treinamento do modelo

O treinamento utiliza a função de perda **CrossEntropyLoss** e o otimizador **Adam**.

| Parâmetro | Configuração |
|---|---|
| Otimizador | Adam |
| Taxa de aprendizado | 0.01 |
| Função de perda | CrossEntropyLoss |
| Épocas | 200 |
| Estratégia | Full-batch |

O processo de treinamento segue cinco operações fundamentais:

```python
otimizador.zero_grad()
saida = modelo(Xtr)
perda = criterio(saida, ytr)
perda.backward()
otimizador.step()
```

A evolução da perda é armazenada para análise gráfica.

### 03 — Avaliação do modelo

Após o treinamento, o modelo é colocado em modo de avaliação utilizando `modelo.eval()` e `torch.no_grad()`.

São realizadas as seguintes análises:

- Cálculo da acurácia de treinamento e teste.
- Construção da matriz de confusão.
- Identificação das classes com maior ocorrência de erros.
- Verificação das probabilidades geradas pelo Softmax.
- Comparação entre `CrossEntropyLoss` e `NLLLoss` com `log_softmax`.

### 04 — Desafios experimentais

A atividade também propõe investigações complementares sobre o comportamento da rede neural.

| Desafio | Experimento |
|---|---|
| Otimizadores | Comparar SGD e Adam |
| Camadas ocultas | Testar 2, 4, 16 e 64 neurônios |
| Número de épocas | Comparar 20, 50, 100 e 200 épocas |
| Mini-batches | Utilizar DataLoader com batch de 16 amostras |

A lista solicita a realização de pelo menos um desses desafios.

---

## 📊 Resultados esperados

De acordo com os critérios de referência do enunciado, a implementação deve apresentar resultados próximos aos seguintes valores:

| Métrica | Referência esperada |
|---|---:|
| Parâmetros treináveis | 403 |
| Perda inicial | ≈ 1,10 |
| Perda final | Menor que 0,001 |
| Acurácia de treinamento | 100% |
| Acurácia de teste | ≈ 90% |
| Classificação de Iris setosa | Sem erros |

> **Nota:** estes valores são referências fornecidas pela lista de exercícios. Os resultados efetivamente obtidos devem ser conferidos na execução do notebook.

---

## 🛠️ Tecnologias utilizadas

| Tecnologia | Finalidade |
|---|---|
| **Python** | Linguagem de programação |
| **PyTorch** | Construção e treinamento da MLP |
| **NumPy** | Operações numéricas e matriz de confusão |
| **Scikit-learn** | Carregamento da base Iris |
| **Matplotlib** | Visualização da curva de perda |
| **Google Colab** | Ambiente de execução |

---

## 🚀 Como executar

### 1. Preparar o ambiente

O projeto pode ser executado utilizando Google Colab ou Jupyter Notebook.

### 2. Instalar as dependências

```bash
pip install torch numpy scikit-learn matplotlib notebook
```

### 3. Executar a atividade

Abra o notebook da atividade e execute as células na ordem indicada para realizar:

1. Carregamento e preparação dos dados.
2. Construção da arquitetura MLP.
3. Treinamento da rede neural.
4. Visualização da evolução da perda.
5. Avaliação das previsões.
6. Análise dos resultados e desafios experimentais.

---

## 💡 Considerações finais

A atividade permite compreender o fluxo completo de desenvolvimento de uma rede neural utilizando PyTorch, desde a preparação dos dados até a avaliação do modelo.

O uso da diferenciação automática simplifica o treinamento e permite concentrar a análise na arquitetura, na otimização e na interpretação dos resultados.

Além disso, os experimentos complementares possibilitam investigar como diferentes escolhas de hiperparâmetros influenciam o desempenho e a capacidade de generalização da rede.

---

<div align="center">

### 👩‍💻 Autoria

**Alane Damasceno Moreno**

Bacharelado em Ciência da Computação  
Instituto Federal de Educação, Ciência e Tecnologia do Ceará  
**IFCE — Campus Aracati**

**Disciplina:** Inteligência Artificial  
**Professor:** Prof. Me. Gabriel Duarte  
**Ano:** 2026

</div>
