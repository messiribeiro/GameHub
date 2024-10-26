### Sprint 1: Filtro de Perfis de Usuários por Interesse em Jogos em Comum

**Valor:** Permitir que os usuários encontrem novos jogadores dispostos a jogar juntos, facilitando a formação de grupos com interesses semelhantes.

---

## User Stories e Regras de Negócio

### Cadastro e Autenticação de Usuários (RF-1)
**Como** um novo usuário, **eu quero** me cadastrar e autenticar na plataforma, **para** poder utilizar a funcionalidade de filtragem de perfis.

![iPhone 14   15 Pro Max - 2](https://github.com/user-attachments/assets/44e4c56d-7710-496d-a069-64c58288cf47)

![iPhone 14   15 Pro Max - 20](https://github.com/user-attachments/assets/843ea8df-c86e-4240-8cde-29bd009d7b67)

#### Regra de Negócio
- O sistema deve permitir o cadastro de novos usuários com validação de dados
- O sistema deve autenticar usuários usando um método seguro, como JWT.
- Durante o cadastro o usuário irá informar os jogos que deseja integrar em seu perfil

#### Tarefas:

**Backend:**
- Implementar lógica para cadastro de usuários com validação de dados. 
- Implementar autenticação de usuários com JWT
- Lógica para que o usuário possa adicionar jogos ao seu perfil

**Frontend:**
- Criar UI para o cadastro de usuários (formulário com campos necessários)
- Criar UI para a autenticação de usuários (login).

#### Critérios de Aceitação:
- Usuários devem ser capazes de se cadastrar e receber uma confirmação.
- Usuários devem ser autenticados e redirecionados para a tela principal

---

### Filtro de Perfis por Interesses em Jogos (RF-5)
**Como** um usuário autenticado, **eu quero** filtrar perfis de outros usuários com interesses em jogos em comum, **para** encontrar pessoas para jogar

![iPhone 14   15 Pro Max - 21](https://github.com/user-attachments/assets/31b6ecd0-2117-4ff9-80a0-59e2415578ec)

#### Regra de Negócio
- O sistema deve permitir que os usuários filtrem perfis com base nos jogos de interesse
- A busca deve retornar resultados paginados.

#### Tarefas:

**Backend:**
- Implementar a lógica de filtragem de perfis baseada em interesses de jogos. 
- Criar endpoints RESTful para busca e filtragem de perfis de usuários. 
**Frontend:**
- Criar componentes de UI para a exibição de perfis filtrados. 
- Implementar a lógica de paginação na interface de usuário. 

#### Critérios de Aceitação:
- Os perfis devem ser filtrados corretamente com base nos interesses selecionados.
- Os resultados devem ser exibidos de forma paginada.

---

### Revisão e Melhorias
**Objetivo:** Garantir que o filtro de usuários funcione corretamente e que a experiência do usuário seja a melhor possível

#### Tarefas:
1. **Revisão de Código**
   - Conduzir revisões de código com a equipe para assegurar a qualidade do código. (Toda a equipe)
   - Implementar testes unitários (Backend)

2. **Implementação de Melhorias**
   - Implementar melhorias com base no feedback coletado durante os testes de usabilidade. (Desenvolvedores 1, 2 e 3)

---
