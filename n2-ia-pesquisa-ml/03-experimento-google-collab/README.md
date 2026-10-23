<div align="center">

# 💻 03 — Experimento no Google Colab
### Regressão Logística × Multilayer Perceptron (MLP)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![scikit--learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white) ![Colab](https://img.shields.io/badge/Colab-F9AB00?style=flat-square&logo=googlecolab&logoColor=white)

</div>

## Sobre o experimento

Este diretório contém o notebook destinado à comparação de **Regressão Logística e MLP** para classificação de tumores mamários. A variável experimental principal é o **limiar de decisão**, usado para transformar a probabilidade prevista em classe.

O experimento utiliza o dataset Breast Cancer Wisconsin Diagnostic, disponível no `scikit-learn`. Trata-se de uma investigação acadêmica com dados públicos, **não de uma ferramenta de diagnóstico clínico**.

## Protocolo

| Etapa | Procedimento |
|---|---|
| Dados | 569 amostras, 30 características e duas classes |
| Classe positiva | Maligno = 1 (recodificação explícita) |
| Partição | 80% treino e 20% teste, estratificados |
| Padronização | `StandardScaler` dentro do `Pipeline` |
| Baseline | `LogisticRegression` |
| Rede neural | `MLPClassifier` |
| Validação | 5-fold estratificada no treinamento |
| Limiares avaliados | 0,1; 0,2; ...; 0,9 |
| Métricas | FN, FP, recall, precisão, F1 e ROC-AUC |

## Como executar

1. Abra o arquivo `.ipynb` no [Google Colab](https://colab.research.google.com/).
2. Se necessário, instale as dependências.
3. Execute as células em ordem.
4. Confira a separação entre treino, validação e teste.
5. Gere as tabelas e gráficos e registre os resultados da sua execução.

```bash
pip install numpy pandas matplotlib scikit-learn
```

## Arquivos desta pasta

| Arquivo sugerido | Finalidade |
|---|---|
| `N2_Limiares_MLP_Regressao_Logistica_Colab.ipynb` | Notebook principal |
| `resultados/` | Tabelas e arquivos exportados pelo notebook |
| `figuras/` | Curvas, matrizes de confusão e gráficos de limiares |

## Critério de interpretação

O limiar deve ser selecionado com informação do **treinamento/validação**, mantendo o teste reservado para a avaliação final. Uma redução dos falsos negativos pode aumentar os falsos positivos; por isso, os resultados devem ser examinados em conjunto. ROC-AUC mede a capacidade de ordenação ao longo dos limiares e não muda apenas por trocar o ponto de corte de probabilidades fixas.

> Atualize os resultados deste README somente após executar e conferir o notebook.

---

### Navegação

[← Página inicial](../README.md) · [Proposta](../01-proposta/) · [Diário Hermes](../02-diario-hermes/) · [Experimento](../03-experimento-colab/) · [Artigo](../04-artigo-cientifico/) · [Referências](../05-referencias/)

---

**Alane Damasceno Moreno** · Bacharelado em Ciência da Computação · IFCE Campus Aracati · Inteligência Artificial — Prof. Gabriel Duarte · 2026.2
