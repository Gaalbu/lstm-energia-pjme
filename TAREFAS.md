# Divisão de tarefas — LSTM PJME (Davi Corrêa e Gabriel Alencar)

Entrega: notebook no Colab seguindo, na ordem, o pipeline da lauda.
Obrigatório: a dupla precisa participar de **pelo menos um encontro de acompanhamento** com a professora antes da entrega.

## Gabriel — dados, janelas, treino e escolha da janela (seções 0–7) ✅

- [x] Declaração de uso de IA Generativa (rascunho na seção 0)
- [x] Dataset: nome, fonte, alvo (`PJME_MW`), frequência horária, justificativa e gráfico inicial
- [x] Ordenação cronológica e tratamento de lacunas (horas duplicadas/ausentes do horário de verão)
- [x] Divisão treino / validação / teste por data-alvo (65% / 15% / 20% final)
- [x] Normalização Min-Max ajustada só com o treino
- [x] Janelas deslizantes de 24h e 168h com as mesmas datas-alvo (com asserts)
- [x] LSTM com a mesma arquitetura e hiperparâmetros para as duas janelas, um passo à frente
- [x] Tabela com o MAE das duas janelas na validação (escala original) e janela escolhida
- [x] Gráficos extras da validação (curvas de perda, zoom real × previsto, MAE por hora/dia)

## Davi — teste, referências e conclusão (seções 8–10) ✅

- [x] Previsões da LSTM escolhida no teste (`prever_mw(modelos[janela_escolhida], ...)`)
- [x] Referência de **persistência** (último valor observado) nas mesmas datas-alvo
- [x] Referência **sazonal** de 24h (mesma hora do dia anterior) e também a de 168h
- [x] Tabela com o MAE de cada método no teste (MW)
- [x] Gráfico real × LSTM × referências no teste, com o MAE de cada método
- [x] Visualizações complementares do teste
- [x] Conclusão: a janela longa ajudou na validação? Como a LSTM se saiu contra as referências no teste?

## Dupla

- [ ] Revisar a declaração de IA (extensão da contribuição e validação)
- [ ] Marcar e participar de um encontro de acompanhamento
- [ ] Rodar tudo no Colab (*Executar tudo*) sem erros antes de entregar no Classroom
- [ ] Depois de rodar, atualizar os números citados nos textos das seções 8–10 (marcados com ✏️; vêm de uma execução preliminar de 15 épocas em CPU)
