# SVG Country Flag Emoji UserScript

This userscript replaces country flag emojis with SVG images from the Twemoji project. This is particularly useful in browsers like Chrome where some flag emojis may not render correctly.

Initially started as a way to fix the flag emojis like, 🇦🇺, being rendered as AU in Chrome on Windows. I now have a better direct font solution. See: [quarrel/](https://github.com/quarrel/broken-flag-emojis-win11-twemoji)

It was an interesting digression in debouncing and avoiding CSP issues, while keeping it performant.

## Installation

1.  Install a userscript manager like [Tampermonkey](https://www.tampermonkey.net/) or [Violentmonkey](https://violentmonkey.github.io/).
2.  Install the script from [Greasy Fork](https://greasyfork.org/en/scripts/545524-svg-country-flag-emoji-q).

## How it works

The script uses `twemoji.parse()` to find and replace flag emojis with `<img>` tags. The SVG images are fetched from a CDN and cached locally using `GM_setValue` to reduce network requests. To get around Content Security Policy (CSP) issues, the images are served from blobs.

It tries to be nice to other scripts by debouncing its updates, while also not having visible lag.
