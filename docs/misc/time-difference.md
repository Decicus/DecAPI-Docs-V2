---
title: Displays the time difference between two timestamps
botexamples:
  - title: "Time since May 17th, 1814 at 13:37:06 Central European Time"
    url: ":base_url/misc/time-difference?first=1814-05-17T13:37:06%2B02:00"
  - title: "Time since May 17th, 1814 at 13:37:06 Central European Time, localized in Norwegian"
    url: ":base_url/misc/time-difference?first=1814-05-17T13:37:06%2B02:00&lang=no"
  - title: "Time between May 17th, 1814 at 13:37:06 Central European Time and July 4th, 1776 at 12:00:00 US Eastern Time"
    url: ":base_url/misc/time-difference?first=1814-05-17T13:37:06%2B02:00&second=1776-07-04T12:00:00-04:00"
---

# Displays the time difference between two timestamps

Gives you a human-readable time difference between two specified timestamps.  
Timestamps can be in any format that PHP's [`strtotime()`](https://www.php.net/manual/en/datetime.formats.php) function can understand.  
If you wish to specify a timezone, please include that in the timestamp itself. My recommendation is to follow the [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) standard. Example: [/misc/time-difference?first=2022-10-31T13:37:06+02:00]({{ base_url }}/misc/time-difference?first=2022-10-31T13:37:06%2B02:00)

Supports [localization](../index.md#localization-translations)! Example time in German: [/misc/time-difference?first=2022-10-31T13:37:06%2B02:00&lang=de]({{ base_url }}/misc/time-difference?first=2022-10-31T13:37:06%2B02:00&lang=de)

## Endpoint URL

`{{ base_url }}/misc/time-difference?first=2022-10-31T13:37:06%2B02:00`

## Query parameters

- `first` - **Required** - The first timestamp to calculate from.
- `second` - **Optional** - The second timestamp to calculate to. If not specified, the current time will be used.
- `lang` - **Optional** - The language to localize the output to.
    - See the [Localization section on the homepage](../index.md#localization-translations) to see what languages are currently supported.

## Examples

- Time since May 17th, 1814 at 13:37:06 Central European Time: [{{ base_url }}/misc/time-difference?first=1814-05-17T13:37:06%2B02:00]({{ base_url }}/misc/time-difference?first=1814-05-17T13:37:06%2B02:00)
- Time since May 17th, 1814 at 13:37:06 Central European Time, localized in Norwegian: [{{ base_url }}/misc/time-difference?first=1814-05-17T13:37:06%2B02:00&lang=no]({{ base_url }}/misc/time-difference?first=1814-05-17T13:37:06%2B02:00&lang=no)
- Time between May 17th, 1814 at 13:37:06 Central European Time and July 4th, 1776 at 12:00:00 US Eastern Time: [{{ base_url }}/misc/time-difference?first=1814-05-17T13:37:06%2B02:00&second=1776-07-04T12:00:00-04:00]({{ base_url }}/misc/time-difference?first=1814-05-17T13:37:06%2B02:00&second=1776-07-04T12:00:00-04:00)
