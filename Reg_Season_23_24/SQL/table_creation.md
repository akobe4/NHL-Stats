ADDING TABLES TO DATABASE - EVENTS 

**Goals Data Table** 
```SQL
CREATE TABLE goals (
	  game_id varchar(10)
	 ,game_period int
	 ,event_id int
	 ,time_in_period varchar(20)
	 ,time_remaining varchar(20)
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
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Reg_Season_23_24\Data\cleaned_for_sql\goals_clean_sql.csv'
DELIMITER ','
CSV Header;
```

**Shots Data Table**

```SQL
CREATE TABLE shots (
	  game_id varchar(10)
	 ,game_period int
	 ,event_id int
	 ,time_in_period varchar(20)
	 ,time_remaining varchar(20)
	 ,situation_code int
	 ,home_def_code varchar(5)
	 ,type_code int
	 ,event_name varchar(50)
	 ,event_owner_team_id int
	 ,zone_code char(1)
	 ,x_coord int
	 ,y_coord int
	 ,shot_type varchar(50)
	 ,shoot_player_id int 
	 ,goalie_in_id	int
	 ,away_sog int
	 ,home_sog int 
	 ,miss_reason varchar(50)
	 ,block_player_id int
	 ,block_reason	varchar(50)
);
```

```SQL 
COPY shots
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Reg_Season_23_24\Data\cleaned_for_sql\all_shots_clean_sql.csv'
DELIMITER ','
CSV Header;
```

**Faceoff Data Table**

```SQL
CREATE TABLE faceoffs (
	  game_id varchar(10)
	 ,game_period int
	 ,event_id int
	 ,time_in_period varchar(20)
	 ,time_remaining varchar(20)
	 ,situation_code int
	 ,home_def_code varchar(5)
	 ,type_code int
	 ,event_name varchar(50)
	 ,event_owner_team_id int
	 ,zone_code char(1)
	 ,x_coord int
	 ,y_coord int
	 ,l_player_id int
	 ,w_player_id int
);
 ```

 ```SQL
 COPY faceoffs
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Reg_Season_23_24\Data\cleaned_for_sql\faceoffs_clean_sql.csv'
DELIMITER ','
CSV Header;
 ```

**Hits Data Table**

```SQL
CREATE TABLE hits (
	  game_id varchar(10)
	 ,game_period int
	 ,event_id int
	 ,time_in_period varchar(20)
	 ,time_remaining varchar(20)
	 ,situation_code int
	 ,home_def_code varchar(5)
	 ,type_code int
	 ,event_name varchar(50)
	 ,event_owner_team_id int
	 ,zone_code char(1)
	 ,x_coord int
	 ,y_coord int
	 ,hitter_id int
	 ,hittee_id int
);
```

```SQL
 COPY hits
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Reg_Season_23_24\Data\cleaned_for_sql\hits_clean_sql.csv'
DELIMITER ','
CSV Header;
```

**Giveaways Data Table**

```SQL
CREATE TABLE giveaways (
	  game_id varchar(10)
	 ,game_period int
	 ,event_id int
	 ,time_in_period varchar(20)
	 ,time_remaining varchar(20)
	 ,situation_code int
	 ,home_def_code varchar(5)
	 ,type_code int
	 ,event_name varchar(50)
	 ,event_owner_team_id int
	 ,zone_code char(1)
	 ,x_coord int
	 ,y_coord int
	 ,give_player_id int
);
```

```SQL
COPY giveaways
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Reg_Season_23_24\Data\cleaned_for_sql\giveaways_clean_sql.csv'
DELIMITER ','
CSV Header;
```

**Takeaways Data Table**
```SQL
CREATE TABLE takeaways (
	  game_id varchar(10)
	 ,game_period int
	 ,event_id int
	 ,time_in_period varchar(20)
	 ,time_remaining varchar(20)
	 ,situation_code int
	 ,home_def_code varchar(5)
	 ,type_code int
	 ,event_name varchar(50)
	 ,event_owner_team_id int
	 ,zone_code char(1)
	 ,x_coord int
	 ,y_coord int
	 ,take_player_id int
);
```

```SQL
COPY takeaways
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Reg_Season_23_24\Data\cleaned_for_sql\takeaways_clean_sql.csv'
DELIMITER ','
CSV Header;
```

**Penalties Data Table**
```SQL
CREATE TABLE penalties (
	  game_id varchar(10)
	 ,game_period int
	 ,event_id int
	 ,time_in_period varchar(20)
	 ,time_remaining varchar(20)
	 ,situation_code int
	 ,home_def_code varchar(5)
	 ,type_code int
	 ,event_name varchar(50)
	 ,event_owner_team_id int
	 ,zone_code char(1)
	 ,x_coord int
	 ,y_coord int
	 ,penl_code varchar(3)
	 ,penl_type varchar(100)
	 ,penl_len int
	 ,drawn_by_player_id int
	 ,commit_player_id int
);
```

```SQL
COPY penalties
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Reg_Season_23_24\Data\cleaned_for_sql\penalties_clean_sql.csv'
DELIMITER ','
CSV Header;
```