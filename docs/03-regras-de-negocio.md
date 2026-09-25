# Seu Chico — Regras de Negócio

## RB-001 — Perfil profissional do prestador

### Descrição

O prestador deve possuir um perfil profissional contendo informações relevantes para que o cliente possa conhecer o profissional antes de solicitar um serviço.

### Objetivo

Aumentar a confiança e fornecer informações para apoiar a decisão do cliente.

### Atores envolvidos

* Prestador
* Cliente
* Sistema

### Comportamento esperado

O sistema deve disponibilizar as informações públicas definidas para o perfil do prestador.

---

## RB-002 — Compatibilidade entre serviço e área de atendimento

### Descrição

Uma solicitação de serviço deve considerar o serviço oferecido pelo prestador, sua área de atendimento e sua disponibilidade.

### Objetivo

Evitar solicitações incompatíveis com os serviços ou localização de atendimento do prestador.

### Atores envolvidos

* Cliente
* Prestador
* Sistema

### Comportamento esperado

O sistema deve apresentar ao cliente prestadores compatíveis com os critérios da solicitação.

---

## RB-003 — Avaliação e denúncia entre usuários

### Descrição

Após a conclusão de uma solicitação de serviço, tanto o cliente quanto o prestador poderão avaliar a experiência e registrar uma denúncia caso identifiquem comportamento inadequado ou uma violação das regras da plataforma.

### Objetivo

Promover confiança, transparência e segurança para todos os usuários da plataforma, permitindo que experiências positivas sejam registradas e situações inadequadas sejam reportadas.

### Atores envolvidos

* Cliente
* Prestador
* Sistema
* Administrador

### Comportamento esperado

O sistema deve permitir que ambas as partes registrem avaliações e denúncias relacionadas ao atendimento. As avaliações serão associadas ao histórico dos usuários e as denúncias serão encaminhadas para o processo de análise e moderação da plataforma.

---

## RB-004 — Análise e validação de denúncias

### Descrição

Toda denúncia registrada na plataforma deverá passar por um processo de análise antes que qualquer penalidade seja aplicada ao usuário denunciado. A análise deverá considerar as informações fornecidas na denúncia e, quando disponíveis, os registros e evidências relacionados à ocorrência.

A denúncia poderá ser classificada como **procedente**, **improcedente** ou **necessita de análise adicional**.

### Objetivo

Evitar punições automáticas ou injustificadas, garantindo que as medidas de moderação sejam baseadas na análise da ocorrência e nas regras da plataforma.

### Atores envolvidos

* Cliente
* Prestador
* Administrador
* Sistema

### Comportamento esperado

O sistema deve registrar cada denúncia com seu respectivo status de análise. Somente denúncias classificadas como **procedentes** deverão ser contabilizadas no histórico de infrações do usuário denunciado.

---

## RB-005 — Sistema de reputação e Ghost Mode

### Descrição

Quando um usuário acumular **4 denúncias consideradas procedentes**, sua conta deverá ser automaticamente colocada em **Ghost Mode** pelo período de **30 dias**.

Durante esse período, o perfil do usuário não deverá ser divulgado nas buscas ou recomendações da plataforma, e o usuário ficará impedido de contratar ou prestar serviços.

### Objetivo

Criar um mecanismo de responsabilização e proteção dos usuários, reduzindo a exposição de contas que apresentem um histórico recorrente de violações das regras da plataforma.

### Atores envolvidos

* Cliente
* Prestador
* Administrador
* Sistema

### Comportamento esperado

Ao atingir 4 denúncias procedentes, o sistema deverá alterar o status da conta para **Ghost Mode** e registrar a data de início e término da suspensão.

Durante o período de suspensão:

* O perfil não poderá ser exibido nas buscas ou recomendações;
* O usuário não poderá prestar serviços;
* O usuário não poderá contratar serviços;
* Novas solicitações de contratação ficarão indisponíveis.

Após o período de 30 dias, o sistema poderá reativar a conta de acordo com as regras de moderação da plataforma.

