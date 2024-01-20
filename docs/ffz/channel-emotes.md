---
title: List FrankerFaceZ channel emotes
botexamples:
  - title: "Get channel emotes"
    url: ":base_url/ffz/emotes/:channel"
---

# List FrankerFaceZ channel emotes

Returns a space-separated list of [FrankerFaceZ](https://www.frankerfacez.com/) emotes available in the channel.  
For users that have the FrankerFaceZ browser extension installed (or use a FrankerFaceZ-enabled chat client), the result will display as emotes in chat.

## Endpoint URL

`{{ base_url }}/ffz/emotes/YOUR_TWITCH_CHANNEL_NAME`

See [example](#example) below for usage with a real Twitch channel name.

## Required URL parameters

- `channel` - The Twitch channel name to retrieve emotes from.

## Example

This example uses the Twitch channel name: `decicus`  
Make sure to replace `decicus` in the URL with the correct Twitch channel name for the channel you wish to get the emotes for.

- Listing channel emotes: [{{ base_url }}/ffz/emotes/decicus]({{ base_url }}/ffz/emotes/decicus)
