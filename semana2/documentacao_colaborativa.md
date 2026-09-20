# Documentação Colaborativa: Aplicativo de Carona Universitária

## 1. Divisão de Papéis e Personas

*   **Engenheiro de Requisitos (Douglas Karan):** Responsável por conduzir as entrevistas, documentar as necessidades e mediar os conflitos de interesse entre as partes.
*   **Gestor do Sistema:(Lariça)**
   *   **Persona:** Mariana, 28 anos, administradora de TI da universidade.
   *   **O que quer do sistema:** Uma plataforma segura, fácil de manter e integrada ao sistema de autenticação da universidade (SSO), garantindo que apenas alunos ativos usem.
   *   **O que a frustra hoje:** Aplicativos de terceiros que geram retrabalho para o suporte técnico interno ou que possuem vulnerabilidades no vazamento de dados dos alunos.
*   **Dono do Sistema (Sponsor/DCE) (Eduardo):**
   *   **Persona:** Prof. Roberto, 55 anos, Pró-Reitor de Assuntos Estudantis.
   *   **O que quer do sistema:** Uma solução de baixo custo operacional que melhore a mobilidade, promova a sustentabilidade e reduza a superlotação do estacionamento do campus.
   *   **O que o frustra hoje:** O alto custo financeiro com o fretamento de ônibus universitários e as constantes reclamações de falta de vagas de estacionamento.


## 2. Entrevistas (Notas do Engenheiro de Requisitos)

*   **Lucas (Usuário Final):** Durante a entrevista, Lucas frisou que a agilidade é essencial. Ele deseja abrir o app e imediatamente ver quem está indo para a universidade no seu horário. Mencionou que a segurança é uma preocupação, sugerindo um sistema de avaliação com estrelas. Solicitou também que o pagamento/rateio seja feito de forma automática ou via integração com PIX, para evitar o momento constrangedor da cobrança entre amigos.
*   **Mariana (Gestora do Sistema):** O ponto inegociável para ela é a segurança da informação. A autenticação *deve* ser vinculada ao login acadêmico. Se um aluno for suspenso ou trancar a matrícula, ele deve perder o acesso instantaneamente. Ela também requisitou a geração de logs detalhados de todas as viagens para facilitar auditorias caso ocorram incidentes.
*   **Roberto (Dono do Sistema):** Deixou claro que o orçamento para o projeto é limitado. Ele não quer pagar altas taxas mensais por APIs de mapas de terceiros. Seu foco é a "sustentabilidade financeira" do projeto. Ele sugeriu que carros com mais de 3 passageiros ganhassem acesso a vagas exclusivas no campus, mas reforçou que a infraestrutura de TI do app deve ser barata.
*   **Carlos (Regulador):** Exigiu que o aplicativo tenha Termos de Uso explícitos que classifiquem o serviço como "carona solidária" (rateio de custos) e não como serviço de transporte privado de passageiros. Para evitar problemas legais, sugeriu que o aplicativo imponha um teto no valor cobrado, baseado na distância, impedindo que o motorista tenha lucro.

## 3. Registro de Conflito

*   **O Conflito:** Tensão entre **Roberto (Dono do Sistema)** e **Lucas (Usuário Final)**.
*   **O Cenário:** Lucas solicitou veementemente que o aplicativo tivesse uma funcionalidade de rastreamento em tempo real do trajeto no mapa (estilo Uber), alegando ser fundamental para a segurança e para saber se a carona está chegando. Roberto, ao analisar os custos, exigiu que essa funcionalidade fosse cortada, pois o consumo intensivo de APIs de geolocalização e mapas em tempo real custaria muito caro mensalmente, inviabilizando o baixo custo operacional do projeto.
*   **Mediação (Engenheiro de Requisitos):** O mediador interveio validando ambas as preocupações: a necessidade de segurança e previsibilidade do Lucas, e a restrição orçamentária estrita do Roberto.
*   **Resolução:** O mediador propôs um meio-termo. O aplicativo não terá mapa de acompanhamento em tempo real integrado. Em vez disso, o sistema utilizará serviços de mapas gratuitos apenas no momento da criação da carona para calcular a distância e o limite de rateio. Para resolver a dor do usuário final, o app terá um botão "Compartilhar Viagem" que abrirá o WhatsApp do usuário (ferramenta externa e gratuita), permitindo que ele envie sua localização ao vivo do próprio celular. Além disso, o app terá botões simples de mudança de status operados pelo motorista ("Saindo", "Cheguei"). Ambas as partes aceitaram a solução, mantendo a segurança do usuário sem gerar custos extras de API para o dono do sistema.

