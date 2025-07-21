**Draft Info Data Table**
```SQL
CREATE TABLE draft (
	  player_id int
	 ,current_team char(3)
	 ,first_name varchar(50)
	 ,last_name varchar(50)
	 ,draft_year int
	 ,draft_team char(3)
	 ,draft_round int 
	 ,pick_in_round int
	 ,pick_overall int
);
```

```SQL
COPY draft
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Player_Info_23_24\Data\player_data_clean_sql\draft_info_clean_sql.csv'
DELIMITER ','
CSV Header;
```

**Goalie Game Data Table**
```SQL
CREATE TABLE goalie_game_data (
	  season_id int
	 ,game_type_id int
	 ,game_id int
	 ,player_team char(3)
	 ,opponent_team char(3)
	 ,home_road char(1)
	 ,game_date date
	 ,player_id int 
	 ,goals int
	 ,assists int
	 ,games_started int 
	 ,decision char(1)
	 ,shots_against int
	 ,goals_against int 
	 ,save_perc decimal(4,3)
	 ,so int
	 ,pim int
	 ,toi varchar(20)
);
```
```SQL
COPY goalie_game_data
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Player_Info_23_24\Data\player_data_clean_sql\goalie_game_data_clean_sql.csv'
DELIMITER ','
CSV Header;
```

**Skater Game Data Table**
```SQL 
CREATE TABLE skater_game_data (
	  season_id int
	 ,game_type_id int
	 ,game_id int 
	 ,player_team char(3)
	 ,opponent_team char(3)
	 ,home_road char(1)
	 ,game_date date
	 ,player_id int 
	 ,goals int 
	 ,assists int 
	 ,points int 
	 ,plus_minus int 
	 ,pp_goals int 
	 ,pp_points int 
	 ,game_winning_goals int 
	 ,ot_goals int 
	 ,shots int 
	 ,shifts int 
	 ,sh_goals int 
	 ,sh_points int 
	 ,pim int 
	 ,toi varchar(20)
);
```

```SQL
COPY skater_game_data
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Player_Info_23_24\Data\player_data_clean_sql\skater_game_data_clean_sql.csv'
DELIMITER ','
CSV Header;
```

**Roster Data Table**

```SQL 
CREATE TABLE roster (
	  season_id int
	 ,first_name varchar(50)
	 ,last_name varchar(50)
	 ,sweater_number int
	 ,player_position char(1)
	 ,shoots_catches char(1)
	 ,birthdate date
	 ,birth_city varchar(100)
	 ,birth_country char(3)
	 ,weight int 
	 ,height int
);
```

```SQL 
COPY roster
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Player_Info_23_24\Data\player_data_clean_sql\roster_clean_sql.csv'
DELIMITER ','
CSV Header;
```