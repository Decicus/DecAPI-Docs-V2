---
date: 2023-08-11
slug: twitch-follower-endpoints-august-2023
categories:
    - Twitch
tags:
    - twitch
---

# Twitch - Follower-related Endpoints - August 2023

_This is an archived post from August 2023, originally posted on [GitHub Gist](https://gist.github.com/Decicus/daf7234366387636d5d2fe9f59ba0f11)._  

I should've mentioned this when I first saw the [original announcement](https://discuss.dev.twitch.tv/t/follows-endpoints-and-eventsub-subscription-type-are-now-available-in-open-beta/43322), but I suppose now is better than never.

As [announced on the Twitch developer forums](https://discuss.dev.twitch.tv/t/legacy-follows-api-and-eventsub-shutdown-timeline-updated/46769), at September 6, 2023 5:00:00 PM UTC Twitch will begin the process of shutting down the now deprecated ["Get User Follows"](https://dev.twitch.tv/docs/api/reference/#get-users-follows) API endpoint.

This will affect the following DecAPI endpoints:

- [/twitch/followage](https://docs.decapi.me/twitch?endpoint=followage%2F%3Achannel%2F%3Auser)
- [/twitch/followed](https://docs.decapi.me/twitch?endpoint=followed%2F%3Achannel%2F%3Auser)
- [/twitch/followers](https://docs.decapi.me/twitch?endpoint=followers%2F%3Achannel)
- [/twitch/following](https://docs.decapi.me/twitch?endpoint=following%2F%3Auser)

It would technically also affect the "followcount" API, but I plan on migrating that to their new API endpoint, so that should keep working as-is.

As for the other 4 endpoints listed above, please consider them to be **deprecated** in the short-term.
Primarily 2 reasons for this:

1. As I've stated in the past, I don't like having to deal with tokens (such as what subcount/subpoints require), which is now going to be required to retrieve the "follower relationship" between a channel and a user in the new API. The _follower count_ of a channel does not require any authentication, so that should be fine as mentioned earlier.
2. While DecAPI currently has support for authentication (subcount/subpoints), the implementation wasn't designed to support different sets of authentication permissions. I really want to revamp that whole system before I even attempt to tackle support of follower APIs and subscriber APIs side-by-side.

Even if I do decide to re-implement follower APIs, I plan on dropping both `/twitch/followers` (list of a channel's followers) and `/twitch/following` (list of channels the specified user is currently following - requires a separate authentication permission anyway) indefinitely.
My focus would then be primarily `/twitch/followed` (the date & date when a specific user followed a specific channel) and `/twitch/followage` (how long since a specific user followed a specific channel), but once again this isn't going to be something I do short-term.