![image](https://github.com/user-attachments/assets/9b86f33a-8519-4cc8-9ae3-c6149e235c97)# Sprint 3: Sistema de Publicações no Feed

**Valor:** Permitir que os usuários façam publicações no feed, interajam com as publicações de outros usuários e visualizem um feed de atividades.

## Requisitos Funcionais:
- **RF14:** Permitir que os usuários façam publicações no feed.
- **RF15:** Permitir que os usuários curtam e comentem nas publicações.
- **RF16:** Exibir um feed de publicações dos usuários.
- **RF17:** Permitir que os usuários excluam suas próprias publicações.

## Requisitos Não-Funcionais:
- **RNF1:** A senha do usuário precisa estar criptografada.
- **RNF2:** Os dados da aplicação precisam estar persistidos no PostgreSQL.
- **RNF4:** O usuário deve ser identificado por um JWT (JSON Web Token).
- **RNF6:** A aplicação deve ter alta disponibilidade.
- **RNF7:** Deverão ser feitos testes unitários e de integração com a biblioteca faker js.
- **RNF8:** As publicações devem ser carregadas de forma eficiente e paginada.

## Desenvolvimento do Backend
**Objetivo:** Implementar a funcionalidade de publicações no feed e interações com as publicações.


### Valor: Sistema de Publicações (Lauro)

#### RF12: Permitir que usuários comentem nas publicações dos outros

#### Regras de Negócio

- Somente usuários autenticados podem comentar.

#### Critérios de Aceitação

- O sistema deve permitir que usuários adicionem comentários nas postagens.
- O sistema deve exibir comentários na ordem cronológica.

### Tarefas:

- Implementar a lógica para criação de publicações no feed.
- Criar endpoints RESTful para criar, ler, atualizar e excluir publicações.
- Garantir que as publicações sejam carregadas de forma paginada.

### Valor:Interações com Publicações (Lucas)

#### RF13: Permitir que usuários curtam as publicações dos outros

#### Regras de Negócio

- Apenas usuários autenticados podem curtir postagens.

#### Critérios de Aceitação

- O sistema deve permitir que usuários curtam ou descurtam postagens.
- O sistema deve mostrar o total de curtidas na postagem.

### Tarefas:

- Implementar a lógica para curtir e comentar nas publicações.
- Criar endpoints RESTful para gerenciar curtidas e comentários.
- Garantir que apenas usuários autenticados possam interagir com as publicações.

### Testes de Backend (Lauro)
- Escrever testes unitários e de integração para as funcionalidades de publicações e interações.
- Utilizar a lib faker para gerar dados de teste e garantir a cobertura de todos os casos possíveis.

## Desenvolvimento do Frontend
**Objetivo:** Implementar a interface de usuário para o sistema de publicações no feed e interações.

### Tarefas:
#### Desenvolvimento dos Componentes de UI para Publicações (Micael)

Objetivo: Como um usuário, eu quero visualizar um feed atualizado para ver as atividades mais recentes dos meus amigos.

![image](https://github.com/user-attachments/assets/92f0cab7-32f5-487f-b7c3-3bbd5e423310)

- Criar componentes de UI para exibir o feed de publicações.
- Implementar a interface para criar novas publicações.
- Criar componentes de UI para curtir e comentar nas publicações.

#### Integração com os Endpoints do Backend (Almir)

Objetivo: Como um usuário, eu quero interagir com as publicações diretamente na interface para que a experiência seja dinâmica

![image](https://github.com/user-attachments/assets/331bffb3-7afe-4843-9730-df1dcf5d08ee)
![image](https://github.com/user-attachments/assets/e7eeaf40-6ee0-4f20-af55-026436f64d48)


- Integrar os componentes de UI com os endpoints de publicações do backend.
- Garantir que as publicações sejam carregadas de forma paginada na interface de usuário.
- Implementar a lógica de interações (curtidas e comentários) no frontend.

#### Autenticação no Frontend (Micael)

Objetivo: Como um usuário, eu quero que minha sessão seja mantida de forma segura para que eu possa acessar as funcionalidades sem me autenticar repetidamente

- Garantir que apenas usuários autenticados possam acessar as funcionalidades de publicações e interações.
- Implementar a lógica de autenticação no frontend utilizando JWT para proteger o acesso às funcionalidades.

#### Testes de Usabilidade e Ajustes (Almir)

- Conduzir testes de usabilidade com usuários reais para a funcionalidade de publicações no feed.
- Coletar feedback e realizar ajustes na interface de usuário para melhorar a experiência.

## Testes e Revisão (Todos)
**Objetivo:** Garantir que a funcionalidade de publicações no feed e interações funcionem corretamente.

### Tarefas:

#### Testes de Usabilidade com Usuários Reais
- Conduzir testes de usabilidade com um grupo de usuários reais para as funcionalidades de publicações no feed.
- Coletar feedback sobre a experiência do usuário e identificar possíveis melhorias.

#### Correções e Melhorias
- Implementar melhorias e/ou correções com base no feedback dos usuários.
- Atualizar a documentação e realizar quaisquer ajustes necessários antes do próximo ciclo de desenvolvimento.
