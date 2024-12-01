---
title: "Twitch user's avatar URL"
botexamples:
  - title: "Get avatar URL of the current avatar for Twitch user specified after the command"
    url: ":base_url/twitch/avatar/:user"
---

# Twitch user's avatar URL

Returns the avatar URL of a Twitch user.

**Note**: This endpoint is cached for up to 30 minutes. Avatar updates may not be immediately reflected.

## Endpoint URL

`{{ base_url }}/twitch/avatar/TWITCH_USERNAME_HERE`

See [examples](#examples) below for usage with an actual Twitch username.

## Required URL parameters

- `user` - **Required** - Twitch username to get the avatar for.

## Examples

- Decicus' current avatar on Twitch: [{{ base_url }}/twitch/avatar/decicus]({{ base_url }}/twitch/avatar/decicus)