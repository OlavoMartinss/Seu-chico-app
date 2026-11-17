# 13. Decisões Arquiteturais — Dona Chica

## 1. Objetivo

Este documento registra as principais decisões arquiteturais e tecnológicas da Dona Chica, estabelecendo uma referência técnica para o desenvolvimento, manutenção e evolução do produto.

As decisões aqui descritas devem orientar tanto o desenvolvedor quanto ferramentas de inteligência artificial utilizadas durante a implementação.

## 2. Arquitetura geral

A Dona Chica será desenvolvida inicialmente como uma aplicação web responsiva, preparada para uma futura expansão para dispositivos Android.

A arquitetura deverá utilizar um backend centralizado, responsável pelas regras de negócio, autenticação, autorização e comunicação com o banco de dados.

O futuro aplicativo Android deverá consumir a mesma API da aplicação web, evitando duplicação de regras e estruturas de dados.

## 3. Decisões tecnológicas

| Camada | Tecnologia | Decisão |
|---|---|---|
| Linguagem | TypeScript | Adotada |
| Framework web | Next.js | Adotado |
| Biblioteca de interface | React | Adotada |
| Estilização | Tailwind CSS | Adotado |
| Componentes | shadcn/ui | Adotado |
| Ícones | Lucide Icons | Adotado |
| Formulários | React Hook Form | Adotado |
| Validação | Zod | Adotado |
| Banco de dados | PostgreSQL | Adotado |
| Infraestrutura de dados | Supabase | Adotado |
| ORM | Prisma | Adotado |
| Autenticação | Supabase Auth | Adotado |
| Hospedagem | Vercel | Planejado |
| Versionamento | Git e GitHub | Adotados |
| Aplicativo Android | React Native e Expo | Futuro |

## 4. Justificativas

### TypeScript
Utilizado para proporcionar tipagem estática, melhorar a previsibilidade do código e reduzir erros durante o desenvolvimento.

### Next.js e React
Escolhidos para construir uma aplicação web moderna, componentizada e preparada para expansão.

### Tailwind CSS e shadcn/ui
Utilizados para acelerar a construção das interfaces, manter consistência visual e facilitar a reutilização de componentes.

### PostgreSQL e Supabase
O PostgreSQL será o sistema de gerenciamento do banco de dados. O Supabase será utilizado como plataforma de infraestrutura, oferecendo serviços integrados ao banco.

### Prisma
Será utilizado como ORM para facilitar a comunicação entre a aplicação e o banco de dados, além de auxiliar na organização das consultas e migrações.

### Supabase Auth
Será responsável pela autenticação dos usuários, com integração às regras de autorização da aplicação.

### React Native e Expo
Serão utilizados futuramente para desenvolver a versão Android, reaproveitando conhecimentos, componentes compartilháveis quando viável e a API centralizada.

## 5. Alternativas consideradas

As seguintes tecnologias foram consideradas, mas não fazem parte da configuração inicial:

- Neon: alternativa de infraestrutura PostgreSQL.
- Drizzle ORM: alternativa ao Prisma.
- Clerk: alternativa ao Supabase Auth.
- Jest: alternativa ao Vitest.
- Vercel Analytics: alternativa ou complemento ao PostHog.
- Turborepo: poderá ser introduzido quando a estrutura com aplicações web e mobile justificar um monorepositório.

A escolha poderá ser revisada caso surjam necessidades técnicas que justifiquem a mudança.

## 6. Princípios arquiteturais

1. Separação de responsabilidades entre interface, regras de negócio e persistência.
2. Reutilização de componentes sempre que apropriado.
3. Centralização das regras de negócio no backend.
4. Validação de dados no cliente e, obrigatoriamente, no servidor.
5. Controle de acesso baseado no tipo de conta e nas permissões.
6. Proteção de dados pessoais e informações sensíveis.
7. Código organizado, legível e documentado.
8. Testes das funcionalidades críticas.
9. Compatibilidade com a futura aplicação Android.
10. Uso de inteligência artificial como ferramenta auxiliar, com revisão humana das alterações.

## 7. Segurança e integridade

A aplicação deverá considerar:

- Autenticação e autorização adequadas.
- Proteção das rotas e operações privadas.
- Políticas de acesso ao banco de dados.
- Proteção de credenciais e variáveis de ambiente.
- Validação de entradas no servidor.
- Tratamento seguro de erros.
- Proteção contra acesso indevido a dados de outros usuários.

Nenhuma informação sensível deverá ser exposta no código público ou no repositório.

## 8. Uso de inteligência artificial no desenvolvimento

Ferramentas de inteligência artificial poderão auxiliar na geração, revisão, refatoração e documentação do código.

Entretanto, todo código gerado deverá passar por revisão e testes antes de ser considerado concluído.

A inteligência artificial não deverá modificar decisões arquiteturais, regras de negócio ou estruturas críticas sem autorização do desenvolvedor.

## 9. Status das decisões

Este documento representa a arquitetura inicialmente planejada. As decisões poderão ser atualizadas conforme a implementação, testes e necessidades reais do produto.

**Status:** Arquitetura inicial definida.

**Projeto:** Dona Chica

**Documento:** 13 — Decisões Arquiteturais
