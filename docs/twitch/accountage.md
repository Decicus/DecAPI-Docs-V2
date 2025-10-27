---
title: "Account age for a user"
botexamples:
  - title: "Get account age for a Twitch user specified after the command"
    url: ":base_url/twitch/accountage/:user"
  - title: "Get account age for a Twitch user specified after the command, with more precision"
    url: ":base_url/twitch/accountage/:user?precision=7"
cached: true
---

# Account age for a Twitch user

Gives you the "account age" of a Twitch user. In other words the amount of time passed since their account was created.  
This works similar to [twitch/creation](/twitch/creation).

## Endpoint URL

`{{ base_url }}/twitch/accountage/TWITCH_USERNAME_HERE`

See [examples](#examples) below for usage with an actual Twitch username.

## Required URL parameters

- `user` - **Required** - Twitch username to get the account age for.

## Query parameters

- `precision` - Optional - Maximum precision in the time returned. Defaults to 2, maximum is 7.
    - If the account is old enough, specifying 7 will give you: years, months, weeks, days, hours, minutes, and seconds.
    - With the default precision of 2, you would only get years and months.

## Examples

- How long since Decicus' Twitch account was created: [{{ base_url }}/twitch/accountage/decicus]({{ base_url }}/twitch/accountage/decicus)
- How long since Decicus' Twitch account was created with more precision, giving all values down to the second: [{{ base_url }}/twitch/accountage/decicus?precision=7]({{ base_url }}/twitch/accountage/decicus?precision=7)