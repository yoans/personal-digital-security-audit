# Assets

## og-cover.png

LinkedIn, Twitter, Facebook, and Slack require a raster image (PNG or JPG) for link previews. SVG is not reliably rendered.

To generate `og-cover.png` from `og-cover.svg`:

**Option 1: Browser screenshot**
1. Open `og-cover.svg` in any browser
2. Set window to 1200x630
3. Screenshot, save as `assets/og-cover.png`

**Option 2: Command line (if you have ImageMagick or rsvg-convert)**
```
rsvg-convert -w 1200 -h 630 assets/og-cover.svg -o assets/og-cover.png
```
or
```
magick assets/og-cover.svg -resize 1200x630 assets/og-cover.png
```

**Option 3: Online converter**
Upload `og-cover.svg` to any SVG-to-PNG converter (e.g., cloudconvert.com), download as PNG, save to `assets/og-cover.png`.

Once `og-cover.png` exists, the meta tags in `index.html` will resolve correctly when LinkedIn fetches a preview.
