# Sistema de Organização de Estudos — Divisão de Tarefas do Grupo

> Projeto Final A3 — Projeto e Engenharia de Software

---

## 1. Visão Geral do Projeto

**Problema:** Alunos têm dificuldade em organizar o que precisam estudar, acompanhar prazos de provas e trabalhos, e medir se estão progredindo no conteúdo.

**Objetivo:** Oferecer uma plataforma onde o aluno cadastra suas matérias, organiza conteúdos e tarefas de estudo, e acompanha visualmente seu progresso e prazos.

**Público-alvo:** Estudantes (ensino médio, cursinho ou faculdade) que precisam organizar rotina de estudos.

**Stack sugerida:**
- Front-end: React (com componente de calendário, ex: FullCalendar)
- Back-end: Node.js + Express (ou Django/Flask)
- Banco: PostgreSQL ou MySQL
- Autenticação: JWT

---

## 2. Divisão da Equipe (5 integrantes)

| Papel | Integrante | Responsabilidades principais |
|---|---|---|
| **Product Owner / Documentação** | Pessoa 1 | Escopo, requisitos, documentação final, Canvas, backlog no Trello/Jira |
| **Modelagem / UX** | Pessoa 2 | Casos de uso, fluxos, diagrama de classes, protótipo de telas |
| **Back-end / Banco de Dados** | Pessoa 3 | API, modelo de dados/DER, autenticação, regras de negócio |
| **Front-end** | Pessoa 4 | Telas, integração com API, calendário, responsividade |
| **QA / Integração / Apresentação** | Pessoa 5 | Testes, ajustes finais, GitHub (organização de commits), apresentação/pitch |

> 💡 Se o grupo tiver **4 pessoas**, a coluna "QA / Integração / Apresentação" pode ser absorvida entre o back-end e o front-end, com todos ajudando nos testes finais.

---

## 3. Requisitos Funcionais (responsável: Pessoa 3, revisado por todos)

| # | Requisito |
|---|---|
| RF01 | O sistema deve permitir cadastro e login de usuário |
| RF02 | O sistema deve permitir cadastrar matérias (nome, cor, professor opcional) |
| RF03 | O sistema deve permitir cadastrar tarefas/conteúdos vinculados a uma matéria |
| RF04 | O sistema deve permitir marcar uma tarefa como concluída |
| RF05 | O sistema deve permitir editar e excluir matérias e tarefas |
| RF06 | O sistema deve exibir um calendário/cronograma com as tarefas por data |
| RF07 | O sistema deve permitir cadastrar eventos de avaliação (provas/trabalhos) |
| RF08 | O sistema deve exibir um painel de progresso (% de tarefas concluídas) |
| RF09 | O sistema deve permitir filtrar tarefas por matéria e por status |
| RF10 | O sistema deve exibir alerta para tarefas com prazo próximo |

## 4. Requisitos Não Funcionais

| # | Requisito |
|---|---|
| RNF01 | Usabilidade: interface simples, poucos cliques para cadastrar tarefa |
| RNF02 | Responsividade: funcionar bem em desktop e celular |
| RNF03 | Desempenho: listagem de tarefas em menos de 2s |
| RNF04 | Segurança: senha armazenada com hash |
| RNF05 | Disponibilidade: aplicação acessível a qualquer momento |

---

## 5. Modelo de Dados (DER) — responsável: Pessoa 3

**Usuario**
- id_usuario (PK), nome, email (único), senha_hash, data_criacao

**Materia**
- id_materia (PK), id_usuario (FK), nome, cor, professor

**Tarefa**
- id_tarefa (PK), id_materia (FK), titulo, descricao, data_limite, status, data_criacao

**Avaliacao**
- id_avaliacao (PK), id_materia (FK), titulo, data, peso

**Relacionamentos:**
- Usuario 1—N Materia
- Materia 1—N Tarefa
- Materia 1—N Avaliacao

---

## 6. Backlog por Sprint (alinhado ao cronograma da A3)

### Sprint 1 — Pré-projeto e Canvas (até 06/10)
- [ ] Definir problema, objetivo e público-alvo — **Pessoa 1**
- [ ] Preencher Canvas do projeto — **Pessoa 1**
- [ ] Levantar requisitos funcionais e não funcionais — **Pessoa 1 + Pessoa 3**
- [ ] Criar quadro de gestão (Trello/GitHub Projects) — **Pessoa 5**
- [ ] Criar repositório no GitHub — **Pessoa 5**

### Sprint intermediária — Modelagem
- [ ] Casos de uso e fluxos principais/alternativos — **Pessoa 2**
- [ ] Diagrama de classes — **Pessoa 2 + Pessoa 3**
- [ ] Modelo de dados / DER — **Pessoa 3**
- [ ] Protótipo das telas (Figma ou similar) — **Pessoa 2 + Pessoa 4**

### Sprint 2 — Desenvolvimento e entrega final (até 03/11 → 17/11)
- [ ] Configurar banco de dados — **Pessoa 3**
- [ ] Desenvolver API (cadastro, login, CRUD matérias/tarefas/avaliações) — **Pessoa 3**
- [ ] Desenvolver telas (cadastro, login, calendário, painel de progresso) — **Pessoa 4**
- [ ] Integrar front-end com back-end — **Pessoa 4 + Pessoa 3**
- [ ] Implementar autenticação (JWT) — **Pessoa 3**
- [ ] Testar funcionalidades e corrigir bugs — **Pessoa 5**
- [ ] Escrever documentação final (template do professor) — **Pessoa 1**
- [ ] Preparar apresentação/pitch — **Pessoa 5 + todos**
- [ ] Gravar/organizar demonstração da aplicação — **Pessoa 5**

---

## 7. Checklist de Entregas Finais

- [ ] Software funcional (código-fonte + instruções de instalação/execução)
- [ ] Banco de dados ou script de criação
- [ ] Documentação completa (template oficial)
- [ ] Link do repositório GitHub
- [ ] Link do quadro de gestão (Trello/Jira/GitHub Projects)
- [ ] Apresentação final com demonstração ao vivo
