---
title: Evaluate math expression
botexamples:
  - title: "Evaluate expression"
    url: ":base_url/math?exp=:query"
---

# Evaluate math expression

Performs a mathematic operation based on the expression passed to the endpoint.  
Keep in mind to properly URL-encode `exp`, so that certain characters are handled correctly.

Thanks to [mathjs](https://mathjs.org/) for providing the library / API for this endpoint.

## Handling addition (plus) properly

Especially important with the `+` (plus) character. If the `+` character is passed as-is to the URL, it will be interpreted as a space character.  
For the API to consider `+` as an actual "plus" / addition, it needs to be URL-encoded as `%2B`.  
If you're allowing your viewers to use this as a command in your Twitch chat, then there are _some_ bots that have command variables to properly handle this, such as:

- [Fossabot's `$(querystring)`](https://docs.fossabot.com/variables/querystring)
- [Nightbot's `$(querystring)`](https://docs.nightbot.tv/commands/variables/querystring)
- [StreamElements' `${queryescape ${1:}}`](https://docs.streamelements.com/chatbot/variables/queryescape)

The examples at the bottom of this documentation page try to use the correct bot variables for each bot, but the bots listed above are the only ones I know of that will properly encode the `+` character unless done manually.

## Endpoint URL

`{{ base_url }}/math?exp=369%2B51`

## Query parameters

- `exp` - **Required** - The mathematic expression to receive the result from.
- `round` - **Optional** - Round to the specified number of decimal places.
    - If specified with 0 or below, or with no value, the result will be rounded to the nearest whole number.

## Examples

- 369 + 51: [{{ base_url }}/math?exp=369%2B51]({{ base_url }}/math?exp=369%2B51)
- 369.122222 + 51.57474769: [{{ base_url }}/math?exp=369.122222%2B51.57474769]({{ base_url }}/math?exp=369.122222%2B51.57474769)
- 369.122222 + 51.57474769 rounded to 1 decimal place: [{{ base_url }}/math?exp=369.122222%2B51.57474769&round=1]({{ base_url }}/math?exp=369.122222%2B51.57474769&round=1)
- 369.122222 + 50.57474769 rounded to a whole number: [{{ base_url }}/math?exp=369.122222%2B50.57474769&round=0]({{ base_url }}/math?exp=369.122222%2B50.57474769&round=0)
