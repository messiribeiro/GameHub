# Modelo Arquitetural

## 1. Arquitetura Geral

### 1.1 Frontend (Cliente)
**Tecnologia**: React, React Native

**Componentes**:
- Tela de Login e Cadastro
- Tela de Perfil do Usuário
- Tela de Busca de Jogadores
- Tela de Criação de Grupos de Jogo
- Tela de Chat
- Notificações

### 1.2 Backend (Servidor)
**Tecnologia**: Node.js (Framework: Nestjs)

**Componentes**:
- **Autenticação**: Sistema de login e gerenciamento de sessões
- **Perfil do Usuário**: CRUD (Create, Read, Update, Delete) para perfis
- **Busca de Jogadores**: Algoritmo para encontrar jogadores com base em critérios
- **Grupos de Jogo**: CRUD para grupos e gerenciamento de membros
- **Chat**: Sistema de mensagens em tempo real
- **Notificações**: Envio de notificações push para eventos importantes

### 1.3 Banco de Dados
**Tecnologia**: PostgreSQL

**Estrutura**:
- **Usuários**: Dados do perfil, preferências de jogos, histórico de atividades
- **Jogos**: Informações sobre jogos, categorias, e popularidade
- **Grupos de Jogo**: Dados sobre grupos, membros e atividades
- **Mensagens**: Histórico de chat entre usuários

### 1.4 APIs
**APIs Externas**:
- **Autenticação**: Serviços de autenticação social 
- **Dados de Jogos**: APIs para obter informações sobre jogos
- **Pagamento**: APIs para efetuar o pagamento de compras realizadas dentro do aplicativo.


## 2. Fluxo de Dados

1. **Autenticação e Cadastro**:
   - O usuário se registra ou faz login no aplicativo.
   - O backend valida e cria uma sessão para o usuário.

2. **Perfil e Busca**:
   - O usuário edita seu perfil e define preferências de jogos.
   - O backend armazena as informações e permite a busca de jogadores com base nas preferências.

3. **Grupos de Jogo**:
   - O usuário cria ou participa de grupos de jogo.
   - O backend gerencia as interações e a estrutura dos grupos.

4. **Chat e Notificações**:
   - O usuário envia e recebe mensagens em tempo real.
   - O backend gerencia o chat e envia notificações para eventos importantes.

## 3. Considerações Adicionais

- **Escalabilidade**: Devemos considerar que o sistema vai escalar com o aumento do número de usuários.
- **Segurança**: Temos que garantir a proteção dos dados dos usuários e a segurança das comunicações.
- **Desempenho**: Devemos otimizar o desempenho do backend e do frontend para uma boa experiência do usuário.
- **Flexibilidade**: Nossa arquitetura visa tornar o código reutilizável, de fácil manutenção, testável e consequentemente um software mais sucetível a mudanças inevitáveis ​​nos requisitos do cliente (o que sempre acontece).
- **Arquitetura limpa**: É utilizado princípios de injeção e inversão de depedências 

[modelo arquitetural](https://github.com/user-attachments/assets/bf79f8d1-42b9-4bae-a212-d97ca360f918)
[camadas da aplicação](https://github.com/user-attachments/assets/16f385b0-a477-4690-a634-dd44872af7db)
[Exemplo de código](https://github.com/lauroolim/arch-pattern)

