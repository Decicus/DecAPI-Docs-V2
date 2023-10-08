# /bttv/emotes/:channel

Returns a space-separated list of [BetterTTV](https://betterttv.com/) emotes available in the channel.

## Required URL parameters

- `channel` - The channel to retrieve emotes from.

### Query parameters

- `types` - A comma-separated list of types to return. Your options are:
    - `all` - **Default if not specified**. Returns all types of emotes.
    - `gif` - Returns only animated GIF emotes.
    - `png` - Returns only static PNG image emotes.

## Example

- Example with all types of emotes (default): [https://decapi.me/bttv/emotes/decicus](https://decapi.me/bttv/emotes/decicus)
- Example with only getting animated GIF emotes: [https://decapi.me/bttv/emotes/decicus?types=gif](https://decapi.me/bttv/emotes/decicus?types=gif)
- Example with only getting static PNG emotes: [https://decapi.me/bttv/emotes/decicus?types=png](https://decapi.me/bttv/emotes/decicus?types=png)
- Example with explicitly getting all types of emotes: [https://decapi.me/bttv/emotes/decicus?types=gif,png](https://decapi.me/bttv/emotes/decicus?types=gif,png)
    - This functionally works the same as `all` (default), but explicitly requests both types of emotes.

### Examples for bots

- [Nightbot](https://nightbot.tv/commands/variable)
    - All types of emotes: `$(urlfetch https://decapi.me/bttv/emotes/$(channel))`
    - Only animated GIF emotes: `$(urlfetch https://decapi.me/bttv/emotes/$(channel)?types=gif)`
    - Only static PNG emotes: `$(urlfetch https://decapi.me/bttv/emotes/$(channel)?types=png)`
- [Streamlabs Chatbot](https://streamlabs.com/chatbot)
    - All types of emotes: `$readapi(https://decapi.me/bttv/emotes/$mychannel)`
    - Only animated GIF emotes: `$readapi(https://decapi.me/bttv/emotes/$mychannel?types=gif)`
    - Only static PNG emotes: `$readapi(https://decapi.me/bttv/emotes/$mychannel?types=png)`
- [Streamlabs Cloudbot](https://streamlabs.com/cloudbot)
    - All types of emotes: `{readapi.https://decapi.me/bttv/emotes/{channel.name}}`
    - Only animated GIF emotes: `{readapi.https://decapi.me/bttv/emotes/{channel.name}?types=gif}`
    - Only static PNG emotes: `{readapi.https://decapi.me/bttv/emotes/{channel.name}?types=png}`
- [StreamElements](https://streamelements.com/)
    - All types of emotes: `${customapi.https://decapi.me/bttv/emotes/${channel}}`
    - Only animated GIF emotes: `${customapi.https://decapi.me/bttv/emotes/${channel}?types=gif}`
    - Only static PNG emotes: `${customapi.https://decapi.me/bttv/emotes/${channel}?types=png}`
- [Fossabot](https://docs.fossabot.com/variables/customapi)
    - All types of emotes: `$(customapi https://decapi.me/bttv/emotes/$(channel))`
    - Only animated GIF emotes: `$(customapi https://decapi.me/bttv/emotes/$(channel)?types=gif)`
    - Only static PNG emotes: `$(customapi https://decapi.me/bttv/emotes/$(channel)?types=png)`
- [Deepbot](https://deepbot.tv/)
    - All types of emotes: `@customapi@[https://decapi.me/bttv/emotes/@stream@]`
    - Only animated GIF emotes: `@customapi@[https://decapi.me/bttv/emotes/@stream@?types=gif]`
    - Only static PNG emotes: `@customapi@[https://decapi.me/bttv/emotes/@stream@?types=png]`
- [PhantomBot](https://phantombot.tv/)
    - All types of emotes: `(customapi https://decapi.me/bttv/emotes/(channelname))`
    - Only animated GIF emotes: `(customapi https://decapi.me/bttv/emotes/(channelname)?types=gif)`
    - Only static PNG emotes: `(customapi https://decapi.me/bttv/emotes/(channelname)?types=png)`