# Relatório - Conceito da Aplicação

## Informações prévias

* Trabalho realizado por: Miguel Cruz e Wesley Augusto
* Relatório: Conceito
* Curso: Engenharia Informática
* Universidade: IADE

## Indice

* Introdução
* Preparação (Setup)
* Ideias
* Problema
* Ideia e Conceito
* Objetivos
* Público-Alvo (Target e Persona)
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

### Android Studio:

O Android Studio é um ambiente de desenvolvimento integrado (IDE), baseado no IDE Intellij Idea, para desenvolver aplicações para dispositivos Android, utilizando maioritariamente as linguagens de programação "Java" e "Kotlin".
O Android Studio possui ainda editor simples de layout, que permite que o desenvolvedor arraste elementos de interface para a "Activity" (tela da aplicação), podendo também pré-visualizar alterações realizadas, etc.
Esta ferramenta será então utilizada para desenvolver toda a interface da aplicação.

### Visual Code:

O Visual Studio Code é um editor de código criado pela Microsoft e disponivel para Windows, Linux e macOS. 
Sendo um dos editores mais reconhecidos e completos do mercado, o Visual Studio Code será usado juntamente com a framework "Spring Boot", de modo a desenvolver models e controllers (elementos importantes da arquitetura MVC, utilizada para desenvolver a app).

### Spring Boot:

O Spring Boot é uma "extensão" da framework Spring, desenvolvida para a linguagem Java. Esta ferramenta será complementada com o editor de código "Visual Studio Code", de forma a facilitar o desenvolvimento da REST API (permitindo posteriormente conectar a app com a base de dados).

### PostgreSQL:

O PostgreSQL é um dos mais conhecidos, avançados e completos SGBD's do mercado. Possui diversas vantagens face a outros SGBD's, tais como a efetuação de consultas complexas em bases de dados, suporte á modelagem MR, diferentes linguagens de programação estruturadas, tais como PL/pgSQL, PL/Python, PL/Java, entre outras.
Será a ultima "camada" da arquitetura MVC, uma vez que será na base de dados onde todas as informações de utilizadores, etc., serão guardadas. 

### GitHub:

O GitHub é uma plataforma de hospedagem de código e documentação, totalmente gratuito e o mais reconhecido no mercado. Permite que qualquer utilizador disponibilize os seus códigos e projetos de forma gratuita, criando repositórios para armazenar esses mesmos códigos/projetos.
No entanto, no contexto deste projeto, o GitHub será utilizado para armazenar toda a documentação a ser entregue nas respectivas entregas do projeto.

### Slack:

O Slack é uma plataforma/app de envio de mensagens, criada para facilitar a comunicação entre pessoas (por exemplo num projeto, empresa, etc.).
Será utilizada para manter uma comunicação mais rápida com os docentes envolvidos no projeto, etc.

### Odoo:

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

## 6. Objetivos

A app estará desenhada especificamente para auxiliar as pessoas que possuem maior dificuldade em se concentrarem nas suas tarefas do dia-a-dia. No entanto, esta poderá ser utilizada por qualquer pessoa, de forma gratuita. 
Para estruturar de forma mais clara o conceito e os propósitos da aplicação, foram definidos vários objetivos a alcançar com a criação da "BusyBrain":

 * Desenvolver e tornar a aplicação totalmente gratuita e leve para todos os dispositivos
 * Interfaces simples e fáceis de manusear
 * Combater o vicio nos dispositivos eletrónicos e a falta de produtividade (contribuindo para o foco e concentração nas tarefas a serem realizadas)
 * Eliminar distrações, priorizando a execução de tarefas do dia-a-dia.
 * Facilitar a gestão do tempo (dentro e fora do tempo de trabalho)
 
### Aplicação Gratuita:

Após breves pesquisas de diversas apps com o mesmo objetivo da "BusyBrain", uma das grandes desvantagens existentes na concorrência era a limitação do uso de algumas funcionalidades, podendo ser somente utilizadas, caso o utilizador comprasse planos "Premium", o que impediria uma utilização completa da app. 
Face a este problema, foi decidido que a "BusyBrain" não possuirá planos pagos, de modo a garantir uma experiência completa ao utilizador. Além de totalmente gratuita, a "BusyBrain" deverá ser uma app "leve" para qualquer dispositivo (garantindo uma melhor acessibilidade), de forma a ajudar a economizar internet, bateria e memória do dispositivo. 

### Interfaces Simples:

A grande acessibilidade da "BusyBrain" complementa-se com a sua interface simples, atrativa e fácil de usar. 
Este requisito é essencial para a aquisição e retenção de utilizadores, assim como incentivá-los a continuar a utilizar a app, reduzindo a probabilidade de "abandono" da app, e incrementando a probabilidade de uso da mesma.
A criação de Layout's simples, evita também problemas futuros, tais como a correção de erros de "navegação" na aplicação, dificuldade quanto a ajustes em diversos dispositivos, entre outros. Todos estes percalços envolvem custos elevados. Desta forma, a criação de uma interface intuitiva, atrativa e simples, beneficia não só os utilizadores como também a aplicação (manutenção, atualizações, correções de bugs, etc.), causando menos problemas e "preocupações" aos desenvolvedores quanto aos custos.
É frequente ocorrerem várias duvidas relativamente ao uso da aplicação por parte dos clientes, no entanto, se a interface for intuitiva, o contacto do cliente com o serviço de apoio será menos frequente. 
Deste modo, os custos do apoio ao cliente podem ser bastante reduzidos. Uma interface amigável e de fácil utilização, minimiza as ocorrências de erros ou dúvidas por parte dos utilizadores, garantindo também uma maior satisfação durante a experiência de utilização da app.

### Combate ao vicio, eliminação de distrações e aumento da produtividade:

A rápida evolução tecnológica das últimas décadas tem vindo a transformar drasticamente a dinâmica das nossas vidas, as nossas rotinas e amplamente a vida social.
Diariamente surgem novas aplicações e serviços para as mais diversas finalidades, de forma a facilitar o nosso dia-a-dia. No entanto, todos estes fatores trariam mais benificios caso não existisse o "excesso" de utilização destes serviços/aplicações (redes sociais, jogos, etc.), que, infelizmente, causa grandes dependências dos pequenos ecrãs.
Sendo estes dispositivos a nossa "vida" em formato digital, não só já não podemos passar tempo sem eles, como os mesmos nos "ocupam" cada vez mais horas diariamente sem nos apercebermos disso. 
Tudo em excesso é prejudicial, e o uso abusivo destes dispositivos não é excepção. Em qualquer situação em que estamos parados (esperar pelo autocarro, pela comida no restaurante ou esperar por um amigo, etc.), o primeiro instinto é pegar no telemóvel para passar mais depressa o tempo.
Estas dependências podem causar graves problemas de saúde, como por exemplo a Depressão, Ansiedade e Insónias.

Desta forma, a "BusyBrain" procura combater este vicio, ajudando o utilizador a evitar estas dependências do aparelho. Através de métodos de concentração e foco comprovados (entre outras configurações e funcionalidades), a "BusyBrain" possibilita ao utilizador largar o aparelho e focar-se nas suas tarefas, aumentando a sua produtividade, aumentando a capacidade de foco e concentração e eliminando possiveis distrações derivadas dos aparelhos eletrónicos.

Através do bloqueio de apps ou bloqueio de websites que o utilizador considere distrativo(as), será possivel evitar possiveis distrações causadas pelos dispositivos. Também será possivel silenciar totalmente o telemóvel ou desativar a ligação Wi-Fi do dispositivo (evitar a recepção notificações, evitar acesso á web, etc.), de forma a alcançar o mesmo objetivo (eliminação de distrações durante o tempo de execução de tarefas).

## Gestão de Tempo

Em qualquer ambiente, seja no trabalho ou na vida pessoal, o tempo passa bastante rápido. No trabalho, por exemplo, é essencial gerir bem o tempo, de forma a cumprir todas as tarefas do dia. No entanto, este feito pode ser dificil de conseguir, uma vez que, com a dependência dos aparelhos eletrónicos e com uma grande capacidade de distração, a organização de tarefas e o cumprimento das mesmas torna-se bastante complicada. 
Gerir o tempo envolve a estruturação de horários e do tempo de execução de cada tarefa a ser realizada durante o dia. Infelizmente, apesar do conceito ser simples, uma boa gestão de tempo é muitas vezes dificil de alcançar.

Por esta razão, a "BusyBrain" está também desenhada especificamente para permitir ao utilizador gerir melhor o seu tempo, tornando-o mais produtivo e menos "stressado" com o tempo disponivel para realizar as suas tarefas.
Através da utilização das 4 principais técnicas de foco e produtividade disponiveis na app, este feito de uma boa gestão do tempo disponivel para executar tarefas tornar-se-á possivel. 

De forma a concretizar este objetivo, a "BusyBrain" ainda acederá á localização do utilizador, exibindo-lhe cafés, restaurantes e bares, que o user poderá frequentar "fora" do tempo de realização das suas tarefas.
A localização também será utilizada para exibir livrarias e  bibliotecas próximas do utilizador, caso este queira comprar ou consultar livros, por exemplo.

Também será possivel criar, editar e ajustar horários, dependendo das necessidades do user.

## 7. Público-Alvo

O público-alvo da "BusyBrain" será toda a população que possua problemas de vicio no telemóvel, distração, gestão de tempo e/ou concenctração durante a realização das suas tarefas diárias e que queiram eliminar distrações, aumentar a produtividade, gerir melhor o seu tempo, etc.
No entanto, apesar da "BusyBrain" ser especificamente desenhada para esse público, qualquer pessoa poderá utilizar a "BusyBrain" e disfrutar de todas as funcionalidades e vantagens que a app oferece.

## 8. Pesquisa

Para entender que configurações poderiam destacar a "BusyBrain" no mercado, foram analisadas 3 aplicações ("Brain Focus", "Focus To-Do" e "Serene") que possuem o mesmo objetivo que a "BusyBrain": Foco e Produtividade. As apps foram instaladas e testadas, sendo ainda analisadas críticas publicadas na página da app na Play Store (excepto a app "Serene", que somente funciona para sistemas macOS). Logicamente, foram analisadas diversas configurações de todas as apps selecionadas.

### Brain Focus:

A "Brain Focus Productivity Timer" é uma app desenvolvida pela empresa "Brain Focus", que serve para gerir melhor o tempo, utilizando essencialmente a técnica Pomodoro.
Após a instalação, foram listadas algumas configurações que podiam tornar a "BusyBrain" mais interessante e completa:

* Desativar Wi-Fi quando iniciada uma sessão de trabalho.
* Diversos "themes" (Vermelho, Verde, Azul, Dark, etc.).
* Notificação antes do fim de uma sessão de trabalho.
* Timer definido pelo user.
* Remoção de anuncios (somente na versão Pro).

### Focus To-Do:

A "Focus To-Do" é uma app que foi desenvolvida pela empresa "Pomodoro Timer & To Do List - SuperElement SoftProdutividade". Esta app combina a técnica Pomodoro com sistema de criação e gestão de tarefas a serem realizadas.
Após a análise desta app, foram também listadas algumas das funcionalidades que esta aplicação oferece:

* Criar tarefas e planear o dia.
* Adicionar notas ás tarefas.
* Bloqueio de apps
* Som ambiente para a sessão de trabalho.
* Tela sempre ativada.

### Serene:

A "Serene" é uma aplicação desenvolvida pela empresa "Serene". É uma das apps mais completas do género e possui uma grande variedade de opções e funcionalidades. Por ser somente desenvolvida para macOS, esta não pôde ser instalada, no entanto foram verifacadas algumas configurações interessantes, a partir do website da própria app, que pudessem servir de base para outras funcionalidades na "BusyBrain":

* Bloqueio de websites
* Silenciador de telemóvel
* Planear as tarefas do dia

//Nota: A "Serene" é uma app paga (4$/mês | 14 dias de trial/demo).

### BusyBrain:

Baseada nas configurações disponiveis nas 3 apps selecionadas (Brain Focus, Focus To-Do, Serene), foi estruturada uma lista de várias funcionalidades que irão compor a app da "BusyBrain":

* Timers com diversos métodos de foco, concentração e produtividade durante a execução de tarefas
* Adicionar, editar e eliminar tarefas
* Adicionar descrições e notas ás tarefas
* Bloquear apps (escolhidas pelo utilizador)
* Bloquear websites (escolhidos pelo utilizador)
* Desativar o Wi-Fi quando uma sessão de trabalho é iniciada
* Som ambiente para as sessões de trabalho
* Small breaks e Long breaks (variam de acordo com o tipo de timer)
* Exibir lista de cafés, bares e restaurantes para os breaks (com GPS em tempo real)
* Exibir lista de livrarias e bibliotecas (com GPS em tempo real)
* Modo "Hardcore Timer"
* Silenciador de telemóvel
* Adicionar, editar e eliminar horários

//Nota: Ao longo do desenvolvimento do projeto algumas funcionalidades poderão ser adicionadas, removidas ou não implementadas.

## 9. Informações adicionais

* Tipos de Timers:
                   
                   
     * Pomodoro Timer (Foco: 25 minutos | Small Break: 5 minutos | Long Break: 30 minutos --> Aconselhado realizar 4 sessões antes do Long Break)
     
     * DeskTime Extra (Foco: 57 minutos | Break: 17 minutos | Long Break: 45 minutos --> Aconselhado realizar 2 sessões antes do Long Break)
     
     * Ultradian Rhythm (Foco: 90 minutos | Break: 30 minutos | Long Break: 60 minutos --> Aconselhado realizar 2 sessões antes do Long Break)
     
     * FlowTime (Foco: Até o utilizador se sentir distraido/cansado | Break: 5 minutos | Long Break: 15 minutos)
     
     * Hardcore Timer (Foco: 45 minutos | Break: 10 minutos | Long Break: 30 minutos --> Aconselhado realizar 4 sessões antes do Long Break)
                   
* Uso da Localização:

     * Procurar por cafés, restaurantes e bares perto do local do utilizador (raio de 10 km | GPS Tracker em tempo real)
     
     * Procurar por livrarias e bibliotecas (raio de 50 km | GPS Tracker em tempo real)
     
* Infos sobre os locais exibidos:

     * Nome do local 
     * Endereço
     * Distância

//Nota: O Hardcore Timer bloqueia totalmente o telemóvel (Wi-Fi, telemovel silenciado, apps bloqueadas e websites bloqueados durante o timer). Até o timer não acabar, não será possivel reativar o uso do telemóvel (bloqueio total).

# 10. Guiões de Teste

Para compreender o progresso do user na app, foram desenvolvidos 3 guiões de teste. O primeiro guião inclui o uso dos timers ("core" da aplicação), e os outros 2 guiões de teste incluem o uso de funcionalidades secundárias:

## Guião de Teste - Core 

### Splash-Screen:

A primeira tela a surgir quando a app é iniciada, será uma tela do tipo "Splash-Screen". Uma tela "Splash-Screen", é uma "Activity" utilizada em quase todas as apps. Geralmente, este tipo de tela apresenta o logótipo da app ou uma barra de "loading". 
Neste contexto, quando a "BusyBrain" for iniciada, uma activity do tipo "Splash-Screen" surgirá na tela do dispositivo. Esta tela ficará visivel por 4 segundos, redirecionando o utilizador para a tela de login da app, após esse tempo de espera.

![Splash Screen](https://static.wixstatic.com/media/302737_b85bc4b786b3456a8a92fcbf6e48d220~mv2.png/v1/fill/w_408,h_750,al_c,lg_1,q_85/302737_b85bc4b786b3456a8a92fcbf6e48d220~mv2.webp)

*Nota: Imagem utilizada somente para fins ilustrativos.

### Login Activity

Após o tempo de espera na tela de Splash-Screen, o utilizador é redirecionado para a tela de Login. Esta activity terá várias opções de Login (Login pela app, pela conta Google ou pelo Facebook). Além destas opções, a tela de Login exibirá também a possibilidade de "Registo", caso o user ainda não possua uma conta na app. O botão de registo redirecionará o utilizador para a tela de registo ("Register Activity"). Para o Login (da app), o utilizador terá de introduzir o seu Username e a sua password (métodos de login com a Google ou Facebook podem variar). Após a inserção dos dados, o user será redirecionado para a tela principal da app (Main Activity).
![Login Page](https://static.wixstatic.com/media/302737_04ae3db966a64b748f96e91babe6cd3b~mv2.png/v1/fill/w_416,h_750,al_c,lg_1,q_85/302737_04ae3db966a64b748f96e91babe6cd3b~mv2.webp)
                   
### Register Activity

Caso o utilizador não possua uma conta na "BusyBrain", este deve-se registar na tela de Registo, que pode ser acedida pela tela de Login. 
Para o registo do user na app, este terá que introduzir o seu username, email, password, sexo (Masculino ou Feminino) e numero de telemóvel. O username será posteriormente exibido na barra lateral da "activity" principal, e o Email e Numero de telemóvel serão posteriormente utilizados para o utilizador receber notificações de atualizações, caso o mesmo deseje recebê-las.

![Register Page](https://static.wixstatic.com/media/302737_038b203d0fd148fa84eca913ee70e754~mv2.png/v1/fill/w_411,h_733,al_c,lg_1,q_85/302737_038b203d0fd148fa84eca913ee70e754~mv2.webp)

### Main Activity

Após o Registo (ou Login) do utilizador, este será redirecionado para a "Main Page" da app. A tela principal exibirá um timer por definição (Pomodoro Timer), assim como os botões de "Play", "Pause" e "Restart", para iniciar, pausar e reiniciar o Timer. Na parte inferior da tela principal, estão exibidos os botões "Small Break" e "Long Break". Ao clicar num desses botões, o utilizador será novamente redirecionado para as activities de "Small Break" ou "Long Break", dependendo do botão ativado. 
Na tela principal ainda se encontra um botão "hamburguer", que exibirá uma barra lateral com diversas configurações que podem ser personalizadas durante a sessão de trabalho.

![Main Activity](https://static.wixstatic.com/media/302737_51db1c79239e4a188a2473e6fe473022~mv2.png/v1/fill/w_410,h_729,al_c,lg_1,q_85/302737_51db1c79239e4a188a2473e6fe473022~mv2.webp)

![DeskTime Timer](https://static.wixstatic.com/media/302737_c632e847634e485cb7c5beb880df347c~mv2.png/v1/fill/w_408,h_731,al_c,lg_1,q_85/302737_c632e847634e485cb7c5beb880df347c~mv2.webp)

![Ultradian Rythm](https://static.wixstatic.com/media/302737_681c86f24b994661a1dec72bf5d5f0dd~mv2.png/v1/fill/w_405,h_725,al_c,lg_1,q_85/302737_681c86f24b994661a1dec72bf5d5f0dd~mv2.webp)

![FlowTime Timer](https://static.wixstatic.com/media/302737_765b9727138d4e71ad0668c8b26e1e2b~mv2.png/v1/fill/w_409,h_726,al_c,lg_1,q_85/302737_765b9727138d4e71ad0668c8b26e1e2b~mv2.webp)

![Hardcore Timer](https://static.wixstatic.com/media/302737_e5adf5c95b21406ba121218cb9ec1173~mv2.png/v1/fill/w_406,h_727,al_c,lg_1,q_85/302737_e5adf5c95b21406ba121218cb9ec1173~mv2.webp)

*Nota: Todos os timers terão o mesmo "layout", no entanto com gradientes distintos.

### Small Break Activity

A tela de "Small Break" pode ser acedida clicando no botão "Small Break", que se encontra na zona inferior de cada uma das telas de "timer" (Pomodoro Timer, DeskTime Timer, Ultradian Timer e FlowTime Timer). As telas de "Small Breaks" possuem os mesmos layouts das telas de "timer", no entanto, com algumas diferenças:

* O botão com o icone de uma "roda dentada", permite aceder ás definições.
* O menu "hamburguer", permite aceder ás funcionalidades que utilizam a localização do user.
* A opção "Back to Timer", permite regressar á tela do timer que está a ser utilizado.
* A opção "Long Break", permite aceder á tela do "intervalo maior".
* O botão de "Play" permite iniciar o "break timer". 

![Pomodoro Small Break](https://static.wixstatic.com/media/302737_912154eb7fc04b059e02d9cb8dfddb95~mv2.png/v1/fill/w_405,h_727,al_c,lg_1,q_85/302737_912154eb7fc04b059e02d9cb8dfddb95~mv2.webp)

![DeskTime Small Break](https://static.wixstatic.com/media/302737_32aa7318dd4a4464a9d522e554743632~mv2.png/v1/fill/w_401,h_728,al_c,lg_1,q_85/302737_32aa7318dd4a4464a9d522e554743632~mv2.webp)

![Ultradian Small Break](https://static.wixstatic.com/media/302737_db8c18721d4649f8b8ea508b0e49fd32~mv2.png/v1/fill/w_407,h_726,al_c,lg_1,q_85/302737_db8c18721d4649f8b8ea508b0e49fd32~mv2.webp)

![FlowTime Small Break](https://static.wixstatic.com/media/302737_86a43603a376480b891c85bc8e803062~mv2.png/v1/fill/w_407,h_727,al_c,lg_1,q_85/302737_86a43603a376480b891c85bc8e803062~mv2.webp)

![Hardcore Small Break](https://static.wixstatic.com/media/302737_d20e61ec1ab04bbea72f2df12c428c51~mv2.png/v1/fill/w_404,h_728,al_c,lg_1,q_85/302737_d20e61ec1ab04bbea72f2df12c428c51~mv2.webp)

### Long Break 

A tela de Long Break pode ser acedida selecionando a opção "Long Break" na tela do timer. 
Nesta tela estarão disponiveis as funcionalidades de procura de cafés, bares, restaurantes, livrarias e bibliotecas, dependendo da localização atual do user.
A opção representada com o icone de uma chávena de café, exibe os cafés, bares e restaurantes perto do utilizador (utilizando a localização). 
A opção representada com o icone de um livro, exibe livrarias e bibliotecas perto do utilizador (utilizando a localização).
Na zona inferior da tela, encontra-se um botão que, ao ser ativado, redireciona novamente o utilizador á tela do timer.


![Pomodoro Long Break](https://static.wixstatic.com/media/302737_6f1546ab940a4b26ab13c7b63ff4017e~mv2.png/v1/fill/w_404,h_726,al_c,lg_1,q_85/302737_6f1546ab940a4b26ab13c7b63ff4017e~mv2.webp)

![DeskTime Long Break](https://static.wixstatic.com/media/302737_3cbe99409a454f2db4b2fefae1579b55~mv2.png/v1/fill/w_406,h_727,al_c,lg_1,q_85/302737_3cbe99409a454f2db4b2fefae1579b55~mv2.webp)

![Ultradian Long Break](https://static.wixstatic.com/media/302737_6ac565815e0442d6a3f8d7efcfa06058~mv2.png/v1/fill/w_404,h_728,al_c,lg_1,q_85/302737_6ac565815e0442d6a3f8d7efcfa06058~mv2.webp)

![FlowTime Long Break](https://static.wixstatic.com/media/302737_b5316df272664f65bad6f56c66168995~mv2.png/v1/fill/w_405,h_727,al_c,lg_1,q_85/302737_b5316df272664f65bad6f56c66168995~mv2.webp)

![Hardcore Long Break](https://static.wixstatic.com/media/302737_f6cf13f1d6334d9297f3b9fbc6e0278c~mv2.png/v1/fill/w_400,h_722,al_c,lg_1,q_85/302737_f6cf13f1d6334d9297f3b9fbc6e0278c~mv2.webp)

### 



