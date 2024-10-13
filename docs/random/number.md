---
title: Random number between min and max
botexamples:
  - title: "Get a random number between 1 and 100"
    url: ":base_url/random/number/1/100"
  - title: "Get a random number between -3125 and 7101"
    url: ":base_url/random/number/-3125/7101"
---

# Random number between a minimum and maximum value

A random number generator between a specified minimum and maximum value.

Supports both positive and negative numbers. Only integer values (no decimal numbers).

## Endpoint URL

`{{ base_url }}/random/number/-420/1337`

## Query parameters

- `format` - **Optional** - If this parameter is _specified_, it will be formatted using the _default values_ of [`number_format()`](https://www.php.net/manual/en/function.number-format.php)

## Examples

- Get a random number between 1 and 100: [{{ base_url }}/random/number/1/100]({{ base_url }}/random/number/1/100)
- Get a random number between -3125 and 7101: [{{ base_url }}/random/number/-3125/7101]({{ base_url }}/random/number/-3125/7101)
