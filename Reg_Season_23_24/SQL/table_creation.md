ADDING TABLES TO DATABASE - EVENTS 

Goals Data Table 
```SQL
CREATE TABLE goals (
	  game_id varchar(10)
	 ,game_period int
	 ,event_id int
	 ,time_in_period time
	 ,time_remaining time
	 ,situation_code int
	 ,home_def_code varchar(5)
	 ,type_code int
	 ,event_name varchar(50)
	 ,event_owner_team_id int
	 ,zone_code char(1)
	 ,x_coord int
	 ,y_coord int
	 ,shot_type varchar(50)
	 ,goalie_in_id int
	 ,score_player_id int 
	 ,score_player_total int 
	 ,assist_1_player_id int 
	 ,assist_1_player_total int
	 ,assist_2_player_id int
	 ,assist_2_player_total int
	 ,away_score int
	 ,home_score int
);
```

```SQL 
COPY goals
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Reg_Season_23_24\Data\goals_nan_removed.csv'
DELIMITER ','
CSV Header;
```




