# 07. Escopo do MVP — Dona Chica

**Projeto:** Dona Chica  
**Documento:** Escopo do MVP  
**Versão:** 1.0  
**Status:** Planejamento  
**Plataforma inicial:** Web  
**Plataforma futura:** Android (APK)

---

## 1. Objetivo

Este documento define o escopo do Produto Mínimo Viável (MVP — Minimum Viable Product) da Dona Chica, estabelecendo as funcionalidades essenciais para disponibilizar a primeira versão funcional da plataforma.

O MVP será desenvolvido inicialmente como uma aplicação web responsiva, destinada à utilização real por clientes e profissionais.

A proposta é disponibilizar uma plataforma funcional que permita o cadastro de usuários, divulgação de serviços, busca de profissionais, conexão por meio de um sistema de Match e gerenciamento de atendimentos.

Posteriormente, a infraestrutura desenvolvida será aproveitada para a expansão da plataforma para dispositivos Android.

## 2. Estratégia de lançamento

O desenvolvimento será dividido em etapas evolutivas.

### Fase 1 — Aplicação Web

Desenvolvimento e disponibilização da primeira versão funcional da Dona Chica.

Características:
- Aplicação web responsiva.
- Acesso pela internet.
- Cadastro e autenticação de usuários.
- Painéis independentes para clientes e profissionais.
- Gerenciamento de perfis e serviços.
- Sistema de busca e Match.
- Gerenciamento de solicitações e atendimentos.
- API e banco de dados centralizados.

### Fase 2 — Aplicativo Android

Evolução da plataforma para dispositivos Android.

Características:
- Desenvolvimento de uma interface mobile.
- Integração com a API existente.
- Aproveitamento das regras de negócio já implementadas.
- Implementação de notificações e recursos específicos de dispositivos móveis.
- Geração e distribuição do APK.

### Fase 3 — Expansão da plataforma

Implementação de melhorias e funcionalidades complementares.

Características:
- Expansão das categorias de serviços.
- Aprimoramento dos mecanismos de segurança.
- Melhorias no sistema de reputação.
- Evolução do monitoramento de atendimentos.
- Otimização de desempenho e escalabilidade.

## 3. Público-alvo

A primeira versão será direcionada a dois grupos principais:

**Clientes:** pessoas que desejam encontrar, solicitar e contratar serviços de diferentes categorias.

**Profissionais:** pessoas que desejam divulgar suas habilidades, oferecer serviços e conquistar novos clientes.

Cada grupo terá uma conta e um painel de acesso específicos, com funcionalidades e permissões correspondentes ao seu perfil.

## 4. Funcionalidades incluídas no MVP

### 4.1. Cadastro e autenticação

- Cadastro de contas de clientes.
- Cadastro de contas profissionais.
- Login e logout.
- Recuperação de senha.
- Gerenciamento de dados cadastrais.
- Controle de acesso conforme o tipo de conta.

### 4.2. Painel do cliente

- Visualização do painel de contratação.
- Pesquisa de profissionais.
- Busca por categorias de serviços.
- Visualização de perfis profissionais.
- Envio de solicitações.
- Demonstração de interesse em profissionais.
- Gerenciamento de matches.
- Acompanhamento das solicitações e atendimentos.
- Histórico de contratações.

### 4.3. Painel profissional

- Visualização do painel profissional.
- Personalização do perfil.
- Cadastro de múltiplas habilidades.
- Cadastro e gerenciamento de serviços.
- Seleção de categorias profissionais.
- Recebimento de solicitações.
- Demonstração de interesse em solicitações compatíveis.
- Aceitação ou recusa de solicitações.
- Gerenciamento de atendimentos.
- Visualização de avaliações recebidas.

### 4.4. Sistema de Match

O sistema de Match será um dos principais mecanismos de conexão da Dona Chica.

O MVP deverá permitir:

- Demonstração de interesse por parte do cliente.
- Demonstração de interesse por parte do profissional.
- Identificação de interesse mútuo.
- Registro dos matches estabelecidos.
- Disponibilização das informações necessárias para continuidade da contratação.

O Match deverá considerar a compatibilidade entre os serviços solicitados e as habilidades oferecidas pelos profissionais.

### 4.5. Gerenciamento de atendimentos

- Registro das solicitações.
- Atualização do status dos atendimentos.
- Aceitação e recusa de solicitações.
- Histórico de atendimentos.
- Identificação de atendimentos em andamento e concluídos.
- Cancelamento de solicitações conforme as condições definidas pela plataforma.

### 4.6. Segurança e reputação

- Cadastro de informações profissionais.
- Mecanismos de verificação de identidade.
- Sistema de avaliações.
- Registro de reclamações e denúncias.
- Controle de permissões.
- Histórico de ocorrências.
- Mecanismo de restrição de usuários conforme as regras de negócio.

### 4.7. Painel administrativo

- Consulta de usuários cadastrados.
- Gerenciamento de categorias.
- Consulta de denúncias e reclamações.
- Acompanhamento de ocorrências.
- Gerenciamento de restrições.
- Controle administrativo do Ghost Mode.

### 4.8. Infraestrutura

- Backend responsável pela lógica da aplicação.
- API para comunicação entre frontend e backend.
- Banco de dados centralizado.
- Autenticação e autorização.
- Validação e tratamento de dados.
- Registro de erros e eventos relevantes.
- Hospedagem da aplicação web.

## 5. Funcionalidades fora do escopo inicial

As funcionalidades abaixo não serão consideradas obrigatórias para o lançamento inicial, podendo ser incorporadas em versões futuras:

- Aplicativo Android distribuído em APK.
- Publicação na Google Play Store.
- Aplicativo iOS.
- Sistema integrado de pagamentos e repasses financeiros.
- Chat em tempo real.
- Rastreamento contínuo por GPS.
- Notificações push nativas.
- Algoritmos avançados de recomendação.
- Programa de fidelidade.
- Sistema avançado de análise de dados.
- Expansão para múltiplas regiões e mercados.

A exclusão dessas funcionalidades do escopo inicial não impede sua implementação posterior.

## 6. Requisitos mínimos para disponibilização

Por se tratar de uma aplicação destinada ao uso real, o MVP deverá atender a condições mínimas antes de sua disponibilização pública.

- Autenticação funcional e segura.
- Proteção das informações pessoais.
- Controle de permissões por tipo de conta.
- Validação dos dados enviados pelos usuários.
- Tratamento de erros.
- Banco de dados com mecanismos de backup.
- Política de privacidade e termos de uso.
- Canal de atendimento para denúncias.
- Procedimentos administrativos para análise de ocorrências.
- Testes das funcionalidades essenciais.

Funcionalidades relacionadas à segurança dos atendimentos deverão possuir procedimentos operacionais definidos antes de serem apresentadas como recursos de proteção efetivamente disponíveis.

## 7. Critérios de conclusão do MVP

A primeira versão será considerada apta para lançamento quando:

1. Clientes e profissionais conseguirem criar suas respectivas contas.
2. A autenticação e o controle de permissões estiverem funcionando.
3. Os profissionais conseguirem cadastrar e divulgar seus serviços.
4. Os clientes conseguirem pesquisar e visualizar profissionais.
5. O sistema de Match conseguir identificar interesses mútuos.
6. As solicitações e os atendimentos puderem ser gerenciados.
7. O sistema de avaliações e denúncias estiver operacional.
8. O painel administrativo permitir o gerenciamento das ocorrências.
9. Os mecanismos essenciais de segurança e privacidade estiverem implementados.
10. Os principais fluxos da aplicação tiverem sido testados e validados.

## 8. Estratégia de evolução

A Dona Chica será desenvolvida com uma arquitetura que permita a expansão da plataforma sem exigir a reconstrução integral de sua infraestrutura.

A API e o banco de dados serão utilizados como base para futuras interfaces, permitindo que a versão Android aproveite os serviços e as regras de negócio desenvolvidos inicialmente para a aplicação web.

Essa estratégia busca reduzir retrabalho, facilitar a manutenção e garantir maior consistência entre as plataformas.

## 9. Relação com outros documentos

- **Documento 01 — Visão de Produto:** apresenta o propósito e os objetivos da plataforma.
- **Documento 02 — Pesquisa de Campo:** fundamenta as necessidades identificadas.
- **Documento 03 — Regras de Negócio:** estabelece as condições de funcionamento.
- **Documento 04 — Personas:** apresenta os perfis comportamentais dos usuários.
- **Documento 05 — Requisitos Funcionais:** especifica as funcionalidades do sistema.
- **Documento 06 — Requisitos Não Funcionais:** define os critérios de qualidade e segurança.
- **Documento 08 — Fluxos de Usuário:** detalhará a navegação e as interações dos usuários.

---

**Dona Chica — Documentação do Produto**  
*Segurança, autonomia e valorização profissional.*
