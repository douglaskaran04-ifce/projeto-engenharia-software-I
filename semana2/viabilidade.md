# Estudo de Viabilidade

## Índice

1. [Identificação](#1-identificação)
2. [O Sistema](#2-o-sistema)
3. [Viabilidade Técnica](#3-viabilidade-técnica)
4. [Viabilidade Econômica](#4-viabilidade-econômica)
5. [Viabilidade Operacional](#5-viabilidade-operacional)
6. [Conclusão](#6-conclusão)

---

## 1. Identificação

| Campo | Preencher |
|---|---|
| Grupo | Equipe 4 |
| Integrantes | — Lariça Geórgia, José Eduardo, Douglas Karan, Carlos Jefferson, Antônio Hércules|
| Disciplina | Engenharia de Software I |
| Semana | 2 |
| Data | 19/09/2026 |


## 2. O Sistema

Aplicativo de caronas voltado para a comunidade universitária, permitindo que estudantes e funcionários ofereçam e solicitem caronas entre si. O sistema tem como objetivo facilitar o deslocamento, dividir custos de forma justa sem fins lucrativos, e garantir a segurança através da restrição de acesso apenas por autenticação institucional (SSO).

Requisitos consolidados no [Requisitos.md](requisitos.md):

### Requisitos Funcionais (RF)

| ID | Descrição |
|---|---|
| RF-01 | O sistema deve permitir o cadastro de usuários exclusivamente através das credenciais do sistema de autenticação (SSO) da universidade. |
| RF-02 | O sistema deve permitir o acesso (login) de usuários exclusivamente através das credenciais do sistema de autenticação (SSO) da universidade. |
| RF-03 | O sistema deve calcular um valor máximo financeiro para o rateio de cada viagem com base na quilometragem total do trajeto percorrido. |
| RF-04 | O sistema deve exibir o valor máximo financeiro calculado para o rateio de cada viagem. |
| RF-05 | O sistema deve permitir que um passageiro solicite a reserva de uma vaga em uma viagem previamente ofertada. |
| RF-06 | O sistema deve permitir que o motorista aprove solicitações de carona recebidas para a sua viagem. |
| RF-07 | O sistema deve permitir que o motorista recuse solicitações de carona recebidas para a sua viagem. |
| RF-08 | O sistema deve armazenar o histórico de viagens concluídas contendo a data, o horário, o identificador do motorista e os identificadores dos passageiros embarcados. |
| RF-09 | O sistema deve permitir que o passageiro atribua uma nota de 1 a 5 ao motorista após a conclusão do trajeto. |
| RF-10 | O sistema deve permitir que o motorista atribua uma nota de 1 a 5 ao passageiro após a conclusão do trajeto. |

### Requisitos Não-Funcionais (RNF)


---

## 3. Viabilidade Técnica
A equipe possui conhecimentos básicos para desenvolvimento mobile e backend, tornando a construção de um aplicativo de caronas (que envolve perfis de usuários, criação de viagens e sistema de avaliações) realizável. O desenvolvimento deverá abranger as plataformas Android (RNF-06) e iOS (RNF-07), sendo recomendada a utilização de frameworks multiplataforma (como React Native ou Flutter) para evitar duplicar o esforço na criação do aplicativo cliente e adaptar-se melhor a múltiplas resoluções de tela (RNF-02).


O maior desafio técnico identificado é a obrigatoriedade de integração com o sistema de autenticação da universidade (RF-01 e RF-02). Esse tipo de integração exige que a instituição libere acesso a chaves de API, ambientes de homologação e documentação que nem sempre estão disponíveis abertamente, podendo atrasar ou inviabilizar o login se houver burocracia excessiva. Outro ponto é a segurança no armazenamento de dados sensíveis e autenticação (RNF-03). Por fim, o requisito de resposta em até 3 segundos nas buscas por viagens (RNF-01) exigirá consultas espaciais eficientes caso o sistema integre localizações no mapa.


**Risco identificado:** Dificuldades burocráticas ou técnicas de integração com o sistema de autenticação da universidade e garantia de consultas de busca otimizadas.
**Mitigação:** Iniciar o contato com a TI da universidade o mais cedo possível para alinhar o acesso ao sistema de autenticação da universidade, e criar provas de conceito antecipadas da busca no banco de dados.



## 4. Viabilidade Econômica
Diferente de aplicativos comerciais, este projeto é voltado estritamente à comunidade acadêmica, com divisão restrita de custos e vedação explícita de fins lucrativos em Termo de Uso (RF-03 e RNF-05). Isso significa que o sistema não gerará lucro com taxas por corrida ou assinaturas, impossibilitando a arrecadação de verba direta por parte dos desenvolvedores.

Os custos de desenvolvimento inicial se traduzem em tempo e esforço da equipe estudantil. Já a manutenção contínua dependerá de infraestrutura básica em nuvem (servidores para o backend e banco de dados) e das taxas anuais das lojas de aplicativos App Store e Google Play. O benefício primário é o retorno social expressivo: a comunidade universitária vai economizar bastante nos custos diários de deslocamento, promovendo interação e reduzindo o impacto ambiental. A viabilidade a longo prazo pode ser sustentada caso a própria instituição "abrace" a infraestrutura (fornecendo os servidores) em reconhecimento ao benefício gerado para os estudantes.


## 5. Viabilidade Operacional
Muitos usuários (estudantes, professores e funcionários) já são usuários assíduos de apps de transporte (Uber, 99) ou carona (BlaBlaCar), o que significa que o fluxo do aplicativo, desde solicitar reservas (RF-05) até o sistema de avaliações bilaterais (RF-09, RF-10), é extremamente familiar. A curva de aprendizagem tende a ser rápida.

Haveria inicialmente natural desconfiança quanto à segurança de embarcar no carro de um "desconhecido". Contudo, o diferencial operacional é o filtro institucional: ao exigir autenticação via SSO (RF-01, RF-02), o sistema garante que apenas membros da comunidade universitária utilizem o app, o que cria um "filtro de segurança" forte. Somado ao fato de motoristas poderem aprovar e recusar solicitações de carona (RF-06, RF-07) e das avaliações pós-viagem, a confiança tende a se estabelecer rapidamente.

---


## 6. Conclusão

- [ ] Viável
- [X] Viável com ressalvas
- [ ] Não viável

O projeto de caronas universitárias é altamente justificável em sua viabilidade operacional e nos seus propósitos econômico-sociais. No entanto, é considerado "viável com ressalvas" devido ao alto nível de dependência de terceiros (neste caso, a burocracia e disponibilidade da TI da universidade) para concretizar os requisitos centrais de cadastro e login. Se a universidade negar integração, o pilar de segurança e restrição de público precisará ser repensado ou o projeto se tornará inviável da maneira como foi proposto.
