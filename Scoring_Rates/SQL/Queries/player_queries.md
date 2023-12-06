Players with the most blocks per game
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

Results
player_name	team	game_date	game_num	player_position	blocks
Ivan Provorov	PHI	2022-10-13	2022020012	D	10
David Savard	MTL	2022-10-12	2022020007	D	9
Ivan Provorov	PHI	2022-10-27	2022020112	D	9
Alec Martinez	VGK	2022-11-16	2022020256	D	9
Connor Clifton	BOS	2023-01-09	2022020644	D	9
Alexander Romanov	NYI	2022-10-13	2022020014	D	9
Adam Larsson	SEA	2022-11-02	2022020155	D	8
Alec Martinez	VGK	2022-10-25	2022020096	D	8
Alex Goligoski	MIN	2022-12-04	2022020393	D	8
Erik Gudbranson	CBJ	2022-12-20	2022020502	D	8
Ivan Provorov	PHI	2023-01-22	2022020735	D	8
Victor Hedman	TBL	2023-02-26	2022020942	D	8
Mark Giordano	TOR	2022-11-16	2022020251	D	8
Joel Edmundson	MTL	2022-11-05	2022020184	D	8
Nikita Zadorov	CGY	2022-11-24	2022020305	D	8
Andrew Peeke	CBJ	2023-02-12	2022020840	D	8



