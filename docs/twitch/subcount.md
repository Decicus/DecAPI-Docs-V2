---
title: "Subcount - Subscriber count for a Twitch channel"
botexamples:
  - title: "Get the subscriber count for a channel"
    url: ":base_url/twitch/subcount/:channel"
  - title: "Get the subscriber count with a subtraction applied"
    url: ":base_url/twitch/subcount/:channel?subtract=2"
cached: true
---

# Subcount - Subscriber count for a Twitch channel

Retrieves the current subscriber count for the specified Twitch channel.

!!! warning "Requires channel owner to have authorized DecAPI for subscriber access"
    The channel owner must authorize DecAPI to access their subscriber data in order for this endpoint to return subscriber information.

    If the channel owner already uses other DecAPI Twitch endpoints with subscriber data access, such as _[random subscriber](random-sub.md)_ or _[subpoints](subpoints.md)_, then no further action is needed.

    If you are the channel owner, you can authorize DecAPI via this link: [Authorize DecAPI for Twitch Subscriber Access]({{ base_url }}/auth/twitch?redirect=randomsub&scopes=channel:read:subscriptions+user:read:email)

## Endpoint URL

`{{ base_url }}/twitch/subcount/CHANNEL_USERNAME_HERE`

## Required URL parameters

- `channel` - **Required** - Twitch channel to retrieve the subscriber count for.

## Query parameters

- `subtract` - Optional
    - Subtracts the specified integer from the returned subscriber count. Example: if you have 102 subs and set `subtract=2`, the endpoint will return `100`.
    - There's effectively no minimum or maximum, so with a high enough subtraction you may get negative numbers.

## Notes

- As of October 2nd, 2021 the subscriber count no longer includes lifetime bot subscriptions or the broadcaster's own subscription. You may need to adjust (or remove) the `subtract` parameter if it was previously used to adjust it for these factors.

## Examples

- Decicus' subscriber count: [{{ base_url }}/twitch/subcount/decicus]({{ base_url }}/twitch/subcount/decicus)
- Decicus' subscriber count, subtracting 2 from the total: [{{ base_url }}/twitch/subcount/decicus?subtract=2]({{ base_url }}/twitch/subcount/decicus?subtract=2)