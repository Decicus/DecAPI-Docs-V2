# Welcome to DecAPI's documentation

Here you will find documentation for DecAPI's endpoints and some examples on how to use them.  
If you would like to contribute to the documentation, take a look at the [:fontawesome-brands-github: GitHub repository](https://github.com/Decicus/DecAPI-Docs).

## Questions and support

If you have any questions or need support, feel free to join the [:fontawesome-brands-discord: Discord server][Discord] and ask in the `#support` channel.

For other ways of contacting me, see the [contact page](contact.md).

## Localization / translations

DecAPI now has some basic localization support for certain endpoints. Primarily it's only used for `/twitch` endpoints.

To use the localization options, use the two-letter language code defined in [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) in the `GET` parameter lang. The default value is `en` (English) and you would (for example) use `de` for German, or `no` for Norwegian. English is also used as a "fallback" if a language isn't supported for certain types of messages.

Keep in mind that the translations are provided by volunteers. If you'd like to translate something into another language, take a look at the ['lang' directory on :fontawesome-brands-github: GitHub][GitHub-Lang-Dir] for examples. Feel free to visit [the :fontawesome-brands-discord: Discord server][Discord] if you need assistance getting started.

### Translation examples

- Example #1: Accountage with precision 7 and language set to Norwegian - [https://decapi.me/twitch/accountage/decicus?precision=7&lang=no](https://decapi.me/twitch/accountage/decicus?precision=7&lang=no)
- Example #2: Accountage with only language set to Norwegian - [https://decapi.me/twitch/accountage/decicus?lang=no](https://decapi.me/twitch/accountage/decicus?lang=no)

### Currently support languages

You should always check ['lang' directory on :fontawesome-brands-github: GitHub][GitHub-Lang-Dir] for the most up-to-date list of supported languages, but here's a quick overview:

| **Language code** | **Language name** |
| --- | --- |
| `en` | English - Default |
| `cs` | Czech |
| `de` | German |
| `es` | Spanish |
| `fr` | French |
| `ko` | Korean |
| `nl` | Dutch |
| `no` | Norwegian |
| `pt` | Portuguese |
| `ro` | Romanian |
| `ru` | Russian |
| `tr` | Turkish |

[Discord]: https://decapi.link/discord
[GitHub-Lang-Dir]: https://github.com/Decicus/DecAPI/tree/master/resources/lang