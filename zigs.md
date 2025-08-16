🚀 Projeto: Plataforma de Ensino Gamificada
Status: Em Desenvolvimento

Tecnologias Utilizadas: <img src="https://skillicons.dev/icons?i=flutter,firebase&theme=dark" />

Descrição
Este projeto foi desenvolvido com o objetivo de criar uma plataforma educacional para escolas, permitindo a aplicação de tarefas, provas e a disponibilização de conteúdo de forma digital. A solução foi projetada para modernizar a sala de aula, com foco em engajamento através de gamificação e fornecendo feedback em tempo real para professores e alunos.

Principais Funcionalidades
Acesso Baseado em Papel (RBAC): Interfaces e funcionalidades distintas para Professores e Alunos, garantindo que cada um tenha acesso apenas às ferramentas relevantes para seu papel.

Painel do Professor:

Dashboard Central: Acesso rápido a todas as ferramentas de gerenciamento.

Gerenciamento de Atividades: Crie, visualize, edite e delete atividades.

Modos de Atividade Dinâmicos: Suporte para atividades "Clássicas" (com prazo final) e "Flash" (estilo Kahoot, com cronômetro por questão).

Criação de Questões: Adicione questões de múltipla escolha ou dissertativas, com suporte para upload de imagens.

Sistema de Frequência (Chamada): Registre e consulte o histórico de presença dos alunos por curso e data.

Painel de Desempenho: Acompanhe o progresso dos alunos, visualize as atividades que eles completaram e suas pontuações.

Painel do Aluno:

Lista de Atividades: Visualize todas as atividades disponíveis para o seu curso, com ícones que diferenciam os modos.

Quiz Interativo: Responda a atividades nos modos Clássico ou Flash através de uma interface limpa e reativa.

Gamificação: O modo Flash inclui um cronômetro em tempo real para criar um ambiente de aprendizado mais dinâmico e competitivo.

Acompanhamento de Pontuação: A pontuação é calculada e salva automaticamente ao final de cada atividade.

Meu Papel e Principais Aprendizados
Este projeto foi desenvolvido individualmente, com responsabilidade total sobre o design da arquitetura, desenvolvimento front-end em Flutter e a implementação do backend no Firebase.

O maior desafio foi criar uma arquitetura de dados flexível no Cloud Firestore que suportasse as diferentes funcionalidades, como os múltiplos modos de atividade e o rastreamento de pontuação individual. A decisão de adicionar um mapa activityScores no documento de cada usuário, por exemplo, foi um aprendizado crucial que possibilitou a criação do painel de desempenho do professor de forma eficiente.

O principal aprendizado técnico foi a gestão de estado em tempo real no Flutter para a funcionalidade do quiz "Flash". A implementação de um Timer que interage com o ciclo de vida do widget (StatefulWidget) para controlar a contagem regressiva, o avanço automático entre as questões e evitar vazamentos de memória foi uma experiência desafiadora e de grande valor. A utilização de Cloud Functions para automatizar a limpeza de dados do usuário também reforçou a importância de manter a integridade do banco de dados.

📸 Evidências Visuais
