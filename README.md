# SQL

2030-05-03
use test;

select *
from player;

set SQL_SAFE_UPDATES=0;
update player
set position = 'FW'
where player_id=2000002;

select player_id as ID,player_name as name
from player
where weight>90;
/* */
select player_name, concat(height,'cm') 
from player
where height>170
/==========================================================================================
use test;

select *
from player;

update player
set position = 'FW'
where player_id=20000002;



create table alpaco_student(
id int not null,
name varchar(10) not null,
email varchar(30) not null,
phone_number varchar(20) not null,
alpaco_office_id varchar(20) not null,
constraint alpaco_student_PK primary key (id),
constraint alpaco_student_FK foreign key (alpaco_office_id) references alpaco(alpaco_office_id) 
);

create table brand(
brand_id varchar(20) not null,
Name varchar(20) not null,
constraint brand_PK primary key(brand_id)
);

create table movie(
id int not null,
movie_name varchar(100) not null,
brand_id varchar(100) not null,
sit varchar(20) not null,
constraint movie_PK primary key(id),
constraint movie_FK foreign key (brand_id) references brand(brand_id)
);
-- ALTER TABLE PLAYER DROP COLUMN EMAIL;
-- ALTER TABLE PLAYER MODIFY PLAYER_NAME VARCHAR(100) NOT NULL;
