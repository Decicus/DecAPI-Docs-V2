---
title: Get latest DayZ blog post
botexamples:
  - title: "Get latest blog post without any filtering"
    url: ":base_url/dayz/news"
  - title: "The latest blog post that contains the word 'update' in the post title"
    url: ":base_url/dayz/news?search=update"
---

# Get latest DayZ blog post

Gives you the latest blog post from the [DayZ website](https://dayz.com/).

## Endpoint URL

`{{ base_url }}/dayz/news`

### Query parameters

- `search` - Optional. If specified it will only give you the latest blog post where the post title contains the specified text. This parameter is *case-insensitive*.

## Example

- Get latest blog post (without any filtering): [{{ base_url }}/dayz/news]({{ base_url }}/dayz/news)
- The latest blog post that contains the word "update" (case-insensitive) in the post title: [{{ base_url }}/dayz/news?search=update]({{ base_url }}/dayz/news?search=update)