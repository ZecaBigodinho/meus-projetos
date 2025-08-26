### 📱 Projeto Cantina Digital
Um aplicativo completo e funcional desenvolvido em Flutter com back-end serverless no Firebase. O projeto simula um sistema de pedidos para uma cantina escolar (CantinaSenac), permitindo que alunos realizem pedidos e a equipe da cantina gerencie as operações em tempo real.

### 🚀 Visão Geral
O projeto foi construído de forma incremental, começando com uma base de dados local (mock) e evoluindo para uma solução de nuvem completa e robusta, integrando os principais serviços do Firebase. A aplicação distingue dois tipos de usuários (alunos e administradores da cantina), cada um com sua própria interface e permissões.

### ✨ Funcionalidades Principais
### * **Autenticação Completa:**
* **Login com e-mail e senha.**
* **Cadastro de novos usuários (com criação de perfil no banco de dados).**
* **Recuperação de senha por e-mail.**
* **Sistema de Logout seguro.**
* **Distinção de papéis (aluno vs. cantina) com base em dados do Firestore.**

### * **Experiência do Aluno:**
* **Visualização do cardápio em tempo real com busca por nome e filtro por categoria.**
* **Tela de detalhes do produto com descrição e avaliações de outros usuários.**
* **Carrinho de compras com gerenciamento de estado local.**
* **Fluxo de pedido com pagamento simulado.**
* **Tela "Meus Pedidos" para acompanhar o status dos pedidos em tempo real.**
* **Sistema de avaliação de produtos para pedidos já entregues.**

### * **Painel do Administrador (Cantina):**
* **Dashboard com acesso às funcionalidades de gerenciamento.**
* **Visualização de todos os pedidos em tempo real.**
* **Atualização do status dos pedidos (ex: "Em Preparo", "Pronto para Retirada").**
* **Gerenciamento completo de produtos (CRUD - Criar, Ler, Atualizar, Excluir).**
* **Upload de imagens de produtos para o Firebase Storage diretamente do app.**

### * **Sistema de Back-end e Notificações:**
* **Notificações push em tempo real enviadas automaticamente para o cliente quando o status do pedido é atualizado para "Pronto para Retirada", utilizando Firebase Cloud Functions.**
