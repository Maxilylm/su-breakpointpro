# BreakpointPro

> See one URL rendered side by side at five device sizes at once.

**[Live demo](https://su-breakpointpro.vercel.app)**

Checking a layout across breakpoints normally means dragging a browser window or cycling through DevTools device presets one at a time. BreakpointPro renders the same page in a row of sandboxed iframes — each sized to a real device's viewport and CSS-scaled down so they all fit on screen — so a broken breakpoint is visible at a glance. Because it relies on iframe embedding, sites that send `X-Frame-Options` or a restrictive `frame-ancestors` CSP will refuse to load; it is aimed at previewing your own site during development.

## Features

- Five built-in viewports: iPhone SE, iPhone 14 Pro, iPad, Laptop, and Desktop
- Add custom width × height frames, and remove them again
- Portrait / landscape toggle that swaps dimensions across every frame
- Zoom slider (20–100%) that scales all previews together while iframes keep their true pixel width
- URL normalization, so `example.com` works without typing the scheme
- Each frame is labeled with its device name and exact dimensions

## Stack

- Vanilla JavaScript ES modules, no framework or runtime dependencies
- Sandboxed `<iframe>` elements with CSS `transform: scale()` for the previews
- Vite as the dev server and bundler

## Running locally

```bash
npm install
npm run dev
```

---

Part of a series of 91 small web apps. [Browse them all](https://su-slopmachine.vercel.app).
