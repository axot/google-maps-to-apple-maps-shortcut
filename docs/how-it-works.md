# How It Works

The shortcut converts a Google Maps share link into an Apple Maps directions link.

## Flow

1. Receive input from the iOS share sheet.
2. Detect URLs in the shared input.
3. Expand the Google Maps short URL.
4. Retry expansion briefly if the first expansion still returns the original short URL.
5. Extract the destination from the expanded URL's `q=` parameter.
6. Build an Apple Maps URL:

```text
http://maps.apple.com/?daddr=<destination>&dirflg=d
```

7. Open the URL.

## Why `q=`

Google Maps share links are inconsistent:

- A normal place may expand to a place name and address.
- A dropped pin may expand to latitude and longitude.
- A "selected location" may not have a business/place ID, but can still have `q=lat,lng`.

The `q=` parameter is the common destination signal across these cases.

## Apple Maps URL

The shortcut uses Apple's documented Map Links format:

```text
http://maps.apple.com/?daddr=<destination>&dirflg=d
```

`daddr` sets the destination. `dirflg=d` requests driving directions.

## Current Shortcut Metadata

- Name: `Apple Map`
- iCloud link: https://www.icloud.com/shortcuts/32e44c7daedf4909884206cb362ce4da
- Share sheet enabled: yes
- Signing status: approved

## References

- Apple Map Links: https://developer.apple.com/library/archive/featuredarticles/iPhoneURLScheme_Reference/MapLinks/MapLinks.html
- Apple Shortcuts sharing: https://support.apple.com/guide/shortcuts/share-shortcuts-apdf01f8c054/ios
- Google Maps URLs: https://developers.google.com/maps/documentation/urls/get-started
