# 📱 Cantina Senac Digital - Solução de Autoatendimento

![Flutter](https://img.shields.io/badge/Flutter-3.0%2B-blue) ![Firebase](https://img.shields.io/badge/Firebase-Core-orange) ![Status](https://img.shields.io/badge/Status-MVP%20Finalizado-green)

> **Acabe com as filas.** Uma solução completa de pedidos móveis, agendamento de retirada e carteira digital para otimizar o intervalo no Senac.

## 🚀 Sobre o Projeto

O **Cantina Senac Digital** nasceu para resolver a "dor" mais comum dos intervalos acadêmicos: perder tempo na fila para comprar comida.

Este aplicativo permite que alunos e funcionários realizem pedidos antecipados, paguem via carteira digital e apenas retirem o produto no balcão "Fura-Fila" usando um comprovante digital seguro. Para a gestão, oferece um painel administrativo completo para controle de pedidos e cardápio em tempo real.

---

## ✨ Funcionalidades Principais

### 🎓 Para o Aluno (App Mobile)
* **Fura-Fila (Agendamento):** O aluno escolhe o horário exato que deseja retirar o lanche (ex: 09:30).
* **Carteira Digital (Senac Pay):** Sistema de saldo pré-pago simulado. O aluno recarrega e gasta sem precisar de cartão ou dinheiro na hora.
* **Cardápio Interativo:** Fotos, descrições, preços e avaliações (estrelas) dos produtos.
* **Carrinho Inteligente:** Adição de múltiplos itens e cálculo automático.
* **Comprovante Digital (Voucher):** Tela com QR Code visual e número do pedido para retirada rápida.
* **Timeline de Pedido:** Acompanhamento visual do status (Pendente -> Preparando -> Pronto -> Entregue).

### 👨‍🍳 Para a Cantina (Painel Administrativo)
* **Gestão de Pedidos em Tempo Real:** Os pedidos aparecem instantaneamente, ordenados por urgência (horário agendado).
* **Controle de Status:** Botões simples para avançar o pedido na cozinha.
* **Gerenciamento de Cardápio (CRUD):**
    * Adicionar, Editar e Remover produtos.
    * **Upload de Fotos:** Sistema otimizado que permite enviar fotos da galeria do celular ou computador diretamente para o banco de dados (Base64).
    * Controle de estoque (pausar vendas).

---

## 🛠️ Tecnologias Utilizadas

O projeto segue a arquitetura **Clean Architecture** (separação entre Camada de Apresentação, Modelos e Serviços).

* **Frontend:** [Flutter](https://flutter.dev/) (Dart) - Compatível com Android, iOS e Web.
* **Backend (Serverless):** [Google Firebase](https://firebase.google.com/).
    * **Firestore Database:** Banco de dados NoSQL em tempo real.
    * **Firebase Auth:** Sistema de autenticação e login.
* **Gestão de Estado:** `ValueNotifier` e `ChangeNotifier` (Nativo e leve).
* **Armazenamento de Imagens:** Otimização via Base64 (Armazenamento direto no documento para redução de custos de infraestrutura no MVP).

---

## 🔮 Roteiro de Evolução & Investimento (Roadmap)

Este projeto foi desenvolvido como um **MVP (Produto Viável Mínimo)** funcional, focado em validar a experiência do usuário com custo zero de infraestrutura.

Para a implantação oficial em larga escala no Senac, buscamos investimento para as seguintes melhorias de infraestrutura e segurança:

### 1. Infraestrutura de Banco de Dados (Escalabilidade)
* **Situação Atual:** Utilizamos o plano gratuito (Spark) do Firebase, com imagens salvas como texto (Base64) para economizar.
* **Atualização Necessária:** Migração para um banco de dados dedicado (PostgreSQL via Supabase ou plano Blaze do Firebase) e uso de **Storage Dedicado (CDN)** para imagens em alta resolução sem impactar a performance do banco.

### 2. Integração Financeira Real
* **Situação Atual:** O sistema simula recargas e pagamentos ("Sandbox") para demonstrar o fluxo.
* **Atualização Necessária:** Integração com **Gateway de Pagamento Real** (API do Mercado Pago ou Pagar.me) para processar Pix automático e Cartão de Crédito com conciliação bancária e emissão de Nota Fiscal (NFC-e).

### 3. Segurança & Compliance
* **Situação Atual:** Regras de segurança básicas para demonstração.
* **Atualização Necessária:** Implementação de regras de segurança rígidas no Firestore (Security Rules), criptografia de ponta a ponta e adequação à **LGPD** (Lei Geral de Proteção de Dados).

---

## 🚀 Como Rodar o Projeto

### Pré-requisitos
* Flutter SDK instalado.
* Conta no Firebase configurada.

### Instalação
1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/cantina-senac.git](https://github.com/seu-usuario/cantina-senac.git)
    cd cantina-senac
    ```

2.  **Instale as dependências:**
    ```bash
    flutter pub get
    ```

3.  **Execute o projeto:**
    * **Para Web (Recomendado para imagens):**
        ```bash
        flutter run -d chrome --web-renderer html
        ```
    * **Para Mobile (Android):**
        Conecte seu celular via USB e rode:
        ```bash
        flutter run
        ```

---

## 👥 Equipe

* **Desenvolvedor:** Pedro Paulo IF
* **Contato:** pedropaulo4hire@gmail.com

---
*Projeto desenvolvido para fins acadêmicos e demonstração de viabilidade técnica no Senac.*
