# 05. Requisitos Funcionais — Dona Chica

**Projeto:** Dona Chica  
**Documento:** Requisitos Funcionais  
**Versão:** 1.0  
**Status:** Em desenvolvimento  
**Referência:** Visão de Produto, Pesquisa de Campo, Regras de Negócio e Personas.

---

## 1. Objetivo

Este documento especifica os requisitos funcionais da plataforma Dona Chica, descrevendo as funcionalidades e comportamentos que o sistema deverá oferecer aos seus usuários.

Os requisitos foram organizados com base nas necessidades identificadas durante a pesquisa de campo, nas personas desenvolvidas e nas regras de negócio estabelecidas para o produto.

## 2. Tipos de usuários

A plataforma contará com dois tipos de contas, cada uma com seu próprio painel e conjunto de funcionalidades.

### 2.1. Cliente

Usuário que utiliza a plataforma para encontrar profissionais, solicitar serviços e acompanhar contratações.

### 2.2. Profissional

Usuário que utiliza a plataforma para divulgar suas habilidades, cadastrar serviços, receber solicitações e gerenciar atendimentos.

### 2.3. Administrador

Perfil responsável pelo gerenciamento da plataforma, acompanhamento de ocorrências e aplicação das medidas administrativas previstas nas regras de negócio.

---

## 3. Requisitos funcionais

### 3.1. Cadastro e autenticação

| ID | Requisito | Prioridade |
|---|---|---|
| RF-001 | O sistema deve permitir o cadastro de contas de clientes. | Alta |
| RF-002 | O sistema deve permitir o cadastro de contas profissionais. | Alta |
| RF-003 | O sistema deve permitir autenticação de usuários por meio de credenciais. | Alta |
| RF-004 | O sistema deve permitir recuperação de acesso à conta. | Alta |
| RF-005 | O sistema deve identificar o tipo de conta e direcionar o usuário ao painel correspondente. | Alta |
| RF-006 | O sistema deve permitir que o usuário visualize e atualize seus dados cadastrais. | Média |

### 3.2. Gerenciamento de perfis

| ID | Requisito | Prioridade |
|---|---|---|
| RF-007 | O sistema deve disponibilizar um perfil específico para clientes. | Alta |
| RF-008 | O sistema deve disponibilizar um perfil profissional personalizável. | Alta |
| RF-009 | O profissional deve poder cadastrar múltiplas habilidades e experiências. | Alta |
| RF-010 | O profissional deve poder selecionar diferentes categorias de atuação. | Alta |
| RF-011 | O profissional deve poder adicionar informações e descrições sobre os serviços oferecidos. | Média |
| RF-012 | O sistema deve permitir a visualização pública das informações profissionais autorizadas. | Alta |

### 3.3. Cadastro e gerenciamento de serviços

| ID | Requisito | Prioridade |
|---|---|---|
| RF-013 | O profissional deve poder cadastrar serviços na plataforma. | Alta |
| RF-014 | O profissional deve poder editar e atualizar seus serviços. | Média |
| RF-015 | O profissional deve poder remover serviços cadastrados. | Média |
| RF-016 | O sistema deve disponibilizar categorias para organização dos serviços. | Alta |
| RF-017 | O sistema deve permitir a inclusão de diferentes modalidades de serviços, incluindo atividades domésticas, culinárias, religiosas e esotéricas. | Média |

### 3.4. Busca e descoberta de profissionais

| ID | Requisito | Prioridade |
|---|---|---|
| RF-018 | O cliente deve poder pesquisar profissionais disponíveis na plataforma. | Alta |
| RF-019 | O sistema deve permitir filtros por categoria de serviço. | Alta |
| RF-020 | O sistema deve permitir a visualização dos perfis profissionais encontrados. | Alta |
| RF-021 | O sistema deve apresentar informações relevantes para auxiliar a escolha do profissional. | Alta |
| RF-022 | O sistema deve considerar critérios de compatibilidade entre a solicitação do cliente e os serviços oferecidos pelos profissionais. | Média |

### 3.5. Sistema de Match

| ID | Requisito | Prioridade |
|---|---|---|
| RF-023 | O sistema deve permitir que clientes demonstrem interesse em profissionais ou serviços. | Alta |
| RF-024 | O sistema deve permitir que profissionais demonstrem interesse em solicitações de serviços compatíveis. | Alta |
| RF-025 | O sistema deve identificar a existência de interesse mútuo entre cliente e profissional. | Alta |
| RF-026 | O sistema deve registrar os matches estabelecidos. | Alta |
| RF-027 | O sistema deve disponibilizar aos usuários as informações necessárias para dar continuidade à contratação após o match. | Alta |

### 3.6. Contratação e gerenciamento de atendimentos

| ID | Requisito | Prioridade |
|---|---|---|
| RF-028 | O cliente deve poder solicitar serviços aos profissionais. | Alta |
| RF-029 | O profissional deve poder visualizar as solicitações recebidas. | Alta |
| RF-030 | O profissional deve poder aceitar ou recusar solicitações. | Alta |
| RF-031 | O sistema deve permitir o acompanhamento do status das solicitações. | Alta |
| RF-032 | O sistema deve registrar o histórico de atendimentos dos usuários. | Média |
| RF-033 | O sistema deve permitir o gerenciamento dos atendimentos em andamento. | Alta |

### 3.7. Segurança e verificação

| ID | Requisito | Prioridade |
|---|---|---|
| RF-034 | O sistema deve disponibilizar mecanismos de verificação de identidade dos profissionais. | Alta |
| RF-035 | O sistema deve permitir a implementação de procedimentos de checagem de antecedentes dos profissionais. | Alta |
| RF-036 | O sistema deve disponibilizar mecanismos de monitoramento dos atendimentos em tempo real. | Alta |
| RF-037 | O sistema deve permitir que usuários registrem denúncias e reclamações. | Alta |
| RF-038 | O sistema deve disponibilizar informações sobre os procedimentos de segurança da plataforma. | Média |

### 3.8. Avaliações e reputação

| ID | Requisito | Prioridade |
|---|---|---|
| RF-039 | O cliente deve poder avaliar profissionais após a conclusão de um atendimento. | Alta |
| RF-040 | O sistema deve permitir o registro de comentários relacionados às avaliações. | Média |
| RF-041 | O sistema deve apresentar avaliações nos perfis profissionais. | Alta |
| RF-042 | O sistema deve manter um histórico de avaliações e reclamações. | Média |

### 3.9. Gerenciamento de denúncias e Ghost Mode

| ID | Requisito | Prioridade |
|---|---|---|
| RF-043 | O sistema deve registrar e armazenar reclamações e denúncias. | Alta |
| RF-044 | O administrador deve poder consultar ocorrências registradas. | Alta |
| RF-045 | O sistema deve contabilizar as reclamações associadas a cada usuário. | Alta |
| RF-046 | O sistema deve permitir a aplicação do Ghost Mode conforme os critérios estabelecidos nas regras de negócio. | Alta |
| RF-047 | O sistema deve restringir temporariamente as funcionalidades de contratação ou prestação de serviços dos usuários penalizados. | Alta |
| RF-048 | O sistema deve controlar o período de duração das restrições aplicadas. | Alta |

### 3.10. Administração da plataforma

| ID | Requisito | Prioridade |
|---|---|---|
| RF-049 | O administrador deve possuir acesso a um painel administrativo. | Alta |
| RF-050 | O administrador deve poder consultar usuários cadastrados. | Alta |
| RF-051 | O administrador deve poder gerenciar denúncias e ocorrências. | Alta |
| RF-052 | O administrador deve poder acompanhar restrições aplicadas aos usuários. | Alta |
| RF-053 | O administrador deve poder gerenciar categorias de serviços. | Média |

---

## 4. Regras de prioridade

Os requisitos foram classificados em três níveis:

- **Alta:** funcionalidade essencial para o funcionamento e a segurança da plataforma.
- **Média:** funcionalidade importante, mas que pode ser implementada em etapas posteriores.
- **Baixa:** funcionalidade complementar, sem impacto direto no funcionamento inicial do produto.

## 5. Critérios gerais de aceitação

Uma funcionalidade será considerada implementada quando:

1. Atender ao comportamento descrito no requisito.
2. Respeitar as regras de negócio relacionadas.
3. Respeitar as permissões do tipo de usuário.
4. Apresentar respostas adequadas para operações realizadas com sucesso ou erro.
5. Ter seu funcionamento validado por testes.

## 6. Considerações técnicas

Os requisitos apresentados representam as funcionalidades planejadas para a Dona Chica.

Algumas funcionalidades dependem de definições técnicas e operacionais posteriores, especialmente:

- Integração com serviços de verificação de identidade e antecedentes.
- Tecnologia e mecanismos utilizados no monitoramento em tempo real.
- Critérios definitivos de funcionamento do sistema de Match.
- Tratamento, validação e moderação de denúncias.
- Políticas de contratação, cancelamento e pagamento.

Essas definições serão detalhadas nos documentos de arquitetura, requisitos não funcionais e documentação da API.

## 7. Relação com outros documentos

- **Documento 01 — Visão de Produto:** apresenta a proposta e os objetivos da plataforma.
- **Documento 02 — Pesquisa de Campo:** fundamenta as necessidades dos usuários.
- **Documento 03 — Regras de Negócio:** estabelece as condições de funcionamento.
- **Documento 04 — Personas:** representa os principais perfis de usuários.
- **Documento 06 — Requisitos Não Funcionais:** especificará os critérios de qualidade e desempenho do sistema.

---

**Dona Chica — Documentação do Produto**  
*Segurança, autonomia e valorização profissional.*
