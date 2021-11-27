# Fichas SQL
## Ficha de "GROUP BY"

select count(*) NStudents --EXIBIR O NUMERO DE ELEMENTOS DA TABELA ESTUDANTE (NUMERO DE ESTUDANTES)
from students

select * from students

select count(stu_email) NEmails --EXIBIR O NUMERO DE EMAILS PRESENTES NA TABELA "ESTUDANTES" (EXCEPTO OS "NULL") 
from students

select count(distinct stu_place) NPlaces  --EXIBIR O NUMERO DE LOCAIS COM NOMES DIFERENTES ("DISTINCT" PARA LOCAIS COM NOMES DIFERENTES | COUNT - MOSTRA O NUMERO DE ELEMENTOS)
from students

select max(stu_id) --EXIBIR O ELEMENTO DA TABELA DE ESTUDANTES QUE CONTEM O VALOR DO ID MAIS ELEVADO
from students

select min(EXTRACT (year FROM age(current_date, stu_bdate)))
from students

select min(stu_bdate)
from students

--PARA CALCULAR A MEDIA...UTILIZAMOS A FUNCAO AVG()

select avg(stu_id) as mediaid --CALCULA A MEDIA DE ID'S (1+2+3+4+5+6+7+8+9+10+11+12+13+14+15+16+17+18+19+20)/20
from students

select stu_name, count(*) -- OBTER O NOME DOS ESTUDANTES QUE NÃO POSSUEM EMAIL
from students
where stu_email is NULL
group by stu_name

select stu_name, count(*) -- OBTER O NOME DOS ESTUDANTES QUE VIVEM EM CASCAIS
from students
where stu_place = 'Cascais'
group by stu_name

select stu_gender, count(*) --AGRUPAMENTO POR GÉNERO, OBTENDO O NUMERO DE ELEMENTOS (ESTUDANTES), PERTENCENTES A UM GÉNERO (M ou F)
from students
group by stu_gender

select stu_place, count(*) NEstudantes --AGRUPAMENTO POR LOCAL, OBTENDO O NUMERO DE ELEMENTOS (ESTUDANTES), PERTENCENTES A UM LOCAL
from students
group by stu_place

select stu_cour_id, count(*) --AGRUPAMENTO POR CURSO, OBTENDO O NUMERO DE ELEMENTOS (ESTUDANTES), PERTENCENTES A UM CURSO (ID DO CURSO)
from students
group by stu_cour_id

select EXTRACT (year from stu_bdate) ano, count(*) NEstudantes --AGRUPAMENTO POR ANO DE NASCIMENTO, OBTENDO O NUMERO DE ELEMENTOS (ESTUDANTES), PERTENCENTES A UM ANO DE NASCIMENTO
from students
group by stu_bdate

--- FUNÇÃO DE "HAVING" ---

select stu_cour_id, count(*) --CURSOS COM MAIS DE 2 ESTUDANTES
from students
group by stu_cour_id
having count(*) > 2

select stu_place, count(*) -- LOCAIS ONDE VIVEM 2 ESTUDANTES
from students 
group by stu_place
having count(*) = 2

select stu_cour_id, count(*) -- CURSOS COM MAIS DE 2 ESTUDANTES DO SEXO FEMININO
from students
group by stu_cour_id, stu_gender
having count(*) > 2 and stu_gender = 'F'
