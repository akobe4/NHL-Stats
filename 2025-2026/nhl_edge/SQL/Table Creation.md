**Table Creation NHL Edge Stats 2024-2025**

**Max Shot Speed Data Table**
```SQL
CREATE TABLE max_shot_speed (
	skater_id int
	,shooter_team char(3)	
	,max_speed_imp decimal 
	,max_speed_met decimal
	,max_speed_percentile decimal
	,game_date date 
	,away_team char(3)
	,home_team char(3)
	,away_team_score int	
	,home_team_score int
	,game_period int
	,time_in_period varchar(20)
);
```

```SQL
COPY max_shot_speed
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Skaters\max_shot_speed.csv'
DELIMITER ','
CSV Header;
```

**Skater Info Data Table**
```SQL
CREATE TABLE skater_info (
	player_id int	
	,first_name varchar(40)
	,last_name varchar(40)
	,birth_date date
	,is_active boolean
	,current_team_id int
	,skater_position	char(1)
	,shoots_catches char(1)
	,height_inches int
	,height_cm int
	,weight_lbs int
	,weight_kg int
	,birth_city varchar(50)
	,birth_state_prov varchar(50)	
	,birth_country char(3)
	,draft_year	int
	,draft_team char(3)
	,draft_round int
	,draft_pick_in_round int
	,draft_overall_pick int
	,hero_image varchar
);
```

```SQL
COPY skater_info
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Skaters\player_info_skaters_clean.csv'
DELIMITER ','
CSV Header;
```

**Teams Data Table**
```SQL
CREATE TABLE teams(
	team_id int
	,team char(3)
);
```

```SQL
COPY teams
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Skaters\teams.csv'
DELIMITER ','
CSV Header;
```


**Max Skating Speed Burst Data Table**
```SQL
CREATE TABLE max_skating_speed_burst(
	skater_id int
	,skater_team char(3)	
	,max_speed_imp	decimal
	,max_speed_met decimal
	,max_speed_percentile decimal
	,game_date date
	,away_team char(3)
	,home_team char(3)
	,away_team_score int
	,home_team_score int
	,game_period int
	,time_in_period varchar(20)
);
```

```SQL
COPY max_skating_speed_burst
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Skaters\max_skating_speed_burst.csv'
DELIMITER ','
CSV Header;
```

**Shot Location Data Table**
```SQl
CREATE TABLE shot_location(
	skater_id int
	,behind_net_sog int
	,behind_net_goals int
	,beyond_red_line_sog int
	,beyond_red_line_goals int
	,center_point_sog int
	,center_point_goals int
	,crease_sog int
	,crease_goals int
	,high_slot_sog int
	,high_slot_goals int
	,l_circle_sog int
	,l_circle_goals int
	,l_corner_sog int
	,l_corner_goals int
	,l_net_side_sog int
	,l_net_side_goals int
	,l_point_sog int
	,l_point_goals int
	,low_slot_sog int
	,low_slot_goals int
	,o_neutral_zone_sog int
	,o_neutral_zone_goals int
	,outside_l_sog int
	,outside_l_goals int
	,outside_r_sog int
	,outside_r_goals int
	,r_circle_sog int
	,r_circle_goals int
	,r_corner_sog int
	,r_corner_goals int
	,r_net_side_sog int
	,r_net_side_goals int
	,r_point_sog int
	,r_point_goals int
);
```

```SQL
COPY shot_location
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Skaters\shot_location_data.csv'
DELIMITER ','
CSV Header;
```

**Shot Speed Data Table**
```SQL
CREATE TABLE shot_speed(
	first_name varchar(30)
	,last_name varchar(30)
	,max_speed_imp decimal
	,max_speed_met decimal
	,avg_speed_imp decimal
	,avg_speed_met decimal
	,shots_over_100 int
	,shots_90_to_100 int
	,shots_80_to_90 int
	,shots_70_to_80 int
);
```

```SQL
COPY shot_speed
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Skaters\shot_speed_data.csv'
DELIMITER ','
CSV Header;
```

**Skating Speed Data Table**
```SQL
CREATE TABLE skating_speed(
	skater_id int
	,max_speed_imp decimal
	,max_speed_met decimal
	,max_speed_percentile decimal
	,bursts_over_22 int
	,bursts_over_22_percentile decimal
	,bursts_20_to_22 int
	,bursts_20_to_22_percentile decimal
	,bursts_18_to_20 int
	,bursts_18_to_20_percentile decimal
);
```

```SQL
COPY skating_speed
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Skaters\skating_speed_data.csv'
DELIMITER ','
CSV Header;
```

**Zone Start Data Table**
```SQL
CREATE TABLE zone_start(
	skater_id int
	,o_zone_pctg decimal
	,o_zone_pctg_percentile decimal
	,n_zone_pctg decimal
	,n_zone_pctg_percentile decimal
	,d_zone_pctg decimal
	,d_zone_pctg_percentile decimal
);
```

```
COPY zone_start
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Skaters\zone_start_data.csv'
DELIMITER ','
CSV Header;
```