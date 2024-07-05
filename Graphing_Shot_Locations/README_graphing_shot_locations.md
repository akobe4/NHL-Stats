**Graphing Shot Locations**
Game 2023010071 - preseason game MTL @ TOR

- game data was pulled from the NHL API: https://statsapi.web.nhl.com/api/v1/game/2023010071/feed/live. 
- dataframe was created including: team_id, period, event_index, event_id, event_type, x_coor, y_coor, rinkside 
- after review of the data it was determined that for blocked shots the team recorded was the blocking team. For the purposes of this we want the team to be the shooting team - this was updated in the data 
- teammate blocks were also recorded as the blocking team, and as we  had just changed this we switched the team back to the actual shooting team for the 3 teammate blocks (event_id's 84, 112 and 141)
-teammate blocks were determined by reviewing the play-by-play
- when graphing shots there was one blocked shot (event_id 242) that seemed to have been taken from the defensive zone – video was reviewed and it was determined that the play-by-play was incorrectly recorded as a MTL shot blocked by TOR, when it should have been a TOR shot blocked by MTL. Team id was updated.
- teams switch ends after each period and shoot at both nets, coordinate data was transformed so all shots were on the same net 
- rink image link: https://www.istockphoto.com/vector/hockey-rink-hockey-field-ice-arena-for-nhl-and-winter-sport-game-ice-pitch-in-top-gm1353575675-428636223?clarity=false 
- the following link is mentioned in the Notebook, but is where the code came from for graphing on the rink: https://towardsdatascience.com/nhl-analytics-with-python-6390c5d3206d