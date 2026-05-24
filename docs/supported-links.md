# Supported Google Maps Links

The shortcut is designed to handle the common Google Maps share links used on iPhone.

## Supported Cases

- Google Maps short links: `https://maps.app.goo.gl/...`
- Business and POI place cards.
- Plain addresses.
- Dropped pins.
- Selected locations.
- Coordinates-only destinations.
- Japanese and non-Latin place names.
- Expanded URLs with `q=place+name`, `q=address`, or `q=lat,lng`.

## Conversion Strategy

The shortcut expands the Google Maps share URL and extracts the destination from the expanded URL. The destination is then passed to Apple Maps with:

```text
http://maps.apple.com/?daddr=<destination>&dirflg=d
```

This lets Apple Maps handle both human-readable place/address strings and latitude/longitude coordinates.
