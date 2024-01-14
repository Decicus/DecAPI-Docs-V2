# Rate limits

For the _most part_ requests to DecAPI are not rate limited. However, there are a few exceptions to prevent abuse of the service.  
If your application requires more requests than what is listed below, I suggest you look into using the API of the service directly instead.  
Rate limits are applied based on the IP address the request originates from.

## Currently rate limited routes

### :fontawesome-brands-twitch: Twitch

Twitch endpoints are rate limited to 100 requests per 60 seconds.  
[Official Twitch API documentation][Twitch-API-Docs]

### :fontawesome-brands-steam: Steam

Steam endpoints are rate limited to 15 requests per 60 seconds.  
[Web API documentation for the official Steam API][Steam-API]

## Bypassing rate limits

Most people will be fine with the few (and relatively generous) rate limits I have applied.  
However, if you notice you're getting rate limited relatively often, you have the following options:

- [:fontawesome-brands-twitch: Use the official Twitch API directly][Twitch-API-Docs]
    - Keep in mind that Twitch's official API also [has their own rate limits](https://dev.twitch.tv/docs/api/guide/#twitch-rate-limits)
- [:fontawesome-brands-steam: Use the official Steam web APIs directly][Steam-API]
- [:fontawesome-brands-github: Host DecAPI yourself and configure your own rate limits](https://github.com/Decicus/DecAPI#setup)

[Steam-API]: https://developer.valvesoftware.com/wiki/Steam_Web_API
[Twitch-API-Docs]: https://dev.twitch.tv/docs