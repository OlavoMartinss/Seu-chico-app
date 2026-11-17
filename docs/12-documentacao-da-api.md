# 12. Documentação da API — Dona Chica

**Projeto:** Dona Chica  
**Documento:** Documentação da API  
**Versão:** 1.0  
**Status:** Especificação inicial

---

## 1. Objetivo

Este documento apresenta a especificação inicial da API da plataforma Dona Chica, descrevendo sua finalidade, organização, operações previstas, padrões de comunicação e requisitos de segurança.

A API será responsável por intermediar a comunicação entre as interfaces da plataforma e o backend.

A documentação servirá como referência para o desenvolvimento da aplicação web e, futuramente, do aplicativo Android.

**Observação:** os endpoints apresentados são propostas de organização. Eles não representam necessariamente rotas já implementadas. Os caminhos, métodos e contratos deverão ser ajustados para corresponder à API efetivamente desenvolvida.

## 2. Visão Geral

A API da Dona Chica deverá centralizar as operações relacionadas a:

- Cadastro e autenticação.
- Gerenciamento de contas.
- Perfis de clientes e profissionais.
- Categorias e serviços.
- Busca de profissionais.
- Interesses e Matches.
- Solicitações e agendamentos.
- Avaliações.
- Denúncias.
- Administração e moderação.

A aplicação web e o futuro aplicativo Android deverão consumir os mesmos serviços, evitando a duplicação de regras de negócio.

## 3. Padrão de Comunicação

Como convenção inicial, propõe-se uma API REST com comunicação por HTTP e troca de dados em JSON.

### 3.1 Métodos HTTP

| Método | Finalidade |
|---|---|
| GET | Consultar informações |
| POST | Criar registros ou executar operações |
| PUT | Substituir um recurso |
| PATCH | Atualizar parcialmente um recurso |
| DELETE | Remover um recurso, quando permitido |

### 3.2 Formato de Dados

As requisições e respostas deverão utilizar JSON, salvo operações específicas de envio de arquivos.

Exemplo:

```json
{
  "name": "Nome do usuário",
  "email": "usuario@email.com"
}
```

### 3.3 Versionamento

A API deverá possuir uma estratégia de versionamento para permitir futuras alterações sem comprometer as aplicações existentes.

Convenção proposta:

`/api/v1/`

O padrão definitivo deverá ser confirmado durante a implementação.

## 4. Organização dos Endpoints

Os endpoints serão organizados por domínio funcional.

### 4.1 Autenticação

| Método | Endpoint proposto | Finalidade |
|---|---|---|
| POST | `/api/v1/auth/register` | Cadastrar usuário |
| POST | `/api/v1/auth/login` | Autenticar usuário |
| POST | `/api/v1/auth/logout` | Encerrar sessão |
| POST | `/api/v1/auth/forgot-password` | Solicitar recuperação de senha |
| POST | `/api/v1/auth/reset-password` | Redefinir senha |
| GET | `/api/v1/auth/me` | Consultar usuário autenticado |

### 4.2 Clientes

| Método | Endpoint proposto | Finalidade |
|---|---|---|
| GET | `/api/v1/clients/me` | Consultar perfil do cliente |
| PATCH | `/api/v1/clients/me` | Atualizar perfil |
| GET | `/api/v1/clients/me/appointments` | Consultar atendimentos |
| GET | `/api/v1/clients/me/requests` | Consultar solicitações |

### 4.3 Profissionais

| Método | Endpoint proposto | Finalidade |
|---|---|---|
| GET | `/api/v1/professionals` | Listar profissionais |
| GET | `/api/v1/professionals/{id}` | Consultar profissional |
| GET | `/api/v1/professionals/me` | Consultar próprio perfil |
| PATCH | `/api/v1/professionals/me` | Atualizar perfil profissional |
| GET | `/api/v1/professionals/me/services` | Listar serviços cadastrados |

### 4.4 Serviços e Categorias

| Método | Endpoint proposto | Finalidade |
|---|---|---|
| GET | `/api/v1/categories` | Listar categorias |
| GET | `/api/v1/services` | Listar serviços |
| GET | `/api/v1/services/{id}` | Consultar serviço |
| POST | `/api/v1/services` | Cadastrar serviço |
| PATCH | `/api/v1/services/{id}` | Atualizar serviço |
| DELETE | `/api/v1/services/{id}` | Remover serviço, quando permitido |

### 4.5 Busca

| Método | Endpoint proposto | Finalidade |
|---|---|---|
| GET | `/api/v1/search/services` | Pesquisar serviços |
| GET | `/api/v1/search/professionals` | Pesquisar profissionais |

A busca poderá receber parâmetros de consulta, como categoria, localização e outros filtros definidos para o produto.

Exemplo conceitual:

`/api/v1/search/professionals?category=1&city=Natal`

Os parâmetros definitivos dependerão da implementação.

### 4.6 Interesses e Match

| Método | Endpoint proposto | Finalidade |
|---|---|---|
| POST | `/api/v1/interests` | Registrar interesse |
| GET | `/api/v1/interests` | Consultar interesses do usuário |
| DELETE | `/api/v1/interests/{id}` | Remover interesse, quando permitido |
| GET | `/api/v1/matches` | Consultar Matches |
| GET | `/api/v1/matches/{id}` | Consultar Match específico |

A formação do Match deverá ser processada pelo backend, considerando as regras de reciprocidade definidas pelo produto.

Não será permitido que uma interface confirme unilateralmente um Match sem que as condições necessárias sejam atendidas.

### 4.7 Solicitações e Agendamentos

| Método | Endpoint proposto | Finalidade |
|---|---|---|
| POST | `/api/v1/requests` | Criar solicitação |
| GET | `/api/v1/requests` | Listar solicitações |
| GET | `/api/v1/requests/{id}` | Consultar solicitação |
| PATCH | `/api/v1/requests/{id}/status` | Atualizar situação |
| GET | `/api/v1/appointments` | Listar agendamentos |
| GET | `/api/v1/appointments/{id}` | Consultar agendamento |
| PATCH | `/api/v1/appointments/{id}` | Atualizar agendamento |

As operações deverão validar a identidade dos participantes e as regras de transição de status.

### 4.8 Avaliações

| Método | Endpoint proposto | Finalidade |
|---|---|---|
| POST | `/api/v1/reviews` | Registrar avaliação |
| GET | `/api/v1/professionals/{id}/reviews` | Consultar avaliações de profissional |
| GET | `/api/v1/reviews/{id}` | Consultar avaliação |

A API deverá validar se o atendimento relacionado permite o registro de uma avaliação.

### 4.9 Denúncias e Moderação

| Método | Endpoint proposto | Finalidade |
|---|---|---|
| POST | `/api/v1/reports` | Registrar denúncia |
| GET | `/api/v1/reports` | Consultar denúncias autorizadas |
| GET | `/api/v1/admin/reports` | Listar denúncias para administração |
| PATCH | `/api/v1/admin/reports/{id}` | Atualizar análise da denúncia |
| GET | `/api/v1/admin/users` | Consultar usuários na administração |
| PATCH | `/api/v1/admin/users/{id}/status` | Atualizar situação de usuário |

As rotas administrativas deverão exigir autorização específica.

## 5. Autenticação e Autorização

A API deverá proteger as operações que exigem identificação do usuário.

Requisitos previstos:

- Validar a identidade do usuário.
- Controlar o acesso aos recursos.
- Diferenciar permissões de clientes e profissionais.
- Restringir operações administrativas.
- Impedir alterações não autorizadas em perfis de terceiros.
- Validar a propriedade dos recursos consultados ou modificados.

A estratégia de autenticação, incluindo a utilização de sessões ou tokens, será documentada após a definição técnica.

## 6. Exemplo de Requisição

Exemplo conceitual de cadastro:

**Método:** POST

**Endpoint:** `/api/v1/auth/register`

Corpo da requisição:

```json
{
  "name": "Maria Silva",
  "email": "maria@email.com",
  "password": "senha-de-exemplo",
  "phone": "84999999999",
  "account_type": "client"
}
```

A API deverá validar os dados e verificar as regras de cadastro antes de criar a conta.

O exemplo é ilustrativo. Os campos obrigatórios e o formato definitivo serão definidos na implementação.

## 7. Exemplo de Resposta

Exemplo de resposta de sucesso:

```json
{
  "success": true,
  "message": "Cadastro realizado com sucesso.",
  "data": {
    "id": "uuid-exemplo",
    "name": "Maria Silva",
    "email": "maria@email.com",
    "account_type": "client"
  }
}
```

A resposta não deverá expor senhas, hashes ou informações internas de autenticação.

## 8. Padronização de Erros

A API deverá utilizar códigos HTTP apropriados e mensagens consistentes.

| Código | Significado |
|---|---|
| 200 | Operação realizada com sucesso |
| 201 | Registro criado |
| 204 | Operação concluída sem conteúdo de resposta |
| 400 | Requisição inválida |
| 401 | Usuário não autenticado |
| 403 | Acesso não autorizado |
| 404 | Recurso não encontrado |
| 409 | Conflito de informações |
| 422 | Dados enviados não passaram pela validação |
| 429 | Limite de requisições excedido |
| 500 | Erro interno do servidor |

Exemplo conceitual:

```json
{
  "success": false,
  "message": "Não foi possível processar a solicitação.",
  "errors": {
    "email": [
      "O endereço de e-mail informado já está cadastrado."
    ]
  }
}
```

As mensagens de erro deverão ser claras, sem revelar detalhes internos do servidor.

## 9. Paginação e Filtros

Listagens extensas deverão utilizar paginação para evitar respostas excessivamente grandes.

Parâmetros propostos:

- `page`: página solicitada.
- `limit`: quantidade de registros.
- `search`: termo de pesquisa.
- `category`: categoria desejada.
- `city`: cidade.
- `status`: situação do registro.

A API deverá validar os parâmetros e limitar a quantidade máxima de resultados por requisição.

## 10. Segurança da API

A implementação deverá considerar:

- Uso obrigatório de HTTPS em produção.
- Validação de dados recebidos.
- Proteção contra requisições maliciosas.
- Controle de permissões no backend.
- Limitação de tentativas de autenticação.
- Proteção de credenciais e tokens.
- Controle de acesso a informações pessoais.
- Registro de operações administrativas relevantes.
- Proteção contra exposição de dados sensíveis.

## 11. Integração com as Aplicações

A API será o ponto central de integração entre as interfaces da Dona Chica.

### Aplicação Web

Será a primeira interface a consumir os endpoints da API.

### Aplicativo Android

Será desenvolvido posteriormente e utilizará os mesmos endpoints, respeitando as permissões e regras de negócio existentes.

### Painel Administrativo

Utilizará operações específicas, protegidas por permissões administrativas.

## 12. Testes da API

A API deverá ser validada por meio de testes que contemplem:

- Cadastro de usuários.
- Autenticação.
- Recuperação de acesso.
- Controle de permissões.
- Cadastro e atualização de serviços.
- Busca de profissionais.
- Formação de Matches.
- Criação de solicitações.
- Gerenciamento de agendamentos.
- Registro de avaliações.
- Registro e análise de denúncias.
- Proteção das rotas administrativas.

Os testes deverão verificar tanto os cenários de sucesso quanto as respostas para operações inválidas ou não autorizadas.

## 13. Decisões Pendentes

As seguintes definições deverão ser registradas conforme a implementação avançar:

- Framework e linguagem utilizados.
- Endereço base da API.
- Padrão definitivo de versionamento.
- Estratégia de autenticação.
- Formato definitivo das respostas.
- Contratos dos endpoints.
- Regras de paginação.
- Estratégia de documentação interativa.
- Política de limites de requisições.
- Ferramentas de testes automatizados.

## 14. Relação com Outros Documentos

- `01-visao-do-produto.md`
- `02-pesquisa-de-campo.md`
- `03-regras-de-negocio.md`
- `04-personas.md`
- `05-requisitos-funcionais.md`
- `06-requisitos-nao-funcionais.md`
- `07-escopo-do-mvp.md`
- `08-fluxos-de-usuario.md`
- `09-arquitetura-do-produto.md`
- `10-arquitetura-tecnica.md`
- `11-modelagem-do-banco-de-dados.md`

---

**Dona Chica — Documentação Técnica**
