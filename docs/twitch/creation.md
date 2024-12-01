---
title: "Creation date and time for a Twitch user"
botexamples:
  - title: "Get creation date and time for a Twitch user specified after the command"
    url: ":base_url/twitch/creation/:user"
  - title: "Get creation date and time for a Twitch user specified after the command, using the timezone in <i>Oslo (Norway)</i> and the format <code>2024-06-01 18:15:34 CEST</code>"
    url: ":base_url/twitch/creation/:user?tz=Europe/Oslo&format=Y-m-d H:i:s T"
  - title: "Get creation date and time for a Twitch user specified after the command, using the timezone in <i>Los Angeles (US Pacific Time)</i> and the format <code>2024-06-01 06:15:34 PM PDT</code>"
    url: ":base_url/twitch/creation/:user?tz=America/Los_Angeles&format=Y-m-d h:i:s A T"
---

# Creation date & time for a Twitch user

Gives you the creation date and time of a Twitch user.
If you're only interested in how old a Twitch account is, check out [twitch/accountage](/twitch/accountage).

## Endpoint URL

`{{ base_url }}/twitch/creation/TWITCH_USERNAME_HERE`

See [examples](#examples) below for usage with an actual Twitch username.

## Required URL parameters

- `user` - **Required** - Twitch username to get the creation date & time for.

## Query parameters

- `format` - Optional - Format of the date and time. Default is `M j. Y - h:i:s A (e)`
    - See the available formatting options on [PHP.net's documentation](https://www.php.net/manual/en/datetime.format.php#refsect1-datetime.format-parameters).
- `tz` - Optional - Timezone to use for the date and time. Default is `UTC`.
    - The timezone list is the same as the ones available in [misc/time](/misc/time).

## Examples

- What date & time Decicus' account was created: [{{ base_url }}/twitch/creation/decicus]({{ base_url }}/twitch/creation/decicus)
- What date & time Decicus' account was created, using the timezone in Oslo (Norway) and the format: `2011-10-22 15:38:29 CEST`: [{{ base_url }}/twitch/creation/decicus?tz=Europe/Oslo&format=Y-m-d H:i:s T]({{ base_url }}/twitch/creation/decicus?tz=Europe/Oslo&format=Y-m-d H:i:s T)
- What date & time Decicus' account was created, using the timezone in Los Angeles (US Pacific Time) and the format: `2011-10-22 06:38:29 AM PDT`: [{{ base_url }}/twitch/creation/decicus?tz=America/Los_Angeles&format=Y-m-d h:i:s A T]({{ base_url }}/twitch/creation/decicus?tz=America/Los_Angeles&format=Y-m-d h:i:s A T)