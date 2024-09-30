### Sprint 1: Filtro de Perfis de Usuários por interesse em jogos em comum

**Valor**:  Permitir que os usuários encontrem novos jogadores dispostos a jogarem juntos 

**Requisitos**:
1. RF1: Cadastrar usuários
2. RF2: Autenticar usuários
3. RF3: exibir os dados de um perfil de usuário
4. RF5: filtrar perfis de usuários por interesses de jogos

**Requisitos Não funcionais**:
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
    - Logica de autenticação de usuários no sistema 

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

1. **Testes de Usabilidade com Usuários Reais**
    
    - Conduzir testes de usabilidade com um grupo de usuários reais.
    - Coletar feedback e identificar possíveis melhorias
2. **Correções e Melhorias**
    - Implementar melhorias e/ou correções com base no feedback dos usuários.