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
