# Justificativa do Modelo de Processo: App de Caronas Universitárias

Com base na conversa em grupo que analisou todo o conteúdo do projeto (Justificativa, Requisitos, Viabilidade e Diagramas UML), o modelo de processo mais adequado para conduzir o desenvolvimento deste sistema é o **Modelo Ágil**, utilizando o framework **Scrum**.

## Por que o Modelo Ágil é o ideal?

1. **Alta Necessidade de Evolução e Adaptação:** O documento da Semana 1 prevê explicitamente manutenções do tipo **Evolutiva** (como adicionar pagamentos via PIX futuramente) e **Adaptativa** (atualizações constantes para acompanhar novas versões do Android/iOS e mudanças nas APIs de mapas). Modelos ágeis são feitos sob medida para produtos que mudam constantemente com a tecnologia.
2. **Requisitos Dinâmicos e Negociáveis:** O registro de conflito da Semana 2 mostrou que requisitos importantes, como o mapa em tempo real, foram cortados e substituídos pelo compartilhamento via WhatsApp por questões de custo de API. O Ágil, com o conceito de *Backlog* permite essa flexibilidade de trocar, adicionar ou remover funcionalidades sem quebrar o processo.
3. **Mitigação do Risco Técnico Principal:** O Estudo de Viabilidade alertou que a integração com o login (SSO) da universidade é o maior gargalo. No modelo Ágil, a equipe pode focar nesse risco logo na primeira *Sprint* criando um MVP (Mínimo Produto Viável). Se a TI da universidade bloquear o acesso, o projeto falha rápido (*fail fast*), evitando desperdício de tempo e dinheiro.

## Por que os outros modelos foram descartados?

*   **Cascata:** Exige que todos os requisitos sejam definidos e congelados no início. É inadequado para aplicativos mobile por exemplo, pois se a Apple ou Google mudarem uma regra, ou se a TI atrasar a liberação do SSO, o projeto inteiro empaca.
*   **Incremental:** Embora seja melhor que o Cascata por entregar o app em partes (incrementos), o modelo Incremental tradicional ainda exige que a arquitetura e os requisitos de todos os incrementos sejam planejados logo no início. Ele não tem a flexibilidade do Ágil para descartar uma funcionalidade no meio do caminho com base no feedback rápido do usuário.
*   **Espiral:** O modelo espiral foca intensamente na análise de riscos por meio de múltiplos protótipos descartáveis. Embora o projeto tenha riscos (como o SSO), o Espiral é voltado para sistemas de altíssima complexidade e custo extremo como softwares bancários críticos. Para um app de caronas desenvolvido por uma equipe de 5 a 15 pessoas, o Espiral seria burocrático e caro demais, sendo assim, o Ágil já gerencia os riscos de forma mais leve e eficiente através das *Sprints*.
