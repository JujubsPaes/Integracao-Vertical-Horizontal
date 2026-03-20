# Atividade — Aplicação de SDCD no Projeto Integrador

**Enunciado:** Com base nos conceitos estudados sobre Sistemas Digitais de Controle Distribuído (SDCD), analise como um sistema desse tipo poderia ser aplicado no contexto do Projeto Integrador. Considere a seguinte arquitetura de referência:

> Sensor de Temperatura → ESP32 → MQTT → Servidor → Aplicativo Mobile → Dashboard → Gestão da Fábrica

Descreva o papel de cada componente, o fluxo de dados ao longo da cadeia, as decisões que podem ser tomadas a partir do dashboard e as vantagens do modelo distribuído nesse contexto.

---

## Análise

A arquitetura proposta para o Projeto Integrador III reproduz, em escala didática, os princípios operacionais dos Sistemas Digitais de Controle Distribuído aplicados à automação de processos industriais. A lógica de distribuir o processamento entre dispositivos localizados próximos ao fenômeno físico monitorado — conectados a uma camada central de consolidação e visualização — espelha o paradigma que orienta os sistemas distribuídos em plantas de grande porte, conforme descrito por Moraes e Castrucci (2007) ao tratarem das arquiteturas de controle distribuído na engenharia de automação.

### 1. Papel de Cada Componente

O **sensor de temperatura** atua como elemento primário de campo, responsável pela conversão de uma grandeza física mensurável em sinal elétrico ou digital. Sua posição no processo representa o ponto de aquisição de dados sem o qual toda a cadeia subsequente seria privada de informação real sobre o estado da planta.

O **ESP32** desempenha uma função análoga à do controlador distribuído em um SDCD convencional. Posicionado junto ao sensor, realiza a leitura periódica, executa conversão e filtragem inicial do sinal e transmite os dados processados pela rede local. Sua proximidade ao ponto de medição confere ao sistema capacidade de processamento local e resposta imediata a condições críticas, mesmo diante de instabilidade na conectividade de rede — característica que Groover (2011) identifica como traço definidor do paradigma da descentralização do controle em manufatura.

O **protocolo MQTT**, baseado no modelo publish/subscribe, opera como meio de transporte das mensagens entre o controlador local e o servidor. Sua arquitetura assíncrona e o baixo consumo de recursos o tornam especialmente adequado para aplicações de Internet das Coisas em contextos industriais, conforme documentado pela OASIS (2019).

O **servidor** corresponde à camada de processamento e persistência dos dados recebidos. Na hierarquia do SDCD, equivale ao nível de supervisão e consolidação: recebe as mensagens publicadas, aplica lógica de armazenamento e disponibiliza as informações para consumo pelas interfaces de visualização.

O **aplicativo mobile** oferece acesso remoto aos dados do processo, ampliando a mobilidade do operador ou gestor sem necessidade de presença física na instalação.

O **dashboard** consolida graficamente os dados coletados, apresentando indicadores em tempo real, séries históricas e alertas. Exerce função equivalente à de um sistema SCADA na arquitetura industrial tradicional, permitindo à gestão uma visão abrangente e atualizada do estado operacional.

### 2. Fluxo de Dados

O fluxo tem origem no ambiente físico: o sensor detecta a variação térmica do processo e produz um sinal correspondente. O ESP32 realiza a leitura periódica, converte o dado em valor numérico e o publica em um tópico MQTT. O broker encaminha a mensagem ao servidor, que a recebe, valida contra limites configurados e persiste em banco de dados. Esses dados são então disponibilizados por meio de uma API às interfaces de visualização — aplicativo mobile e dashboard —, que os renderizam em formato gráfico com indicadores em tempo real, históricas e alertas visuais. A gestão da fábrica acessa essas interfaces e obtém visibilidade do estado operacional sem necessidade de inspecionar equipamentos individualmente.

### 3. Decisões e Ações a partir do Dashboard

Com base nas informações consolidadas no dashboard, diferentes ações podem ser desencadeadas:

- **Controle de processo:** identificação de desvios de temperatura que exijam intervenção, como acionamento de sistemas de resfriamento ou interrupção de etapa crítica.
- **Prevenção de falhas:** análise de tendências que sinalizem degradação de equipamentos antes que ocorra parada não programada.
- **Monitoramento de conformidade:** acompanhamento contínuo das condições de operação para validação frente a parâmetros técnicos estabelecidos.
- **Gestão energética:** correlação entre variações térmicas e consumo de energia para otimização de acionamentos.
- **Rastreabilidade:** registro automático de variáveis de processo para fins de auditoria, qualidade e conformidade regulatória.

### 4. Vantagens do Sistema Distribuído

A arquitetura distribuída adotada no projeto apresenta vantagens estruturais que vão além do desempenho pontual de cada componente:

- **Isolamento de falhas:** a indisponibilidade de um ESP32 compromete apenas o ponto de medição sob sua responsabilidade, mantendo o restante do sistema operacional.
- **Redução de infraestrutura física:** controladores posicionados próximos aos sensores eliminam a necessidade de longos percursos de cabeamento.
- **Escalabilidade:** novos sensores e controladores podem ser incorporados ao sistema sem reconfigurações estruturais, bastando a adição de dispositivos e a criação de novos tópicos de comunicação.
- **Processamento local:** o ESP32 pode executar lógica básica de controle e garantir respostas imediatas a condições críticas mesmo sem conectividade momentânea com o servidor.
- **Visibilidade integrada:** o dashboard centraliza dados de múltiplos pontos em uma interface única, eliminando a fragmentação de informações típica de sistemas sem integração.
- **Facilidade de manutenção:** a localização distribuída dos controladores simplifica a identificação e substituição de componentes com falha, reduzindo o tempo de intervenção técnica.

---

## Referências

GROOVER, M. P. **Automação industrial e sistemas de manufatura.** São Paulo: Pearson, 2011.

LARA, Carla Eduarda Orlando de Moraes de. **Automação e controle industrial.** Curitiba: Contentus, 2021.

MORAES, Cícero Couto de; CASTRUCCI, Plinio de Lauro. **Engenharia de automação industrial.** São Paulo: LTC, 2007.

OASIS. **MQTT Version 5.0: OASIS Standard.** OASIS Open, 2019. Disponível em: https://docs.oasis-open.org/mqtt/mqtt/v5.0/mqtt-v5.0.html. Acesso em: 20 mar. 2026.
