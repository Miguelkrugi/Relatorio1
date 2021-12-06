# Código de criação da Base de Dados

### Próxima Atualização: 22 Novembro (correção de erros, melhoria de apresentação do documento, adicionadas novas queries, etc.)

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

### Tabela "utilizador_tarefa"

create table utilizador_tarefa(

  user_id_tarefa SERIAL primary key,                         
  user_identifier int,                        
  CONSTRAINT fk_user_identifier FOREIGN KEY(user_identifier) REFERENCES utilizador(user_id),	                      
  task_identifier int,                               
  CONSTRAINT fk_task_identifier FOREIGN KEY(task_identifier) REFERENCES tarefa(task_id)	                             
  	
);

### Tabela "Local"

create table place(

  place_id SERIAL primary key,                          
  place_name varchar(100) not null,                          
  place_endereco varchar(300) not null,                         
  place_distancia int,                             
  place_categoria_id int,                              
  CONSTRAINT fk_placecategoriaid FOREIGN KEY(place_categoria_id) REFERENCES categorialocal(categoria_id)                    
  place_latitude double,                             
  place_longitude double                            

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
   wasThere bit (boolean),                                   
   utilizador_id int,                                      
   CONSTRAINT fk_utilizador_id FOREIGN KEY(utilizador_id) REFERENCES utilizador(user_id),                              
   local_id int,                                     
   CONSTRAINT fk_local_id FOREIGN KEY(local_id) REFERENCES place(place_id)                            

);

### Tabela "marcacao_favorito"

create table marcacao_favorito(

   favorite_id SERIAL primary key,                                     
   isFavorite bit (boolean),                                        
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

    data_convivio date,                           
    convivio_id SERIAL primary key,                        
    grupo_id int,                             
    CONSTRAINT fk_grupo_id FOREIGN KEY(grupo_id) REFERENCES grupo(group_id),                                           
    placee_id int,                             
    CONSTRAINT fk_place_id FOREIGN KEY(placee_id) REFERENCES place(place_id)                             

);

### Tabela "bloqueamento"

create table bloqueamento(

    bloqueamento_id SERIAL primary key,                                   
    utilizador_id int,                                          
    CONSTRAINT fk_user_id FOREIGN KEY(utilizador_id) REFERENCES utilizador(user_id),                                     
    blocked_status boolean (bit),                                     
    
);

### Tabela "app"

create table app(

  app_id SERIAL primary key,                                
  app_name varchar(50)                                        

) inherits (bloqueamento);


### Tabela "website"

create table website(

website_id SERIAL primary key,
website_domain_id int,
CONSTRAINT fk_domain_id FOREIGN KEY (website_domain_id) REFERENCES website_domains(id_website)	

) inherits (bloqueamento);

### Tabela "website_domains"

create table website_domains(

   id_website SERIAL primary key,
   domain_website varchar(120)

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

insert into tipotarefa (tasktype_nome) 
values ('Reunião')

insert into tipotarefa (tasktype_nome) 
values ('Palestra')

insert into tipotarefa (tasktype_nome) 
values ('Entrevista')

insert into tipotarefa (tasktype_nome) 
values ('Culinária')

insert into tipotarefa (tasktype_nome) 
values ('Desporto')


### Tabela "prioridadetarefa"

insert into prioridadetarefa (taskpriority_type) 
values ('Low')

insert into prioridadetarefa (taskpriority_type) 
values ('Medium')

insert into prioridadetarefa (taskpriority_type) 
values ('High')

insert into prioridadetarefa (taskpriority_type) 
values ('Urgent')


### Tabela "bloqueamento"

insert into bloqueamento(utilizador_id, blocked_status) 
values ('1', '1') 

insert into bloqueamento(utilizador_id, blocked_status) 
values('1', '1') 

insert into bloqueamento(utilizador_id, blocked_status) 
values('2', '1')

insert into bloqueamento(utilizador_id, blocked_status) 
values('3','1') 

insert into bloqueamento(utilizador_id, blocked_status) 
values('1', '1')

insert into bloqueamento(utilizador_id, blocked_status) 
values('4','1') 


### Tabela "utilizador_tarefa"

insert into utilizador_tarefa (user_identifier, task_identifier) 
values ('1', '4')

insert into utilizador_tarefa (user_identifier, task_identifier) 
values ('8', '4')

insert into utilizador_tarefa (user_identifier, task_identifier) 
values ('2', '1')

insert into utilizador_tarefa (user_identifier, task_identifier) 
values ('3', '1')

### Tabela "app"

insert into app(bloqueamento_id, utilizador_id, blocked_status, app_name) 
values('1','1','1','Facebook') 

insert into app(bloqueamento_id, utilizador_id, blocked_status, app_name) 
values('2','1','1','YouTube') 

insert into app(bloqueamento_id, utilizador_id, blocked_status, app_name) 
values('3','2','1','Wikipedia') 

insert into app(bloqueamento_id, utilizador_id, blocked_status, app_name) 
values('4','3','1','Kalorias') 

### Tabela "website"

insert into website(bloqueamento_id, utilizador_id, blocked_status, website_domain) 
values('5','1','1','facebook.com')

insert into website(bloqueamento_id, utilizador_id, blocked_status, website_domain) 
values('6','4','1','reddit.com')

### Tabela "grupo"

insert into grupo(group_name, group_description, tarefa_id) 
values ('Cook Dinner Group', 'Group to cook the dinner', '4')

insert into grupo(group_name, group_description, tarefa_id) 
values ('Grupo da tarefa 4', 'Isto é o grupo da tarefa 4 na BD', '4') 

insert into grupo(group_name, group_description, tarefa_id) 
values ('Grupo da tarefa 3', 'Isto é o grupo da tarefa 3 na BD', '3') 

insert into grupo(group_name, group_description, tarefa_id) 
values('Grupo para TPC Matematica', 'Isto é um grupo para o trabalho de matematica', '1')


### Tabela "convivio"

insert into convivio(data_convivio, grupo_id, placee_id) 
values('2021-11-02', '3', '4') 

insert into convivio(data_convivio, grupo_id, placee_id) 
values('2021-11-02', '3', '4') 


### Tabela "categorialocal"

insert into categorialocal (categoria_name) 
values ('Cafe')

insert into categorialocal (categoria_name) 
values ('Bar')

insert into categorialocal (categoria_name) 
values ('Restaurante')

insert into categorialocal (categoria_name) 
values ('Livraria')

insert into categorialocal (categoria_name) 
values ('Biblioteca')

### Tabela "Local"

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

### Tabela "marcacao_presenca"

insert into marcacao_presenca (wasthere, utilizador_id, local_id) 
values ('1', ‘1’, ‘3’)

insert into marcacao_presenca (wasthere, utilizador_id, local_id) 
values ('0', ‘3’, ‘5’)

### Tabela "marcacao_favorito"

insert into marcacao_presenca (isfavorite, utilizador_id, local_id) 
values ('1', ‘5’, ‘3’)

insert into marcacao_presenca (isfavorite, utilizador_id, local_id) 
values ('0', ‘1’, ‘5’)

insert into marcacao_presenca (isfavorite, utilizador_id, local_id) 
values ('1', ‘3’, ‘5’)


## Queries (relativas ás Custom Queries da API - podem sofrer alterações com o avanço do projeto)

#### Para ver os participantes de cada grupo criado na app

select * from utilizador 
inner join utilizador_tarefa on user_id = user_identifier
inner join tarefa on task_id = task_identifier

#### Filtrar websites bloqueados

SELECT * FROM website WHERE blocked_status = '1'

#### Filtrar websites desbloqueados

SELECT * FROM website WHERE blocked_status = '0'

#### Filtrar apps bloqueadas

SELECT * FROM app WHERE blocked_status = '1'

#### Filtrar apps desbloqueadas

SELECT * FROM app WHERE blocked_status = '0'

# OUTROS (NECESSITAM DE SER COMENTADOS - QUERIES DA API)
#### NOTA: AS QUERIES ENVOLVEM INNER JOINS, ETC:

select marcarpresencas.presenca_id AS presencaId, users.user_name AS Username, locais.place_name AS Nameofplace
from marcacao_presenca AS marcarpresencas
inner join utilizador users on users.user_id = marcarpresencas.utilizador_id
inner join place locais on marcarpresencas.local_id = locais.place_id
where wasthere = '1' 

select marcacoesp.presenca_id AS preId, userss.user_name AS username, localss.place_name AS nome
from marcacao_presenca AS marcacoesp
inner join utilizador userss on userss.user_id = marcacoesp.utilizador_id
inner join place localss on marcacoesp.local_id = localss.place_id
where wasthere = '1'and userss.user_id=:userid


select marcacoes.favorite_id AS favId, users.user_name AS Username, locals.place_name AS Nameofplace, marcacoes.isfavorite AS Status
from marcacao_favorito AS marcacoes 
inner join utilizador users on users.user_id = marcacoes.utilizador_id
inner join place locals on marcacoes.local_id = locals.place_id

select * from marcacao_presenca

insert into marcacao_presenca(wasthere, utilizador_id, local_id)
values('1', 2, 4)

# Para organizar:

select convivios.convivio_id AS idconvivio, convivios.data_convivio AS dataconvivio, groupss.group_name AS nomegrupo, placess.place_name
from convivio AS convivios
inner join grupo AS groupss on groupss.group_id = convivios.grupo_id
inner join place AS placess on placess.place_id = convivios.placee_id
where groupss.group_id=:grupoid

--convivios.convivio_id AS idconvivio

--convivios.data_convivio AS dataconvivio

select * from utilizador_tarefa

select participantes.user_id_tarefa AS idparticipante, usersss.user_name AS nameparticipante, tarefasss.task_title
from utilizador_tarefa AS participantes
inner join utilizador AS usersss on usersss.user_id = participantes.user_identifier
inner join tarefa AS tarefasss on tarefasss.task_id = participantes.task_identifier


select * from tarefa


