# SVG Country Flag Emoji Fix

This userscript replaces country flag emojis with SVG images from the Twemoji project. This is particularly useful in browsers like Chrome where some flag emojis may not render correctly.

## Installation

1.  Install a userscript manager like [Tampermonkey](https://www.tampermonkey.net/) or [Violentmonkey](https://violentmonkey.github.io/).
2.  Install the script from [Greasy Fork](https://greasyfork.org/en/scripts/499718-svg-country-flag-emoji-q).

## How it works

The script uses `twemoji.parse()` to find and replace flag emojis with `<img>` tags. The SVG images are fetched from a CDN and cached locally using `GM_setValue` to reduce network requests.
