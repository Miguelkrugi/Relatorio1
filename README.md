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

* Introdução
* Preparação (Setup)
* Ideias
* Problema
* Ideia e Conceito
* Objetivos
* Público-Alvo (Target)
* Pesquisa
* Guião de Utilização
* Informações Adicionais

## 1. Introdução

No âmbito multi-disciplinar do 1º Semestre do 2º ano de Licenciatura em Engenharia Informática do Instituto de Artes Visuais, Design e Marketing (IADE), foi proposto um projeto semestral, que consiste na Idealização, Implementação e Apresentação de uma aplicação mobile (app), desenvolvida para dispositivos Android.  

Este projeto abrange todas as Unidades Curriculares do Semestre (Base de Dados, Programação de Dispositivos Móveis, Programação Orientada a Objetos, Matemática Discreta, Competências Comunicacionais e Projeto de Desenvolvimento Móvel), assim como a utilização e aplicação dos conhecimentos adquiridos em cada uma das UC’s, ao longo do semestre. O projeto seguirá essencialmente a arquitetura MVC (Model, View, Controller), utilizada frequentemente para o desenvolvimento de aplicações. Com o uso de ferramentas como "Android Studio", "Spring Boot" e "PostgreSQL", será possivel criar e implementar as funcionalidades desejadas para a aplicação a ser desenvolvida. 

O projeto será complementado com relatórios quinzenais, de forma a demonstrar o progresso de desenvolvimento da aplicação ao longo do semestre.  

Este relatório foi criado para permitir uma melhor compreensão sobre a estrutura, conceito e possivel funcionamento da app a desenvolver durante o periodo letivo.  

## 2. Preparação (Setup)

A primeira semana letiva, (13 de Setembro - 16 de Setembro), foi dedicada á preparação do setup para permitir o desenvolvimento do projeto. Foram instalados os programas "Android Studio", "Visual Code / Spring Boot", "GitHub", "PostgreSQL", "Slack" e "Odoo", cada um deles possuindo a sua função, que, posteriormente, ajudarão a desenvolver a aplicação. Outras fontes de pesquisa tais como "GeeksForGeeks", "DevMedia" ou "YouTube" foram utilizadas para consulta do funcionamento de cada um destes programas mencionados anteriormente, de forma a permitir uma maior familiarização para com os mesmos. De seguida encontram-se listadas as funções de cada ferramenta utilizada para o desenvolvimento do projeto:

### Android Studio

O Android Studio é um ambiente de desenvolvimento integrado (IDE), baseado no IDE Intellij Idea, para desenvolver aplicações para dispositivos Android, utilizando maioritariamente as linguagens de programação "Java" e "Kotlin".
O Android Studio possui ainda editor simples de layout, que permite que o desenvolvedor arraste elementos de interface para a "Activity" (tela da aplicação), podendo também pré-visualizar alterações realizadas, etc.
Esta ferramenta será então utilizada para desenvolver toda a interface da aplicação.

### Visual Code

O Visual Studio Code é um editor de código criado pela Microsoft e disponivel para Windows, Linux e macOS. 
Sendo um dos editores mais reconhecidos e completos do mercado, o Visual Studio Code será usado juntamente com a framework "Spring Boot", de modo a desenvolver models e controllers (elementos importantes da arquitetura MVC, utilizada para desenvolver a app).

### Spring Boot

O Spring Boot é uma "extensão" da framework Spring, desenvolvida para a linguagem Java. Esta ferramenta será complementada com o editor de código "Visual Studio Code", de forma a facilitar o desenvolvimento da REST API (permitindo posteriormente conectar a app com a base de dados).

### PostgreSQL 

O PostgreSQL é um dos mais conhecidos, avançados e completos SGBD's do mercado. Possui diversas vantagens face a outros SGBD's, tais como a efetuação de consultas complexas em bases de dados, suporte á modelagem MR, diferentes linguagens de programação estruturadas, tais como PL/pgSQL, PL/Python, PL/Java, entre outras.
Será a ultima "camada" da arquitetura MVC, uma vez que será na base de dados onde todas as informações de utilizadores, etc., serão guardadas. 

### GitHub

O GitHub é uma plataforma de hospedagem de código e documentação, totalmente gratuito e o mais reconhecido no mercado. Permite que qualquer utilizador disponibilize os seus códigos e projetos de forma gratuita, criando repositórios para armazenar esses mesmos códigos/projetos.
No entanto, no contexto deste projeto, o GitHub será utilizado para armazenar toda a documentação a ser entregue nas respectivas entregas do projeto.

### Slack

O Slack é uma plataforma/app de envio de mensagens, criada para facilitar a comunicação entre pessoas (por exemplo num projeto, empresa, etc.).
Será utilizada para manter uma comunicação mais rápida com os docentes envolvidos no projeto, etc.

### Odoo

O Odoo permite a criação de deadlines e tasks para uma melhor organização e gestão do projeto (não exigida no briefing).

*Nota: Na fonte "YouTube", foram consultados os seguintes canais ("Edureka", "Amigoscode" e "freecodecamp"). Mais informações sobre as ferramentas utilizadas estão disponiveis na secção “Informações Adicionais”. 

## 3. Ideias

Durante a primeira semana, o grupo reuniu-se algumas vezes para realizar um Brainstorming, de modo a propor e a discutir ideias que cumprissem o requisito obrigatório para o desenvolvimento do projeto: a Localização.  

Uma das preocupações do grupo foi encontrar soluções para os problemas e necessidades da população. 

Várias ideias surgiram durante os Brainstorming, todas com finalidades e propósitos distintos, baseando-se em diversas necessidades da população. 

Para compreender melhor o progresso de Idealização da aplicação, estão de seguida listadas todas as ideias que surgiram, até ao momento da decisão final da ideia a seguir, para a construção da aplicação: 

### HardGear:

A HardGear foi a primeira ideia a surgir durante um dos Brainstorming realizados. O principal objetivo seria facilitar a compra de produtos Hardware e Acessórios, através da utilização da localização do utilizador. 
O utilizador pesquisaria o produto desejado (peças para PC, videojogos, consolas, etc), e a app devolveria uma ListView com as lojas num determinado raio de km. Permitiria posteriormente ao utilizador, comparar as distâncias e os preços e selecionar a loja mais acessivel para adquirir o produto desejado. Para facilitar o percurso da localização atual até á loja, seria utilizado um sistema de GPS Tracker em tempo real. 

Contudo, a ideia foi descartada após o surgimento de outras ideias mais abrangentes (Public Target), acessiveis e interessantes. 

### PayWrite:

A PayWrite surgiu durante a primeira aula da UC de Projeto de Desenvolvimento Móvel, no entanto foi descartada no decorrer da mesma aula. A PayWrite seria uma aplicação gratuita, que pagaria aos seus utilizadores para escreverem Crónicas, Criticas, Opiniões ou até livros, de forma a incentivar os jovens para a prática da escrita, envolvendo-os na área da Literatura. 
No entanto, a PayWrite não utiliza o requisito principal do projeto para nenhuma das suas funcionalidades, sendo, deste modo, descartada. 

### BookFinder:

O BookFinder foi a terceira ideia a surgir, ainda baseada na área da Literatura. Esta aplicação permitiria, utilizando a localização, encomendar os livros desejados de forma mais rápida, utilizando estafetas, por exemplo. Possuiria também uma lista de livros favoritos e uma lista de livros comprados. 
Considerando o valor dos livros somado com o valor da viagem do estafeta, foi concluido que o preço poderia não ser tão apelativo quanto comparado com os preços dos mesmos livros vendidos em lojas fisicas (Worten, FNAC, etc), razão pela qual esta ideia foi descartada. 

### GlitchFix:

A GlitchFix surgiu no fim da primeira semana letiva(13 de Setembro - 16 de Setembro), e foi uma forte concorrente da app selecionada, devido á sua forte utilidade e simplicidade de manuseamento. Esta aplicação seria um "market" de diversos serviços como manutenção, lavagem de automóveis, limpezas ao domicilio, entre outros. Com apenas a um clique de distância, a app permitiria ao utilizador pesquisar pelo serviço desejado e requisitar o mesmo, sem demoras. 
Bastaria selecionar o serviço desejado, e um especialista (próximo ao local do utilizador - localização) dirigiria-se ao domicilio para realizar o serviço. No fim do mesmo, ocorreria o pagamento em PayPal ou em dinheiro. 
Contudo, apesar da enorme utilidade, atratividade e simplicidade que esta app poderia ter, a dúvida sobre a qualidade e "veracidade" dos serviços descartou esta ideia, uma vez que a GlitchFix possuiria uma outra aplicação: a GlitchFix Business, que permitiria ao especialista registar o seu serviço e posteriormente disponibilizado na GlitchFix. 

## 4. Problema

Como é sabido, a tecnologia tem evoluido exponencialmente nos ultimos anos. Diariamente são criados novos dispositivos, apps e outros vários tipos de tecnologias e serviços, de forma a atender ás necessidades da população. Atualmente, já existem aplicações para todo o tipo de finalidades, desde serviços ao domicilio, até ao entretenimento, passando pela saúde e informação. 

Todos os dias, surgem novos problemas e tentam-se criar soluções eficazes e simples para reduzir o seu impacto negativo na sociedade, utilizando a tecnologia. No entanto, tudo em excesso é prejudicial, e o uso da tecnologia não é excepção. Com o surgimento de jogos e redes sociais, por exemplo, um grande problema surgiu, fruto do excesso da utilização destas aplicações, que, através dos seus algoritmos (recomendação constante de conteúdos baseados nos gostos do utilizador), contribuiu para o vicio em dispositivos eletrónicos, principalmente por parte dos jovens, que cada vez mais se tornam dependentes desses meios. Dependências essas que posteriormente prejudicam a vida tanto profissional quanto pessoal do individuo, impedindo-o muitas vezes, de concretizar as suas tarefas e obrigações diariamente.  

Problema derivado desses vicios é a grande facilidade de distração, dificultando o foco e a concentração em tarefas importantes do dia-a-dia.  Posteriormente, essa dificuldade desencadeia uma má gestão do tempo disponivel.   

 Foi a pensar neste grande problema, que surgiu a "BusyBrain", uma aplicação que promete melhorar o foco e a gestão de tempo nas mais variadas tarefas do dia-a-dia, seja em que ambiente for, facilitando alcançar algo extremamente benéfico no nosso dia-a-dia: a produtividade. 
 
## 5. Ideia e Conceito

Devido não só á falta de produtividade que afeta grande parte da sociedade, mas como também devido á má gestão de tempo, fortemente influenciada por esse problema, foi idealizada uma app para garantir o foco e a concentração nas tarefas diárias, utilizando diversos métodos comprovados para tal: a “BusyBrain”.

A "BusyBrain" (cérebro ocupado / cérebro focado), será uma aplicação simples e fácil de usar, com uma interface atrativa e moderna. Apesar de existirem várias apps com o mesmo propósito, a “BusyBrain” promete "expandir" as configurações presentes em qualquer app que possua o mesmo objetivo, distinguindo-a no mercado.  

Entre diversas configurações, o utilizador poderá escolher de entre 4 técnicas comprovadas que contribuem para um maior foco e produtividade ao realizar tarefas do quotidiano  (Pomodoro Timer, DeskTime, Ritmos Ultradian e FlowTime), selecionar música ambiente, bloquear Wi-Fi quando um "timer de foco" iniciar, bloquear outras apps que o utilizador considere distrativas e silenciar totalmente o telemóvel durante o periodo(s) de execução das tarefas. Caso o utilizador tenha muita dificuldade em se concentrar nas suas tarefas, poderá optar pelo "Hardcore Timer", que proibe obrigatoriamente o utilizador de aceder a aplicações que considere distrativas até o timer estipulado (30 minutos ou 60 minutos) terminar. 

Além disso, a app também permitirá adicionar tarefas a serem realizadas no tempo estipulado, assim como adicionar notas em cada uma delas.  

A localização (requisito obrigatório para a realização do projeto) será utilizada para exibir cafés, bares e restaurantes próximos do utilizador, cujos estabelecimentos poderá frequentar nos intervalos entre as tarefas. Caso o utilizador tenha interesse, poderá também  procurar por livrarias e bibliotecas próximas de si, caso queira consultar ou comprar livros.  

Após selecionar o local, um GPS/Tracker será ativado (em tempo real), exibindo a rota, que se inicia na localização atual do utilizador, terminando no local previamente selecionado. 

Para tornar a app mais acessivel, esta será totalmente gratuita, sem planos pagos (algo bastante comum em aplicações do mesmo género).  

## 2. Aplicação Escolhida

Após debates de diversas ideias propostas, surgiu a <strong>BusyBrain.</strong> 
A BusyBrain seria então, uma aplicação simples de usar, com grande utilidade e que ajudaria a resolver um problema que é bastante recorrente nos dias de hoje: <strong>Foco e Produtividade.</strong>
A sua forte concorrente foi a app "GlitchFix", porque tinha caracteristicas semelhantes á BusyBrain.
No entanto, a decisão recaiu sobre a BusyBrain, por ter uma maior utilidade e o seu desenvolvimento ser mais simples. Utiliza diversos métodos de concentração nas diversas tarefas do dia a dia, contribui para a produtividade do utilizador, assim como uma melhor gestão do tempo.
Após dias de discussão e de esboços de estruturas para ambas as aplicações, e de acordo com as caracteristicas descritas acima concluimos que a melhor solução seria a BusyBrain.

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

 Todas as pessoas que tenham dificuldades de foco em tarefas do dia-a-dia, de gestão de tempo e até de bom proveito do mesmo, poderão utilizar o BusyBrain. Desta forma, a aplicação não possui um público-alvo especifico, no entanto, esta está desenhada especificamente para ajudar a melhorar a produtividade durante a execução de tarefas do dia-a-dia, melhorar o foco durante essas execuções, permitir uma melhor gestão do tempo e aproveitamento do mesmo através de diversas funcionalidades que destacam a BusyBrain no mercado de apps com o mesmo propósito.
 
## 7. Aplicações-Base (Pesquisa de apps semelhantes) 
















