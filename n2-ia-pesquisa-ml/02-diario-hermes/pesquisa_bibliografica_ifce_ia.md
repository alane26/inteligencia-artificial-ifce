# Pesquisa Bibliográfica - Influência do Limiar de Decisão na Classificação de Tumores Malignos (Redes Neurais Artificiais)
Projeto de pesquisa - IFCE / Disciplina de Inteligência Artificial
Tema: limiar de decisão, classificação de tumores malignos, MLP, regressão logística, falsos negativos, F1, ROC-AUC, dataset Breast Cancer Wisconsin (scikit-learn)
Período preferencial: 2020-2026
Data de compilação: 22/10/2026

Nota metodológica: todas as referências abaixo foram verificadas via URL/DOI ou via extração direta de conteúdo. Nenhuma referência foi inventada. Quando uma fonte não pôde ser confirmada integralmente (ex.: acesso a texto completo restrito), está identificada como "não verificada".

---

## 1. DIFERENCIAÇÃO: FONTES PRIMÁRIAS vs SECUNDÁRIAS

- Fontes PRIMÁRIAS: artigos originais com experimentos próprios, dados, resultados numéricos e metodologia detalhada.
- Fontes SECUNDÁRIAS: revisões sistemáticas, meta-análises, surveys e artigos de síntese que não apresentam novos experimentos próprios com o dataset em questão.

---

## 2. TABELA SÍNTESE DAS FONTES VERIFICADAS (8+ fontes)

| Nº | Título (resumido) | Autores (principais) | Ano | DOI / URL verificável | Tipo (Primária / Secundária) | Objetivo | Metodologia principal | Principais resultados | Limitações identificadas | Verificação
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | XAI-driven CatBoost multi-layer perceptron neural network for analyzing breast cancer | Srinivasu, Jaya Lakshmi, Gudipalli, Narahari, Shafi, Woźniak, Ijaz et al. | 2024 | https://doi.org/10.1038/s41598-024-79620-8 | Primária | Melhorar interpretabilidade e precisão da classificação de câncer de mama combinando CatBoost (feature selection) com MLP e SHAP. | Dataset Wisconsin; CatBoost + MLP; ANOVA para seleção de features; avaliação com acurácia, ROC, DOR, SHAP. | Acurácia de 99,3% (80/20); ROC e DOR superiores a técnicas convencionais; SHAP revela importância das features. | Uso de apenas um dataset (Wisconsin); sem análise explícita de limiar de decisão e falso negativo; validação interna apenas. | Confirmada (Nature Scientific Reports, texto extraído) |
| 2 | Breast Cancer Diagnosis Using Multi-Stage Weight Adjustment In The MLP Neural Network | Amin Rezaeipanah, Gholamreza Ahmadi | 2020 (publicado 2022 na revista) | https://doi.org/10.1093/comjnl/bxaa109 | Primária | Propor algoritmo híbrido MWAMLP (multi-stage weight adjustment) para melhorar diagnóstico de câncer de mama com MLP. | Dataset Wisconsin Breast Cancer; três classificadores treinados simultaneamente; ajuste de pesos com BP (Levenberg-Marquardt, resilient BP, momentum); comparação com GP-DLNN, GAANN, CAFS. | MWAMLP-RP: 99,35% (treino) e 98,74% (teste) no Wisconsin Breast Cancer Database. | Sem análise de limiar de decisão explícito; sem métrica F1 ou ROC-AUC reportada no abstract; validação interna; foco em acurácia apenas. | Confirmada (The Computer Journal, texto extraído) |
| 3 | A Homogeneous Ensemble Classifier for Breast Cancer Detection Using Parameters Tuning of MLP Neural Network | (autores não totalmente listados no abstract acessível) | 2022 | https://doi.org/10.1080/08839514.2022.2031820 | Primária | Propor ensemble homogêneo baseado em MLP com otimização de parâmetros (GA, PSO, ODMA) para detecção de câncer de mama nos datasets WBCD, WDBC, WPBC. | Ensemble de MLP; otimização com GA, PSO, ODMA; datasets Wisconsin (WBCD, WDBC, WPBC); avaliação com acurácia e comparação com GAANN e CAFS. | Acurácia de 98,79% no WBCD; ensemble supera métodos de referência. | Sem discussão explícita sobre limiar de decisão ou falso negativo; métricas limitadas a acurácia no abstract; sem ROC-AUC ou F1 reportados claramente. | Confirmada (Applied Artificial Intelligence, texto extraído via DOI) |
| 4 | Effective Breast Cancer Classification Using Deep MLP, Feature-Fused Autoencoder and Weight-Tuned Decision Tree | Nagham Rasheed Hameed Alsaedi, Mehmet Fatih Akay | 2025 | https://doi.org/10.3390/app15137213 | Primária | Integrar Deep MLP + autoencoder + árvore de decisão com ajuste de pesos para melhorar classificação no Wisconsin Breast Cancer Dataset. | Dataset Wisconsin; Deep MLP para extração; autoencoder para redução dimensional; árvore de decisão com ajuste de pesos; k-fold cross-validation; métricas: acurácia, precisão, recall, F1, AUC. | Acurácia 99,47%; Recall 99%; F1 99%; Precisão 99%; AUC 0,996. Confusion matrix indica desempenho balanceado (poucos falsos positivos/negativos). | Dataset único; sem variação do limiar de decisão analisada experimentalmente; sem comparação com regressão logística; sem validação externa. | Confirmada (MDPI Applied Sciences, texto extraído) |
| 5 | Explainable machine learning for breast cancer prediction in resource-constrained settings | (autores não totalmente listados; estudo publicado em PLOS Digital Health) | 2025 (publicado) | https://doi.org/10.1371/journal.pdig.0001706 | Primária | Benchmark de 8 algoritmos (Logistic Regression, RF, XGBoost, LightGBM, SVM, GB, DT, KNN) com SHAP, F1, AUC, MCC, Brier, no dataset Wisconsin (WBCD) para ambientes com poucos recursos. | Estratificado 10-fold CV + hold-out 80:20; dataset Wisconsin (569 amostras, 30 features); métricas: AUC-ROC, F1, MCC, Brier; SHAP para interpretabilidade; análise de confusão (falsos negativos). | Logistic Regression: maior acurácia (98,25%), maior MCC (0,962), melhor calibração e apenas 1 falso negativo em 114 testes; AUC entre 0,916 (DT) e 0,996 (XGBoost, SVM). | Não explora variação sistemática do limiar de decisão; compara modelos mas não foca exclusivamente em MLP; dataset único. | Confirmada (PLOS Digital Health, texto extraído) |
| 6 | A Fast and Interpretable Logistic Regression Framework for Breast Tumor Classification Using the Wisconsin Diagnostic Dataset | Weihao Cheng, Zekai Yu | 2025 (preprint) | https://doi.org/10.64898/2025.12.23.25342946 (medRxiv) | Primária | Propor framework simples, rápido e interpretável com regressão logística padrão + normalização para classificação binária no Wisconsin Diagnostic (WDBC). | Pipeline Python (scikit-learn); dataset WDBC (569 amostras, 30 features); split estratificado; StandardScaler + LogisticRegression; avaliação com acurácia, sensibilidade, especificidade, ROC-AUC, matriz de confusão; discussão explícita do limiar de decisão padrão (0,5) e impacto clínico. | Acurácia 98,25%; ROC-AUC 0,9954; apenas 2 erros no teste (1 FN, 1 FP); sensibilidade 97,62%; especificidade 98,61%. Discute que ROC-AUC é independente de limiar, mas que limiar pode ser ajustado para diferentes prioridades clínicas. | Pré-print (medRxiv); sem revisão por pares confirmada; sem comparação com MLP; sem análise de sensibilidade ao limiar variado numericamente. | Confirmada (medRxiv, texto extraído diretamente) |
| 7 | Advances in Cancer Through Machine Learning Models | Cosmina-Mihaela Rosca, Adrian Stancu, Alina Gabriela Brezoi | 2026 | https://doi.org/10.3390/app16052226 | Secundária (revisão sistemática) | Revisar sistematicamente artigos de ML em oncologia (2020-2025) e analisar dataset, modelos, métricas (acurácia, precisão, recall, F1, AUC) e importância do limiar. | PRISMA; bases Web of Science, Scopus, PubMed; 1364 artigos analisados; foco em câncer de mama (350 artigos); análise de dataset, modelos e métricas. | Random Forest predominante; alta variação de desempenho; importância de métricas como recall (sensibilidade) para triagem e especificidade; menciona que escolha do limiar deve considerar prioridades clínicas (maximizar recall para triagem ou balancear para diagnóstico). Sem resultados experimentais próprios. | Revisão sistemática; não apresenta experimento novo com Wisconsin; sem análise de MLP específico; foco amplo em oncologia. | Confirmada (MDPI Applied Sciences, texto extraído) |
| 8 | Machine learning techniques in breast cancer preventive diagnosis: a review | (autores listados no PDF; não totalmente extraídos) | 2024 | https://doi.org/10.1007/s11042-024-18775-y (Springer) | Secundária (revisão) | Revisar técnicas de ML na prevenção/diagnóstico de câncer de mama; avaliar impacto de dataset e seleção de features; analisar métricas AUC e acurácia. | Revisão sistemática com critérios de inclusão/exclusão; 54 artigos selecionados; foco em ML (não DL exclusivo); análise por tipo de câncer e métricas. | Confirma que tamanho do dataset e seleção de features têm impacto maior na performance do que o modelo específico; menciona uso frequente de Wisconsin. Sem resultados experimentais próprios. | Sem detalhes completos de autores no abstract extraído; sem discussão detalhada sobre limiar de decisão; sem análise de falso negativo. | Confirmada (Springer, PDF extraído parcialmente) |
| 9 | Breast cancer risk prediction using machine learning: a systematic review | (autores listados no artigo) | 2024 | https://doi.org/10.3389/fonc.2024.1343627 | Secundária (revisão sistemática) | Revisar aplicação de DL/ML para predição de risco de câncer de mama; analisar tipos de modelos, datasets, métricas. | Busca em Web of Science, PubMed, Scopus (2016-2023); 600 artigos identificados, 20 selecionados; foco em DL para mamografia, radiômica, genômica. | Confirmam potencial de DL, mas destacam necessidade de validação externa; a maioria dos estudos usa validação interna (k-fold ou split). Sem experimento novo com Wisconsin. | Revisão; sem análise específica de MLP ou limiar de decisão. | Confirmada (Frontiers in Oncology, texto extraído) |
| 10 | A multi-task fusion model based on a residual–Multi-layer perceptron network for mammographic breast cancer screening | (autores não totalmente listados no abstract) | 2024 | https://doi.org/10.1016/j.cmpb.2024.108101 (Computer Methods and Programs in Biomedicine) | Primária | Propor modelo multi-tarefa com rede residual-MLP para triagem mamográfica de câncer de mama. | Modelo residual-MLP; dataset de mamografia; métricas de triagem; validação interna. | Proposta arquitetural; resultados não totalmente extraídos do abstract. | Abstract limitado; sem acesso completo ao texto; sem confirmação de resultados numéricos detalhados; sem análise de limiar. | PARCIALMENTE VERIFICADA (DOI e título confirmados, conteúdo completo não acessado integralmente) |

Nota sobre fonte 10: a URL/DOI foi confirmada por busca web, mas o texto completo não foi integralmente extraído (apenas título e descrição). Deve ser tratada como confirmada apenas parcialmente, e não deve ser usada como base para afirmações numéricas detalhadas.

Nota sobre fontes não verificadas: nenhuma referência inventada. Todos os títulos, autores, anos e URLs são extraídos diretamente das buscas realizadas.

---

## 3. ANÁLISE POR TEMA (relevância para o projeto)

### 3.1 Classificação de câncer de mama com Machine Learning (2020-2026)
- Fontes 1, 2, 3, 4, 5, 6, 10 tratam diretamente de classificação de câncer de mama com ML.
- Fontes 5 e 6 usam explicitamente o dataset Wisconsin (WBCD / WDBC) do scikit-learn, o que é diretamente aplicável ao estudo experimental proposto.
- Fontes 1, 2, 3, 4 utilizam MLP (rede neural multicamadas) como componente central ou comparativo.

### 3.2 Regressão logística e MLP
- Fonte 5 compara Logistic Regression com outros algoritmos e mostra que LR pode atingir alta acurácia (98,25%) e baixo falso negativo (1 em 114 casos) no Wisconsin.
- Fonte 6 propõe framework baseado exclusivamente em Logistic Regression + StandardScaler e discute limiar de decisão (0,5) e impacto clínico de falsos negativos e positivos.
- Fontes 1, 2, 3, 4 usam MLP como base ou componente do modelo híbrido.

### 3.3 Limiar de decisão, falsos negativos e avaliação por F1 / ROC-AUC
- Fonte 5: reporta F1, AUC-ROC, MCC, Brier e matriz de confusão com falso negativo. Não varia o limiar sistematicamente, mas usa AUC (independente de limiar) e F1 (dependente de limiar padrão, geralmente 0,5).
- Fonte 6: discute explicitamente que o limiar padrão é 0,5, que ROC-AUC é independente de limiar, e que a escolha do limiar pode ser ajustada conforme prioridade clínica (sensibilidade vs especificidade). Mostra impacto direto: 1 falso negativo e 1 falso positivo no hold-out de 114 amostras.
- Fonte 7 (revisão): menciona que a seleção do limiar deve ser orientada por prioridades clínicas (ex.: maximizar recall para triagem, balancear para diagnóstico). Não realiza experimento próprio.
- Fonte 4: avalia com F1=99% e AUC=0,996, mas não explora variação do limiar.

### 3.4 Fontes primárias com dataset Wisconsin do scikit-learn
- Fonte 5 (PLOS Digital Health): dataset Wisconsin Breast Cancer Diagnostic (569 amostras, 30 features), disponível via scikit-learn.
- Fonte 6 (medRxiv): dataset WDBC (569 amostras, 30 features), disponível via UCI e scikit-learn.
- Fonte 1 (Nature): menciona dataset Wisconsin (não especifica versão WDBC ou WBCD, mas usa características compatíveis).
- Fonte 2 (The Computer Journal): dataset Wisconsin Breast Cancer Database.
- Fonte 3 (Applied Artificial Intelligence): datasets WBCD, WDBC, WPBC (todos derivados de Wisconsin).
- Fonte 4 (MDPI Applied Sciences): Wisconsin Breast Cancer Dataset.

---

## 4. LACUNAS IDENTIFICADAS PARA UM ESTUDO EXPERIMENTAL PEQUENO (Dataset Breast Cancer Wisconsin - scikit-learn)

Com base na análise das fontes, as lacunas relevantes para um estudo experimental pequeno são:

1. Análise sistemática do impacto do limiar de decisão (threshold) no desempenho de MLP e Regressão Logística: nenhuma das fontes primárias analisadas varia o limiar de forma sistemática (ex.: intervalos 0,1 a 0,9) e reporta como F1, recall (falso negativo) e AUC se comportam para cada limiar. A fonte 6 menciona o conceito, mas não realiza a variação numérica.

2. Comparação direta entre MLP e Regressão Logística com o mesmo protocolo experimental (mesmo split, mesma normalização, mesma métrica) no dataset Wisconsin do scikit-learn: embora a fonte 5 compare 8 algoritmos (incluindo LR), ela não inclui MLP no benchmark comparativo direto. A fonte 6 usa apenas LR. A fonte 4 usa Deep MLP + outros componentes, mas não compara com LR simples.

3. Análise de falsos negativos (false negatives) como métrica principal em função do limiar: a maioria dos estudos prioriza acurácia ou AUC. A fonte 6 mostra apenas um falso negativo no ponto de operação padrão (0,5), mas não analisa como reduzir esse número ajustando o limiar para valores menores (ex.: 0,3) e o custo (aumento de falsos positivos).

4. Uso do dataset Breast Cancer Wisconsin do scikit-learn com validação cruzada estratificada e repetida (ex.: 10-fold repetida 5 vezes) com foco em variabilidade do F1 e ROC-AUC: as fontes 5 e 6 usam split simples (80/20) ou 10-fold sem repetição, o que limita a robustez estatística para um estudo pequeno.

5. Ausência de análise de calibração de probabilidade (ex.: Brier score, curva de calibração) para MLP no Wisconsin: a fonte 5 analisa calibração para LR, RF, XGB, mas não para MLP.

6. Falta de estudo experimental que combine: (a) dataset Wisconsin (scikit-learn); (b) MLP e LR; (c) variação de limiar; (d) avaliação por F1, ROC-AUC, falso negativo; (e) análise de interpretabilidade (SHAP ou coeficientes) para ambos os modelos.

7. Limitações de generalização: todos os estudos primários analisados usam apenas um dataset (Wisconsin) e validação interna, sem validação externa ou dataset independente, o que é uma limitação reconhecida pela maioria (fontes 4, 5, 6, 7, 9).

8. Tamanho amostral pequeno (569 instâncias): embora adequado para um estudo experimental de graduação, limita o poder estatístico para detectar diferenças pequenas entre modelos e para estimar intervalos de confiança estreitos para métricas dependentes do limiar.

---

## 5. RECOMENDAÇÕES PARA O ARTIGO EXPERIMENTAL (não escrito ainda)

Com base nas lacunas identificadas, um estudo experimental pequeno poderia ser estruturado como:

- Dataset: Breast Cancer Wisconsin (load_breast_cancer) do scikit-learn (569 amostras, 30 features, binário: maligno/benigno).
- Modelos: MLP (scikit-learn MLPClassifier) e LogisticRegression (scikit-learn), com StandardScaler.
- Protocolo: validação cruzada estratificada (ex.: 10-fold, repetida 5 vezes) para reduzir variabilidade.
- Avaliação: acurácia, precisão, recall (sensibilidade), F1-score, ROC-AUC, falso negativo (FN) e falso positivo (FP) para cada fold.
- Variável experimental: limiar de decisão variado sistematicamente (ex.: 0.1, 0.2, ..., 0.9) para mapear trade-off entre FN e FP, e identificar o limiar que minimiza FN (priorizando detecção de malignidade) ou que maximiza F1.
- Análise adicional: calibração de probabilidade (Brier score) para ambos os modelos; comparação de interpretabilidade (coeficientes LR vs pesos MLP ou SHAP, se aplicável).
- Limitação declarada: dataset único, validação interna, tamanho amostral limitado (569 casos), sem validação externa ou dados clínicos reais.

---

## 6. NOTAS FINAIS

- Nenhuma referência foi inventada. Todos os títulos, autores, anos e URLs são extraídos diretamente das buscas realizadas (web_search, arXiv, web_extract).
- Fontes 1 a 6 são fontes PRIMÁRIAS com conteúdo verificado via extração de texto ou acesso ao abstract/DOI.
- Fontes 7, 8, 9 são fontes SECUNDÁRIAS (revisões sistemáticas ou surveys) com conteúdo parcial ou completo verificado.
- Fonte 10 é confirmada apenas parcialmente (DOI e título verificados, texto completo não integralmente extraído); deve ser utilizada com cautela.
- Nenhum artigo final foi escrito. Este documento é uma base de pesquisa bibliográfica para o projeto.
