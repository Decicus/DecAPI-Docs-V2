---
title: DayZ map search via iZurvive
botexamples:
  - title: "Allow users to search for a Chernarus map location"
    url: ":base_url/dayz/izurvive?search=:query"
---

# DayZ map search via iZurvive

_This endpoint has not been updated in quite some time._  
_While most existing locations in the API should still work fine, any new locations added to the map in later times may not be available in the search results._  
_It also currently only supports Chernarus+ (the original map), even if iZurvive supports multiple._

Searches for locations based on the search query string, and returns a location name together with a URL to the location on [iZurvive](https://www.izurvive.com/).

You can also visit the URL [{{ base_url }}/dayz/izurvive?list]({{ base_url }}/dayz/izurvive?list) to get a list of all locations available in this API endpoint.

## Endpoint URL

`{{ base_url }}/dayz/izurvive?search=Zeleno`

### Query parameters

- `search` - **Required** - The search query string to search for. This parameter is *case-insensitive*.

## Example

- Find the first location that matches the search text `Zeleno`: [{{ base_url }}/dayz/izurvive?search=Zeleno]({{ base_url }}/dayz/izurvive?search=Zeleno)
