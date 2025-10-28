---
title: "ID - Twitch user ID for a username"
---

# ID - Twitch user ID for a username

Returns the numeric Twitch user ID for the specified username.  
This is mostly useful for developers who need the user ID for API calls or integrations.

## Endpoint URL

`{{ base_url }}/twitch/id/TWITCH_USERNAME_HERE`

## Required URL parameters

- `user` - **Required** - Twitch username to resolve to a user ID.

## Notes

- If the username is invalid or does not exist, the endpoint will return an error, such as "User not found".

## Examples

- Twitch user ID for the user "decicus": [{{ base_url }}/twitch/id/decicus]({{ base_url }}/twitch/id/decicus)