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


**Query to get player names and ID's**
```SQL
SELECT player_id
	,first_name ||' '|| last_name AS player_name
	,birth_country
FROM roster
```

## Projected Rosters 
Projected rosters for each team was taken from daily faceoff's NHL line combinations.

**Query to add a table with projected roster for the 2024-2025 season**
```SQL
CREATE TABLE projected_roster_2425(
		player_name varchar
	   ,player_id int
	   ,team char(3)
);

COPY projected_roster_2425
FROM 'C:\Users\akobe\OneDrive\Desktop\Lighthouse\After\NHL-Stats\Reg_Season_23_24\SQL\Comparison\Results\projected_roster_2425.csv'
DELIMITER ','
CSV Header;
```

**Query to get projected skater team data**
```SQL
SELECT p.team AS team_name
	,SUM(s.goals) AS total_goals
	,SUM(s.pp_goals) AS total_pp_goals
	,SUM(s.sh_goals) AS total_sh_goals
	,SUM(s.shots) AS total_shots
	,SUM(s.pim) AS total_pims
FROM projected_roster_2425 p
LEFT JOIN skater_game_data s ON p.player_id = s.player_id
GROUP BY team_name
ORDER BY team_name;
```

**Query for projected team takeaways**
```SQL
SELECT p.team AS team_name
	,COUNT(t.take_player_id) AS total_takeaways
FROM projected_roster_2425 p
LEFT JOIN takeaways t ON p.player_id = take_player_id
GROUP BY team_name
ORDER BY team_name;
```

**Query for projected goalie team data**
```SQl
SELECT p.team
	,SUM(g.shots_against) AS total_shots_against
	,SUM(g.goals_against) AS total_goals_against
	,ROUND(AVG(g.save_perc), 3) AS avg_save_perc
	,SUM(g.goals) AS total_goals
	,SUM(g.pim) AS total_pim
FROM projected_roster_2425 p
LEFT JOIN goalie_game_data g ON p.player_id = g.player_id
GROUP BY team
ORDER BY team;
```