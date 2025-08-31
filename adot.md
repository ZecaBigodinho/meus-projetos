### Adote+ 🐾
O Adote+ é um aplicativo móvel de código aberto, desenvolvido em Flutter, com o objetivo de criar uma ponte entre animais que precisam de um lar e pessoas dispostas a adotá-los. Além da adoção, a plataforma facilita a busca por pets perdidos e apoia ONGs parceiras, centralizando esforços para o bem-estar animal.

### 📜 Visão Geral
Este projeto nasceu da necessidade de uma ferramenta acessível e centralizada para a comunidade de proteção animal. O aplicativo oferece um ecossistema completo onde usuários podem:

* **Adotar um Amigo: Navegar por uma lista de pets disponíveis para adoção, com filtros de busca por espécie, sexo e nome.**
* **Encontrar Pets Perdidos: Visualizar publicações de animais perdidos na região para ajudar a encontrá-los ou publicar um alerta sobre seu próprio pet desaparecido.**
* **Apoiar ONGs: Conhecer o trabalho de organizações parceiras e encontrar formas de contribuir financeiramente ou com voluntariado.**
* **Publicar e Gerenciar: Usuários podem criar publicações para adoção ou de pets perdidos, além de editar e remover seus próprios anúncios.**

### 📂 Estrutura de Diretórios
O núcleo do projeto está contido no diretório lib, que segue uma arquitetura orientada a funcionalidades para garantir escalabilidade e manutenibilidade.

lib/
├── main.dart                 # Ponto de entrada da aplicação e configuração do roteador
├── firebase_options.dart     # Configuração do projeto Firebase
├── models/                   # Modelos de dados (objetos de negócio)
│   ├── ong_model.dart
│   ├── pet_model.dart
│   └── lost_pet_model.dart
├── pages/                    # Telas (UI) da aplicação
│   ├── apresentar_page.dart
│   ├── cadastro_login_page.dart
│   ├── criar_perfil_page.dart
│   ├── principal_tela_page.dart
│   ├── pets_lista_page.dart
│   └── ...                   # Demais telas
├── services/                 # Lógica de negócio e comunicação com APIs externas
│   ├── cloudinary_service.dart
│   ├── firebase_auth_service.dart
│   └── firestore_service.dart
└── widgets/                  # Componentes de UI reutilizáveis
    ├── app_drawer.dart
    └── nova_publicacao_widget.dart
main.dart: Arquivo principal que inicializa o Firebase e define todas as rotas de navegação do aplicativo usando o pacote go_router.

/models: Contém as classes que modelam os dados da aplicação, como Pet e Ong. Garante uma estrutura de dados consistente e fortemente tipada.

/pages: Cada arquivo representa uma tela completa do aplicativo, responsável por compor a interface e gerenciar seu estado local.

/services: Camada de abstração que lida com toda a lógica de negócio e comunicação externa, como autenticação com Firebase, operações no Firestore e upload de imagens para o Cloudinary.

/widgets: Armazena componentes de UI customizados e reutilizáveis, como o menu de navegação (AppDrawer), para manter o código limpo e evitar repetição.


### 🛠️ Tecnologias e Arquitetura
O Adote+ foi construído com tecnologias modernas e uma arquitetura cliente-servidor, utilizando o melhor do ecossistema Flutter e Firebase.

Componente	Tecnologia/Serviço	Propósito
Framework	Flutter	Desenvolvimento de UI nativa e performática para Android e iOS.
Linguagem	Dart	Linguagem de programação principal, otimizada para UI.
Autenticação	Firebase Authentication	Gerenciamento seguro de contas de usuário (email/senha).
Banco de Dados	Cloud Firestore	Banco de dados NoSQL em tempo real para armazenar dados de pets, ONGs e usuários.
Hospedagem de Mídia	Cloudinary	Serviço especializado para armazenamento, otimização e entrega de imagens.
Roteamento	go_router	Gerenciamento de navegação e rotas de forma robusta e centralizada.
APIs Externas	url_launcher	Interação com aplicativos externos, como WhatsApp e Email.
Seleção de Imagens	image_picker	Acesso à galeria e câmera do dispositivo para upload de fotos.

### A arquitetura de alto nível separa a aplicação em três camadas principais:

* **Apresentação (UI): Formada pelos diretórios pages/ e widgets/.**
* **Lógica de Negócio (Services): Centralizada no diretório services/.**
* **Dados (Data): Representada pelo diretório models/ e pelos serviços de backend (Firebase/Cloudinary).**
