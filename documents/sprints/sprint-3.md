# Sprint 3: Sistema de Publicações no Feed

**Valor:** Permitir que os usuários façam publicações no feed, interajam com as publicações de outros usuários e visualizem um feed de atividades.

## User Stories e Regras de Negócio

### User Story 1
Como um usuário registrado, eu quero poder fazer publicações de texto no feed, para que eu possa compartilhar atualizações com meus amigos.

![image](https://github.com/user-attachments/assets/92f0cab7-32f5-487f-b7c3-3bbd5e423310)

#### Regra de Negócio
- Somente usuários autenticados podem criar publicações.

#### Tarefas:
**Backend:**
- Criar um endpoint RESTful para criar publicações. (Lauro)

**Frontend:**
- Criar a interface para nova publicação. (Micael)
- Implementar a lógica para enviar publicações ao backend. (Micael)

#### Critérios de Aceitação:
- O sistema deve permitir que usuários autenticados criem publicações.
- As publicações devem ser exibidas no feed após a criação.

---

### User Story 2
Como um usuário, eu quero poder curtir e comentar nas publicações, para que eu possa interagir com o conteúdo dos outros.

![image](https://github.com/user-attachments/assets/e7eeaf40-6ee0-4f20-af55-026436f64d48)


#### Regra de Negócio
- Apenas usuários autenticados podem curtir e comentar nas publicações.

#### Tarefas:
**Backend:**
- Criar endpoints RESTful para curtir e descurtir (Lucas)
- e endpoints RESTful para comentar em publicações (Lucas)

**Frontend:**
- Criar componentes de UI para curtir. (Lauro)
- Criar componentes de UI para comentar. (Almir)

#### Critérios de Aceitação:
- O sistema deve permitir que usuários curtam e descurtam publicações.
- O sistema deve exibir o total de curtidas em cada publicação.
- Os comentários devem ser exibidos em ordem cronológica.
- O usuário não pode curtir mais de uma vez a mesma publicação

---

### User Story 3
Como um usuário, eu quero visualizar um feed de publicações, para que eu possa acompanhar as atividades mais recentes dos meus amigos.

![image](https://github.com/user-attachments/assets/331bffb3-7afe-4843-9730-df1dcf5d08ee)

#### Regra de Negócio
- O sistema deve carregar publicações de forma paginada.

#### Tarefas:
**Backend:**
- Criar um endpoint RESTful para buscar publicações paginadas. (Lauro)
- Lógica para armazenar o estado do usuário (Online/Offline) (Lauro)

**Frontend:**
- Criar componentes de UI para exibir o feed de publicações. (Micael)
- Implementar a lógica para carregar publicações de forma paginada. (Micael)
- UI que retorna se o usuário está Online/Offline e o tempo referente a esses estados (Tharcio)

#### Critérios de Aceitação:
- O feed deve mostrar as publicações mais recentes.
- As publicações devem ser carregadas de forma eficiente.

---

### User Story 4
Como um usuário, eu quero poder excluir minhas próprias publicações e comentários, para que eu possa remover conteúdo indesejado.

#### Regra de Negócio
- Somente o autor da publicação pode excluí-la.

#### Tarefas:
**Backend:**
- Criar um endpoint RESTful para excluir publicações. (Micael)
- Criar um endpoint RESTful para excluir comentários. (Almir)

**Frontend:**
- Implementar a lógica de exclusão de publicações na interface. (Micael)
- Implementar a lógica de exclusão de comentários na interface. (Almir)

#### Critérios de Aceitação:
- O sistema deve permitir que o autor exclua suas publicações.
- As publicações excluídas não devem mais aparecer no feed.

---

### User Story 5
Como um usuário, eu quero enviar imagens e vídeos nas minhas publicações, para que eu possa enriquecer meu conteúdo.

#### Regra de Negócio
- Apenas usuários autenticados podem enviar mídias.

#### Tarefas:
**Backend:**
- Implementar a lógica para upload de imagens e vídeos. (Lauro)
- Configurar S3 para armazenamento (Lauro)
- Validar  tipos de arquivo e tamanhos permitidos (Lauro)

**Frontend:**
- Criar componentes de UI para enviar mídias. (Lucas)
- Implementar a lógica para envio de mídias ao backend. (Almir)

#### Critérios de Aceitação:
- O sistema deve permitir o upload de imagens e vídeos.
- As mídias devem ser exibidas corretamente nas publicações.
- As mídias devem estar sendo armazenadas no serviço da AWS (S3)
