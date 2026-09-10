# sx-reference-assets-horse

Public reference images for the SIXT "Horse" ad-video pillar's video-generation
pipeline. Public hosting is required because the video-generation model needs
a real `https://` URL for `start_image_url`/`end_image_url` — a local file
can't be passed directly, and embedding an image as base64 costs ~37,000
tokens per call vs. ~30 for a URL (same reasoning as `sixt-rbb-onboarding`'s
own `known-cities.json` reference images, hosted at
`BielerG/sx-reference-assets`).

## Structure

```
<city>/<format>/<part>/start.jpg
<city>/<format>/<part>/end.jpg
```

- `<city>` — e.g. `miami`
- `<format>` — `9x16` or `16x9`
- `<part>` — `horse-part1`, `horse-part2`, or `packshot-car`

Referenced from the `sixt-horse` project's `lib/horse/known-scenes.json`.
