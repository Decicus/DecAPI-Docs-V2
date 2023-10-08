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

- Example with all types of emotes (default): [{{ base_url }}/bttv/emotes/decicus]({{ base_url }}/bttv/emotes/decicus)
- Example with only getting animated GIF emotes: [{{ base_url }}/bttv/emotes/decicus?types=gif]({{ base_url }}/bttv/emotes/decicus?types=gif)
- Example with only getting static PNG emotes: [{{ base_url }}/bttv/emotes/decicus?types=png]({{ base_url }}/bttv/emotes/decicus?types=png)
- Example with explicitly getting all types of emotes: [{{ base_url }}/bttv/emotes/decicus?types=gif,png]({{ base_url }}/bttv/emotes/decicus?types=gif,png)
    - This functionally works the same as `all` (default), but explicitly requests both types of emotes.

### Examples for bots

- [Nightbot](https://nightbot.tv/commands/variable)
    - All types of emotes: `$(urlfetch {{ base_url }}/bttv/emotes/$(channel))`
    - Only animated GIF emotes: `$(urlfetch {{ base_url }}/bttv/emotes/$(channel)?types=gif)`
    - Only static PNG emotes: `$(urlfetch {{ base_url }}/bttv/emotes/$(channel)?types=png)`
- [Streamlabs Chatbot](https://streamlabs.com/chatbot)
    - All types of emotes: `$readapi({{ base_url }}/bttv/emotes/$mychannel)`
    - Only animated GIF emotes: `$readapi({{ base_url }}/bttv/emotes/$mychannel?types=gif)`
    - Only static PNG emotes: `$readapi({{ base_url }}/bttv/emotes/$mychannel?types=png)`
- [Streamlabs Cloudbot](https://streamlabs.com/cloudbot)
    - All types of emotes: `{readapi.{{ base_url }}/bttv/emotes/{channel.name}}`
    - Only animated GIF emotes: `{readapi.{{ base_url }}/bttv/emotes/{channel.name}?types=gif}`
    - Only static PNG emotes: `{readapi.{{ base_url }}/bttv/emotes/{channel.name}?types=png}`
- [StreamElements](https://streamelements.com/)
    - All types of emotes: `${customapi.{{ base_url }}/bttv/emotes/${channel}}`
    - Only animated GIF emotes: `${customapi.{{ base_url }}/bttv/emotes/${channel}?types=gif}`
    - Only static PNG emotes: `${customapi.{{ base_url }}/bttv/emotes/${channel}?types=png}`
- [Fossabot](https://docs.fossabot.com/variables/customapi)
    - All types of emotes: `$(customapi {{ base_url }}/bttv/emotes/$(channel))`
    - Only animated GIF emotes: `$(customapi {{ base_url }}/bttv/emotes/$(channel)?types=gif)`
    - Only static PNG emotes: `$(customapi {{ base_url }}/bttv/emotes/$(channel)?types=png)`
- [Deepbot](https://deepbot.tv/)
    - All types of emotes: `@customapi@[{{ base_url }}/bttv/emotes/@stream@]`
    - Only animated GIF emotes: `@customapi@[{{ base_url }}/bttv/emotes/@stream@?types=gif]`
    - Only static PNG emotes: `@customapi@[{{ base_url }}/bttv/emotes/@stream@?types=png]`
- [PhantomBot](https://phantombot.tv/)
    - All types of emotes: `(customapi {{ base_url }}/bttv/emotes/(channelname))`
    - Only animated GIF emotes: `(customapi {{ base_url }}/bttv/emotes/(channelname)?types=gif)`
    - Only static PNG emotes: `(customapi {{ base_url }}/bttv/emotes/(channelname)?types=png)`