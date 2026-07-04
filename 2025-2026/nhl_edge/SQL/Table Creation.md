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



