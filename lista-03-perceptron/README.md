# 🧠 Lista 03 — Implementando o Perceptron

Implementação **do zero, utilizando NumPy**, do **Perceptron de Rosenblatt**, com o objetivo de compreender seu processo de aprendizagem, a regra de atualização dos pesos e sua relação com a separabilidade linear dos dados.

A atividade aplica o mesmo algoritmo às portas lógicas **OR, AND e XOR** e, como desafio, a um problema de classificação utilizando a base de dados **Iris**.

---

## 🎯 Objetivos

- implementar manualmente o Perceptron;
- compreender a função de ativação degrau;
- aplicar a regra de correção de erro;
- acompanhar a atualização dos pesos e do bias;
- analisar a convergência do algoritmo;
- compreender o conceito de separabilidade linear;
- observar a limitação do Perceptron no problema XOR;
- aplicar o algoritmo em um conjunto de dados real.

---

## 🧮 Regra de aprendizado

O Perceptron calcula inicialmente o potencial de ativação:

\[
z = w_1x_1 + w_2x_2 + b
\]

A classificação é realizada utilizando uma função degrau:

\[
\hat{y} =
\begin{cases}
1, & z \geq 0 \\
0, & z < 0
\end{cases}
\]

Quando ocorre um erro de classificação, os pesos são atualizados através de:

\[
w \leftarrow w + \alpha(y-\hat{y})x
\]

e o bias:

\[
b \leftarrow b + \alpha(y-\hat{y})
\]

O treinamento foi implementado manualmente em **NumPy**, sem utilizar bibliotecas de aprendizado de máquina para ajustar o modelo.

---

## 🟠 Exercício 1 — Porta OR

A primeira aplicação utiliza a porta lógica **OR**, um problema linearmente separável.

Foram realizadas:

- criação manual da base de dados;
- visualização das classes;
- análise manual das primeiras atualizações;
- implementação da função `treina_perceptron`;
- registro dos erros por época;
- análise da convergência;
- cálculo da acurácia;
- visualização da fronteira de decisão.

### Resultado

O Perceptron converge na **4ª época**:

```text
erros = [2, 2, 1, 0]
w = (1, 1)
b = -1
```

---

## 🟢 Exercício 2 — Porta AND

O mesmo algoritmo foi aplicado à porta lógica **AND**.

Foram analisados:

- número de erros por época;
- quantidade de épocas necessárias;
- pesos e bias finais;
- acurácia;
- fronteira de decisão;
- comparação da convergência com a porta OR.

### Resultado

O Perceptron converge na **6ª época**:

```text
erros = [2, 3, 3, 2, 1, 0]
w = (2, 1)
b = -3
```

A comparação mostra como a disposição dos pontos e a fronteira inicial influenciam a quantidade de atualizações necessárias.

---

## ❌ Exercício 3 — XOR

A porta **XOR** demonstra uma das principais limitações de um Perceptron simples.

As classes encontram-se distribuídas de forma que **não existe uma única reta capaz de separá-las**.

O treinamento foi realizado inicialmente durante 50 épocas e posteriormente durante **1000 épocas**.

Foram analisados:

- erros ao longo das épocas;
- acurácia final;
- oscilação dos pesos;
- ausência de convergência;
- relação com a separabilidade linear;
- Teorema de Convergência do Perceptron.

### Resultado

Mesmo aumentando o número de épocas, o Perceptron **não converge para o XOR**.

Isso ocorre porque aumentar o tempo de treinamento ou a taxa de aprendizado não resolve a ausência de uma fronteira linear capaz de separar as classes.

---

## 🌸 Exercício 4 — Iris

Como desafio, o Perceptron foi aplicado à base **Iris**, considerando somente:

- `setosa` — classe 0;
- `versicolor` — classe 1.

Foram utilizadas duas características:

- comprimento da pétala;
- largura da pétala.

### Implementações

- seleção das duas classes;
- seleção das duas características;
- visualização dos dados;
- análise da separabilidade;
- treinamento utilizando o Perceptron implementado manualmente;
- cálculo da acurácia;
- visualização dos erros;
- construção da fronteira de decisão.

### Resultado

O modelo converge na **3ª época**, alcançando:

```text
w ≈ (0.5, 0.8)
b = -2
acurácia = 1.0
```

---

## 💡 Conclusão

Os experimentos mostram que o Perceptron funciona adequadamente quando os dados são **linearmente separáveis**.

As portas **OR** e **AND**, assim como as classes setosa e versicolor da Iris, possuem uma fronteira linear capaz de separar corretamente os exemplos e, portanto, o algoritmo converge.

O **XOR**, por outro lado, evidencia a limitação de um único Perceptron. Como suas classes não são linearmente separáveis, nenhuma quantidade adicional de épocas é capaz de produzir uma solução.

Essa limitação ajuda a compreender a necessidade de modelos mais complexos, como as **Redes Neurais Multicamadas (MLP)**.

---

## 🛠️ Tecnologias utilizadas

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)

---

## 📂 Estrutura

```text
lista-03-perceptron/
│
├── README.md
├── Lista_Perceptron_IA_Alane_Damasceno.ipynb
└── lista_perceptron.pdf
```

---

### 👩‍💻 Autoria

**Alane Damasceno Moreno**  
Bacharelado em Ciência da Computação  
**IFCE — Campus Aracati**
