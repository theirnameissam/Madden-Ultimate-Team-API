# Madden-Ultimate-Team-API

A view API Endpoints that EA uses for their own MUT Web App. 

###Work In Progress
I''m currently still working on documenting on the params and endpoints. Feel free to help out! 

## Player 

The most interesting API endpoint which seems to be used for everything is "Player"; Player returns 25 players. 
Example Call: 
```http
http://www.easports.com/madden-nfl/ultimate-team/web-app/data/1/cards/player?sort=ovr&name=AUSTIN
```
### Parameters 
**sort**: 'ovr', 'pos', 'spd', 'awr', 'agi', 'str', 'new' || Or any other attribute 

**name**: String || Player Name

**pos**: String || Any Valid Position 

**team**: String || 3 Charecter Team Abreviation
