 <div align="center">

# 🧠 N2 — Inteligência Artificial

### Pesquisa em Machine Learning e Redes Neurais Artificiais

**Influência do limiar de decisão na classificação de tumores mamários: comparação entre MLP e Regressão Logística**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google_Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)
![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=for-the-badge&logo=latex&logoColor=white)

**IFCE — Campus Aracati**  
Bacharelado em Ciência da Computação  
Disciplina de Inteligência Artificial · 2026.2

</div>

---

## 📌 Sobre o projeto

Este repositório documenta o desenvolvimento de uma pesquisa experimental sobre a influência dos limiares de decisão na classificação de tumores mamários, utilizando os modelos Multilayer Perceptron (MLP) e Regressão Logística.

O estudo utiliza o conjunto de dados Breast Cancer Wisconsin Diagnostic e contempla pesquisa bibliográfica assistida pelo Hermes Agent, implementação em Python e análise de métricas de classificação.

## 📂 Navegação pelo projeto

| Seção | Descrição |
|---|---|
| [01 — Proposta de pesquisa](01-proposta/) | Problema, justificativa, objetivos e metodologia |
| [02 — Diário de pesquisa](02-diario-hermes/) | Configuração do Hermes, prompts e triagem bibliográfica |
| [03 — Experimento](03-experimento-colab/) | Notebook, modelos, métricas e gráficos |
| [04 — Artigo científico](04-artigo-cientifico/) | Desenvolvimento e discussão dos resultados |
| [05 — Referências](05-referencias/) | Bibliografia utilizada na pesquisa |

## 🎯 Objetivo

Analisar o efeito da variação do limiar de decisão sobre a identificação de tumores malignos, considerando falsos negativos, recall, F1-score e ROC-AUC.

## 🔬 Metodologia

- **Dataset:** Breast Cancer Wisconsin Diagnostic
- **Amostras:** 569
- **Atributos:** 30
- **Modelos:** Regressão Logística e MLP
- **Validação:** estratificada, com cinco partições no treinamento
- **Limiar de decisão:** 0,1 a 0,9
- **Ambiente:** Python, scikit-learn e Google Colab

## 🤖 Pesquisa bibliográfica com IA

O Hermes Agent foi utilizado com um modelo gratuito da OpenRouter para auxiliar na localização e triagem inicial de referências científicas.

O levantamento inicial identificou dez fontes, entre estudos experimentais e revisões bibliográficas. A documentação das buscas, critérios e verificações está organizada no diário de pesquisa.

## 📊 Resultados experimentais

O notebook apresenta a comparação entre os classificadores e permite analisar como diferentes limiares modificam a distribuição de falsos positivos e falsos negativos.

Os resultados devem ser interpretados no contexto acadêmico, sem aplicação direta ao diagnóstico clínico.

---

<div align="center">

### 👩‍💻 Autoria

**Alane Damasceno Moreno**

Bacharelado em Ciência da Computação  
Instituto Federal de Educação, Ciência e Tecnologia do Ceará  
IFCE — Campus Aracati

**Professor:** Gabriel Duarte

2026

</div>
