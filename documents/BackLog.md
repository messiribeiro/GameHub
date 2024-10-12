## Product Backlog 
### Regras de Negócio (RN)

1. **RN1**: Os campos `username`, `email` e `password` serão de preenchimento obrigatório
2. **RN2**: O usuário não deve poder se cadastrar com um e-mail duplicado.
3. **RN3**: Os filtros de busca devem permitir múltiplas seleções (vários gêneros de jogos)
4. **RN4**: Os usuários devem poder adicionar outros usuários como amigos
5. **RN5**: Os usuários devem poder enviar e receber mensagens privadas
6. **RN6**: Os usuários devem poder criar e participar de grupos de interesse.
7. **RN7**: Somente usuários autenticados com plano premium poderão acessar filtros avançados, como rank e notas de interações.

### Requisitos Funcionais (RF)

1. **RF1**: Cadastrar usuários
2. **RF2**: Autenticar usuários
3. **RF3**: exibir os dados de um perfil de usuário
4. **RF4**: Listar todos os perfis de usuários com paginação
5. **RF5**: filtrar perfis de usuários por interesses de jogos em comum
6. **RF6**: buscar perfis de usuários por palavra-chave
7. **RF7**: visualizar detalhes do perfil de um usuário
8. **RF8**: Adicionar outros usuários como amigos
9. **RF9**: enviar e receber mensagens privadas
10. **RF10**: criar e participar de grupos de interesse
11. **RF11**: Deve ser possivel que usuários atualizem seus perfis de interesse
12. **RF12**: Deve ser possivel que os usuários façam publicações (texto/foto/vídeo)
13. **RF13**: Deve ser possivel que usuários interajam com as publicações dos outros (comentem e curtam)
14. **RF14**: Deve ser possivel que os usuários vejam as publicações de seus amigos em seu feed
15. **RF15**: Deve ser possivel que os usuários gerenciem suas interações públicas (excluir comentarios/postagens)

### Requisitos Não-Funcionais (RNF)

1. **RNF1**: A senha do usuário precisa estar criptografada
2. **RNF2**: Os dados da aplicação precisam estar persistidos no PostgreSQL
3. **RNF3**: Todas as listas de dados precisam estar paginadas.
4. **RNF4**: O usuário deve ser identificado por um JWT (JSON Web Token).
5. **RNF5**: O tempo de resposta para a busca e filtragem de perfis deve ser inferior a 2 segundos
6. **RNF6**: A aplicação deve ter alta disponibilidade
7. **RNF7**: Deverão ser feitos testes unitários e de integração com a biblioteca faker js.