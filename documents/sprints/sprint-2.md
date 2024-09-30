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

1. **Testes de Usabilidade com Usuários Reais**
    - Conduzir testes de usabilidade com um grupo de usuários reais para as funcionalidades de perfil e chat.
    - Coletar feedback sobre a experiência do usuário e identificar possíveis melhorias.

2. **Correções e Melhorias**
    - Implementar melhorias e/ou correções com base no feedback dos usuários.
    - Atualizar a documentação e realizar quaisquer ajustes necessários antes do próximo ciclo de desenvolvimento.