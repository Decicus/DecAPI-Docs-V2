---
title: "Subscriber emotes - Subscriber emotes for a Twitch channel"
botexamples:
  - title: "Get subscriber emotes for a channel"
    url: ":base_url/twitch/subscriber_emotes/:channel"
cached: true
---

# Subscriber emotes - Subscriber emotes for a Twitch channel

Retrieves the subscriber emotes for the specified channel and lists them (space-separated).

Depending on your bot's subscription status and subscription tier, emotes may either be listed as plain text, the actual emotes or a mix of both.

## Endpoint URL

`{{ base_url }}/twitch/subscriber_emotes/CHANNEL_USERNAME_HERE`

## Required URL parameters

- `channel` - **Required** - Twitch channel to retrieve subscriber emotes for.

## Query parameters

- `tiers` - Optional (only available in JSON responses) - When specified, emotes are split into their respective subscriber tiers.

## Notes

- JSON results are supported, pass the header `Accept: application/json` to receive JSON output.

## Examples

- Decicus' subscriber emotes: [{{ base_url }}/twitch/subscriber_emotes/decicus]({{ base_url }}/twitch/subscriber_emotes/decicus)
- LIRIK's subscriber emotes with tiers in JSON: [{{ base_url }}/twitch/subscriber_emotes/lirik?tiers=1]({{ base_url }}/twitch/subscriber_emotes/lirik?tiers=1)
    - Only works when passing the `Accept: application/json` header, example with cURL:  
      `curl -H "Accept: application/json" "{{ base_url }}/twitch/subscriber_emotes/lirik?tiers=1"`