<div align="center">

# 🔎 02 — Diário de Pesquisa
### Entregável E2 · Deep Research com Hermes Agent

![Hermes](https://img.shields.io/badge/Hermes-Agent-7B1FA2?style=flat-square) ![OpenRouter](https://img.shields.io/badge/OpenRouter-modelo%20gratuito-2563EB?style=flat-square)

</div>

## Sobre esta etapa

Este diretório documenta o processo de pesquisa bibliográfica assistida por IA: instalação e configuração do agente, teste de ferramentas, prompt utilizado, rastreabilidade dos resultados e decisões de triagem.

O Hermes Agent foi utilizado **como apoio à busca e organização**, não como substituto da conferência das fontes científicas.

## Ambiente utilizado

| Componente | Registro |
|---|---|
| Sistema | Windows PowerShell |
| Agente | Hermes Agent |
| Provedor | OpenRouter |
| Modelo | `thinkingmachines/inkling:free` |
| Raciocínio solicitado | `high` |
| Diagnóstico | `hermes doctor` |
| Teste de ferramenta | `python --version` → Python 3.14.7 |
| Pesquisa | Busca web e habilidades de pesquisa |

## Levantamento bibliográfico

O levantamento inicial realizado em 22 de outubro de 2026 **retornou dez fontes**, classificadas pelo agente como sete primárias e três secundárias. A fonte nº 10 foi indicada como parcialmente verificada. A classificação e os dados bibliográficos precisam de conferência humana antes da inclusão definitiva.

A triagem registra, para cada referência, sua pertinência, o status preliminar e a justificativa de inclusão, reserva, contextualização ou descarte.

## Evidências

A subpasta `imagens/` pode armazenar os 12 registros em ordem, por exemplo:

| Grupo | Arquivos |
|---|---|
| Instalação e configuração | `01_instalacao_hermes.png` a `04_resumo_configuracao.png` |
| Diagnóstico e execução | `05_diagnostico_ambiente.png` a `08_registro_sessao.png` |
| Ferramentas e pesquisa | `09_habilidades_instaladas.png` a `12_resultado_pesquisa.png` |

## Arquivos desta pasta

| Arquivo sugerido | Finalidade |
|---|---|
| `E2_Diario_IFCE.pdf` | Diário completo com triagem e evidências |
| `E2_Diario_IFCE.tex` | Fonte LaTeX do diário |
| `pesquisa_bibliografica_ifce_ia.md` | Relatório original produzido pelo Hermes |
| `imagens/` | Capturas de tela utilizadas no documento |

## Cuidados de segurança e integridade

- Não incluir chaves de API, tokens, arquivos `.env` ou capturas com credenciais.
- Diferenciar fonte localizada, fonte bibliograficamente conferida e texto integral lido.
- Preservar o prompt utilizado e as decisões de triagem para reprodutibilidade.

---

### Navegação

[← Página inicial](../README.md) · [Proposta](../01-proposta/) · [Diário Hermes](../02-diario-hermes/) · [Experimento](../03-experimento-colab/) · [Artigo](../04-artigo-cientifico/) · [Referências](../05-referencias/)

---

**Alane Damasceno Moreno** · Bacharelado em Ciência da Computação · IFCE Campus Aracati · Inteligência Artificial — Prof. Gabriel Duarte · 2026.2
