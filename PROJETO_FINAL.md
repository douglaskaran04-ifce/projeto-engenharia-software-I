# Projeto Final

## Índice

1. [Identificação](#1-identificação)
2. [Visão Geral do Sistema](#2-visão-geral-do-sistema)
3. [Fundamentos do Sistema (Semana 1)](#3-fundamentos-do-sistema-semana-1)
4. [Requisitos e Viabilidade (Semana 2)](#4-requisitos-e-viabilidade-semana-2)
5. [Modelagem UML (Semana 3)](#5-modelagem-uml-semana-3)
6. [Modelo de Processo (Semana 4)](#6-modelo-de-processo-semana-4)
7. [Cenário de Mudança](#7-cenário-de-mudança)

---

## 1. Identificação

| Campo | Preencher |
|---|---|
| Grupo | Equipe 4 |
| Tema | App de Carona Universitária |
| Integrantes | Lariça Geórgia, José Eduardo, Douglas Karan, Carlos Jefferson, Antônio Hércules |
| Disciplina | Engenharia de Software I |

## 2. Visão Geral do Sistema

> _Aplicativo de caronas universitárias é um projeto para conectar estudantes e funcionários que oferecem e buscam caronas para a universidade. O objetivo é promover segurança, economia de custos, redução de trânsito e sustentabilidade._

---

## 3. Fundamentos do Sistema (Semana 1)

> _O sistema exige Engenharia de Software para gerenciar sua alta complexidade — como geolocalização e match em tempo real — e suportar picos intensos de acesso sem sofrer com quedas, vazamentos de dados ou uma base de código insustentável. Essa robustez, que viabiliza o trabalho coordenado da equipe de desenvolvimento, é sustentada pela aplicação de quatro pilares: a modularidade, que isola responsabilidades em componentes independentes (autenticação, match, chat, avaliações e notificações); a qualidade, focada em confiabilidade, proteção de dados sensíveis e uma usabilidade ágil que não distrai o motorista; a manutenibilidade, que estrutura o projeto para manutenções evolutivas (como integração com PIX) e adaptativas (atualizações de APIs e sistemas operacionais); e as boas práticas, que combinam documentação atualizada, versionamento com Git e rigorosa padronização de código para garantir que todos programem de forma uniforme e livre de conflitos._

🔗 [semana1/](semana1/)

## 4. Requisitos e Viabilidade (Semana 2)

> _O processo de elicitação do aplicativo de caronas envolveu entrevistas com estudantes, setor de TI, patrocinadores e reguladores, resolvendo conflitos de interesse ao substituir mapas integrados onerosos pelo compartilhamento de localização via WhatsApp, equilibrando assim a segurança demandada pelo usuário com o baixo custo exigido pelo projeto. Essa etapa baseou os requisitos funcionais consolidados, focados em login acadêmico (SSO), cálculo de rateio sem fins lucrativos, gestão de reservas e avaliações bilaterais, sustentados por requisitos não-funcionais que exigem buscas rápidas (até 3 segundos), responsividade multiplataforma (Android/iOS), alta disponibilidade e dados criptografados. Ao analisar as dimensões técnica, econômica e operacional, o estudo concluiu que a solução tem altíssimo potencial social e rápida adesão por ser similar a apps do mercado, mas é considerada "viável com ressalvas", uma vez que o aplicativo não gerará lucro e a sua segurança depende inteiramente da aprovação da TI da universidade para integrar o sistema institucional e custear a infraestrutura em nuvem._

🔗 [semana2/requisitos.md](semana2/requisitos.md) · [semana2/viabilidade.md](semana2/viabilidade.md)

## 5. Modelagem UML (Semana 3)

> _Os diagramas detalharam o comportamento e a arquitetura do aplicativo: o Diagrama de Casos de Uso mapeou as interações dos atores (Passageiro, Motorista e o SSO acadêmico) com as funcionalidades centrais do sistema, como criar viagens, solicitar vagas, avaliar usuários e compartilhar rotas via WhatsApp; o Diagrama de Classes definiu a estrutura de dados, aplicando herança a partir de uma classe base Usuario e relacionando entidades essenciais como Carona, Reserva e HistoricoViagem (fundamental para registrar trajetos e notas); por fim, cinco Diagramas de Sequência ilustraram a linha do tempo lógica e as trocas de mensagens entre sistema e banco de dados para os processos críticos do app: autenticação institucional elaborado por Douglas Karan, oferta de carona com cálculo de rateio elaborado por Eduardo, fluxos de reserva elaborado por Lariça, fluxo de aprovação elaborado por Carlos e conclusão do trajeto com avaliação bilateral elaborado pelo Hércules._

🔗 [semana3/Diagrama de Casos de Uso/Diagrama_de_Casos_de_uso.drawio](semana3/), incluindo `Diagrama_de_Casos_de_uso.drawio`

🔗 [semana3/Diagrama de Classes/Diagrama_de_Classe.drawio](semana3/), incluindo `Diagrama_de_Classe.drawio`

🔗 [semana3/Diagramas de Sequência/Ação_1_Autenticação_e_Cadastro_via_SSO_Institucional.drawio](semana3/), incluindo `Ação_1_Autenticação_e_Cadastro_via_SSO_Institucional.drawio`

🔗 [semana3\Diagramas de Sequência\Ação_2_Oferta de Viagem e Cálculo de Rateio (RF-03, RF-04).drawio](semana3/), incluindo `Ação_2_Oferta de Viagem e Cálculo de Rateio (RF-03, RF-04).drawio`

🔗 [semana3/Diagramas de Sequência/Ação_5 Conclusão da Viagem, Histórico e Avaliação.drawio](semana3/) incluindo `Conclusão da Viagem, Histórico e Avaliação.drawio`

## 6. Modelo de Processo (Semana 4)

> _O modelo de processo escolhido para o App de Caronas Universitárias é o Ágil._
>
>_A justificativa fundamenta-se principalmente na baixa estabilidade dos requisitos — o sistema exige manutenções evolutivas constantes (integração futura de pagamentos via PIX) e adaptativas (mudanças em APIs do Google Maps e sistemas operacionais mobile), além de envolver funcionalidades negociáveis, como visto no corte do mapa em tempo real para baratear custos. O perfil da equipe (um grupo de estudantes universitários desenvolvendo o projeto em conjunto de forma iterativa) encaixa-se perfeitamente no formato de equipes multidisciplinares, ágeis e auto-organizadas de 5 a 15 pessoas._
>
>_Por que os outros foram descartados?_
>
>_Cascata: Descartado porque exige requisitos "congelados" desde o início. A rigidez impediria a equipe de adaptar o sistema ao feedback dos usuários ou de lidar rapidamente com o alto risco de a TI da universidade atrasar a integração do login (SSO)._
>
>_Incremental Puro: Embora lide melhor com entregas do que o Cascata, o modelo incremental tradicional ainda exige um planejamento arquitetural pesado logo no início para todos os incrementos, não tendo a mesma flexibilidade do Ágil para descartar ou reinventar rotas no meio do projeto._
>
>_Espiral: O modelo Espiral, voltado para sistemas críticos e complexos, é muito caro e burocrático para o desenvolvimento de um app de caronas por uma equipe pequena. Nesse cenário, a metodologia Ágil é a opção ideal, pois gerencia os riscos de forma mais leve e eficiente através das Sprints._ 
>
>_Framework Escolhido: Scrum Dentro da abordagem ágil, o framework ideal para este sistema é o Scrum. Ele se adequa bem porque traz uma organização essencial para equipes pequenas/acadêmicas por meio de rituais claros (Sprints, Dailies, Reviews), garantindo que o desenvolvimento não perca o foco._
>
>_Como lidar com mudanças: Caso surja uma alteração (por exemplo, o órgão de trânsito exige uma nova restrição ou a universidade altera sua política de SSO), essa mudança não paralisa o trabalho atual. A nova necessidade é transformada em uma nova "História de Usuário" e inserida no Product Backlog. Na próxima reunião de planejamento (Sprint Planning), o grupo avalia e prioriza essa mudança para ser desenvolvida na Sprint seguinte. Isso garante flexibilidade imediata e controle sobre o que está sendo alterado._

🔗 [semana4/](semana4/)

---

## 7. Cenário de Mudança

### O cenário recebido

> _App de Carona - A universidade parceira do aplicativo passou a exigir que só caroneiros e motoristas vinculados oficialmente a ela, com matrícula ativa, possam usar o serviço, e pediu um relatório mensal de todas as viagens realizadas pelos seus usuários._

### Tipo de manutenção

> _Analisando o escopo original do projeto, podemos ver que o sistema já previa o login via SSO (RF-01 e RF-02), mas não exigia a checagem do status ativo da matrícula, tampouco possuía um requisito funcional para a emissão de relatórios gerenciais para a universidade. Com base nisso, esse novo cenário de mudança imposto pela universidade parceira engloba dois tipos de manutenção distintos: Manutenção Adaptativa e Manutenção Perfectiva. A manutenção adaptativa ocorre quando o software precisa ser modificado para continuar funcionando frente a mudanças em seu ambiente externo. No projeto original, bastava ter uma credencial do SSO (RF-01 e RF-02) para acessar o app. Como a universidade parceira — que é o ambiente externo fornecedor da autenticação — alterou a sua política de uso/regra de negócio, restringindo agora apenas a alunos ativos, o aplicativo precisará adaptar sua comunicação com a API do SSO para verificar esse novo status. O software não estava com defeito; ele apenas precisou se adequar a uma nova realidade imposta pelo meio externo. A manutenção perfectiva acontece quando o sistema sofre modificações para atender a novos requisitos dos usuários e ou gestores, melhorando o software ou adicionando novas funcionalidades (features). Ao analisar o Documento de Requisitos da Semana 2, não havia nenhum requisito funcional prevendo a geração de relatórios mensais para a instituição. Portanto, criar essa interface e extrair esses dados do banco de dados, que já armazena o Histórico de Viagens conforme o RF-08, configura uma evolução direta das capacidades do sistema para satisfazer uma nova necessidade da universidade._

### Análise de impacto

> _Escreva aqui_
