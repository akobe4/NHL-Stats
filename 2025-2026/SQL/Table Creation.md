**Table Creation NHL Stats 2024-2025**

**All Shots Data Table**
```SQL
CREATE TABLE all_shots (
	game_id int
	,game_period int	
	,event_id int	
	,time_in_period varchar(20)
	,time_remaining varchar(20)
	,situation_code	int
	,home_def_code varchar(5)	
	,type_code int
	,event_name varchar(50)
	,event_owner_team_id int
	,zone_code char(1)
	,x_coord int
	,y_coord int
	,shot_type varchar(50)
	,shoot_player_id int
	,goalie_in_id int
	,away_sog int
	,home_sog int
	,miss_reason varchar(50)	
	,block_player_id int
	,block_reason varchar(50)
);
```

```SQL
COPY all_shots
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\all_shots.csv'
DELIMITER ','
CSV Header; 
```

**Blocked Shots Data Table**
```SQL 
CREATE TABLE blocked_shots(
	game_id int
	,game_period int
	,event_id int
	,time_in_period varchar(20)
	,time_remaining varchar(20)
	,situation_code int
	,home_def_code varchar(50)
	,type_code int
	,event_name varchar(50)
	,event_owner_team_id int
	,zone_code char(1)
	,x_coord int
	,y_coord int
	,shoot_player_id int
	,block_player_id int
	,block_reason varchar(50)
);
```

```SQL 
COPY blocked_shots
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\blocked_shots.csv'
DELIMITER ','
CSV Header; 
```

**Faceoffs Data Table**
```SQL
CREATE TABLE faceoffs(
	game_id	int
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
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\faceoffs.csv'
DELIMITER ','
CSV Header; 
```

**Game Story Data Table**
```SQL
CREATE TABLE game_story_data(
	game_id int
	,game_date date
	,venue varchar
	,venue_location varchar(50)
	,a_team_id int
	,h_team_id int
	,a_team_code char(3)
	,h_team_code char(3)
	,a_team_score int
	,h_team_score int
	,a_sog int
	,h_sog int
	,a_fo_win_perc decimal(4,3)
	,h_fo_win_perc decimal(4,3)
	,a_pp_perc decimal(4,3)
	,h_pp_perc decimal(4,3)
	,a_pim int
	,h_pim int
	,a_hits int
	,h_hits int
	,a_blocked_shots int
	,h_blocked_shots int
	,a_giveaways int
	,h_giveaways int
	,a_takeaways int
	,h_takeaways int
	,a_ppg int
	,h_ppg int
	,a_total_pp int
	,h_total_pp int
)
```

```SQL
COPY game_story_data
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\game_story_data.csv'
DELIMITER ','
CSV Header; 
```

**Giveaways Data Table**
```SQL
CREATE TABLE giveaways(
	game_id int
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
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\giveaways.csv'
DELIMITER ','
CSV Header; 
```

**Golaie Career Regular Season Stats Data Table**
```SQL
CREATE TABLE goalie_career_reg_stats (
	player_id int
	,games_played int
	,games_started int
	,wins int
	,losses int
	,ot_losses int
	,goals int
	,assists int
	,goals_against int
	,gaa decimal(5,3)
	,pim int
	,save_pctg decimal(5,3)
	,shots_against int
	,shutouts int
);
```

```SQL
COPY goalie_career_reg_stats
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\goalie_career_reg_stats.csv'
DELIMITER ','
CSV Header; 
```

**Goalie Regular Season Stats Data Table**
```SQL
CREATE TABLE goalie_reg_stats(
	player_id int
	,games_played int
	,wins int
	,losses int
	,ot_losses int
	,gaa decimal(5,3)
	,save_pctg decimal(5,3)
	,shut_outs int
);
```

```SQL
COPY goalie_reg_stats
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\goalie_reg_stats.csv'
DELIMITER ','
CSV Header; 
```

**Goals Data Table**
```SQL
CREATE TABLE goals (
	game_id int
	,game_period int
	,event_id int
	,time_in_period varchar(20)
	,time_remaining varchar(20)
	,situation_code int
	,home_def_code varchar(5)
	,type_code int
	,event_name varchar(20)
	,event_owner_team_id int
	,zone_code char(1)
	,x_coord int
	,y_coord int
	,shot_type varchar(20)
	,goalie_in_id int
	,score_player_id int
	,score_player_total int
	,assist_1_player_id int
	,assist_1_player_total int
	,assist_2_player_id int
	,assist_2_player_total int
	,away_score int
	,home_score int
	,video_link varchar
);
```

```SQL
COPY goals
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\goals_clean.csv'
DELIMITER ','
CSV Header; 
```

**Hits Data Table**
```SQL
CREATE TABLE hits(
	game_id	int 
	,game_period int
 	,event_id int
	,time_in_period varchar(20)
	,time_remaining varchar(20)
	,situation_code int
	,home_def_code varchar(5)
	,type_code int
	,event_name varchar(5)
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
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\hits_clean.csv'
DELIMITER ','
CSV Header; 
```

**MIssed Shots Data Table**
```SQL
CREATE TABLE missed_shots (
	game_id int	
	,game_period int
	,event_id int
	,time_in_period varchar(20)
	,time_remaining varchar(20)
	,situation_code int
	,home_def_code varchar(5)
	,type_code int
	,event_name varchar(20)
	,event_owner_team_id int
	,zone_code char(1)
	,x_coord int
	,y_coord int
	,shot_type varchar(20)
	,shoot_player_id int
	,miss_reason varchar(50)
);
```

```SQL 
COPY missed_shots
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\missed_shots_clean.csv'
DELIMITER ','
CSV Header;
```

**Penalties Data Table**
```SQL
CREATE TABLE penalties(
	game_id	int
	,game_period int
	,event_id int
	,time_in_period varchar(20)
	,time_remaining varchar(20)
	,situation_code int
	,home_def_code varchar(5)
	,type_code int
	,event_name varchar(20)
	,event_owner_team_id int 
	,zone_code char(1)
	,x_coord int 
	,y_coord int
	,penl_code varchar(3)
	,penl_type varchar(50)
	,penl_len int
	,drawn_by_player_id int
	,commit_player_id int
);
```

```SQL
COPY penalties
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\Data\csv\penalties_clean.csv'
DELIMITER ','
CSV Header;
```