**Table Creation NHL Edge Goalie Stats 2024-2025**

**Goalie 5v5 Details Data Table**

```SQL
CREATE TABLE goalie_5v5_details(
	goalie_id int
	,save_pctg decimal
	,save_pctg_percentile decimal
	,save_pctg_close decimal
	,save_pctg_close_percentile decimal
	,shots int
	,shots_percentile decimal
	,shots_per_60 decimal
	,shots_per_60_percentile decimal
);
```

```SQL
COPY goalie_5v5_details
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Goalies\goalie_5v5_details_clean.csv'
DELIMITER ','
CSV Header;
```

**Goalie Detail Data Table**

```SQL
CREATE TABLE goalie_details (
	 goalie_id int
	,wins int
	,losses int
	,ot_losses int
	,games_played int 
	,save_pctg decimal 
	,gaa decimal 
	,gaa_percentile decimal 
	,goal_support decimal 
	,goal_support_percentile decimal 
	,point_pctg decimal 
	,point_pctg_percentile decimal 
	,goal_diff_per_60 decimal 
	,goal_diff_per_60_percentile decimal
);
```

```SQL
COPY goalie_details
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Goalies\goalie_detail_data.csv'
DELIMITER ','
CSV Header;
```

**Goalie Shot Location Data Table**
```SQL
CREATE TABLE goalie_shot_location(
	goalie_id int 
	,total_shots_against int 
	,total_goals_against int 
	,total_saves int 
	,total_save_pctg decimal
	,behind_the_net_shots_against int 
	,behind_the_net_goals_against int 
	,behind_the_net_saves int 
	,behind_the_net_save_pctg decimal
	,beyond_red_line_shots_against int 
	,beyond_red_line_goals_against int 
	,beyond_red_line_saves int 
	,beyond_red_line_save_pctg decimal
	,center_point_shots_against int 
	,center_point_goals_against int 
	,center_point_saves int 
	,center_point_save_pctg decimal
	,crease_shots_against int 
	,crease_goals_against int 
	,crease_saves int 
	,crease_save_pctg decimal
	,high_slot_shots_against int 
	,high_slot_goals_against int 
	,high_slot_saves int 
	,high_slot_save_pctg decimal
	,l_circle_shots_against int 
	,l_circle_goals_against int 
	,l_circle_saves int 
	,l_circle_save_pctg decimal 
	,l_corner_shots_against int 
	,l_corner_goals_against int 
	,l_corner_saves int 
	,l_corner_save_pctg decimal
	,l_net_side_shots_against int 
	,l_net_side_goals_against int 
	,l_net_side_saves int 
	,l_net_side_save_pctg decimal
	,l_point_shots_against int 
	,l_point_goals_against int 
	,l_point_saves int 
	,l_point_save_pctg decimal
	,low_slot_shots_against int 
	,low_slot_goals_against int 
	,low_slot_saves int 
	,low_slot_save_pctg decimal 
	,off_neu_zone_shots_against int 
	,off_neu_zone_goals_against int 
	,off_neu_zone_saves int 
	,off_neu_zone_save_pctg decimal 
	,outside_l_shots_against int 
	,outside_l_goals_against int 
	,outside_l_saves int 
	,outside_l_save_pctg decimal
	,outside_r_shots_against int 
	,outside_r_goals_against int 
	,outside_r_saves int 
	,outside_r_save_pctg decimal 
	,r_circle_shots_against int 
	,r_circle_goals_against int 
	,r_circle_saves int 
	,r_circle_save_pctg decimal
	,r_corner_shots_against int 
	,r_corner_goals_against int 
	,r_corner_saves int 
	,r_corner_save_pctg decimal
	,r_net_side_shots_against int 
	,r_net_side_goals_against int 
	,r_net_side_saves int 
	,r_net_side_save_pctg decimal
	,r_point_shots_against int 
	,r_point_goals_against int 
	,r_point_saves int 
	,r_point_save_pctg decimal 
);
```

```SQL
COPY goalie_shot_location
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Goalies\goalie_shot_location_data.csv'
DELIMITER ','
CSV Header;
```

**Goalie Info Data Table**
```SQL
CREATE TABLE goalie_info (
	player_id int 
	,first_name varchar(40)
	,last_name varchar(40)
	,birth_date date 
	,current_team_id int
	,shoots_catches char(1)
	,height_inches int
	,height_cm int 
	,weight_lbs int 
	,weight_kg int 
	,birth_city varchar(50)
	,birth_state_prov varchar(50)
	,birth_country char(3)
	,draft_year int
	,draft_team char(3)
	,draft_round int 
	,draft_pick_in_round int 
	,draft_overall_pick int
	,hero_image varchar
);
```

```SQL
COPY goalie_info
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Goalies\player_info_goalies_clean.csv'
DELIMITER ','
CSV Header;
```

**Save Percentage Details Data Table**
```SQL
CREATE TABLE save_percentage_details(
	goalie_id int 
	,games_above_900 int 
	,games_above_900_percentile decimal
	,pctg_games_above_900 decimal 
	,pctg_games_above_900_percentile decimal
);
```

```SQL
COPY save_percentage_details
FROM
'C:\Users\Alex\Documents\NHL-Stats\2025-2026\nhl_edge\Data\csv\Goalies\save_percentage_details.csv'
DELIMITER ','
CSV Header;
```
