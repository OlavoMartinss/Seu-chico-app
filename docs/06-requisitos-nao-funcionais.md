# 06. Requisitos Não Funcionais — Dona Chica

**Projeto:** Dona Chica  
**Documento:** Requisitos Não Funcionais  
**Versão:** 1.0  
**Status:** Em desenvolvimento  
**Referências:** Visão de Produto, Pesquisa de Campo, Regras de Negócio, Personas e Requisitos Funcionais.

---

## 1. Objetivo

Este documento estabelece os requisitos não funcionais da plataforma Dona Chica, definindo critérios de qualidade, segurança, desempenho, disponibilidade, privacidade e usabilidade.

Seu propósito é orientar as decisões técnicas durante o desenvolvimento, garantindo que a aplicação ofereça uma experiência confiável, acessível e consistente para clientes e profissionais.

## 2. Segurança

A segurança é um dos pilares fundamentais da Dona Chica, considerando que a plataforma conecta pessoas para a realização de serviços em ambientes residenciais e outros espaços privados.

| ID | Requisito | Prioridade |
|---|---|---|
| RNF-001 | O sistema deve proteger as credenciais de acesso dos usuários por mecanismos seguros de autenticação. | Crítica |
| RNF-002 | As senhas devem ser armazenadas utilizando algoritmos seguros de hash, nunca em texto puro. | Crítica |
| RNF-003 | O sistema deve implementar controle de acesso baseado no tipo de usuário e nas respectivas permissões. | Crítica |
| RNF-004 | As comunicações entre cliente, servidor e serviços externos devem utilizar HTTPS. | Crítica |
| RNF-005 | O sistema deve impedir o acesso não autorizado a informações e funcionalidades restritas. | Crítica |
| RNF-006 | O sistema deve registrar eventos relevantes de segurança para auditoria. | Alta |
| RNF-007 | O sistema deve proteger informações sensíveis contra exposição indevida. | Crítica |

## 3. Privacidade e proteção de dados

A plataforma deverá respeitar a legislação brasileira aplicável à proteção de dados pessoais, especialmente a Lei Geral de Proteção de Dados (LGPD).

| ID | Requisito | Prioridade |
|---|---|---|
| RNF-008 | O sistema deve coletar somente os dados pessoais necessários para suas finalidades. | Crítica |
| RNF-009 | O tratamento de dados pessoais deve possuir uma base legal adequada, conforme a LGPD. | Crítica |
| RNF-010 | O sistema deve informar aos usuários como seus dados são coletados, utilizados e armazenados. | Alta |
| RNF-011 | O acesso a dados pessoais deve ser limitado conforme as permissões de cada perfil. | Crítica |
| RNF-012 | O sistema deve disponibilizar mecanismos para atendimento aos direitos dos titulares de dados. | Alta |
| RNF-013 | Dados de localização e informações relacionadas aos atendimentos devem receber proteção adequada. | Crítica |
| RNF-014 | O sistema deve estabelecer procedimentos para retenção e eliminação de dados pessoais, respeitando as obrigações legais. | Alta |

## 4. Desempenho

A aplicação deverá oferecer respostas rápidas e consistentes durante as principais operações realizadas pelos usuários.

| ID | Requisito | Prioridade |
|---|---|---|
| RNF-015 | As operações comuns de navegação devem apresentar tempo de resposta adequado às condições de rede e infraestrutura. | Alta |
| RNF-016 | As pesquisas de profissionais devem ser otimizadas para evitar consultas desnecessariamente lentas. | Alta |
| RNF-017 | O sistema deve processar operações simultâneas sem comprometer a integridade dos dados. | Alta |
| RNF-018 | A aplicação deve utilizar estratégias de otimização para carregamento de imagens e demais recursos. | Média |
| RNF-019 | O backend deve implementar tratamento eficiente de consultas e operações no banco de dados. | Alta |

## 5. Disponibilidade e confiabilidade

| ID | Requisito | Prioridade |
|---|---|---|
| RNF-020 | O sistema deve possuir mecanismos de tratamento de falhas e recuperação de operações. | Alta |
| RNF-021 | O banco de dados deve possuir mecanismos periódicos de backup. | Crítica |
| RNF-022 | O sistema deve preservar a integridade das informações armazenadas. | Crítica |
| RNF-023 | A aplicação deve apresentar mensagens adequadas em situações de indisponibilidade ou falha. | Alta |
| RNF-024 | O sistema deve possuir mecanismos de monitoramento de erros e disponibilidade. | Alta |

## 6. Usabilidade e experiência do usuário

A experiência deverá ser simples, intuitiva e acessível, considerando os diferentes perfis de utilização da plataforma.

| ID | Requisito | Prioridade |
|---|---|---|
| RNF-025 | A interface deve apresentar navegação intuitiva para clientes e profissionais. | Alta |
| RNF-026 | Os painéis de cliente e profissional devem apresentar funcionalidades compatíveis com suas respectivas permissões. | Alta |
| RNF-027 | O sistema deve fornecer feedback visual para ações realizadas pelos usuários. | Alta |
| RNF-028 | A aplicação deve apresentar mensagens claras para erros, confirmações e operações pendentes. | Alta |
| RNF-029 | A interface deve manter consistência visual e funcional entre suas diferentes áreas. | Média |
| RNF-030 | A aplicação deve considerar princípios de acessibilidade digital. | Alta |

## 7. Compatibilidade e responsividade

| ID | Requisito | Prioridade |
|---|---|---|
| RNF-031 | A aplicação deve oferecer interface responsiva para diferentes tamanhos de tela. | Alta |
| RNF-032 | A interface web deve ser compatível com navegadores modernos. | Alta |
| RNF-033 | Os principais recursos devem ser utilizáveis em dispositivos móveis e computadores. | Alta |
| RNF-034 | A apresentação dos componentes deve preservar a consistência visual em diferentes resoluções. | Média |

## 8. Escalabilidade e manutenção

| ID | Requisito | Prioridade |
|---|---|---|
| RNF-035 | A arquitetura deve permitir a evolução de funcionalidades sem exigir a reconstrução integral do sistema. | Alta |
| RNF-036 | O código deve seguir padrões de organização e boas práticas de desenvolvimento. | Alta |
| RNF-037 | Os componentes do sistema devem possuir responsabilidades bem definidas. | Alta |
| RNF-038 | A aplicação deve permitir a integração com serviços e APIs externas. | Alta |
| RNF-039 | O sistema deve possuir documentação técnica suficiente para facilitar sua manutenção. | Alta |
| RNF-040 | O desenvolvimento deve considerar testes automatizados para funcionalidades críticas. | Alta |

## 9. Monitoramento e rastreabilidade

| ID | Requisito | Prioridade |
|---|---|---|
| RNF-041 | O sistema deve manter registros de eventos relevantes para o acompanhamento dos atendimentos. | Alta |
| RNF-042 | As ações administrativas relacionadas a denúncias e restrições devem possuir registros de auditoria. | Crítica |
| RNF-043 | O sistema deve permitir identificar falhas técnicas por meio de registros e ferramentas de monitoramento. | Alta |
| RNF-044 | O acesso a registros de auditoria deve ser restrito a usuários autorizados. | Crítica |

## 10. Considerações técnicas

Os requisitos apresentados estabelecem diretrizes de qualidade para o desenvolvimento da Dona Chica.

Os valores quantitativos de desempenho, disponibilidade e capacidade de processamento deverão ser definidos posteriormente, conforme a arquitetura escolhida, infraestrutura disponível e resultados dos testes.

As funcionalidades de monitoramento, verificação de antecedentes e tratamento de dados sensíveis deverão passar por avaliações específicas de segurança, privacidade e conformidade legal antes de sua implementação.

## 11. Relação com outros documentos

- **Documento 01 — Visão de Produto:** apresenta o propósito e os objetivos da plataforma.
- **Documento 02 — Pesquisa de Campo:** identifica as necessidades dos usuários.
- **Documento 03 — Regras de Negócio:** define as condições de funcionamento.
- **Documento 04 — Personas:** representa os perfis de usuários.
- **Documento 05 — Requisitos Funcionais:** especifica as funcionalidades do sistema.
- **Documento 07 — Escopo do MVP:** delimitará as funcionalidades previstas para a primeira versão.

---

**Dona Chica — Documentação do Produto**  
*Segurança, autonomia e valorização profissional.*
