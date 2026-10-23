<div align="center">

# 📄 01 — Proposta de Pesquisa
### Entregável E1 + Declaração E3
**Influência do limiar de decisão na classificação de tumores mamários**

![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=white) ![Etapa](https://img.shields.io/badge/Etapa-N2-455A64?style=flat-square)

</div>

## Sobre esta etapa

Esta pasta reúne a **proposta de pesquisa da N2** e a declaração de uso de inteligência artificial. O documento E1 apresenta o problema investigado, sua relevância, os objetivos e o protocolo experimental previsto. A declaração E3 descreve a participação das ferramentas de IA e as responsabilidades da autora.

## Questão de pesquisa

> Como a variação do limiar de decisão afeta o recall, o F1-score e os falsos negativos de uma MLP e de uma Regressão Logística, sob o mesmo protocolo experimental?

## Organização do documento

1. Problema de pesquisa e justificativa;
2. Objetivo geral e objetivos específicos;
3. Metodologia experimental;
4. Resultados esperados;
5. Riscos e limitações;
6. Declaração de uso de inteligência artificial (E3);
7. Referências bibliográficas.

## Método previsto — resumo

| Elemento | Definição |
|---|---|
| Dados | Breast Cancer Wisconsin Diagnostic — 569 observações e 30 atributos |
| Modelos | Regressão Logística (baseline) e MLP |
| Divisão | Treino/teste estratificado, 80/20; semente 42 |
| Validação | Cinco partições estratificadas no treino |
| Pré-processamento | StandardScaler dentro de Pipeline |
| Limiares | 0,1 a 0,9 |
| Métricas | Recall, F1, precisão, ROC-AUC e matriz de confusão |
| Execução | Google Colab, CPU, Python e scikit-learn |

## Arquivos desta pasta

| Arquivo sugerido | Finalidade |
|---|---|
| `E1_Proposta_IFCE.pdf` | Proposta diagramada para leitura |
| `E1_Proposta_IFCE.tex` | Código-fonte editável no Overleaf |

> **Nota de entrega:** o E1 deve respeitar o limite de duas páginas de conteúdo, admitindo referências na terceira página, conforme o enunciado. A declaração E3 integra o final do E1. Mantenha a declaração de conferência pessoal somente após realizar essa verificação.

---

### Navegação

[← Página inicial](../README.md) · [Proposta](../01-proposta/) · [Diário Hermes](../02-diario-hermes/) · [Experimento](../03-experimento-colab/) · [Artigo](../04-artigo-cientifico/) · [Referências](../05-referencias/)

---

**Alane Damasceno Moreno** · Bacharelado em Ciência da Computação · IFCE Campus Aracati · Inteligência Artificial — Prof. Gabriel Duarte · 2026.2
