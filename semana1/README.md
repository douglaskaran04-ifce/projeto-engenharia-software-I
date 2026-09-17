# App de Caronas Universitárias

## 1. Escolha do Sistema
**Sistema escolhido:** App de caronas universitárias.
Este projeto consiste em um aplicativo projetado para conectar estudantes e funcionários que oferecem e buscam caronas para a universidade. O objetivo é promover segurança, economia de custos, redução de trânsito e sustentabilidade.

## 2. Justificativa da Escolha (Lógica "casinha x prédio")

* Como na construção de um prédio, o aplicativo necessita ser visto em sua completude. Portanto o sistema apresenta porte médio e complexidade moderada a alta. Ele necessita de integração com serviços de geolocalização (mapas), algoritmos para conectar ("match") rotas compatíveis de motoristas e passageiros, gerenciamento de perfis, sistema de avaliações e chat em tempo real. 
* O aplicativo seria utilizado por milhares de usuários diariamente, concentrando picos de acesso nos horários de entrada e saída das aulas. Para mantê-lo, a equipe provavelmente variaria de 5 a 15 profissionais, incluindo desenvolvedores (mobile e backend), designers de UX/UI, QA e gerentes de produto trabalhando ativamente ao longo do tempo. 
* Se construído sem planejamento — como uma "casinha" em vez de um "prédio" — o sistema poderia falhar drasticamente. Isso geraria indisponibilidade em horários de pico, vazamento de dados sensíveis dos estudantes, e um código tão confuso que qualquer nova alteração poderia quebrar funcionalidades já existentes (efeito dominó).
* Para ter um bom resultado, programar algoritmos corretos não é suficiente. O projeto precisa de arquitetura escalável para suportar muitos acessos simultâneos, segurança robusta para proteger a identidade dos alunos e um planejamento de manutenibilidade para que diferentes desenvolvedores consigam trabalhar juntos sem conflitos. Requer engenharia de software aplicada.

## 3. Aplicação dos Quatro Princípios

### Modularidade e Abstração
Módulos prováveis do sistema com responsabilidades bem separadas:

* **Autenticação e Perfil:** Responsável por login, validação de vínculo universitário (e-mail institucional) e dados do usuário.
* **Gestão de Rotas (Match):** Algoritmo que cruza origens, destinos e horários para sugerir as melhores caronas.
* **Mensageria:** Módulo isolado de chat entre motorista e passageiro após confirmação da carona.
* **Reputação e Avaliação:** Sistema de notas e feedbacks para garantir um ambiente seguro.
* **Notificações:** Alertas em tempo real (push notifications) sobre o status da viagem.

### Qualidade de Software
Os principais pontos de qualidade que considero importantes para esse sistema são:

* **Confiabilidade:** O aplicativo precisa funcionar corretamente e estar disponível quando os estudantes precisarem. Ele não pode apresentar muitos erros ou deixar de enviar informações importantes, como avisos de provas e aulas.
* **Usabilidade:** O aplicativo deve ser fácil de usar e ter uma interface simples. O usuário deve conseguir encontrar as informações sem precisar fazer muitos passos. Isso é ainda mais importante para o motorista, que não deve perder a atenção enquanto estiver dirigindo.
* **Segurança:** O sistema precisa proteger os dados dos usuários e permitir que somente pessoas autorizadas tenham acesso. Dessa forma, evita-se que pessoas de fora da universidade utilizem a plataforma de forma indevida.
    
### Manutenibilidade e Evolução

* **Manutenção mais provável:** Evolutiva e Adaptativa.
* **Exemplo concreto:** Nos primeiros anos, haverá forte manutenção *evolutiva* para adicionar recursos como integração de pagamentos (PIX) para divisão de combustível, ou rotas exclusivas para eventos da faculdade. Também ocorrerá manutenção *adaptativa* contínua para atualizar o aplicativo conforme novas versões dos sistemas operacionais (Android/iOS) ou atualizações nas APIs de mapas (como Google Maps).
  
### Boas Práticas Gerais

* **Documentação:** O grupo documentaria as decisões de arquitetura importantes, como a escolha do banco de dados geográfico, e manteria uma documentação clara da API para alinhar o trabalho entre frontend e backend.
* **Versionamento:** Uso do Git com um fluxo de trabalho estruturado, garantindo que a branch `main` sempre tenha código funcional. As mensagens de commit seguiriam um padrão descritivo (ex: `feat: adiciona filtro de caronas apenas para mulheres`).
* **Padronização:** Adoção de nomenclaturas em inglês para o código fonte (classes, métodos e variáveis) e uso de ferramentas de formatação automática para que todo o código tenha a mesma "cara", independentemente de qual integrante escreveu.
