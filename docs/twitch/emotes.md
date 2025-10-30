---
title: "Emotes - Get emotes for a Twitch channel"
botexamples:
  - title: "Get all emotes for a channel (bits, subscriber and follower emotes)"
    url: ":base_url/twitch/emotes/:channel"
  - title: "Get only bits and follower emotes"
    url: ":base_url/twitch/emotes/:channel?types=bitstier,follower"
cached: true
---

# Emotes - Get emotes for a Twitch channel

Gets the available emotes for the specified Twitch channel, such as bits emotes, subscriber emotes and follower emotes.

Optional filtering can be done via the `types` query parameter.

!!! note ":fontawesome-brands-twitch: Only Twitch emotes"
    This endpoint only retrieves Twitch-native emotes. It does not include third-party emotes from services such as BetterTTV, FrankerFaceZ or 7TV.
    
    For BetterTTV emotes, you can use the _[BetterTTV emotes](/bttv/channel-emotes/)_ endpoint.

    Likewise, for FrankerFaceZ emotes, you can use the _[FrankerFaceZ emotes](/ffz/channel-emotes/)_ endpoint.

    7TV is currently not supported by DecAPI.

## Endpoint URL

`{{ base_url }}/twitch/emotes/CHANNEL_USERNAME_HERE`

## Required URL parameters

- `channel` - **Required** - Twitch channel to retrieve subscriber emotes for.

## Query parameters

- `types` - Optional. Filter by emote "category" (type). Comma-separated list of the following values:
    - `bitstier` - Bits emotes
    - `subscriptions` - Subscriber emotes
    - `follower` - Follower emotes
    - The default (not specified) is to return all emotes of every type.

## Examples

- All of LIRIK's emotes (all types): [{{ base_url }}/twitch/emotes/lirik]({{ base_url }}/twitch/emotes/lirik)
- Decicus' subscriber emotes: [{{ base_url }}/twitch/emotes/decicus?types=subscriptions]({{ base_url }}/twitch/emotes/decicus?types=subscriptions)
- Halifax's follower emotes: [{{ base_url }}/twitch/emotes/halifax?types=follower]({{ base_url }}/twitch/emotes/halifax?types=follower)
- Katie's bits and subscriber emotes (no follower emotes): [{{ base_url }}/twitch/emotes/katie?types=bitstier,subscriptions]({{ base_url }}/twitch/emotes/katie?types=bitstier,subscriptions)