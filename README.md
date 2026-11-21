# LSTM para previsão do consumo horário de energia — PJM East (24h × 168h)

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Gaalbu/lstm-energia-pjme/blob/main/notebooks/LSTM_PJME_energia.ipynb)

Trabalho de **Implementação de uma Rede Neural Recorrente LSTM para Previsão de Séries Temporais** — disciplina
Inteligência Computacional / Machine Learning, turma **CC6NA** (2026.2), Profa. Polyana Santos Fonseca Nascimento.

**Dupla:** Davi Corrêa e Gabriel Alencar

## Problema

| | |
|---|---|
| Dataset | [Hourly Energy Consumption](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption) (Kaggle) — arquivo `PJME_hourly.csv`, dados da PJM Interconnection |
| Alvo | `PJME_MW` — consumo de energia em MW, frequência horária (2002–2018) |
| Tarefa | prever o consumo da **próxima hora** (um passo à frente) |
| Comparação | LSTM com janela deslizante de **24h** × **168h** (mesma arquitetura, mesmas datas-alvo); a vencedora na validação é comparada no teste com a **persistência** e a **referência sazonal** |

## Estrutura

```
data/PJME_hourly.csv               cópia do CSV original do Kaggle (para rodar sem conta no Kaggle)
notebooks/LSTM_PJME_energia.ipynb  notebook da entrega (Colab)
TAREFAS.md                         divisão de tarefas da dupla
```

## Como rodar

Clique no botão **Abrir no Colab** acima e use *Ambiente de execução → Executar tudo* (de preferência com GPU T4).
O notebook baixa o CSV direto deste repositório, então não é preciso fazer upload de nada.

Localmente: `pip install pandas numpy matplotlib scikit-learn tensorflow` e abra o notebook a partir da pasta `notebooks/`.

## Divisão de tarefas

Resumo (detalhes e checklist em [TAREFAS.md](TAREFAS.md)):

- **Gabriel** — seções 0–7: dataset e gráfico inicial, tratamento de lacunas, divisão cronológica e normalização,
  janelas de 24h e 168h, treino das duas LSTMs, tabela de MAE na validação e escolha da janela. ✅
- **Davi** — seções 8–10: avaliação no teste contra persistência e referência sazonal, gráficos do teste e conclusão.
- **Dupla** — revisar a declaração de IA, participar do encontro de acompanhamento e rodar tudo no Colab antes de entregar.
