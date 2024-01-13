---
title: Query a server's current player count (PC)
botexamples:
  - title: "Query player count for a specific server"
    url: ":base_url/dayz/players?ip=127.0.0.1&port=2302&query=27016"
---

# Query a server's current player count (PC)

Returns the current player count for a specific server.  
For instance, a server with currently _4 players_ out of a maximum of _60 players_ will return: `4/60`

**Note**: This _may_ support servers for other games using the Steam query protocol, but has only really been tested with DayZ servers. Your mileage may vary.

## Endpoint URL

`{{ base_url }}/dayz/players?ip=127.0.0.1&port=2302&query=27016`

### Query parameters

If you're not sure what the query port is for your server, you can use my [DayZ server search](https://cactus.tools/dayz/servers) website and use the "Query port" column to figure it out.  

- `ip` - **Required**. The IP address of the server.
- `port` - **Required**. The game port of the server.
- `query` - Semi-optional. The query port of the server.
    - If the query port is not specified, it will default to "game port plus 24714". For example: `2302 + 24714 = 27016`
    - However, if this does not work for your server, you can specify the query port manually. A valid query port is necessary to get the player count.

## Example

- Current player count of `ZERO DEER ISLE | 1PP | NO BASES | VANILLA+`: [{{ base_url }}/dayz/players?ip=51.89.155.180&port=2302&query=27016]({{ base_url }}/dayz/players?ip=51.89.155.180&port=2302&query=27016)
