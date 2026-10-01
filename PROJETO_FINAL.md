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

> _Escreva aqui_

🔗 [semana1/](semana1/)

## 4. Requisitos e Viabilidade (Semana 2)

> _Escreva aqui_

🔗 [semana2/requisitos.md](semana2/requisitos.md) · [semana2/viabilidade.md](semana2/viabilidade.md)

## 5. Modelagem UML (Semana 3)

> _os diagramas detalharam o comportamento e a arquitetura do aplicativo: o Diagrama de Casos de Uso mapeou as interações dos atores (Passageiro, Motorista e o SSO acadêmico) com as funcionalidades centrais do sistema, como criar viagens, solicitar vagas, avaliar usuários e compartilhar rotas via WhatsApp; o Diagrama de Classes definiu a estrutura de dados, aplicando herança a partir de uma classe base Usuario e relacionando entidades essenciais como Carona, Reserva e HistoricoViagem (fundamental para registrar trajetos e notas); por fim, cinco Diagramas de Sequência ilustraram a linha do tempo lógica e as trocas de mensagens entre sistema e banco de dados para os processos críticos do app: autenticação institucional elaborado por Douglas Karan, oferta de carona com cálculo de rateio elaborado por Eduardo, fluxos de reserva elaborado por Lariça, fluxo de aprovação elaborado por Carlos e conclusão do trajeto com avaliação bilateral elaborado pelo Hércules._

🔗 [semana3/Diagrama de Casos de Uso/Diagrama_de_Casos_de_uso.drawio](semana3/Diagrama_de_Casos_de_uso.drawio), incluindo `Diagrama_de_Casos_de_uso.drawio`

🔗 [semana3/Diagrama de Classes/Diagrama_de_Classe.drawio](semana3/Diagrama de Classes/Diagrama_de_Classe.drawio), incluindo `Diagrama_de_Classe.drawio`

🔗 [semana3/Diagramas de Sequência/Ação_1_Autenticação_e_Cadastro_via_SSO_Institucional.drawio](semana3/Diagramas de Sequência/Ação_1_Autenticação_e_Cadastro_via_SSO_Institucional.drawio), incluindo `Ação_1_Autenticação_e_Cadastro_via_SSO_Institucional.drawio`

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

> _Escreva aqui_

### Análise de impacto

> _Escreva aqui_
