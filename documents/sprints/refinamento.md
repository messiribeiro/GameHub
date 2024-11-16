# Refinamento: Sistema de Doações com Metas e Benefícios para Jogos

---

## Objetivo da Sprint
Desenvolver o sistema de doações com metas e benefícios para jogos, permitindo que GameDevs organizem suas campanhas de arrecadação, disponibilizem benefícios exclusivos para doadores e integrem validações diretamente em seus jogos.

---

## User Stories e Regras de Negócio

### **1. Perfil de Jogo com Sistema de Doações (RF-30)**

**Como** GameDev, **eu quero** criar perfis específicos para meus jogos com metas de arrecadação, **para** organizar campanhas e engajar doadores.

#### Regras de Negócio
- Apenas GameDevs podem criar e gerenciar perfis de jogos.
- Cada perfil deve incluir título, descrição, metas de arrecadação, benefícios e imagem de capa.
- Deve haver um botão "Apoie" no perfil, redirecionando para a interface de doações.

#### Tarefas

**Backend:**
- Criar endpoints para adicionar, editar e excluir perfis de jogos. 
- Implementar lógica para associar perfis aos usuários GameDevs. 

**Frontend:**
- Desenvolver interface para criação e edição de perfis de jogos. 
- Exibir perfis com informações completas, incluindo botão "Apoie". 

#### Critérios de Aceitação
- GameDevs podem criar, editar e excluir perfis de jogos.
- Os perfis devem exibir informações detalhadas e permitir navegação para a interface de doações.

---

### **2. Sistema de Doações via Mercado Pago (RF-31)**

**Como** um usuário da plataforma, **eu quero** doar para apoiar um jogo, **para** ajudar no desenvolvimento e receber benefícios exclusivos.

#### Regras de Negócio
- As doações serão realizadas via integração com a API do Mercado Pago.
- Uma porcentagem (5%) da doação será destinada à plataforma, com o restante enviado ao GameDev.
- O sistema deve gerar um código único para cada doação, vinculando-o ao jogo e ao usuário doador.

#### Tarefas

**Backend:**
- Integrar a API do Mercado Pago para gerenciar doações.
- Implementar lógica para calcular e armazenar as porcentagens destinadas à plataforma e ao GameDev. 
- Criar endpoint para gerar e armazenar códigos únicos de doação. 

**Frontend:**
- Desenvolver interface de doação, incluindo cálculo automático de valores e taxa da plataforma. 
- Exibir confirmação e código gerado após a doação. 

#### Critérios de Aceitação
- O sistema deve processar doações via Mercado Pago, calcular taxas e armazenar dados com segurança.
- Cada doação gera um código único exibido ao usuário e associado ao jogo.

---

### **3. Benefícios para Doadores e Validação de Códigos (RF-32)**

**Como** GameDev, **eu quero** validar códigos de doação diretamente no meu jogo, **para** liberar benefícios exclusivos aos apoiadores.

#### Regras de Negócio
- Cada código de doação deve incluir informações como ID do usuário, ID do jogo e valor doado.
- O GameDev terá acesso a um endpoint para verificar a autenticidade de códigos e os benefícios associados.

#### Tarefas

**Backend:**
- Criar endpoint para validação de códigos, retornando informações sobre o doador e o valor investido. 
- Implementar lógica para escalonar benefícios conforme o valor doado. 

**Frontend:**
- Exibir benefícios desbloqueados ao usuário após a validação do código. 

#### Critérios de Aceitação
- O endpoint de validação deve retornar informações corretas e ser seguro.
- O sistema deve escalar benefícios de acordo com o valor doado.

---

### **4. Escalonamento de Benefícios para Doadores (RF-33)**

**Como** usuário da plataforma, **eu quero** receber benefícios proporcionais ao valor da minha doação, **para** obter recompensas mais significativas.

#### Regras de Negócio
- Benefícios serão definidos pelo GameDev e associados a intervalos de valores doados.
- O sistema deve permitir a configuração e exibição de diferentes níveis de benefício.

#### Tarefas

**Backend:**
- Criar modelo e endpoints para gerenciar níveis de benefícios vinculados aos perfis de jogos. 

**Frontend:**
- Desenvolver interface para exibição de níveis de benefício e suas condições. 

#### Critérios de Aceitação
- Benefícios são corretamente escalonados com base no valor doado.
- Níveis de benefício são exibidos no perfil do jogo.

---

## Critérios Gerais de Aceitação da Sprint
1. GameDevs conseguem criar perfis de jogos com metas e benefícios.
2. Usuários podem doar via Mercado Pago e receber códigos únicos.
3. O sistema valida códigos e retorna informações precisas.
4. Benefícios são ajustados proporcionalmente ao valor doado.
