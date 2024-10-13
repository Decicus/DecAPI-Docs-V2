---
title: Get the global player count for a Steam game
botexamples:
  - title: "Total player count for DayZ on Steam"
    url: ":base_url/steam/global-players?appid=221100"
---

# Get the global player count for a Steam game

Returns the current global player count for a specified Steam game.  

The "app ID" of a Steam game can be found in the URL of the game's store page.

For example:

- Counter-Strike 2 has the app ID `730`: [https://store.steampowered.com/app/730/CounterStrike_2/](https://store.steampowered.com/app/730/CounterStrike_2/)
- DayZ has the app ID `221100`: [https://store.steampowered.com/app/221100/DayZ/](https://store.steampowered.com/app/221100/DayZ/)
- Half-Life 2 has the app ID `220`: [https://store.steampowered.com/app/220/HalfLife_2/](https://store.steampowered.com/app/220/HalfLife_2/)

## Endpoint URL

`{{ base_url }}/steam/global-players?appid=PUT_APPID_FOR_GAME_HERE`

See [example](#example) below for usage with an actual Steam game.

## Query parameters

- `appId` - **Required** - The Steam AppID of the game to get the player count for.

## Example

- Total player count for DayZ on Steam: [{{ base_url }}/steam/global-players?appid=221100]({{ base_url }}/steam/global-players?appid=221100)
