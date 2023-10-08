---
date: 2023-06-05
slug: twitter-changes-june-2023
categories:
    - Twitter
tags:
    - twitter
---

# Twitter Changes - June 2023

_This is an archived post from June 2023, originally posted on [GitHub Gist](https://gist.github.com/Decicus/dac2f0212b5243cb7f4c0506cd0deea7)._  
_It is no longer relevant to the current version of DecAPI, as the Twitter APIs have been deprecated from DecAPI._

## June 6th, 2023

Following up on yesterday's Twitter changes:

- `search` (and `strict`) parameters should now work again.
- `include_replies` will also work.
- The initial re-implementation yesterday would exclude pinned tweets regardless of when they were posted, which has now been fixed. Pinned tweets can now be included as a "latest tweet", assuming it actually is the latest tweet or matches `search`.

Some things that I forgot to mention yesterday:
- Tweets are cached for up to 2 minutes (120 seconds) _per user and depending on with/without replies_.
    - Essentially that means if you request the latest tweet of a user **without** replies first, and **with** replies afterwards, they will be cached separately.
- Due to the way tweets are now retrieved, an uncached request may be a bit slow (a few seconds). Cached requests should be relatively fast (< 1 second).

--- 

## June 5th, 2023

The DecAPI Twitter endpoints recently broke, due to the Twitter API changes announced a few months back (let's ignore my own procrastination for now).

Some of them have now been fixed, mainly "latest tweet" and "latest tweet URL". The "fix" isn't fully complete, has some functionality lacking and is a bit experimental. There's a chance it will completely break again in the near future, but we'll see.

One issue with the current code is that if your latest tweet is also your pinned tweet, it will skip it. I'll fix it another day. 🙃

Functionality that **no longer works**, though I don't think many people relied on them as much:
- `search` - Filters tweet by text.
    - `strict` as well, since it was used alongside `search`
- `include_replies` - Tweets that are replies to other users on Twitter cannot be retrieved at this time, though this isn't much different from the default behavior.
- `skip` - Only the latest tweet will be fetched

Functionality that **should still work**:
- `howlong` - _How long_ since the tweet was posted.
- `url` - Includes the direct URL to the tweet.

If you notice any oddities with how the tweets are formatted, please let me know in [#support on Discord](https://decapi.link/discord) or via email: [alex@thomassen.xyz](mailto:alex@thomassen.xyz)\*. Ideally with a link to the tweet so I can test with the exact case.

\* I don't really check Twitter as often anymore, so I'll probably miss any DMs, tweets/replies about any issues.