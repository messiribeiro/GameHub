# Refinamento: Barra de Busca, Perfis Específicos de Jogos, Configurações de Conta e Acréscimo para novos jogos

**Valor:** Melhorar a usabilidade da plataforma, permitindo que usuários encontrem outros facilmente e personalizem suas experiências, aumentando a interatividade e promovendo um espaço mais seguro e customizável.

---

## User Stories e Regras de Negócio

### Barra de Busca de Usuários (RF-20)

**Como** um usuário, **eu quero** buscar outros usuários na plataforma, **para** facilitar a conexão e interação com pessoas com interesses semelhantes.

![Section 1](https://github.com/user-attachments/assets/bcb96904-90d3-4940-baf2-629741009051)


#### Regra de Negócio
- A barra de busca deve permitir a pesquisa por nome de usuário

#### Tarefas

**Backend:**
- Implementar endpoint de busca de usuários, com filtros de nome de usuário *(Lauro)*

**Frontend:**
- Criar interface para a barra de busca com opções de filtro. *(Micael)*
- Exibir os resultados de busca em uma lista, com destaque para usuários premium e gamedevs. *(Almir)*

#### Critérios de Aceitação
- A busca deve exibir usuários corretamente, com opção de filtro por nome
- Usuários premium e gamedevs devem ser destacados nos resultados.

---

### Perfis Específicos de Jogos Adicionados (RF-21)

**Como** um usuário gamedev, **eu quero** ter perfis específicos para cada jogo que adiciono, **para** organizar e promover meus projetos de forma individual.

![iPhone 14   15 Pro Max - 51](https://github.com/user-attachments/assets/cbfcff8f-9d72-4fcd-b442-1ef3ce3a53b3)


#### Regra de Negócio
- Apenas usuários premium gamedev podem adicionar perfis específicos para jogos.
- Cada perfil de jogo deve incluir informações como título, descrição, imagem, gênero e links para download ou plataformas de venda.

#### Tarefas

**Backend:**
- Criar endpoints para adicionar, editar e excluir perfis de jogos para gamedevs. *(Lauro)*

**Frontend:**
- Criar interface para exibição de perfis de jogos  *(Micael)*
- Implementar a lógica para que os perfis dos jogos tenham as postagens dos usuarios que marcarem o perfil *(Micael)*

#### Critérios de Aceitação
- Gamedevs devem conseguir adicionar, editar e excluir perfis de jogos.
- Perfis de jogos devem ser exibidos corretamente no perfil do usuário gamedev, incluindo todas as informações especificadas.

---

### Barra de Configurações de Conta (RF-22)

**Como** um usuário, **eu quero** acessar uma barra de configurações, **para** editar minha senha e excluir minha conta de forma segura e prática.

![Section 19](https://github.com/user-attachments/assets/e10e0b35-d2c8-4acd-b054-e4e288552635)

![Section 13](https://github.com/user-attachments/assets/c6ff8245-dc56-4212-a701-aeb7ccbd905e)


#### Regra de Negócio
- Os usuários devem conseguir editar sua senha mediante confirmação da senha atual.
- A exclusão de conta deve ser definitiva e requerer confirmação do usuário.

#### Tarefas

**Backend:**
- Implementar endpoints para atualização de senha e exclusão de conta. *(Lucas)*
- Adicionar autenticação para verificar a senha atual antes de permitir a alteração. *(Lauro)*

**Frontend:**
- Criar interface de configurações com campos para alteração de senha e opção para excluir conta. *(Almir)*
- Implementar confirmação para exclusão de conta, com aviso de que a ação é irreversível. *(Almir)*

#### Critérios de Aceitação
- A senha deve ser editável após confirmação da senha atual.
- A exclusão de conta deve ser definitiva, com confirmação e aviso ao usuário.

---

### Regras de Pagamento para Jogos Extras (RF-23)

**Como** um usuário premium dos planos Gamedev Basic ou Gamedev, **eu quero** pagar uma taxa adicional para adicionar mais jogos que o limite padrão do meu plano permite, **para** expandir minha visibilidade na plataforma.

![iPhone 14   15 Pro Max - 50](https://github.com/user-attachments/assets/6ce8ac8d-f670-4bfe-9c06-cda4e750d75f)


#### Regras de Negócio
- **Plano Gamedev Basic:** Após adicionar 2 jogos, o usuário deve pagar uma taxa adicional de R$5 para cada novo jogo que queira incluir.
- **Plano Gamedev:** Após adicionar 10 jogos, o usuário deve pagar uma taxa adicional de R$5 para cada jogo extra.
- **Após o Pagamento:** O jogo extra deve ser liberado imediatamente para inclusão no perfil do usuário.

#### Tarefas

**Backend:**
- Implementar lógica de verificação do limite de jogos com base no plano antes de permitir a adição de um novo jogo. *(Lucas)*
- Criar endpoint para processar o pagamento de jogos adicionais e liberar espaço para o novo jogo após a confirmação. *(Lauro)*

**Frontend:**
- Exibir uma notificação informando ao usuário que ele atingiu o limite de jogos e oferecer a opção de pagamento adicional para incluir outro jogo. *(Almir)*
- Implementar UI para confirmar o pagamento do jogo extra com detalhes de custo, exibindo o status da liberação após o pagamento. *(Micael)*

#### Critérios de Aceitação
- O sistema deve verificar o limite de jogos e oferecer a opção de pagamento adicional de acordo com o plano do usuário.
- Após o pagamento, o usuário deve poder adicionar o novo jogo imediatamente.
- Usuários devem ser informados sobre a opção de upgrade para o plano Gamedev quando atingirem o limite do plano Gamedev Basic.
