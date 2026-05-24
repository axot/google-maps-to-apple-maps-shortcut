# Google Maps to Apple Maps Shortcut

Open a place found in **Google Maps** directly in **Apple Maps** for turn-by-turn navigation on iPhone.

This iOS Shortcut is built for people who search in Google Maps but prefer Apple Maps navigation.

[Install the Shortcut](https://www.icloud.com/shortcuts/32e44c7daedf4909884206cb362ce4da)

## Why

Google Maps is often better for search, reviews, and place discovery. Apple Maps is often better integrated with iPhone, CarPlay, Siri, Apple Watch, and system-level navigation.

This shortcut bridges that gap:

1. Search or select a place in Google Maps.
2. Tap Share.
3. Run `Apple Map`.
4. Apple Maps opens directions to that destination.

## Features

- Works from the Google Maps share sheet.
- Handles `maps.app.goo.gl` short links.
- Expands Google Maps links before parsing.
- Uses Google Maps `q=` destinations, including coordinates for dropped pins and "selected location" links.
- Opens Apple Maps with driving directions.
- Includes a clear alert if Google Maps ever changes its share URL format.
- No account, server, tracking, or analytics.

## Install

Install from iCloud:

https://www.icloud.com/shortcuts/32e44c7daedf4909884206cb362ce4da

The signed `.shortcut` file is also stored in this repository:

[shortcut/Apple Map.shortcut](shortcut/Apple%20Map.shortcut)

## Usage

1. Open Google Maps on iPhone.
2. Search for a place or tap a pin.
3. Tap the share button.
4. Select `Apple Map`.
5. Apple Maps opens the route.

If the shortcut does not appear in Google Maps' share sheet, open the Shortcuts app once after installation, then reopen Google Maps and try the share sheet again.

## How It Works

Google Maps usually shares a short URL like:

```text
https://maps.app.goo.gl/...
```

The shortcut expands that URL, extracts the destination from the expanded Google Maps URL, then creates an Apple Maps directions URL:

```text
http://maps.apple.com/?daddr=<destination>&dirflg=d
```

See [docs/how-it-works.md](docs/how-it-works.md) for the full flow.

## Supported Link Types

Google Maps does not use one stable URL shape for every place. Places, dropped pins, selected locations, and business listings can resolve differently.

This shortcut handles the common Google Maps share formats, including normal places, addresses, dropped pins, selected locations, Japanese place names, and coordinates-only destinations.

See [docs/supported-links.md](docs/supported-links.md) for details.

## Privacy

The shortcut runs locally in Apple's Shortcuts app. It does not send data to any custom server. It only interacts with:

- Google Maps URLs you explicitly share.
- Apple's Maps URL handler when opening directions.

## Compatibility

Tested with Google Maps for iOS and Apple Maps on iPhone.

## Disclaimer

This project is not affiliated with, endorsed by, or sponsored by Apple or Google. Apple Maps, Google Maps, iPhone, and iOS are trademarks of their respective owners.

## Contributing

If you open an issue, the most useful details are:

- The Google Maps share URL.
- The type of place: business, dropped pin, selected location, transit stop, etc.
- The Apple Maps result.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT License. See [LICENSE](LICENSE).
