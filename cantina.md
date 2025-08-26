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

### 🏛️ Arquitetura
A aplicação segue uma arquitetura de cliente-servidor com um back-end totalmente serverless fornecido pelo Firebase.
* **O aplicativo Flutter (cliente) se comunica diretamente com os serviços do Firebase (Auth, Firestore, Storage) para a maioria das operações.**
* **O Cloud Firestore é a fonte única de verdade para todos os dados persistentes (usuários, produtos, pedidos, avaliações), utilizando streams para atualizações em tempo real na interface.**
* **As Cloud Functions fornecem uma lógica de back-end reativa e automatizada, desacomplando a responsabilidade de enviar notificações do aplicativo cliente. Quando o administrador atualiza um pedido no Firestore, uma função é acionada na nuvem para enviar a notificação push.**

## 📂 Estrutura de Diretórios

A estrutura de pastas do projeto segue as convenções da comunidade Flutter para organização e escalabilidade.

```
cantina/
├── android/              # Configurações específicas do Android
├── assets/
│   └── icon/
│       └── icon.png      # Ícone de alta resolução para o app
├── functions/            # Projeto Node.js/TypeScript para as Cloud Functions
│   └── src/
│       └── index.ts      # Lógica de back-end para notificações
├── lib/
│   ├── main.dart         # Ponto de entrada da aplicação
│   ├── firebase_options.dart # Gerado pelo FlutterFire
│   ├── models/           # Classes de modelo de dados (Product, Order, etc.)
│   ├── screens/          # Widgets que representam cada tela do app
│   └── services/         # Lógica de negócio e comunicação com Firebase
├── pubspec.yaml          # Definição de dependências e metadados do projeto
└── cors.json             # Arquivo de configuração de CORS para o Firebase Storage
```

## 💻 Tecnologias Utilizadas

| Categoria          | Tecnologia                                                              |
| :----------------- | :---------------------------------------------------------------------- |
| **Cross-Platform** | [Flutter](https://flutter.dev/)                                         |
| **Linguagem (App)**| [Dart](https://dart.dev/)                                               |
| **Back-end** | [Firebase (Serverless)](https://firebase.google.com/)                   |
| **Autenticação** | [Firebase Authentication](https://firebase.google.com/docs/auth)        |
| **Banco de Dados** | [Cloud Firestore](https://firebase.google.com/docs/firestore) (NoSQL)   |
| **Armazenamento** | [Firebase Storage](https://firebase.google.com/docs/storage)            |
| **Notificações** | [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging)|
| **Lógica de Back-end**| [Cloud Functions for Firebase](https://firebase.google.com/docs/functions) (TypeScript) |
| **Estado (Simples)** | [ValueNotifier](https://api.flutter.dev/flutter/foundation/ValueNotifier-class.html)                   |
| **Ícone do App** | [flutter\_launcher\_icons](https://pub.dev/packages/flutter_launcher_icons)                          |
