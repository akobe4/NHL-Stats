ADDING TABLES TO DATABASE

Goalies Data Table
```SQL
CREATE TABLE goalies (
	  game_num varchar(10)	
	 ,game_date date
	 ,team_id varchar(2)
	 ,team_code varchar(3)	
     ,player_id varchar(7)	
	 ,player_name varchar(255)
	 ,catches varchar(1)
	 ,toi varchar(12)	
	 ,assists int
	 ,goals int
	 ,pim int 
	 ,shots int	
	 ,saves int	
	 ,pp_saves int
	 ,sh_saves int	
	 ,ev_saves int	
	 ,sh_shots int	
	 ,ev_shots int	
	 ,pp_shots int	
	 ,decision varchar(1)
	 ,sv_perc numeric	
	 ,pp_sv_perc numeric	
	 ,sh_sv_perc numeric	
	 ,ev_sv_perc numeric	
	 ,home_away varchar(4)
);
```

```SQL 
COPY goalies
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Scoring_Rates\Data\player_data\goalie_data_clean.csv'
DELIMITER ','
CSV Header;
```

Players Data Table
```SQL 
CREATE TABLE players (
	  game_num varchar(10)	
	 ,game_date date
	 ,team_id varchar(2)
	 ,team_code varchar(3)	
     ,player_id varchar(7)	
	 ,player_name varchar(255)
	 ,shoots varchar(1)
	 ,player_position varchar(2)
	 ,toi numeric	
	 ,assists int
	 ,goals int
	 ,shots int
	 ,hits int
	 ,pp_goals int
	 ,pp_assists int
	 ,pim int
	 ,fo_perc numeric
	 ,fo_wins int
	 ,fo_taken int
	 ,takeaways int
	 ,giveaways int
	 ,sh_goals int
	 ,sh_assists int
	 ,blocks int
	 ,plus_minus int
	 ,even_toi numeric
	 ,pp_toi numeric
	 ,sh_toi numeric
	 ,home_away varchar(4)
);
```

```SQL
COPY players
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Scoring_Rates\Data\player_data\player_data_clean.csv'
DELIMITER ','
CSV Header;
```

Game Data Table
```SQL
CREATE TABLE games (
	  team_id varchar(2)
	 ,team_code varchar(3)
	 ,game_num varchar(10)
	 ,game_date date
	 ,goals int
	 ,pim int
	 ,shots int
	 ,pp_perc numeric
	 ,ppg int 
	 ,pp_opp int
	 ,fo_win numeric	
	 ,blocks int	
	 ,takeaways int	
	 ,giveaways int	
	 ,hits int
	 ,home_away varchar(4)	
);
```

```SQL
COPY games
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Scoring_Rates\Data\game_data\game_data_clean.csv'
DELIMITER ','
CSV Header;
```