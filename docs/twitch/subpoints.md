---
title: "Subpoints - Subscriber points for a Twitch channel"
botexamples:
  - title: "Get the subscriber points for a channel"
    url: ":base_url/twitch/subpoints/:channel"
cached: true
---

# Subpoints - Subscriber points for a Twitch channel

Retrieves the amount of subscriber points for the specified Twitch channel.

!!! warning "Requires channel owner to have authorized DecAPI for subscriber access"
    The channel owner must authorize DecAPI to access their subscriber data in order for this endpoint to return subscriber information.

    If the channel owner already uses other DecAPI Twitch endpoints with subscriber data access, such as _[random subscriber](random-sub.md)_ or _[subcount](subcount.md)_, then no further action is needed.

    If you are the channel owner, you can authorize DecAPI via this link: [Authorize DecAPI for Twitch Subscriber Access]({{ base_url }}/auth/twitch?redirect=subpoints&scopes=channel:read:subscriptions+user:read:email)

## Endpoint URL

`{{ base_url }}/twitch/subpoints/CHANNEL_USERNAME_HERE`

## Required URL parameters

- `channel` - **Required** - Twitch channel to retrieve the subscriber points for.

## Notes

- As of October 2nd, 2021 the subscriber points value is now accurately retrieved from the Twitch API. The legacy `subtract` adjustment no longer applies and will be ignored.

## Examples

- Decicus' subscriber points: [{{ base_url }}/twitch/subpoints/decicus]({{ base_url }}/twitch/subpoints/decicus)