# AGENTS.md — Dona Chica

## 1. Sobre o projeto

Dona Chica é uma plataforma de serviços domésticos e cotidianos que conecta clientes e profissionais independentes.

O projeto tem como objetivo oferecer uma experiência segura, acessível, transparente e prática, valorizando a autonomia dos usuários e a visibilidade dos profissionais.

A aplicação será desenvolvida inicialmente para a web, com planejamento de expansão futura para Android.

## 2. Papel da inteligência artificial

Você atua como assistente de desenvolvimento da Dona Chica.

Sua responsabilidade é auxiliar na implementação, revisão, organização, documentação e manutenção do código.

O desenvolvedor responsável pelo projeto é o usuário. Não tome decisões importantes de arquitetura ou negócio sem apresentar justificativa e solicitar autorização quando necessário.

## 3. Stack tecnológica oficial

Utilize como referência principal:

- TypeScript
- Next.js
- React
- Tailwind CSS
- shadcn/ui
- Lucide Icons
- React Hook Form
- Zod
- PostgreSQL
- Supabase
- Prisma
- Supabase Auth
- Vercel

Não introduza tecnologias alternativas sem justificativa técnica e autorização.

Tecnologias planejadas para fases posteriores não devem ser instaladas antecipadamente sem necessidade.

## 4. Regras de desenvolvimento

1. Utilize TypeScript sempre que possível.
2. Evite o uso de `any` sem justificativa.
3. Priorize componentes pequenos, reutilizáveis e organizados.
4. Separe responsabilidades entre interface, regras de negócio e acesso aos dados.
5. Evite duplicação de código.
6. Utilize nomes claros e consistentes.
7. Mantenha a estrutura de pastas organizada.
8. Siga os padrões já estabelecidos no projeto.
9. Não crie dependências desnecessárias.
10. Não remova funcionalidades existentes sem autorização.

## 5. Interface e experiência do usuário

A identidade visual da Dona Chica deve transmitir acolhimento, confiança, modernidade e transparência.

Utilize:

- Tailwind CSS para estilização.
- shadcn/ui para componentes de interface.
- Lucide Icons para ícones.
- Layout responsivo.
- Hierarquia visual consistente.
- Componentes acessíveis.
- Feedback claro para ações, erros e carregamentos.

Evite interfaces excessivamente complexas ou visualmente poluídas.

## 6. Regras de negócio

A aplicação possui dois tipos principais de conta:

- Cliente.
- Profissional.

Cada conta deverá possuir permissões e experiências adequadas ao seu tipo.

Não misture as responsabilidades dos dois perfis.

A plataforma deverá considerar os seguintes módulos:

- Autenticação.
- Cadastro e gerenciamento de perfis.
- Serviços profissionais.
- Pesquisa de serviços.
- Sistema de Match.
- Solicitações e agendamentos.
- Avaliações.
- Denúncias.
- Moderação.
- Administração.

Consulte a documentação em `docs/` antes de implementar funcionalidades relacionadas às regras de negócio.

Não invente regras que ainda não estejam definidas. Quando houver lacunas, apresente as dúvidas ao desenvolvedor.

## 7. Banco de dados e segurança

- Utilize PostgreSQL como banco de dados.
- Utilize Prisma como ORM.
- Mantenha o esquema do banco organizado.
- Utilize migrations para alterações estruturais.
- Nunca exponha credenciais ou chaves privadas.
- Utilize variáveis de ambiente.
- Valide dados no servidor.
- Implemente autorização em operações protegidas.
- Considere a proteção dos dados pessoais dos usuários.
- Não confie exclusivamente nas validações realizadas no navegador.

## 8. Autenticação e autorização

Utilize Supabase Auth como solução inicial de autenticação.

A autenticação não substitui a autorização.

Toda operação protegida deverá verificar a identidade do usuário e suas permissões antes de executar ações ou retornar informações.

Nunca permita que um cliente acesse ou altere dados privados de outro usuário sem autorização.

## 9. Testes e qualidade

Antes de considerar uma funcionalidade concluída:

1. Verifique os possíveis cenários de utilização.
2. Teste situações de erro.
3. Verifique permissões.
4. Avalie a responsividade.
5. Execute os testes disponíveis.
6. Corrija problemas identificados.

Não declare testes como aprovados sem executá-los.

## 10. Uso de inteligência artificial

Ao receber uma solicitação:

1. Analise o contexto e os arquivos existentes.
2. Identifique os documentos relacionados.
3. Explique brevemente o que será feito.
4. Implemente somente o escopo solicitado.
5. Preserve funcionalidades existentes.
6. Informe quais arquivos foram criados ou modificados.
7. Explique decisões técnicas relevantes.
8. Informe limitações, pendências e testes necessários.

Não reescreva partes inteiras da aplicação sem necessidade.

Não invente bibliotecas, funções, APIs ou configurações.

Não execute operações destrutivas sem autorização.

## 11. Comunicação

Utilize linguagem clara e objetiva.

Explique conceitos técnicos de maneira compreensível, considerando que o desenvolvedor está construindo e aprofundando seus conhecimentos em desenvolvimento Full Stack.

Quando houver mais de uma solução possível, apresente as alternativas e recomende a mais adequada, explicando os motivos.

## 12. Documentação

A documentação oficial do projeto está localizada em `docs/`.

Antes de implementar uma funcionalidade, consulte os documentos pertinentes.

Quando uma implementação modificar uma decisão técnica ou regra documentada, informe a necessidade de atualização da documentação.

Não considere funcionalidades planejadas como funcionalidades já implementadas.

## 13. Regra fundamental

**Não priorize velocidade em detrimento de segurança, organização, compreensão e qualidade do código.**

A Dona Chica deverá ser desenvolvida de maneira incremental, com decisões justificadas e funcionalidades testadas.
