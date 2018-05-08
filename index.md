# O que é o CMMI

O CMMI (Capability Maturity Model Integration ou Modelo Integrado de Maturidade em Capacitação) trata-se de um modelo (atualmente na versão 1.3), com um enfoque voltado para a medição da capacidade de maturidade de processos de software.

Um processo representa, dentro da área de software, um conjunto de atividades cujo objetivo é atingir uma meta previamente estipulada. Já por capacidade e maturidade de um processo, deve-se ter a noção do grau de qualidade com o qual um processo atinge um resultado esperado.

Ao todo, são 5 níveis de maturidade que atestam, por sua vez, o grau de evolução que uma organização se encontra num determinado momento. O objetivo maior, considerando o CMMI e seus diferentes conceitos, está justamente na produção de software com maior qualidade e menos propenso a erros.

Porém, nessa apresentação, iremos tratar mais especificamente de somente um dos níveis de maturidade.

# Nível 2 de Maturidade - Gerenciado / Gerido

O nível 2 de maturidade do CMMI é definido ,principalmente, pelo gerenciamento dos requisitos de seus projetos, bem como o planejamento, a medição e o controle dos diferentes processos envolvendo o desenvolvimento de um software. Basicamente, ele é sobre planejar a execução e confrontar o executado contra o que foi planejado inicialmente.

Entre abril de 2002 e junho de 2006 foram conduzidas 1581 avaliações em 1337 organizações.

- 18,2%: nível 5 (Em otimização)
- 4,4%: nível 4 (Quantitativamente gerenciado / Gerido quantitativamente)
- 33,8%: nível 3 (Definido)
- **33,3%: nível 2 (Gerenciado / Gerido)**
- 1,9%: nível 1 (Inicial / Ad-hoc)
- 8,4%: sem qualificação (Não fornecido)

# Processo

## Requisitos

### Reserva de Requisitos

- Tela inicial
    - Design da tela
- Lista de tópicos disponíveis no aplicativo
- Estatísticas do jogo
    - Performance ao final de cada jogo

### Requisitos das iterações

- Iteração 1 (dias 1 a 15)
    - Criação do banco de questões
        - Foi desenvolvido um Crawler para encontrar essas respostas automaticamente de forma automática e rápida
    - Implementação utilizando _parser_ para carregamento dos arquivos e construção de objetos de transferência de dados
    

- Iteração 2 (dias 16 a 30)
    - Implementação inicial do aplicativo
        - Jogo em processo
            - Desenvolvimento das questões
            - Interação com o usuário

## Projeto

### Visão

A visão desse trabalho é, em suma, a criação de um "jogo sério" na área de engenharia de software, de forma que ele possa ser utilizado como uma forma alternativa de estudo com a finalidade de estimular o aprendizado dos estudantes sobre os conceitos da área, mais especificamente sobre a área de testes unitários de software.

### Próximas iterações

Nas próximas iterações vamos incrementar nosso banco de dados de perguntas com a ajuda do Crawler desenvolvido pelo grupo e vamos implementar a tela de final de jogo com estatísticas acerca daquela rodada (acertos, erros, etc).

### Gestão de configuração

- Criação do banco de questões
- Criação do modelo de jogo em progresso
- Implementar funcionalidades do jogo

## Organização e Contribuições do grupo

- Dono do Produto: Vitor Menezello
- Mestre Scrum: Luiz Otávio
- Desenvolvedores:
    - Desenvolvimento do aplicativo:
        - Breno Rodrigues
        - Gabriel Oliveira
        - Ivan Soares
        - Marina Moreira
        - Pedro Brum
        - Rafael Grandsire
        - Ronald Pereira
    - Desenvolvimento do crawler:
        - Ivan Soares
        - Pedro Dalla
    - Desenvolvimento da base de dados:
        - Pedro Dalla
    - Decisões de Implementação:
        - Rafael Grandsire
    - Desenvolvimento do site:
        - Ronald Pereira

## Decisões da iteração

- Banco de perguntas

O banco será armazenado em formato de arquivos JSON, contendo título, texto, opções e gabarito das perguntas. Foi escolhido JSON pelo fato de ser um arquivo leve, compacto, fácil de ser interpretado e fácil de ser gerado, pois já existem muitas bibliotecas de várias linguagens já implementadas com métodos para tratar JSON com maior facilidade.

- Crawler de questões

O Crawler é um script que extrai questões de um site na internet, as trata e gera uma saída com essas informações. Atualmente, está sendo utilizado o site [qconcursos](https://www.qconcursos.com) na seção de Engenharia de Software -> Testes de Software. Esse crawler gera uma saída contendo as informações necessárias para a montagem do banco de questões no formato JSON, que serão utilizados pelo aplicativo.

- Implementação do "jogo em progresso"

- Definição de como dispor perguntas e respostas na tela
- Definição de como modelar a interação com o usuário

- Decisões de processo

Será utilizado a estratégia de Pair Programming, de forma a aumentar a assertividade do código produzido, elevando também a sua qualidade. Serão feitos rodízios entre os desenvolvedores do grupo, de forma que seja possível, ao final do trabalho, que cada um do desenvolvimento tenha tido um contato com cada uma das áreas que participaram do desenvolvimento como um todo desse aplicativo. Além disso, será feita uma revisão dos artefatos produzidos ao final do trabalho.

## Desafios encontrados

- Banco de perguntas
    - Selecionar as questões mais relevantes para o jogo
    - Limite de requisições para o Crawler
        - Temporizações maiores para buscar o conteúdo

- Desenvolvimento para Android
    - Utilização da ferramenta Android Studio
        - Instalação da ferramenta e todos seus periféricos por todos os desenvolvedores do grupo
    - Implementação de funcionalidades do jogo

- Coordenação dos membros do grupo
    - Comunicação como um fator-chave para o desenvolvimento
        - Grupo no Whatsapp e conferências de vídeo no Hangouts
        - Utilização do GitHub para hospedagem do código, mas também como uma forma de comunicação dos desenvolvedores e acompanhamento das iterações pelo Mestre Scrum e Dono do Produto
    - Alocação de tarefas visando a habilidade individual
        - Tempo restrito para desenvolvimento nos fez optar por colocar mais responsabilidades de cada área em quem já teve algum contato com ela

## Produto

Todo o código do produto será posteriormente disponibilizado (atualmente ele está sendo hospedado no GitHub em um repositório privado para evitar problemas de autoria e/ou possíveis interferências externas) nesse link:

[Unit Test Quiz](https://https://github.com/ronaldpereira/unit-test-quiz)