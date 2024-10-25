# Sprint 4: Adição de Jogos por Usuários Premium e Sistema de Pagamento

**Valor:** Permitir que usuários premium (assinantes do plano "gamedev") adicionem seus jogos à rede social, aumentando a visibilidade de seus projetos e facilitando a interação com a comunidade. Também implementaremos um sistema de pagamento para que os usuários possam se tornar premium.

## User Stories e Regras de Negócio

### Adição de Jogos por Usuários Premium (RF-16)
**Como** um usuário premium (gamedev), **eu quero** adicionar meus jogos à rede social, **para** promover meu trabalho e facilitar a interação com os jogadores.

#### Regra de Negócio
- Apenas usuários premium podem adicionar jogos à plataforma.
- Os jogos devem incluir informações como título, descrição, gênero, imagem e links para plataformas de distribuição.
- Uma vez adicionados, os jogos ficarão visíveis para todos os usuários da rede social.

#### Tarefas:

**Backend:**
- Criar endpoints RESTful para permitir que usuários premium adicionem, editem e excluam jogos. (Lauro)

**Frontend:**
- Criar UI para que usuários premium possam adicionar jogos (campos para título, descrição, imagem, etc.). (Micael)
- Implementar lógica para exibir os jogos adicionados no perfil do usuário. (Micael)

#### Critérios de Aceitação:
- Usuários premium devem conseguir adicionar, editar e excluir jogos de seus perfis.
- Os jogos devem ser exibidos corretamente nos perfis dos desenvolvedores.

---

### Sistema de Pagamento para Tornar-se Premium (RF-17)
**Como** um usuário, **eu quero** pagar para me tornar premium, **para** ter a capacidade de adicionar meus jogos e acessar funcionalidades exclusivas.

#### Regra de Negócio
- O sistema deve suportar métodos de pagamento como cartão de crédito, débito e PayPal.
- Usuários devem ser promovidos a premium imediatamente após a confirmação do pagamento.

#### Tarefas:

**Backend:**
- Integrar um serviço de pagamento (Stripe/PayPal). (Lucas)
- Implementar lógica para atualizar o status do usuário para premium após confirmação de pagamento. (Lauro)

**Frontend:**
- Criar interface para o processo de pagamento. (Almir)
- Implementar lógica para enviar os dados de pagamento ao backend e exibir o status de pagamento. (Almir)
- Implementar um selo de "gamedev" para os usuarios que aderirem ao plano 

#### Critérios de Aceitação:
- O sistema deve aceitar pagamentos via cartão de crédito, débito e PayPal.
- O status do usuário deve ser atualizado para premium imediatamente após o pagamento ser processado.
- O usuário deve receber uma confirmação de sucesso ou erro após o pagamento.

---

### Gestão de Assinaturas (RF-18)
**Como** um usuário premium, **eu quero** gerenciar minha assinatura (cancelar ou renovar), **para** ter controle sobre meus pagamentos recorrentes.

![image](https://github.com/user-attachments/assets/de0dbeac-af9e-4c94-a7a3-d4db713cd18b)

#### Regra de Negócio
- Usuários premium podem cancelar ou renovar suas assinaturas a qualquer momento.
- O sistema deve alertar os usuários sobre a expiração de suas assinaturas.

#### Tarefas:

**Backend:**
- Implementar lógica para cancelar ou renovar assinaturas. (Lauro)
- Configurar alertas automáticos para a expiração de assinaturas. (Lucas)

**Frontend:**
- Criar UI para que os usuários gerenciem suas assinaturas. (Micael)
- Implementar lógica de alertas e gerenciamento de assinatura. (Micael)

#### Critérios de Aceitação:
- Usuários devem ser capazes de cancelar ou renovar suas assinaturas.
- O sistema deve enviar alertas automáticos para expiração de assinaturas.

---

### Benefícios de Usuário Premium (RF-19)
**Como** um usuário premium, **eu quero** ter acesso a funcionalidades exclusivas, **como** um selo premium no perfil e meus jogos listados no meu perfil de gamedev.

![image](https://github.com/user-attachments/assets/bf38415a-0edf-4f69-9dca-aac921d92c4e)

#### Regra de Negócio
- Usuários premium devem ter um selo destacado em seus perfis.
- Usuários premium, assinantes do plano "gamedev" podem ter perfis de gamedev

#### Tarefas:

**Backend:**
- Implementar lógica para adicionar o selo premium aos perfis. (Lucas)
- Exibir no perfil do gamedev os jogos que ele adicionou na plataforma (Lauro)

**Frontend:**
- Criar UI para exibir o selo premium nos perfis. (Almir)
- Implementar lógica de destaque de usuários premium nas buscas. (Micael)

#### Critérios de Aceitação:
- Perfis de usuários premium devem exibir o selo.
- Usuários premium devem aparecer em destaque nas buscas.
