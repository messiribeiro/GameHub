## Product Backlog 

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
16. **RF16**: Adição de Jogos por Usuários Premium 
17. **RF17**: Sistema de Pagamento para Tornar-se Premium
18. **RF18**: Gestão de Assinaturas
19. **RF19**: Benefícios de Usuário assinantes do plano gamedev (perfil de gamedev/ selo de gamedev)

### Requisitos Não-Funcionais (RNF)

1. **RNF1**: A senha do usuário precisa estar criptografada
2. **RNF2**: Os dados da aplicação precisam estar persistidos no PostgreSQL
3. **RNF3**: Todas as listas de dados precisam estar paginadas.
4. **RNF4**: O usuário deve ser identificado por um JWT (JSON Web Token).
5. **RNF5**: O tempo de resposta para a busca e filtragem de perfis deve ser inferior a 2 segundos
6. **RNF6**: A aplicação deve ter alta disponibilidade
7. **RNF7**: Deverão ser feitos testes unitários e de integração com a biblioteca faker js.