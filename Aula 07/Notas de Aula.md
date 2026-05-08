# Notas de Aula — Aula 07

**Docente:** Prof. Me. Deivison S. Takatu  
**Data:** 08/05/2026  
**Tema:** MES (Manufacturing Execution System)

---

## Registro da Aula

A sétima aula abordou os sistemas MES, situando-os como camada intermediária entre o planejamento corporativo — representado pelo ERP — e a execução automatizada do chão de fábrica, conduzida por CLPs e sistemas supervisórios. A aula explorou as funções do MES, seu papel na rastreabilidade e no cálculo de indicadores de desempenho, e a forma como sua integração com os demais sistemas transforma a fábrica em um ambiente orientado por dados.

## Tópicos Trabalhados

- Posicionamento do MES na Pirâmide da Automação
- Funções principais: ordens de produção, rastreabilidade, qualidade e indicadores de desempenho
- Integração MES com ERP, SCADA/CLP e sistemas de Business Intelligence
- Relação do MES com o contexto da Indústria 4.0

## MES — Manufacturing Execution System

O MES é o sistema responsável por acompanhar, controlar e registrar a produção enquanto ela acontece. Sua posição na pirâmide o coloca exatamente entre o planejamento (ERP, nível 5) e a execução automatizada (SCADA e CLP, níveis 2 e 3), exercendo mediação bidirecional: recebe ordens planejadas no ERP e as transforma em atividades coordenadas no chão de fábrica; ao mesmo tempo, coleta dados de execução e os retorna ao ERP como informação gerencial — produção realizada, custos incorridos, tempos e perdas.

Entre suas funções essenciais estão a gestão de ordens de produção, o controle de recursos (máquinas, operadores, materiais), a coleta automatizada de dados de processo, o controle de qualidade com registro de inspeções e refugos, a rastreabilidade de lotes — com identificação de máquina, operador e horário para cada produto — e o cálculo de indicadores de desempenho como o OEE (Overall Equipment Effectiveness).

## Fluxo de Integração

```
ERP (planejamento) → MES (coordenação) → SCADA/CLP (supervisão e controle) → Sensores/Atuadores (campo)
```

- **ERP ↔ MES:** troca de ordens de produção, consumo de materiais, quantidades produzidas e custos reais.
- **MES ↔ SCADA/CLP:** troca de status de máquinas, alarmes, contadores e parâmetros de processo.
- **MES ↔ BI:** geração de painéis analíticos e relatórios para análise gerencial.

## Observação

A ausência de um MES cria um vazio funcional entre o planejamento e a execução: o ERP planeja com base em estimativas, e a produção acontece sem retroalimentar o sistema de gestão com dados reais. O MES é o componente que fecha essa lacuna, tornando a fábrica integrada, rastreável e capaz de operar com base em informação confiável e atualizada.
