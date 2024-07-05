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



