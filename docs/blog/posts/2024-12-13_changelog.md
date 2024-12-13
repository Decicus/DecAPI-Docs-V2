---
date: 2024-12-13
slug: 2024-12-13-changelog
categories:
    - Changelog
tags:
    - changelog
---

# Changelog for December 13th, 2024

## :fontawesome-brands-youtube: YouTube

The "Latest video" endpoint has received some improvements:

- You can use the `shorts_url` parameter to get a URL that goes to the "Shorts layout" of YouTube, if your video is a "Shorts" video - Feature request on [GitHub (issue #113)](https://github.com/Decicus/DecAPI/issues/113)
    - Example: `https://decapi.me/youtube/latest_video?shorts_url=1&handle=@NileRedExtra`
    - Regular videos will still give you a URL that looks like: `https://youtu.be/VIDEO_ID_HERE`. 
    - However, "Shorts" (videos under 1 minute) will give you a URL that looks like: `https://youtube.com/shorts/VIDEO_ID_HERE`.
- You can now pass your YouTube `@` 'handle' instead of channel ID or legacy username. This was previously not supported.
    - Simply pass it with the `@` prefix, like so: [`https://decapi.me/youtube/latest_video?handle=@NileRed`](https://decapi.me/youtube/latest_video?handle=@NileRed)
    - Note that while the example above uses the `handle` parameter, as long as you put `@` before the actual handle, you can use the `id` or `user` parameter as well.