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

## Sprint backlog
### Sprint 1: Filtro de Perfis de Usuários por interesse em jogos em comum
**Valor**:  Permitir que os usuários encontrem novos jogadores dispostos a jogarem juntos 

**Requisitos**:
1. RF1: Cadastrar usuários
2. RF2: Autenticar usuários
3. RF3: exibir os dados de um perfil de usuário
4. RF5: filtrar perfis de usuários por interesses de jogos

1. RNF1: A senha do usuário precisa estar criptografada
2. RNF2: Os dados da aplicação precisam estar persistidos no PostgreSQL
3. RNF4: O usuário deve ser identificado por um JWT (JSON Web Token).
4. RNF5: O tempo de resposta para a busca e filtragem de perfis deve ser inferior a 2 segundos
5. RNF7: Deverão ser feitos testes unitários e de integração com a biblioteca faker js.
6. RNF3: Todas as listas de dados precisam estar paginadas.

**Desenvolvimento do Backend**

**Objetivo**: Implementar a lógica de filtragem de usuários por jogos de interesse em comum

**Tarefas**:

1. **Lógica de criação de usuário**
    
    - lógica para criação e armazenamento de novos usuários no sistema
    - lógica para criação e armazenamento de novos jogos no sistema
    - relacionamento entre as entidades User e Game, para que cada usuário possa associar múltiplos jogos ao seu perfil 

2. **Criação de Endpoints para Busca e Filtragem de Perfis**

    - Implementar a lógica de filtragem baseada em interesses de jogos em comum.
    - Criar endpoints RESTful para busca e filtragem de perfis de usuários.
    - Garantir que os endpoints retornem dados paginados.

3. **Autenticação e Autorização**
    
    - Implementar autenticação de usuários utilizando JWT
    - Garantir que apenas usuários autenticados possam acessar os endpoints de busca e filtragem
    - Implementar a criptografia de senhas dos usuários utilizando bcrypt
    
4. **Testes de Backend**
    
    - Escrever testes unitários e de integração para os endpoints criados
    - Utilizar a lib faker para gerar dados de teste

**Desenvolvimento do Frontend**

**Objetivo**: Implementar a interface de usuário para o filtro.

**Tarefas**:

1. **Desenvolvimento dos Componentes de UI para o Filtro**
    
    - Componentes UI do perfil estático do usuário
    - Criar componentes de UI para a listagem de perfis de usuários
    - Implementar a tela para o usuário escolher os jogos de interesse

2. **Integração com os Endpoints do Backend**
    
    - Integrar os componentes de UI com os endpoints de busca e filtragem do backend
    - Implementar a lógica de paginação na interface de usuario

3. **Autenticação no Frontend**
    
    - Implementar a lógica de autenticação no frontend utilizando JWT.
    - Garantir que apenas usuários autenticados possam acessar a funcionalidade das telas de filtro de perfis.

4. **Testes de Usabilidade e Ajustes**
    
    - Conduzir testes de usabilidade com usuários reais
    - Coletar feedback e realizar ajustes na interface de usuário

**Testes e Revisão** 

**Objetivo**: Garantir que o filtro de usuários funcione corretamente

**Tarefas**:

1. **Testes Unitários e de Integração**
    
    - Realizar testes unitários e de integração no backend e frontend.
    - Garantir que todas as funcionalidades estejam funcionando conforme esperado.
2. **Testes de Usabilidade com Usuários Reais**
    
    - Conduzir testes de usabilidade com um grupo de usuários reais.
    - Coletar feedback e identificar possíveis melhorias
3. **Correções e Melhorias**
    - Implementar melhorias e/ou correções com base no feedback dos usuários.

### Sprint 2: Perfil de Usuário e Chat Privado em Tempo Real
**Valor**: Permitir que os usuários se comuniquem com outros usuários encontrados na feature de filtro de perfis e visualizem informações detalhadas dos perfis.

**Requisitos**:
1. RF3: Exibir os dados de um perfil de usuário
2. RF7: Visualizar detalhes do perfil de um usuário
3. RF8: Adicionar outros usuários como amigos
4. RF9: Enviar e receber mensagens privadas
5. RF10: Criar e participar de grupos de interesse

**Requisitos Não-Funcionais**:
1. RNF1: A senha do usuário precisa estar criptografada
2. RNF2: Os dados da aplicação precisam estar persistidos no PostgreSQL
3. RNF4: O usuário deve ser identificado por um JWT (JSON Web Token).
4. RNF5: O tempo de resposta para a busca e filtragem de perfis deve ser inferior a 2 segundos
5. RNF6: A aplicação deve ter alta disponibilidade
6. RNF7: Deverão ser feitos testes unitários e de integração com a biblioteca faker js.

### Desenvolvimento do Backend

**Objetivo**: Implementar a funcionalidade de visualização de perfil e chat privado em tempo real.

**Tarefas**:

1. **Perfil de Usuário** (Lauro)
    - Implementar a lógica para exibir os dados detalhados do perfil de um usuário.
    - Criar endpoints RESTful para obter detalhes do perfil e permitir que usuários visualizem esses dados.
    - Garantir que a visualização do perfil esteja disponível apenas para usuários autenticados.

2. **Chat Privado em Tempo Real** (Lauro)
    - Implementar a lógica para envio e recebimento de mensagens privadas em tempo real.
    - Utilizar WebSocket ou outra tecnologia de comunicação em tempo real para permitir que mensagens sejam enviadas e recebidas instantaneamente.
    - Criar endpoints RESTful para enviar e buscar mensagens privadas.

3. **Gerenciamento de Amizades** (Lucas)
    - Implementar a lógica para adicionar e gerenciar amigos entre os usuários.
    - Criar endpoints RESTful para enviar solicitações de amizade e aceitar ou recusar solicitações recebidas.

4. **Testes de Backend** (Lucas)
    - Escrever testes unitários e de integração para os endpoints criados, incluindo testes para a funcionalidade de chat em tempo real.
    - Utilizar a lib faker para gerar dados de teste e garantir que os testes cobrem todos os casos possíveis.

### Desenvolvimento do Frontend

**Objetivo**: Implementar a interface de usuário para visualização de perfil e chat privado.

**Tarefas**:
 
1. **Desenvolvimento dos Componentes de UI para Perfil e Chat** (Micael)
    - Criar componentes de UI para exibir os detalhes do perfil de usuário.
    - Implementar a interface para o chat privado, incluindo caixas de mensagem, histórico de chat e notificações.
    - Criar a tela para gerenciar amizades, incluindo envio e recebimento de solicitações.

2. **Integração com os Endpoints do Backend** (Almir)
    - Integrar os componentes de UI com os endpoints de perfil e chat do backend.
    - Garantir que as funcionalidades de perfil e chat estejam devidamente conectadas com a lógica de backend e a comunicação em tempo real.

3. **Autenticação no Frontend** (Micael)
    - Garantir que apenas usuários autenticados possam acessar as funcionalidades de perfil e chat.
    - Implementar a lógica de autenticação no frontend utilizando JWT para proteger o acesso às funcionalidades.

4. **Testes de Usabilidade e Ajustes** (Almir)
    - Conduzir testes de usabilidade com usuários reais para a funcionalidade de perfil e chat.
    - Coletar feedback e realizar ajustes na interface de usuário para melhorar a experiência.

### Testes e Revisão (Todos)

**Objetivo**: Garantir que a funcionalidade de perfil e chat privado em tempo real funcionem corretamente.

**Tarefas**:

1. **Testes Unitários e de Integração**
    - Realizar testes unitários e de integração no backend e frontend para as novas funcionalidades.
    - Garantir que todas as funcionalidades estejam funcionando conforme esperado e não introduzam novos problemas.

2. **Testes de Usabilidade com Usuários Reais**
    - Conduzir testes de usabilidade com um grupo de usuários reais para as funcionalidades de perfil e chat.
    - Coletar feedback sobre a experiência do usuário e identificar possíveis melhorias.

3. **Correções e Melhorias**
    - Implementar melhorias e/ou correções com base no feedback dos usuários.
    - Atualizar a documentação e realizar quaisquer ajustes necessários antes do próximo ciclo de desenvolvimento.