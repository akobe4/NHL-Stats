**Total Season Penalty Minutes by Team**

total penalty minutes taken by each team in the season. Listed most to least penalties. 

```SQL
SELECT te.team
	  ,sum(pe.penl_len) AS total_pen_min
FROM penalties pe
LEFT JOIN teams te ON pe.event_owner_team_id = te.team_id
GROUP BY te.team
ORDER BY total_pen_min DESC;
```

Output

![alt text](image.png)



**Empty Net Goals on the Season**
total number of empty net goals scored by player

```SQL 
SELECT r.first_name || ' ' || r.last_name AS player_name
	,COUNT(g.score_player_id) AS no_of_goals
FROM goals g 
LEFT JOIN roster r ON g.score_player_id = r.player_id
WHERE goalie_in_id IS NULL 
GROUP BY player_name
ORDER BY no_of_goals DESC
;
```

Output 

![alt text](image-1.png)


