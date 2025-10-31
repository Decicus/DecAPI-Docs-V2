---
title: "Random Subcriber - Get random subscriber from a Twitch channel"
botexamples:
  - title: "Get a random subscriber (default: 1 username)"
    url: ":base_url/twitch/random_sub/:channel"
  - title: "Get 3 random subscriber names"
    url: ":base_url/twitch/random_sub/:channel?count=3"
  - title: "Get 2 random subscriber _usernames_ (not display names), separated by `||`"
    url: ":base_url/twitch/random_sub/:channel?count=2&field=user_login&separator=||"
cached: false
---

# Random Subcriber - Get random subscriber from a Twitch channel

Retrieves one or more random subscribers for the specified Twitch channel.

!!! warning "Requires channel owner to have authorized DecAPI for subscriber access"
    The channel owner must authorize DecAPI to access their subscriber data in order for this endpoint to return subscriber information.

    If the channel owner already uses other DecAPI Twitch endpoints with subscriber data access, such as _[subcount](subcount.md)_ or _[subpoints](subpoints.md)_, then no further action is needed.

    If you are the channel owner, you can authorize DecAPI via this link: [Authorize DecAPI for Twitch Subscriber Access]({{ base_url }}/auth/twitch?redirect=randomsub&scopes=channel:read:subscriptions+user:read:email)

## Endpoint URL

`{{ base_url }}/twitch/random_sub/CHANNEL_USERNAME_HERE`

## Required URL parameters

- `channel` - **Required** - Twitch channel to pick a random subscriber from.

## Query parameters

- `count` - Optional - The number of subscribers to retrieve. Default: `1`. (int)
- `field` - Optional - Which field from the subscriber object to return (see Twitch API for available fields)
    - Default: `user_name`, otherwise known as the "Display name" (e.g. username with capitalization, or [localized display names](https://help.twitch.tv/s/article/display-names-on-twitch?language=en_US#localized)).
    - If you want the actual Twitch username (all lowercase, no special characters), use `user_login`.
- `separator` - Optional - Characters to separate multiple values with. Default: `, `

## Examples

- Get one random subscriber display name from Ninja's channel: [{{ base_url }}/twitch/random_sub/ninja]({{ base_url }}/twitch/random_sub/ninja)
- Get 3 random subscriber display name from Ninja's channel: [{{ base_url }}/twitch/random_sub/ninja?count=3]({{ base_url }}/twitch/random_sub/ninja?count=3)
- Get 2 random subscriber _usernames_ (not display names), separated by `||`, from Ninja's channel: [{{ base_url }}/twitch/random_sub/ninja?count=2&field=user_login&separator=||]({{ base_url }}/twitch/random_sub/ninja?count=2&field=user_login&separator=||)