# home.tim

My personal links page. A single file, no build step, no dependencies.

**Live site:** https://num1s0la.github.io/home.tim/

## Features

- Dark night sky with twinkling stars and shooting stars flying right to left
- Animated grass swaying in the wind and falling snow
- Frosted-glass link buttons (Telegram, GitHub, Discord)
- The Discord button copies the username to the clipboard
- Responsive layout: compact on phones, larger on desktop
- Respects `prefers-reduced-motion` (animations are turned off if your system asks for it)
- A hidden easter egg, find it yourself :)

## Customizing

All content lives in the `PROFILE` block at the bottom of `index.html`:

```js
const PROFILE = {
  name: "num1s0la",
  handle: "/home/tim",
  avatar: "",        // e.g. "avatar.png"; empty = plain black circle
  bio: "",
  tags: [],
  links: [
    { title: "Telegram", sub: "@hometim0 · my profile", url: "https://t.me/hometim0" },
    { title: "GitHub",   sub: "num1s0la · projects and code", url: "https://github.com/num1s0la" },
    { title: "Discord",  sub: "num1s0la · copy",          copy: "num1s0la" }
  ]
};
```

- `url` opens a link in a new tab
- `copy` copies the given text to the clipboard instead of opening a link
- `avatar` takes a path to an image placed next to `index.html`

## Deploying to GitHub Pages

1. Upload `index.html` to the root of the repository (the file must be named exactly `index.html`).
2. Go to **Settings → Pages**.
3. Under Build and deployment, choose **Deploy from a branch**, select the `main` branch and the `/ (root)` folder, then click **Save**.
4. After 1-2 minutes the site will be available at `https://<username>.github.io/<repository>/`.

After you update the file, changes may not show up right away because of caching. To check, open the page with `?v=2` appended to the URL.

## Running locally

Just open `index.html` in a browser. Fonts are loaded from Google Fonts, so they need an internet connection, but the page still works with fallback fonts without one.

## Built with

HTML, CSS and a bit of JavaScript (canvas for the stars, grass and snow). Fonts: Unbounded and Manrope.
