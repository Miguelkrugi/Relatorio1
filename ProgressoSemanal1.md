# Relatório de Progresso #1

Com base num dos requisitos de entrega do projeto, será desenvolvido um relatório de progressos semanais, que demonstrarão os progressos do desenvolvimento da "BusyBrain". Este relatório inclui progressos realizados ao nivel de Base de Dados, conexão das interfaces com a "database" (framework - Spring Boot - API Rest) e interfaces. Alterações no projeto (database, Rest API e interfaces) também serão incluidas no relatório semanal.

## Semana 1 (4-10 Outubro)

Durante a primeira semana de desenvolvimento do projeto (dia 4 a 10 de Outubro), foram desenhadas as primeiras versões dos layouts da app, de forma a poderem ser utilizadas como "base" para o posterior desenvolvimento dos layouts definitivos. Após o desenho e implementação dos primeiros layouts (em Android Studio), estes foram organizados tendo em conta o progresso do user na aplicação ("Path"). 
Além do planeamento e desenvolvimento dos layouts da aplicação, foram definidos e desenhados alguns esboços de Modelos Entidade-Relacionamento, que se pudessem adequar á app a ser desenvolvida. Este processo incluiu a definição de entidades envolvidas no contexto da app, atributos das mesmas e as diversas relações entre elas. 
Ao longo da primeira semana, foram ainda pesquisadas diversas API's que poderiam ser utilizadas de forma a implementar com sucesso algumas funcionalidades desejadas. Algumas API´s tais como a Google Maps API, Facebook API e Google Tasks API poderão ser utilizadas para desenvolver o projeto. 
Foram alteradas também informações relativas ao relatório do projeto, maioritariamente os "casos de uso", facilitando a sua compreensão e interpretação. 

## Semana 2 (10-17 Outubro)

Ao decorrer da segunda semana de desenvolvimento da aplicação, foram implementadas as interfaces da app, relativas aos diversos timers que a aplicação disponibilizará ao utilizador. As implementações basearam-se nas "demos" das interfaces desenhadas e idealizadas na primeira semana de desenvolvimento. Juntamente com os layouts de cada tipo de timer, foram implementadas algumas funcionalidades que não envolvem uso de "database", tais como as opções de "Play", "Pause" e "Reset" dos diversos timers disponiveis (telas de timer, "Small Break" e "Long Break") e o "path" entre as diversas "activities" da app (baseado no progresso do utilizador na aplicação descrito no relatório do projeto - guiões de teste). 
Foi também iniciado o desenvolvimento do primeiro protótipo do Modelo Entidade-Relacionamento, utilizando as entidades, atributos e relações definidas na primeira semana (4-10 Outubro).

## Semana 3 (18-24 Outubro)

No decorrer da terceira semana de desenvolvimento do projeto, foram corrigidos alguns erros e bugs relacionados ás activities da app. Juntamente com as correções de bugs, foram criadas e implementadas as activities "Splash Screen", "Login Screen", "Register Screen" e "Tasks Manager Screen", recorrendo ao Android Studio.
Ainda em Android Studio foi iniciada a implementação de "On-boarding Screen" no projeto. 
Foi iniciado o desenvolvimento de uma versão mais detalhada do Modelo Entidade-Relacionamento, representando de uma forma mais aprofundada as entidades envolvidas e as relações entre elas. 
Foram criadas duas personas (posteriormente adicionadas ao relatório do projeto). Para cada uma delas, foram definidas carateristicas que justificassem a necessidade de utilização da nossa aplicação.
Iniciado o desenvolvimento da Documentação REST API, onde foram indicados os métodos de acesso aos dados (CRUD Operations), os seus respetivos endpoints e os titulos e descrições de cada método da API a ser implementada. Foram também incluidos na Documentação os dados necessários para cada método, o resultado esperado para cada um deles, assim como a "descrição" de "Exceptions", caso ocorra algum erro ao realizar o método.
Foram também testadas algumas API's que possam vir a ser uteis para implementar algumas das funcionalidades desejadas para a app ("Google Maps API", "Google Places API" e "Facebook API").
Inicio do desenvolvimento da API (baseado na Documentação REST API), utilizando dados pré-definidos (na "database") para a posterior demonstração do protótipo do projeto.
Foi revisto ainda o "path" (progresso do utilizador na app) da aplicação. 

## Semana 4 (25 Outubro - 31 Outubro)

No decorrer da quarta semana de desenvolvimento, foi realizada uma segunda revisão dos guiões de teste e personas (presentes no relatório do projeto), sendo alteradas, removidas e adicionadas informações ao mesmo. 
Foi revista e alterada a estrutura da Documentação REST, em que, com base no Modelo Entidade-Relação, foram adicionados novos recursos (baseados nas entidades definidas), assim como os métodos de cada Recurso. 
Ainda nesta semana, foi iniciado o esboço da primeira versão definitiva do Modelo Entidade-Relação do projeto, indicando as entidades envolvidas e as relações entre elas.
Com base na Documentação REST, e, maioritariamente no Modelo Entidade-Relação do projeto, foi iniciada a realização do Dicionário de Dados (em Excel), onde se encontram exibidas várias tabelas (indicando as entidades), juntamente com os seus respetivos atributos, restrições de atributos (NULL, NOT NULL, etc.) e tipos de chave para cada um deles.
Ocorreram ainda várias implementações relativas ao design e funcionalidades da app, nomeadamente a tela de Definições da app, assim como a correção de bugs relativas ás telas de "Long Break" de cada timer.
Houveram ainda avanços relativos á definição de API´s a serem utilizadas no projeto.

## Semana 6 (1 - 7 Novembro)

Na quinta semana do projeto, foi retomado e terminado o esboço da primeira versão definitiva e detalhada do Modelo Entidade-Relação do projeto. Foram realizados avanços na estrutura da Documentação API, bem como na realização e implementação dos métodos do recurso "Utilizador" (baseados na primeira versão final do Modelo) 
Foi realizado o "deploy" da API no servidor da plataforma Heroku (juntamente com a base de dados implementada em PostgreSQL), permitindo acessar a API a partir de qualquer PC.
Foram iniciados ainda, os primeiros testes de conexão do Android Studio com a API implementada em Spring Boot e alojada no Heroku. 
Houveram avanços na realização da primeira versão do Dicionário de Dados, que estará completa até dia 7 de Novembro, juntamente com a primeira versão da estrutura da Documentação Rest API.
Foi iniciada também a realização da primeira versão do Diagrama de Classes (baseado no Modelo Entidade-Relação), e que estará completo até ao dia 7 de Novembro.
Foram implementadas e melhoradas algumas funcionalidades da app (sistema de "timers" e definições (Wi-fi desligado em sessões de trabalho e modo silencioso)). 
Por fim, foi terminada a primeira versão dos guiões de teste e personas (poderão sofrer alterações até á segunda entrega, prevista para o dia 12 de Novembro). 
