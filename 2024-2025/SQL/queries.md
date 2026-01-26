**1. Total Hits by Game**
Total hits by game, sorted in descending order 

```SQL 
SELECT game_num
	,game_date
	,a_team_code
	,h_team_code
	,(a_hits + h_hits) AS total_hits
FROM game_story
ORDER BY total_hits DESC;
```

**2. Player Id's**
Pulling the player id's for the league's top 5 goal scorers. 

```SQL 
SELECT player_id
	,first_name
	,last_name
FROM player_info
WHERE last_name IN ('Draisaitl', 'Nylander', 'Ovechkin', 'Thompson', 'Pastrnak');
```

