This worksheet will look at team totals from the 2023-2024 season and compare to the stat totals for the new projected team roster. Team totals will just be the total stats from the 2023-2024 season. The projected team totals will be the sum of the individual stats from the 2023-2024 season. 
 

## Queries 

**Query to get skater team data**
```SQL
SELECT player_team AS team
	,SUM(goals) AS total_goals
	,SUM(pp_goals) AS total_pp_goals
	,SUM(sh_goals) AS total_sh_goals
	,SUM(shots) AS total_shots
	,SUM(pim) AS total_pim
FROM skater_game_data 
GROUP BY player_team
ORDER BY player_team;
```


**Query to get goalie game data**
```SQL
SELECT player_team AS team
	,SUM(shots_against) AS total_shots_against
	,SUM(goals_against) AS total_goals_against
	,ROUND(AVG(save_perc), 3) AS avg_save_perc
	,SUM(goals) AS total_goals
	,SUM(pim) AS total_pim
FROM goalie_game_data
GROUP BY team
ORDER BY team;
```


**Query for takeaways**
```SQL
SELECT te.team AS team
	,COUNT(ta.take_player_id) AS total_takeaways
FROM takeaways ta 
LEFT JOIN teams te ON ta.event_owner_team_id = te.team_id
GROUP BY team
ORDER BY team;
```
