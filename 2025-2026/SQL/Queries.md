**Random Queries**

**Most Popular Names in the NHL**
```SQL
SELECT first_name
	,COUNT(first_name) as Total
FROM player_info
GROUP BY first_name
ORDER BY Total DESC;
```

* does not account for different variations or spellings of names (Alex and Alexander for example show up as different names)

![alt text](image.png)


