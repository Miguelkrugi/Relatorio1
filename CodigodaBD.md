# Código de criação da Base de Dados

### AVISO: Este documento pertence á Base de Dados DEMO. 

## Criação de tabelas

### Tabela "Utilizador"


create table utilizador(

  user_id SERIAL primary key,             
  user_name varchar(20) not null,         
  user_password varchar(30) not null,
  user_email varchar(50)                            
                                                 
);

### Tabela "TipoTarefa"

create table tipotarefa(

   tasktype_id SERIAL primary key,                 
   tasktype_nome varchar(30) not null

);

### Tabela "PrioridadeTarefa"

create table prioridadetarefa(

   taskpriority_id SERIAL primary key,               
   taskpriority_type varchar(10)

);

### Tabela "Tarefa"

create table tarefa(

   task_id SERIAL primary key,                     
   task_title varchar(50) not null,                  
   task_desc varchar(500) DEFAULT 'There is no description for this task',                  
   due_date date NOT NULL DEFAULT CURRENT_DATE,               
   user_task_id int,	                
   CONSTRAINT fk_usertaskid FOREIGN KEY(user_task_id) REFERENCES utilizador(user_id),                         
   task_priority_id int,                     
   CONSTRAINT fk_prioritytarefa FOREIGN KEY(task_priority_id) REFERENCES prioridadetarefa(taskpriority_id),                          
   task_type_id int,                        
   CONSTRAINT fk_tipotarefa FOREIGN KEY(task_type_id) REFERENCES tipotarefa(tasktype_id)                  	

);

### Tabela "tarefa_grupo"

create table tarefa_grupo(

  task_group_id int,	
  CONSTRAINT fk_task_group_id FOREIGN KEY(task_group_id) REFERENCES grupo(group_id)

) inherits tarefa;

### Tabela "utilizador_tarefa"

create table utilizador_tarefa(

  user_id_tarefa SERIAL primary key,                         
  user_identifier int,                        
  CONSTRAINT fk_user_identifier FOREIGN KEY(user_identifier) REFERENCES utilizador(user_id),	                      
  task_identifier int,                               
  CONSTRAINT fk_task_identifier FOREIGN KEY(task_identifier) REFERENCES tarefa(task_id)	                             
  	
);

### Tabela "Place"

create table place(

  place_id SERIAL primary key,                          
  place_name varchar(100) not null,                          
  place_endereco varchar(300) not null,  
  place_latitude double,   
  place_longitude double,                           
  place_google_id varchar(100),
  user_request_id int,
  CONSTRAINT fk_user_request_id FOREIGN KEY(user_request_id) REFERENCES utilizador(user_id)

);

### Tabela "categorialocal"

create table categorialocal(

  categoria_id SERIAL primary key,                                 
  categoria_name varchar(15) not null                                 

);

### Tabela "utilizador_local" 

create table utilizador_local(

  user_local_id SERIAL primary key,                                    
  utilizador_id int,                                        
  CONSTRAINT fk_utilizador_id FOREIGN KEY(utilizador_id) REFERENCES utilizador(user_id)                                    
  local_id int,                                      
  CONSTRAINT fk_local_id FOREIGN KEY(local_id) REFERENCES place(place_id)                               
);

### Tabela "marcacao_presenca"

create table marcacao_presenca(

   presenca_id SERIAL primary key,                                      
   wasthere bit (boolean),                                   
   utilizador_id int,                                      
   CONSTRAINT fk_utilizador_id FOREIGN KEY(utilizador_id) REFERENCES utilizador(user_id),                              
   local_id int,                                     
   CONSTRAINT fk_local_id FOREIGN KEY(local_id) REFERENCES place(place_id)                            

);

### Tabela "marcacao_favorito"

create table marcacao_favorito(

   favorite_id SERIAL primary key,                                     
   isfavorite bit (boolean),                                        
   utilizador_id int,                                 
   CONSTRAINT fk_utilizador_id FOREIGN KEY(utilizador_id) REFERENCES utilizador(user_id),                                     
   local_id int,                                   
   CONSTRAINT fk_local_id FOREIGN KEY(local_id) REFERENCES place(place_id)                               

);

### Tabela "grupo"

create table grupo(

    group_id SERIAL primary key,                                
    group_name varchar(30) not null,                            
    group_description varchar(150),                             
    tarefa_id int,                                
    CONSTRAINT fk_tarefa_id FOREIGN KEY(tarefa_id) REFERENCES tarefa(task_id)                       
	
);

### Tabela "convivio"

create table convivio(

    convivio_id SERIAL primary key,
    data_convivio date,                                                  
    grupo_id int,                             
    CONSTRAINT fk_grupo_id FOREIGN KEY(grupo_id) REFERENCES grupo(group_id),                                           
    placee_id int,                             
    CONSTRAINT fk_place_id FOREIGN KEY(placee_id) REFERENCES place(place_id)                             

);



### Tabela "website"

create table website(

website_id SERIAL primary key,
website_domain_id int,
CONSTRAINT fk_domain_id FOREIGN KEY (website_domain_id) REFERENCES website_domains(id_website),
website_user_block int,
CONSTRAINT fk_user_block FOREIGN KEY (website_user_block) REFERENCES utilizador(user_id),
website_blocked_status bit DEFAULT 1::bit NOT NULL

);

### Tabela "website_domains"

create table website_domains(

   id_website SERIAL primary key,
   domain_website varchar(120),
   website_name varchar(60)

);

## Inserts em tabelas 

### Tabela "tarefa"

insert into tarefa (task_title, task_desc, due_date, user_task_id, task_priority_id, task_type_id) 
values ('Math homework', 'Do the math homework', '2015-03-08', '3', '2', '1')

insert into tarefa (task_title, task_desc, due_date, user_task_id, task_priority_id, task_type_id) 
values ('Cook the dinner', 'Cook the dinner for Christmas Day', '2015-03-08', '3', '1', '3')

insert into tarefa (task_title, task_desc, due_date, user_task_id, task_priority_id, task_type_id) 
values ('Buy groceries', 'Buy all the groceries to lunch', '2020-01-12', '4', '3', '2')

insert into tarefa (task_title, task_desc, due_date, user_task_id, task_priority_id, task_type_id) 
values ('Go to mall', 'Go to the mall to buy clothes', '2021-04-05', '8', 4', '2')

### Tabela "tarefa_grupo"

insert into tarefa_grupo(task_title, task_desc, due_date, user_task_id, task_priority_id, task_type_id, task_group_id, tarefa_id)
values ('Carry shopping items', 'Help with shopping', '2022-01-01', 2,2,1,6,3)

### Tabela "utilizador"

insert into utilizador (user_name, user_password, user_email) 
values ('johndoe', 'johndoeoriginal', 'jdoe@gmail.com')


insert into utilizador (user_name, user_password, user_email) 
values ('marydoe', 'marydoeoriginal', 'mdoe@gmail.com')


insert into utilizador (user_name, user_password, user_email) 
values ('laurendoe', 'laudoeoriginal', 'lauren12doe@gmail.com')


insert into utilizador (user_name, user_password, user_email) 
values ('joaofepas12', 'fepasjoaoxxx12', 'fepas@gmail.com')


insert into utilizador (user_name, user_password, user_email) 
values ('miguel12', 'miguel2002', 'miguel12@gmail.com')


insert into utilizador (user_name, user_password, user_email) 
values ('juliotrinta56', 'julio56password', 'julio56@gmail.com')


insert into utilizador (user_name, user_password, user_email) 
values ('hugoferreira22', 'huguinhopp', 'hugoferras22@gmail.com')

### Tabela "tipotarefa"

insert into tipotarefa (tasktype_nome) 
values ('Individual')

insert into tipotarefa (tasktype_nome) 
values ('Grupo')


### Tabela "prioridadetarefa"

insert into prioridadetarefa (taskpriority_type) 
values ('Low')

insert into prioridadetarefa (taskpriority_type) 
values ('Medium')

insert into prioridadetarefa (taskpriority_type) 
values ('High')

insert into prioridadetarefa (taskpriority_type) 
values ('Urgent')


### Tabela "utilizador_tarefa"

insert into utilizador_tarefa (user_identifier, task_identifier) 
values ('2', '4')

insert into utilizador_tarefa (user_identifier, task_identifier) 
values ('8', '4')

insert into utilizador_tarefa (user_identifier, task_identifier) 
values ('15', '4')

### Tabela "website"

insert into website(website_domain_id, website_user_block, website_blocked_status) 
values('4','8','1')

insert into website(website_domain_id, website_user_block, website_blocked_status) 
values('1','8','1')

### Tabela "grupo"

insert into grupo(group_name, group_description, tarefa_id) 
values ('Shopping group', 'Group to buy stuff in the mall', '4')

insert into grupo(group_name, group_description, tarefa_id) 
values ('ajaja group', 'jaajajaj group', '33') 

### Tabela "convivio"

insert into convivio(data_convivio, grupo_id, placee_id) 
values('2022-01-02', '6', '22') 

insert into convivio(data_convivio, grupo_id, placee_id) 
values('2021-01-02', '10', '18') 

insert into convivio(data_convivio, grupo_id, placee_id) 
values('2021-01-01', '6', '22') 


### Tabela "Local" (DESATUALIZADO DEVIDO A ALTERAÇÕES NA TABELA (DADOS DEPENDEM DO 'GOOGLE PLACES API'))

insert into place (place_name, place_endereco, place_distancia, place_categoria) 
values ('Bar Lemos','Rua Joao Direitinho, Nº 13','500','1')

insert into place (place_name, place_endereco, place_distancia, place_categoria) 
values ('Livraria Eca de Queiroz','Rua Lopes Santini, Nº 24','2310','4')

insert into place (place_name, place_endereco, place_distancia, place_categoria) 
values ('Cafe Dom Joaquim','Avenida da Estrela', Nº 4B','253','2')

insert into place (place_name, place_endereco, place_distancia, place_categoria) 
values ('Cafe O Dante','Rua Neuracia da Alemanha, Nº 12,'1256','1')

insert into place (place_name, place_endereco, place_distancia, place_categoria, place_latitude, place_longitude) 
values ('Livraria Dom Joao I','Rua do Rossio, Nº 22','1156','4', '27372.47571937', '37471.47591811')

### Tabela "marcacao_presenca" ("wasthere" possui valor 'true' por DEFAULT)

insert into marcacao_presenca (wasthere, utilizador_id, local_id) 
values ('1', ‘1’, ‘3’)

insert into marcacao_presenca (wasthere, utilizador_id, local_id) 
values ('0', ‘3’, ‘5’)
insert into marcacao_presenca (wasthere, utilizador_id, local_id) 
values ('1', ‘15’, ‘18’)

### Tabela "marcacao_favorito"

insert into marcacao_presenca (isfavorite, utilizador_id, local_id) 
values ('1', ‘5’, ‘3’)

insert into marcacao_presenca (isfavorite, utilizador_id, local_id) 
values ('0', ‘1’, ‘5’)

insert into marcacao_presenca (isfavorite, utilizador_id, local_id) 
values ('1', ‘3’, ‘5’)

insert into marcacao_favorito (isfavorite, utilizador_id, local_id) 
values ('1', ‘8’, ‘3’)

insert into marcacao_favorito (isfavorite, utilizador_id, local_id) 
values ('0', ‘8’, ‘1’)

### Tabela "website_domains"

insert into website_domains(domain_website) values ('www.youtube.com'), ('www.facebook.com'), ('www.twitter.com'), ('www.instagram.com'),('www.wikipedia.org'),('www.yahoo.com'),('www.whatsapp.com'),('www.netflix.com'),('www.amazon.com'),('www.reddit.com');

## Queries (relativas ás Custom Queries da API)

### Obter websites desbloqueados por um utilizador

select sites.website_id AS websiteId, sites.website_user_block AS userId , users.user_name AS userName, dominios.website_name AS websiteName,dominios.domain_website AS websiteDomain, sites.website_blocked_status AS blockedStatus 
from website AS sites 
inner join website_domains dominios on sites.website_domain_id = id_website 
inner join utilizador users on sites.website_user_block = users.user_id  
where sites.website_blocked_status = '0' and sites.website_user_block=:userid

### Obter websites bloqueados por um utilizador

select sites.website_id AS websiteId, sites.website_user_block AS userId , users.user_name AS userName, dominios.website_name AS websiteName,dominios.domain_website AS websiteDomain, sites.website_blocked_status AS blockedStatus 
from website AS sites 
inner join website_domains dominios on sites.website_domain_id = id_website 
inner join utilizador users on sites.website_user_block = users.user_id 
where sites.website_blocked_status = '1' and sites.website_user_block=:userid

### Obter os participantes de um grupo

select groups.group_id AS groupId, usertask.user_id_tarefa AS participantId, groups.group_name AS groupName, groups.group_description AS groupDesc, users.user_name AS userName, users.user_id AS userId 
from grupo AS groups  
inner join tarefa tarefas on tarefa_id = task_id 
inner join utilizador_tarefa usertask on task_id = task_identifier 
inner join utilizador users on user_identifier = user_id 
where groups.group_id=:groupid

### Obter as tarefas (individuais) de um utilizador

select tarefas.task_title AS taskTitle, tarefas.task_desc AS taskDesc, priority.taskpriority_type AS prioridade, tarefas.task_id AS taskId, tarefas.user_task_id AS usertaskId 
from tarefa AS tarefas
inner join prioridadetarefa priority on priority.taskpriority_id = tarefas.task_priority_id 
inner join tipotarefa tipo on tarefas.task_type_id = tipo.tasktype_id 
inner join utilizador users on tarefas.user_task_id = users.user_id
where tarefas.user_task_id=:usertaskid

### Filtragem de tarefas de um utilizador por prioridade

select tarefas.task_title AS taskTitle, tarefas.task_desc AS taskDesc, priority.taskpriority_type AS prioridade, tarefas.task_id AS taskId, tarefas.user_task_id AS usertaskId 
from tarefa AS tarefas 
inner join prioridadetarefa priority on priority.taskpriority_id = tarefas.task_priority_id 
inner join tipotarefa tipo on tarefas.task_type_id = tipo.tasktype_id
where tarefas.user_task_id=:usertaskid and priority.taskpriority_id=:priority

### Obter todas as tarefas de um grupo (contendo várias informações)

select tarefas.task_id AS taskId, tarefas.task_group_id AS taskgroupId,tarefas.task_title AS taskTitle, tarefas.task_desc AS taskDesc, prioridade.taskpriority_type AS priorityType, userss.user_name AS userName, participante.user_id_tarefa AS participanteId, userss.user_id AS userId  
from tarefa_grupo AS tarefas 
inner join prioridadetarefa AS prioridade on tarefas.task_priority_id = prioridade.taskpriority_id 
inner join grupo AS grupos on tarefas.task_group_id = grupos.group_id 
inner join utilizador_tarefa AS participante on tarefas.user_task_id = participante.user_identifier  
inner join utilizador AS userss on participante.user_identifier = userss.user_id
where tarefas.task_group_id=:taskgroupid

### Obter os locais com presenças de um utilizador

select marcacoes.presenca_id AS presencaId, marcacoes.utilizador_id AS utilizadorId, userss.user_name AS userName,locais.place_name AS placeName, locais.place_endereco AS placeEndereco, locais.place_id AS placeId 
from marcacao_presenca AS marcacoes  
inner join utilizador userss on marcacoes.utilizador_id = userss.user_id  
inner join place locais on marcacoes.local_id = locais.place_id 
where marcacoes.wasthere = '1' and marcacoes.utilizador_id=:utilizadorid

### Obter os locais favoritos de um utilizador

select marcacoes.favorite_id AS favoriteId, marcacoes.utilizador_id AS utilizadorId, locais.place_name AS placeName, locais.place_endereco AS placeEndereco, locais.place_id AS placeId 
from marcacao_favorito AS marcacoes 
inner join utilizador userss on marcacoes.utilizador_id  = userss.user_id 
inner join place locais on marcacoes.local_id = locais.place_id 
where marcacoes.isfavorite = '1'
and marcacoes.utilizador_id=:utilizadorid

### Obter a informação de um local selecionado por um utilizador

select locais.place_id AS placeId, locais.place_name AS placeName, locais.place_endereco AS placeEndereco, locais.place_latitude AS placeLatitude, locais.place_longitude AS placeLongitude, locais.place_favorite AS placeFavorite, locais.place_presenca AS placePresenca, userss.user_id AS userId 
from place AS locais 
inner join utilizador userss on userss.user_id = locais.user_request_id
where userss.user_id=:userid and locais.place_id=:placeid

### Obter todos os grupos de um utilizador

select grupos.group_id AS groupId, grupos.group_name AS groupName, grupos.group_description AS groupDesc, tarefas.task_title AS taskTitle, tarefas.user_task_id AS usertaskId 
from grupo AS grupos 
inner join tarefa tarefas on tarefas.task_id = grupos.tarefa_id
where tarefas.user_task_id=:usertaskid

### Obter informações de um grupo selecionado por um utilizador (da sua lista de grupos)

select grupos.group_id AS groupId, grupos.group_name AS groupName, grupos.group_description AS groupDesc, tarefas.task_title AS taskTitle, tarefas.user_task_id AS usertaskId
from grupo AS grupos 
inner join tarefa tarefas on tarefas.task_id = grupos.tarefa_id
where tarefas.user_task_id=:usertaskid and grupos.group_id=:groupid

### Obter o histórico de convivios de um grupo

select convivios.convivio_id AS convivioId, grupos.group_name AS groupName, tarefas.task_title AS taskTitle, locais.place_name AS placeName, locais.place_endereco AS placeEndereco, convivios.data_convivio AS convivioData 
from convivio AS convivios 
inner join grupo AS grupos on convivios.grupo_id = grupos.group_id 
inner join place as locais on convivios.placee_id = locais.place_id 
inner join tarefa as tarefas on grupos.tarefa_id = tarefas.task_id
where grupos.group_id=:grupoid

### Atualizar o bloqueio de um website 

update website set website_blocked_status = '1' where sites.website_domain_id=:domainid  and sites.website_user_block=:userid

### Atualizar o desbloqueio de um website

update website set website_blocked_status = '0' where sites.website_domain_id=:domainid and sites.website_user_block=:userid

### Atualizar a marcação de presença num local (APÓS A PRIMEIRA MARCAÇÃO)

update marcacao_presenca set wasthere = '1' where marcacoes.utilizador_id=:utilizadorid and marcacoes.local_id=:placeid

### Atualizar a desmarcação de presença num local

update marcacao_presenca set wasthere = '0' where marcacoes.utilizador_id=:utilizadorid and marcacoes.local_id=:placeid

### Atualizar a marcação de favorito num local (APÓS A PRIMEIRA MARCAÇÃO)

update marcacao_favorito set isfavorite = '1' where marcacoes.utilizador_id=:utilizadorid and marcacoes.local_id=:placeid

### Atualizar a desmarcação de favorito num local

update marcacao_favorito set isfavorite = '0' where marcacoes.utilizador_id=:utilizadorid and marcacoes.local_id=:placeid


#### Outros

select * from mensagem

select * from chat

select * from utilizador_tarefa

select * from mensagem

insert into chat(chat_grupo_id) values (1)

insert into mensagem(message_content, message_chat_id, message_user_id)
values('Ola a todos!', 1, 3)

select * from marcacao_favorito

UPDATE marcacao_favorito
SET isfavorite = '1'
WHERE utilizador_id = 3 and local_id = 5

select * from marcacao_presenca

insert into marcacao_presenca(wasthere, utilizador_id, local_id)
values('1', 2, 4)
