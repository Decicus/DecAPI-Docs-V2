---
title: "Follow count - Get the total number of followers of a Twitch channel"
botexamples:
  - title: "Get total number of followers of a Twitch channel"
    url: ":base_url/twitch/followcount/:channel"
cached: true
---

# Follow count - Get the total number of followers of a Twitch channel

Gives you the total number of followers of a specified Twitch channel.

## Endpoint URL

`{{ base_url }}/twitch/followcount/TWITCH_CHANNEL_USERNAME_HERE`

See [examples](#examples) below for usage with an actual Twitch channel.

## Required URL parameters

- `:channel` - The username of the Twitch channel you want to get the follower count for.

## Example usage

- Get the total number of followers of the Twitch channel _Decicus_: [{{ base_url }}/twitch/followcount/decicus]({{ base_url }}/twitch/followcount/decicus)