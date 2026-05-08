# Atividade — MES e o Projeto Integrador

**Enunciado:** Analise os artigos indicados e o relatório de mercado sobre sistemas MES, identificando conceitos centrais como monitoramento em tempo real, integração e apoio à decisão. Relacione esses conceitos ao Projeto Integrador III, destacando funcionalidades como coleta de dados, rastreabilidade e suporte à gestão. Em seguida, elabore um parágrafo com essa relação, incluindo citações das referências. Produza um segundo parágrafo reforçando a fundamentação teórica e a conexão com a Indústria 4.0.

**Referências indicadas:**

SAENZ DE UGARTE, B.; ARTIBA, A.; PELLERIN, R. Manufacturing execution system – a literature review. *Production Planning & Control*, v. 20, n. 6, p. 525–539, 2009.

ARICA, E.; POWELL, D. J. Status and future of manufacturing execution systems. In: *Proceedings of the 2017 IEEE IEEM*. IEEE, 2017. p. 2000–2004.

MARKETS AND MARKETS. *Manufacturing Execution Systems (MES) Market Report.* Disponível em: https://www.marketsandmarkets.com/Market-Reports/manufacturing-execution-systems-mes-market-536.html.

---

## Análise

A revisão da literatura especializada sobre sistemas MES permite identificar três eixos conceituais recorrentes, que se articulam de forma complementar. O primeiro é o monitoramento em tempo real: Saenz de Ugarte, Artiba e Pellerin (2009) situam essa capacidade como a principal distinção funcional do MES em relação aos sistemas de planejamento convencionais, conferindo visibilidade imediata sobre o estado corrente da produção, aspecto que os sistemas de gestão de camadas superiores simplesmente não conseguem oferecer por si mesmos. O segundo eixo diz respeito à integração entre sistemas: Arica e Powell (2017) descrevem o MES como plataforma de mediação bidirecional entre o nível físico da automação e o nível gerencial, convertendo dados operacionais em informação de gestão e traduzindo ordens de planejamento em atividades reais no chão de fábrica. O terceiro eixo, evidenciado pelo relatório de mercado, é o apoio à decisão: organizações que adotam plataformas MES passam a subsidiar suas decisões operacionais com indicadores quantitativos e rastreáveis, reduzindo a dependência de avaliações subjetivas e aumentando a confiabilidade do processo decisório.

### Relação com o Projeto Integrador III

A arquitetura do Projeto Integrador III incorpora os princípios operacionais do MES ao estruturar um fluxo de dados que parte de sensores de campo, transita por controladores distribuídos — os microcontroladores ESP32 — e converge em um sistema com capacidade de registro histórico e apresentação de indicadores via dashboard. Saenz de Ugarte, Artiba e Pellerin (2009) definem o MES como plataforma capaz de integrar dados de máquinas, operadores e ordens de produção, garantindo monitoramento contínuo e rastreabilidade ao longo de todo o ciclo fabril. No PII3, essa funcionalidade se concretiza por meio da coleta automatizada de variáveis operacionais via sensores conectados a microcontroladores, cujas informações são persistidas em servidor e disponibilizadas em interfaces gerenciais para acompanhamento da produção. Arica e Powell (2017) reforçam que o MES transforma dados brutos em indicadores de desempenho interpretáveis, habilitando respostas ágeis a desvios de processo — função que o PII3 reproduz ao propor uma solução que não apenas adquire dados do ambiente produtivo, mas os organiza em conhecimento operacional acionável, integrando coleta, rastreabilidade e suporte à gestão em uma plataforma coesa (MORAES; CASTRUCCI, 2007).

### Fundamentação Teórica e Indústria 4.0

No contexto da Indústria 4.0, o MES ocupa a função de núcleo digital da manufatura inteligente, articulando tecnologias como a Internet Industrial das Coisas, a análise de grandes volumes de dados e os sistemas ciber-físicos com a operação cotidiana do chão de fábrica. Groover (2011) argumenta que a integração vertical — do sensor ao sistema de gestão — constitui fator determinante para a competitividade industrial, premissa que se intensificou com a aceleração da digitalização dos processos produtivos. Arica e Powell (2017) demonstram que o MES evoluiu de uma ferramenta de controle operacional pontual para uma plataforma de conectividade abrangente, capaz de se integrar a repositórios em nuvem e a algoritmos preditivos voltados à antecipação de falhas e à otimização de sequenciamento produtivo. Essa trajetória evolutiva sustenta teoricamente o PII3, cuja concepção prevê não apenas a captura de dados em tempo real, mas sua disponibilização em interfaces acessíveis remotamente — características que Saenz de Ugarte, Artiba e Pellerin (2009) identificam como requisitos fundamentais dos ambientes ciber-físicos orientados à manufatura responsiva. Ao adotar princípios de coleta distribuída, comunicação via protocolos padronizados e visualização gerencial consolidada, o projeto se alinha à fundamentação teórica do MES e às diretrizes da quarta revolução industrial, contribuindo para uma gestão rastreável, orientada por dados e adaptável às demandas do ambiente produtivo contemporâneo (SANTOS, 2024).

---

## Referências

ARICA, E.; POWELL, D. J. Status and future of manufacturing execution systems. In: *Proceedings of the 2017 IEEE International Conference on Industrial Engineering and Engineering Management (IEEM)*. [S.l.]: IEEE, 2017. p. 2000–2004.

GROOVER, M. P. **Automação industrial e sistemas de manufatura.** São Paulo: Pearson, 2011.

MORAES, Cícero Couto de; CASTRUCCI, Plinio de Lauro. **Engenharia de automação industrial.** São Paulo: LTC, 2007.

SAENZ DE UGARTE, B.; ARTIBA, A.; PELLERIN, R. Manufacturing execution system – a literature review. *Production Planning & Control*, v. 20, n. 6, p. 525–539, 2009. DOI: 10.1080/09537280902938613.

SANTOS, Jadir Perpétuo dos. **Sistemas integrados de gestão:** busca de agilidade e redução de riscos em seus processos. Rio de Janeiro: Freitas Bastos, 2024.
