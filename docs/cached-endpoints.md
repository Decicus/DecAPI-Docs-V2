# Cached endpoints

To avoid excessive requests to third-party APIs (particularly Twitch and others), DecAPI implements caching for various API calls. We try to keep cache times relatively short to avoid stale data, but these durations may need to be adjusted based on DecAPI's usage.

While this documentation is regularly updated, the authoritative source for cache settings can be found in [the DecAPI configuration file](https://github.com/Decicus/DecAPI/blob/master/config/twitch.php).

## :fontawesome-brands-twitch: Twitch

| API Endpoint | Cache Duration | Description |
|-------------|----------------|-------------|
| `accountage / creation` | 6 hours | Account creation date is cached. While this could be cached indefinitely since it never changes, we use a finite duration to manage storage. Note: The actual accountage is calculated in real-time using the cached creation date. |
| `avatar` | 30 minutes | Avatar URLs are cached. May return invalid URLs if a user changes their avatar and Twitch removes the old URL quickly. |
| `followage / followed` | 30 minutes* | The follow date/time for a channel. *If someone that isn't following the channel is requested, then it's only cached for 2 minutes. |
| `followcount` | 2 minutes | Number of followers for a channel. |
| `game / title` | 3 minutes | Channel's current game and stream title (cached together as they use the same API endpoint). |
| `subpoints / subcount` | 2 minutes | Subscriber points and count are cached together as they share the same API endpoint. |
| `subscriber_emotes` | 1 hour | Channel emote information. Future emote-related endpoints may share this cache. |
| `uptime / viewercount` | 5 minutes | Stream status and viewer count are cached together. Uptime is calculated in real-time using the cached stream start time, so this will always be up-to-date assuming the stream hasn't restarted. |
| `videos / vod_replay` | 5 minutes | VOD/video information. |

## :fontawesome-brands-youtube: YouTube

| API Endpoint | Cache Duration | Description |
|-------------|----------------|-------------|
| `videoid` | 3 hours | Search results are cached. Only affects exact matches (case-insensitive). |