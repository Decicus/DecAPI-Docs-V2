---
title: List BetterTTV channel emotes
botexamples:
  - title: "All types of emotes (default)"
    url: ":base_url/bttv/emotes/:channel"
  - title: "Only animated GIF emotes"
    url: ":base_url/bttv/emotes/:channel?types=gif"
  - title: "Only static PNG emotes"
    url: ":base_url/bttv/emotes/:channel?types=png"
---

# List BetterTTV channel emotes

Returns a space-separated list of [BetterTTV](https://betterttv.com/) emotes available in the channel.  
For users that have the BetterTTV browser extension installed (or use a BetterTTV-enabled chat client), the result will display as emotes in chat.

## Endpoint URL

`{{ base_url }}/bttv/emotes/:channel`

## Required URL parameters

- `channel` - The Twitch channel name to retrieve emotes from.

### Query parameters

- `types` - **Optional** - A comma-separated list of types to return. Your options are:
    - `all` - **Default if not specified**. Returns all types of emotes.
    - `gif` - Returns only animated GIF emotes.
    - `png` - Returns only static PNG image emotes.

## Example

Examples use the Twitch channel name: `decicus`

- Example with all types of emotes (default): [{{ base_url }}/bttv/emotes/decicus]({{ base_url }}/bttv/emotes/decicus)
- Example with only getting animated GIF emotes: [{{ base_url }}/bttv/emotes/decicus?types=gif]({{ base_url }}/bttv/emotes/decicus?types=gif)
- Example with only getting static PNG emotes: [{{ base_url }}/bttv/emotes/decicus?types=png]({{ base_url }}/bttv/emotes/decicus?types=png)
- Example with explicitly getting all types of emotes: [{{ base_url }}/bttv/emotes/decicus?types=gif,png]({{ base_url }}/bttv/emotes/decicus?types=gif,png)
    - This practically works the same as `all` (default), but explicitly requests both types of emotes.
