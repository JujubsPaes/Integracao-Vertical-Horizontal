# Notas de Aula — Aula 05

**Docente:** Prof. Me. Deivison S. Takatu  
**Data:** 10/04/2026  
**Tema:** Pirâmide da Automação

---

## Registro da Aula

A quinta aula apresentou a Pirâmide da Automação como modelo de organização hierárquica dos sistemas industriais, situando cada nível em relação à sua função, às tecnologias que o compõem e ao fluxo de dados que o conecta aos demais. O modelo foi explorado como instrumento de compreensão da integração vertical — conceito central da disciplina —, evidenciando como informações geradas no chão de fábrica percorrem a estrutura hierárquica até alcançar os sistemas de decisão estratégica.

## Tópicos Trabalhados

- Conceituação e estrutura da Pirâmide da Automação
- Função específica de cada nível hierárquico
- Fluxo de dados entre os níveis e sua relação com a integração vertical
- Dependência mútua entre os níveis para o funcionamento coerente do sistema industrial

## Pirâmide da Automação

A Pirâmide da Automação organiza os sistemas industriais em cinco níveis sobrepostos, cada um com responsabilidade distinta no ciclo produtivo. Os níveis inferiores executam; os intermediários controlam e monitoram; os superiores planejam e decidem. A integração entre todos eles é o que transforma uma coleção de sistemas isolados em um ambiente industrial funcional e orientado por dados.

### Nível 1 — Sensores e Atuadores (Campo)

É o estrato mais próximo do processo físico. Sensores coletam grandezas mensuráveis — temperatura, pressão, nível, proximidade, velocidade — e as convertem em sinais tratáveis pelos sistemas de controle. Atuadores recebem comandos e executam ações físicas: acionam motores, abrem válvulas, movimentam esteiras. Este nível não toma decisões; apenas mede e executa.

### Nível 2 — Controle (CLP / SDCD)

Responsável pelas decisões automáticas em tempo real. Recebe os dados dos sensores, executa a lógica de controle programada e envia comandos aos atuadores. As respostas ocorrem em milissegundos, garantindo a sincronização e a segurança operacional dos equipamentos.

### Nível 3 — Supervisão (SCADA / IHM)

Permite a visualização do processo pelos operadores e o registro histórico dos dados. Sistemas SCADA e IHMs consolidam informações de múltiplos controladores em interfaces gráficas que exibem o estado da planta em tempo real, emitem alarmes e permitem intervenções manuais quando necessário.

### Nível 4 — Execução da Manufatura (MES)

Gerencia a produção em tempo real: libera e acompanha ordens de produção, aloca recursos, monitora o desempenho operacional e calcula indicadores como o OEE. Garante a rastreabilidade do produto ao longo de todo o ciclo fabril e serve como elo entre o chão de fábrica e o planejamento corporativo.

### Nível 5 — Gestão Empresarial (ERP)

Topo da pirâmide. O ERP centraliza o planejamento e a gestão de todos os recursos da organização — produção, logística, finanças, compras, vendas, recursos humanos — em uma única plataforma integrada. As decisões tomadas neste nível se traduzem em ordens e diretrizes que descem a pirâmide e se materializam nas operações de chão de fábrica.

![Pirâmide da Automação](image.png)
![Fluxo de dados entre os níveis](image-1.png)

## Observação

A ausência de integração entre os níveis da pirâmide não significa necessariamente que cada um deixa de funcionar — cada sistema pode operar de forma autônoma. O problema é que, sem integração, a informação não circula: o que acontece no nível 1 não chega ao nível 5, e as decisões estratégicas não encontram respaldo em dados reais da produção. É esse desacoplamento que a integração vertical se propõe a resolver.
