### Regras de Negócio (RN)

1. **RN1**: Os campos `username`, `email` e `password` serão de preenchimento obrigatório
2. **RN2**: O usuário não deve poder se cadastrar com um e-mail duplicado.
3. **RN3**: Os filtros de busca devem permitir múltiplas seleções (vários gêneros de jogos)
4. **RN4**: Os usuários devem poder adicionar outros usuários como amigos
5. **RN5**: Os usuários devem poder enviar e receber mensagens privadas
6. **RN6**: Os usuários devem poder criar e participar de grupos de interesse.

### Requisitos Funcionais (RF)

1. **RF1**: Cadastrar usuários
2. **RF2**: Autenticar usuários
3. **RF3**: exibir os dados de um perfil de usuário
4. **RF4**: Listar todos os perfis de usuários com paginação
5. **RF5**: filtrar perfis de usuários por interesses de jogos
6. **RF6**: buscar perfis de usuários por palavra-chave
7. **RF7**: visualizar detalhes do perfil de um usuário
8. **RF8**: Adicionar outros usuários como amigos
9. **RF9**: enviar e receber mensagens privadas
10. **RF10**: criar e participar de grupos de interesse
11. **RF11**: Deve ser possvel que usuários atualizem seus perfis de interesse
12. **RF12**: Deve ser possvel que usuários comentem nas publicações dos outros
13. **RF13**: Deve ser possvel que usuários curtam as publicações dos outros

### Requisitos Não-Funcionais (RNF)

1. **RNF1**: A senha do usuário precisa estar criptografada
2. **RNF2**: Os dados da aplicação precisam estar persistidos no PostgreSQL
3. **RNF3**: Todas as listas de dados precisam estar paginadas.
4. **RNF4**: O usuário deve ser identificado por um JWT (JSON Web Token).
5. **RNF5**: O tempo de resposta para a busca e filtragem de perfis deve ser inferior a 2 segundos
6. **RNF6**: A aplicação deve ter alta disponibilidade
7. **RNF7**: Deverão ser feitos testes unitários e de integração com a biblioteca faker js.

### Sprint 1: Filtro de Perfis de Usuários
**Valor**:  Permitir que os usuários encontrem novos jogadores dispostos a jogarem juntos 
**Desenvolvimento do Backend**
**Objetivo**: Implementar a lógica de filtragem no servidor.

**Tarefas**:

1. **Configuração do Ambiente de Desenvolvimento**
    
    - Configurar o ambiente de desenvolvimento .
2. **Criação de Endpoints para Busca e Filtragem de Perfis**
    
    - Criar endpoints RESTful para busca e filtragem de perfis de usuários.
    - Implementar a lógica de filtragem baseada em interesses de jogos .
    - Garantir que os endpoints retornem dados paginados.
3. **Autenticação e Autorização**
    
    - Implementar autenticação de usuários utilizando JWT
    - Garantir que apenas usuários autenticados possam acessar os endpoints de busca e filtragem
4. **Criptografia de Senhas**
    
    - Implementar a criptografia de senhas dos usuários utilizando bcrypt
5. **Testes de Backend**
    
    - Escrever testes unitários e de integração para os endpoints criados
    - Utilizar a lib faker para gerar dados de teste

 **Desenvolvimento do Frontend**

**Objetivo**: Implementar a interface de usuário para o filtro.

**Tarefas**:

1. **Desenvolvimento dos Componentes de UI para o Filtro**
    
    - Criar componentes de UI para a listagem de perfis de usuários
    - Implementar filtros de busca por interesses de jogos, palavra-chave, etc
    - Garantir que a interface seja responsiva e funcione em dispositivos móveis e desktops
2. **Integração com os Endpoints do Backend**
    
    - Integrar os componentes de UI com os endpoints de busca e filtragem do backend
    - Implementar a lógica de paginação na interface de usuario
3. **Autenticação no Frontend**
    
    - Implementar a lógica de autenticação no frontend utilizando JWT.
    - Garantir que apenas usuários autenticados possam acessar a funcionalidade de filtro de perfis.
4. **Testes de Usabilidade e Ajustes**
    
    - Conduzir testes de usabilidade com usuários reais
    - Coletar feedback e realizar ajustes na interface de usuário

**Testes e Validação** 

**Objetivo**: Garantir que o filtro funcione corretamente

**Tarefas**:

1. **Testes Unitários e de Integração**
    
    - Realizar testes unitários e de integração no backend e frontend.
    - Garantir que todas as funcionalidades estejam funcionando conforme esperado.
2. **Testes de Usabilidade com Usuários Reais**
    
    - Conduzir testes de usabilidade com um grupo de usuários reais.
    - Coletar feedback e identificar possíveis melhorias
3. **Correções e Melhorias**
    - Implementar melhorias e/ou correções com base no feedback dos usuários.