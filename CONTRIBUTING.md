# Contributing

Thanks for helping improve Google Maps to Apple Maps Shortcut.

## Useful Bug Reports

Please include:

- Google Maps share URL.
- iPhone iOS version.
- Google Maps app version, if known.
- Place type: business, dropped pin, selected location, address, transit stop, etc.
- What happened in Apple Maps.
- What you expected to happen.

## Development Notes

The shortcut is distributed through iCloud and stored here as a `.shortcut` file.

When testing URL handling, check at least:

- Business listing.
- Dropped pin.
- Selected location.
- Plain address.
- Place with Japanese or non-Latin characters.
- Coordinates-only link.

## Pull Requests

For changes to documentation, edit the Markdown files directly.

For shortcut changes, update the iCloud link and replace the `.shortcut` file in `shortcut/`.
