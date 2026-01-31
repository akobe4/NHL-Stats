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

**3.Pulling goal info**
Pulling the goal info required for graphing goal locations of the league's top 5 scorers

```SQl
SELECT g.game_id
	  ,gs.h_team_id
	  ,gs.a_team_id
	  ,g.game_period
	  ,g.time_remaining
	  ,g.home_def_code
	  ,g.event_owner_team_id
	  ,g.x_coord
	  ,g.y_coord
	  ,g.shot_type
	  ,g.score_player_id
FROM goals g
LEFT JOIN game_story gs ON g.game_id = gs.game_num
WHERE g.score_player_id IN (8477934, 8477939, 8471214, 8479420, 8477956);
```