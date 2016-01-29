# Madden-Ultimate-Team-API

A few API Endpoints that EA uses for their own MUT Web App. 

###Work In Progress
I''m currently still working on documenting all the params and endpoints. Feel free to help out! 

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

**team**: String || 3 Charecter Team Abbreviation

###Example Callback

```json
{
"count":25,
"type":"CardList",
"items":
        [
        {
        "acc":93,
        "age":23,
        "agi":94,
        "awr":76,
        "bcv":67,
        "bshd":77,
        "cary":70,
        "cint":74,
        "ctch":78,
        "elus":66,
        "fmov":58,
        "height":73,
        "ht":"6' 1\"",
        "hp":92,
        "impb":45,
        "inj":92,
        "jerseyNumber":33,
        "jkm":58,
        "jmp":91,
        "kacc":13,
        "kpow":14,
        "mcov":76,
        "pac":6,
        "pbft":45,
        "pbk":45,
        "pbst":45,
        "pmov":67,
        "prec":74,
        "pres":75,
        "pur":81,
        "rbft":45,
        "rbk":45,
        "rbst":45,
        "ret":45,
        "rls":35,
        "rrun":25,
        "run":6,
        "scat":77,
        "sfa":61,
        "spd":92,
        "spm":52,
        "sta":89,
        "str":71,
        "tckl":80,
        "tdep":6,
        "tgh":76,
        "tacc":19,
        "tmid":6,
        "tpow":15,
        "trck":58,
        "tsht":6,
        "weight":205,
        "zcov":86,
        "ovr":86,
        "category":"defense",
        "id":12227,
        "value":1,
        "tier":"ELITE",
        "type":"PLAYER",
        "discardValue":360,
        "state":"INVALID",
        "tradeFee":0,
        "auctionFee":0,
        "sequenceNumber":0,
        "limitedEditionCount":0,
        "limitedEditionAvailable":0,
        "injuryLength":null,
        "contractLength":18,
        "injuryType":null,
        "isTradeable":true,
        "isContractExtendable":true,
        "isAuctionable":true,
        "tierColor":"#d30d17",
        "dataType":"PlayerCard",
        "instanceId":12227,
        "cardImageUrl":"\/madden-nfl\/ultimate-team\/web-app\/data\/1\/asset\/netres\/x%252FJpa3utOZgB9J6Z5dHhhEE3JTP4cS%252Ba1YqEqJ01iQI%253D",
        "cardImageId":"32,1|card-00001647",
        "description":"Team of the Week: Some of the best players from each week of the NFL season.",
        "longDescription":"Conference: Allowed only 1 catch. Totaled 1 tackle, 2 pass break ups, and 1 interception.",
        "program":{
          "name":"Team of the Week",
          "stampImage":"|stmp-00000015","id":21,"color":65322,"hexColor":"#00ff2a","description":""
          },
        "teamInfo":{
          "abbr":"CAR",
          "name":"Carolina Panthers",
          "logoRight":"http:\/\/madden-assets-cdn.pulse.ea.com\/madden16\/logos\/20\/220-right.png",
          "logoLeft":"http:\/\/madden-assets-cdn.pulse.ea.com\/madden16\/logos\/20\/220-left.png","id":21,
          "logoRightGradient":"http:\/\/madden-assets-cdn.pulse.ea.com\/madden16\/logos\/20\/220-right-gradient.png",
          "logoLeftGradient":"http:\/\/madden-assets-cdn.pulse.ea.com\/madden16\/logos\/20\/220-left-gradient.png"},
          "position":"FS",
          "lastName":"Boston",
          "firstName":"Tre",
          "name":"Tre Boston",
          "cardBack":[
            "ht",
            "spd",
            "agi",
            "awr",
            "tckl",
            "mcov",
            "zcov",
            "pres",
            "prec"
            ],
          "chemistry":{
            "manDefense":9
          },
          "portrait":{
            "id":6352,
            "imgUrlSmall":"http:\/\/madden-assets-cdn.pulse.ea.com\/madden16\/portraits\/small\/6352.png",
            "imgUrlLarge":"http:\/\/madden-assets-cdn.pulse.ea.com\/madden16\/portraits\/large\/6352.png"
          }
    }
]
```

## Auctions

Find recent auctions for a specific player. 

Example Call:
```http
http://www.easports.com/madden-nfl/ultimate-team/web-app/data/1/auctions/6814
```
### Parameters 

**instanceId**: Instance ID from the players object || Added behind the url
