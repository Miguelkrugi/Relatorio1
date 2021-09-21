# Relatório - Conceito da Aplicação

## Informações prévias

* Trabalho realizado por: Miguel Cruz e Wesley Augusto
* Relatório: Conceito
* Curso: Engenharia Informática
* Universidade: IADE

## Introdução

No âmbito multi-disciplinar do 1º Semestre do 2º ano de Licenciatura em Engenharia Informática do Instituto de Artes Visuais, Design e Marketing (IADE), foi proposto um projeto semestral, que consiste na Idealização, Implementação e Apresentação de uma aplicação mobile (app), desenvolvida para dispositivos Android. 
Este projeto abrange os conhecimentos de todas as Unidades Curriculares do Semestre (Base de Dados, Programação de Dispositivos Móveis, Programação Orientada a Objetos, Matemática Discreta, Competências Comunicacionais e Projeto de Desenvolvimento Móvel), assim como a utilização e aplicação dos conhecimentos adquiridos em cada uma das UC, ao longo do semestre. 
O projeto seguirá essencialmente a arquitetura MVC (Model, View, Controller), utilizada frequentemente para o desenvolvimento de aplicações. Com o uso das ferramentas Android Studio, Spring Boot e PostgreSQL, será possivel criar e implementar as funcionalidades desejadas da app. 

De seguida encontram-se os tópicos que irão ser abordados neste relatório, permitindo uma melhor compreensão do conceito por detrás do projeto a desenvolver:

## Indice:

* Preparação
* Ideias
* Aplicação Escolhida
* Problema
* Ideia e Conceito
* Objetivos
* Público-Alvo (Target)
* Aplicações-Base (Pesquisa de apps semelhantes)
* Informações Adicionais

## 1. Preparação

A primeira semana letiva do semestre (13 de Setembro - 16 de Setembro), foi dedicada á preparação do setup para permitir o desenvolvimento do projeto. Foram instalados os programas "Android Studio", "Visual Code / Spring Boot", "GitHub", "PostgreSQL", "Slack" e "Odoo", cada um deles possuindo a sua função, que, consequentemente, acabará por permitir o avanço do desenvolvimento da aplicação mobile.
Outras referências tais como "GeeksForGeeks", "DevMedia" ou "YouTube" foram utilizadas para consulta do funcionamento de cada um destes programas mencionados anteriormente, de forma a permitir uma maior familiarização para com os mesmos. 

Funções de cada ferramenta utilizada:

* Android Studio --> Interface da Aplicação Mobile
* Visual Code --> IDE para uso da framework "Spring Boot"
* Spring Boot --> Framework para a construção de API e implementação de controllers e models
* PostgreSQL --> Base de Dados
* GitHub --> Publicar futuros relatórios e atualizações quinzenais
* Slack --> Comunicação de grupo, bem como para com os restantes colegas de curso
* Odoo --> Criação de deadlines e tasks para melhor gestão do projeto (não exigida no briefing do projeto)

*Nota: Na fonte "YouTube", foram consultados os seguintes canais ("Edureka", "Amigoscode" e "freecodecamp")

## 2. Ideias

Durante a primeira semana, o grupo reuniu-se algumas vezes para realizar um Brainstorming, e discutir ideias que pudessem recorrer á localização do utilizador (requisito obrigatório para o desenvolvimento do projeto) e que permitissem solucionar problemas da sociedade.
Várias ideias foram descartadas, no entanto, após várias discussões, uma foi selecionada. Encontram-se, de seguida, algumas ideias que foram propostas mas no entanto, descartadas:

### HardGear:

A HardGear foi a primeira ideia a surgir durante um dos Brainstorming realizados. O principal objetivo seria facilitar compras de produtos Hardware e Acessórios, utilizando a localização do utilizador.
O utilizador pesquisaria o produto desejado (peças para PC, videojogos, consolas, etc), e a app devolveria uma ListView com as lojas num determinado raio de km. Permitiria posteriormente ao utilizador, comparar as distâncias e os preços e selecionar a loja mais acessivel para adquirir o produto desejado.
Para facilitar o percurso da localização atual até á loja, seria utilizado um sistema de GPS Tracker em tempo real.

Contudo, a ideia foi descartada após o surgimento de outras ideias mais abrangentes (Public Target), acessiveis e interessantes.

### PayWrite:

A PayWrite surgiu durante a primeira aula da UC de Projeto de Desenvolvimento Móvel, no entanto foi descartada no decorrer da aula. A PayWrite seria uma aplicação gratuita, que pagaria aos seus utilizadores para escreverem Crónicas, Criticas, Opiniões ou até livros, de forma a influenciar os jovens, e envolvê-los na Literatura.
No entanto, devido á falta de ideia de implementação de uma funcionalidade que utilizasse o principal requisito do projeto (localização), esta ideia foi descartada.

### BookFinder:

O BookFinder foi a terceira ideia a surgir, ainda baseada na Literatura. Esta aplicação permitiria, utilizando a localização, encomendar os livros desejados de forma mais rápida, utilizando estafetas, por exemplo.
Possuiria ainda lista de favoritos, de forma a guardar futuros pedidos que possam ocorrer, e ainda uma lista de livros comprados.
Considerando o valor dos livros somado com o valor da viagem do estafeta, foi concluido que o preço poderia não ser tão menor quando os preços dos livros vendidos em lojas habituais (Worten, FNAC, etc). 
Desta forma, a ideia foi descartada.

### GlitchFix:

A GlitchFix surgiu no fim da semana (13 de Setembro - 16 de Setembro), e foi uma forte concorrente da app selecionada, devido á alta utilidade, simplicidade e necessidade.
Esta aplicação seria um "market" de diversos serviços como manutenção, lavagem de automoveis, limpezas ao domicilio, entre outros, com apenas a um clique de distância, permitindo ao utilizador pesquisar pelo serviço desejado e requisitar o mesmo, sem demoras.
Bastava selecionar o serviço desejado, e um especialista (próximo ao local do utilizador - localização) dirigiria-se ao domicilio para realizar o serviço. No fim do mesmo, ocorreria o pagamento em PayPal ou em dinheiro.
Contudo, apesar da enorme utilidade, atratividade e simplicidade que esta app poderia ter, a dúvida sobre a qualidade e "veracidade" dos serviços descartou esta ideia, visto que a GlitchFix possuiria uma outra aplicação: a GlitchFix Business, que permitiria ao especialista registar o seu serviço e posteriormente disponibilizado na GlitchFix.

## 2. Aplicação Escolhida

Após debates de diversas ideias propostas, surgiu a <strong>BusyBrain.</strong> 
A BusyBrain seria então, uma aplicação simples de usar, com grande utilidade e que ajudaria a resolver um problema que é bastante recorrente nos dias de hoje: <strong>Foco e Produtividade.</strong>
A sua forte concorrência foi a ideia da app "GlitchFlix", uma vez que era dificil encontrar pontos que "desiquilibrassem a balança", de forma a facilitar a escolha.
No entanto, foi optada uma solução mais util e simples de desenvolver, utilizando diversos métodos de foco em tarefas comprovados e bastante utilizados, permitindo gerir e aproveitar o tempo durante as tarefas do dia-a-dia.
Após dias de discussão e de esboços de estruturas para ambas as aplicações, foi concluido que a melhor solução a adotar seria a BusyBrain.

## 3. Problema

Um dos problemas que grande parte da sociedade sofre, é a distração, que muitas vezes prejudica negativamente qualquer pessoa no seu dia-a-dia, quer seja no trabalho, em casa, na faculdade, e em qualquer outro lugar. Consequentemente, a distração desencadeia uma má gestão do tempo disponivel e o bom aproveitamento do mesmo. 
Aplicações como Instagram, Twitter ou WhatsApp são fortes influenciadores da distração durante a execução de tarefas do quotidiano. 
Foi a pensar nestas grandes necessidades que será desenvolvida a "BusyBrain", uma aplicação que promete melhorar o foco e a gestão de tempo nas mais variadas tarefas do dia-a-dia, seja em que ambiente for, facilitando alcançar algo extremamente benéfico no nosso dia-a-dia: a <strong>produtividade.</strong>

## 4. Ideia e Conceito

Como foi dito anteriormente, foi com base na falta de produtividade que afeta grande parte da sociedade atual (com o surgimento de redes sociais, por exemplo), que foi pensada a app "BusyBrain" (cérebro ocupado / cérebro focado).
A BusyBrain será uma aplicação simples e fácil de usar, com uma interface atrativa e simples.
Apesar de existirem várias apps com o mesmo propósito, a BusyBrain promete "expandir" as configurações presentes em qualquer app que possua o mesmo objetivo. Com funcionalidades que distingam a BusyBrain de todas as outras apps do mesmo género.
A app também permitirá adicionar tarefas a serem realizadas no tempo estipulado, assim como adicionar notas em cada uma delas.
Entre outras configurações, o utilizador poderá escolher de entre 4 técnicas comprovadas que permitem um maior foco e produtividade ao realizar tarefas, selecionar música ambiente, bloquear Wi-Fi quando um timer de foco iniciar e bloquear outras apps que o utilizador considere distrativas. 
Caso o utilizador tenha muita dificuldade em se concentrar nas suas tarefas, poderá optar pelo "Hardcore Timer", que proibe obrigatoriamente o utilizador de aceder a aplicações que considere distrativas até o timer estipulado (30 minutos ou 60 minutos) terminar.
A localização será utilizada para exibir cafés, bares e restaurantes próximos do utilizador, cujos estabelecimentos poderá frequentar nos intervalos entre as tarefas, entre outras funcionalidades (como procurar por livrarias e bibliotecas próximas do utilizador, caso queira comprar livros etc...). Após selecionar o local, um GPS será ativado (em tempo real), da rota que se inicia na localização atual do utilizador, e termina no local escolhido.

## 5. Objetivos

Apesar das vantagens que o BusyBrain poderá oferecer, o seu principal objetivo será sempre promover a produtividade do utilizador de uma forma simples e eficaz. Com a ajuda de diversas funcionalidades como o bloqueio de aplicações, será possivel atingir outros objetivos a que a aplicação se compromete a atingir, como melhorar a capacidade de foco do utilizador. 
Gerir o tempo e saber aproveitá-lo, é também um dos objetivos do BusyBrain. Desta forma, utilizando a localização do utilizador, esse objetivo será possivel de alcançar, exibindo sempre os locais mais próximos para o utilizador aproveitar da melhor forma possivel o seu tempo livre de tarefas.
Para os utilizadores que queiram adquirir conhecimento, o BusyBrain (utilizando a localização), conseguirá também indicar bibliotecas e livrarias próximas do utilizador. 
A acessibilidade da app também é essencial. Desta forma, não existirá limites para bloqueios de apps ou websites. Todas as funcionalidades serão gratuitas, de maneira a garantir uma experiência completa ao utilizador, destacando-se de muitas outras aplicações deste género, no mercado.

## 6. Público-Alvo

Uma das grandes qualidades do BusyBrain será, entre outras, a acessibilidade, não existindo assim, um público-alvo especifico. Todas as pessoas que tenham dificuldades de foco em tarefas do dia-a-dia, de gestão de tempo e até de bom proveito do mesmo, poderão utilizar o BusyBrain.
A app está desenhada especificamente para ajudar a resolver este tipo de problemas que é muitas vezes prejudicial seja em que ambiente for.












