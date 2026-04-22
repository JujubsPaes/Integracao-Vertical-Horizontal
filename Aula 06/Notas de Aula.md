# Notas de Aula — Aula 06

**Docente:** Prof. Me. Deivison S. Takatu  
**Data:** 22/04/2026  
**Tema:** ERP (Enterprise Resource Planning)

---

## Registro da Aula

A sexta aula foi dedicada ao estudo dos sistemas ERP, posicionando-os como o nível mais alto da Pirâmide da Automação e como principal instrumento de integração entre os processos organizacionais. A aula explorou o conceito, os módulos que compõem um sistema ERP, os efeitos da integração automática entre eles e, por fim, um estudo de caso prático com as ferramentas ERPNext e Odoo.

## Tópicos Trabalhados

- Papel do ERP na integração industrial e na pirâmide da automação
- Definição e características de um sistema ERP
- Módulos principais e integração entre eles
- Estudo de caso: ERPNext e Odoo como exemplos de soluções abertas

## ERP — Enterprise Resource Planning

O ERP é um sistema integrado de gestão que centraliza informações e processos de toda a organização em uma única plataforma. Conecta áreas como finanças, vendas, recursos humanos, estoque, compras e produção, eliminando a fragmentação que resulta do uso de sistemas isolados ou planilhas desconectadas. O principal valor do ERP não está apenas no controle individual de cada módulo, mas na integração automática entre eles: uma ação em qualquer setor gera efeitos imediatos nos demais, garantindo consistência e eliminando retrabalho.

Do ponto de vista da Pirâmide da Automação, o ERP ocupa o nível 5 — o nível estratégico. Ele não atua diretamente no chão de fábrica, mas é o sistema que recebe os resultados da produção e os transforma em informação gerencial para suporte à decisão. Em conjunto com o MES (nível 4), fecha o ciclo de integração vertical: o ERP planeja, o MES executa, e os dados de execução retornam ao ERP para retroalimentar o planejamento.

## Módulos de um ERP e Sua Integração

| Evento | Módulo de Origem | Módulos Impactados | Resultado |
|---|---|---|---|
| Venda realizada | Vendas | Financeiro, Estoque | Geração de receita e baixa no estoque |
| Produção iniciada | Produção (PCP) | Estoque | Consumo de matéria-prima |
| Estoque mínimo atingido | Estoque | Compras | Geração automática de pedido de compra |
| Pedido de compra aprovado | Compras | Financeiro | Geração de contas a pagar |
| Contratação de funcionário | RH | Financeiro | Impacto na folha de pagamento |
| Atraso na produção | Produção | Vendas, Logística | Reprogramação de entrega |

A integração automática entre módulos transforma o ERP em um sistema nervoso da organização: nenhum setor opera em isolamento, e a informação flui de forma estruturada por toda a empresa.

## Estudo de Caso — ERPNext e Odoo

Foram apresentadas duas soluções de código aberto como exemplos práticos dos conceitos discutidos: **ERPNext** e **Odoo**. Ambas oferecem os módulos essenciais de um ERP — finanças, estoque, produção, vendas, compras, RH — em plataformas customizáveis e escaláveis. A análise dessas ferramentas demonstrou que os princípios de integração estudados não são exclusividade de grandes fornecedores proprietários, mas podem ser implementados por empresas de diferentes portes e maturidades digitais.

## Observação

O ERP fecha o ciclo da integração vertical ao conectar, em uma única visão gerencial, o que acontece no chão de fábrica com o planejamento estratégico da organização. Sem essa camada, a empresa pode até automatizar sua produção, mas permanece incapaz de utilizar os dados gerados para decisões de negócio consistentes e baseadas em evidências.
