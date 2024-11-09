# Refinamento: Perfis Específicos de Jogos e Funcionalidade Premium para Gamers

**Valor:** Melhorar a usabilidade da plataforma, permitindo que usuários encontrem outros jogadores de forma personalizada e aprimorem sua experiência com funcionalidades exclusivas, promovendo uma interação mais segura e customizável.

---

## User Stories e Regras de Negócio

### Implementação de Assinatura Premium com Stripe (RF-20)

**Como** um usuário, **eu quero** poder assinar o plano de "Usuário Premium" de forma segura, **para** ter acesso a funcionalidades exclusivas, como filtros personalizados e métricas avançadas de interação.

#### Regras de Negócio
- A plataforma deve permitir o pagamento de uma assinatura única para o plano "Usuário Premium" utilizando o Stripe.
- Usuários premium terão acesso a um filtro personalizado para buscar jogadores com base em critérios como rank, tempo de jogo e notas de interações.
- Assinantes premium também poderão visualizar métricas detalhadas de interações com outros usuários.

#### Tarefas

**Backend:**
- Configurar a integração com a API do Stripe para gerenciar a assinatura do plano "Usuário Premium", incluindo endpoints para criação, cancelamento e verificação de status de assinatura. *(Lauro)*
- Definir o plano de assinatura "Usuário Premium" na API do Stripe, com o valor mensal ou anual conforme definido. *(Lucas)*
- Implementar lógica no backend para garantir que apenas usuários premium possam acessar as funcionalidades exclusivas, como o filtro personalizado. *(Lucas)*

**Frontend:**
- Criar uma interface de seleção para o plano "Usuário Premium", destacando as vantagens e funcionalidades exclusivas. *(Almir)*
- Implementar a interface de pagamento com Stripe para assinatura, exibindo confirmação e status da assinatura após o pagamento. *(Micael)*

#### Critérios de Aceitação
- O sistema deve permitir que os usuários assinem o plano "Usuário Premium" por meio do Stripe e visualizem o status da assinatura.
- Após a confirmação do pagamento, o sistema deve atualizar o status do usuário para premium, concedendo acesso imediato ao filtro personalizado e demais funcionalidades exclusivas.
- Usuários não premium não devem conseguir acessar funcionalidades reservadas aos assinantes premium.

---

### Funcionalidades Premium para Gamers (RF-21)

**Como** um usuário premium, **eu quero** utilizar filtros e métricas exclusivas de interação, **para** que minhas conexões sejam mais personalizadas e relevantes.

#### Regra de Negócio
- Apenas usuários premium terão acesso a filtros avançados, como rank, notas de interações e métricas de tempo de jogo.

#### Tarefas

**Backend:**
- Criar endpoint para filtrar usuários por rank nos jogos. *(Lucas)*
- Implementar endpoint para registrar e exibir notas de interação entre usuários, com atualizações baseadas na experiência do usuário. *(Lauro)*
- Adicionar funcionalidade para calcular e exibir o tempo de jogo dos usuários. *(Lauro)*

**Frontend:**
- Desenvolver interface para aplicar o filtro por rank de usuário e exibir resultados adequadamente. *(Micael)*
- Criar interface para visualização das notas de interação entre usuários premium. *(Almir)*
- Exibir o tempo de jogo dos usuários em perfis e em filtros específicos para premium. *(Micael)*

#### Critérios de Aceitação
- Filtros e métricas exclusivas devem ser exibidos corretamente para usuários premium.
- As notas de interação e o tempo de jogo devem ser atualizados e exibidos em tempo real para as interações.

---

### Perfis Específicos de Jogos para Usuários GameDev (RF-21)

**Como** um usuário com perfil gamedev, **eu quero** ter perfis específicos para cada jogo que adiciono, **para** organizar e promover meus projetos de forma individual.

#### Regra de Negócio
- Apenas usuários com o perfil gamedev premium podem adicionar perfis específicos para jogos.
- Cada perfil de jogo deve incluir informações como título, descrição, imagem, gênero e links para download ou plataformas de venda.

#### Tarefas

**Backend:**
- Criar endpoints para adicionar, editar e excluir perfis de jogos para gamedevs. *(Lauro)*

**Frontend:**
- Criar interface para exibição de perfis de jogos. *(Micael)*
- Implementar a lógica para que os perfis dos jogos exibam postagens dos usuários que marcaram o perfil do jogo. *(Micael)*

#### Critérios de Aceitação
- Usuários gamedevs devem conseguir adicionar, editar e excluir perfis de jogos.
- Perfis de jogos devem ser exibidos corretamente no perfil do usuário gamedev, incluindo todas as informações especificadas.
