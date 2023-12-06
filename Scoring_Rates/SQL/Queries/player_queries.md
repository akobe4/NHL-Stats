**Players with the most blocks per game**
```SQL
SELECT player_name
	  ,team_code AS team
	  ,game_date
	  ,game_num
	  ,player_position
	  ,blocks
FROM players 
ORDER BY blocks DESC
LIMIT 20
```

The limit 20 gets all the players with 8 blocks per game

**Results**

![Alt text](image.png)


**Players with the most total blocks on the season (top 10)**
```SQL
SELECT player_name
	  ,team_code
	  ,sum(blocks) AS total_blocks
FROM players 
GROUP BY player_name, team_code
ORDER BY total_blocks DESC
LIMIT 10
```

**Results**

![Alt text](image-1.png)



