## Projeto: Plataforma de Ensino Gamificada
Status: Em Desenvolvimento

Tecnologias Utilizadas:

Descrição
Este projeto foi desenvolvido com o objetivo de criar uma plataforma educacional para escolas, permitindo a atribuição digital de tarefas, testes e entrega de conteúdo. A solução foi pensada para modernizar a sala de aula, com foco em engajamento e feedback em tempo real para professores e alunos.

Principais Funcionalidades
Acesso Baseado em Papel (RBAC): Interfaces e funcionalidades distintas para Professores e Alunos, garantindo que cada um tenha acesso apenas às ferramentas relevantes.

Painel do Professor:

Gerenciamento de Atividades: Crie, visualize, edite e delete atividades.

Modos de Atividade Dinâmicos: Suporte para atividades "Clássicas" (com prazo final) e "Flash" (estilo Kahoot, com cronômetro por questão).

Criação de Questões: Adicione questões de múltipla escolha ou dissertativas, com suporte para upload de imagens.

Sistema de Frequência (Chamada): Registre e consulte o histórico de presença dos alunos por curso e data.

Painel de Desempenho: Visualize os resultados das atividades, com a pontuação individual de cada aluno que a completou.

Painel do Aluno:

Lista de Atividades: Visualize todas as atividades disponíveis para o seu curso.

Quiz Interativo: Responda a atividades nos modos Clássico ou Flash, com uma interface limpa e reativa.

Gamificação: O modo Flash inclui um cronômetro em tempo real para criar um ambiente de aprendizado mais dinâmico e competitivo.

Acompanhamento de Pontuação: A pontuação é calculada e salva automaticamente ao final de cada atividade.

Desafios Técnicos e Aprendizados
O principal desafio técnico do projeto foi o desenho da arquitetura de dados no Cloud Firestore para suportar consultas complexas de forma eficiente. Por exemplo, para exibir o painel de desempenho, foi necessário buscar dados de duas coleções diferentes (users e activities) e combiná-los no frontend, uma operação que exigiu um modelo de dados bem planejado, com o uso de um mapa activityScores no documento de cada usuário.

Outro ponto-chave foi a implementação da lógica de estado para o modo "Flash", utilizando Timers e o ciclo de vida de StatefulWidgets no Flutter para criar uma experiência de cronômetro em tempo real, confiável e sem vazamentos de memória. A automação de tarefas no backend, como a limpeza de dados de um usuário deletado através de uma Cloud Function, também foi um aprendizado importante sobre a manutenção da integridade dos dados.
