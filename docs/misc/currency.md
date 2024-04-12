---
title: Convert currency
botexamples:
  - title: "Convert from user specified number of EUR (euros) to NOK (Norwegian Krone)"
    url: ":base_url/misc/currency?from=EUR&to=NOK&value=:query"
  - title: "Convert from user specified number of EUR (euros) to NOK (Norwegian Krone), round to 2 decimal places"
    url: ":base_url/misc/currency?from=EUR&to=NOK&value=:query&round=2"
---

# Convert currency

Convert currency from one currency to another.  
Currency rates are cached for up to 24 hours, so don't expect the precise latest rates.

Regular currencies follow the [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) standard.  
Some cryptocurrencies are also supported.

You can see a list of supported currencies/cryptocurrencies here: [{{ base_url }}/misc/currency?list]({{ base_url }}/misc/currency?list)

## Endpoint URL

`{{ base_url }}/misc/currency?from=EUR&to=NOK&value=1`

## Query parameters

- `from` - **Required** - The currency to convert _from_.
- `to` - **Required** - The currency to convert _to_.
- `value` - **Required** - The amount of `from` you wish to convert.
- `round` - **Optional** - Round to the specified number of decimal places.
    - If specified with 0 or below, or with no value, the result will be rounded to the nearest whole number.
- `list` - **Optional** - If specified, will return a list of supported currencies.
    - ⚠ This will prevent any other parameters from being used. Only use this parameter by itself when you wish to see what currencies are available.

## Examples

- Convert _from_ 1 EUR (Euro), _to_ NOK (Norwegian Krone): `{{ base_url }}/misc/currency?from=EUR&to=NOK&value=1`
- Convert _from_ 15 USD (US Dollar), _to_ NOK (Norwegian Krone) and round to 2 decimal places: `{{ base_url }}/misc/currency?from=USD&to=NOK&value=15&round=2`
