# AppADay 083 - Homebrew Label Lab

**Design a print-ready craft beer label in your browser, then export it as a PNG.**

Live: https://augustineiacopelli.github.io/appaday-083-homebrew-label-lab/
Portfolio: https://augustineiacopelli.github.io/appaday/

## What it does

Enter a beer name, style, ABV, IBU, and a brewery line, then pick a motif and color scheme and watch the label render live on canvas. When you like it, download a print-ready PNG at the exact pixel dimensions for your chosen size and resolution.

You can design by hand or hand the wheel to Claude. Describe your beer in plain language ("a hazy summer IPA bursting with mango and citrus, playful and bright") and Claude art-directs the whole thing: it returns a name, style, ABV, IBU, brewery line, the best-fitting motif, and a custom color palette, which the app applies instantly. The label always stays fully editable and prints crisp, because it is drawn as vector-quality canvas art rather than a generated raster image.

## Formats and sizes

Three label types, each with real-world size presets, plus a custom width-by-height option in inches and a 150 / 300 DPI toggle so the exported PNG is dimensionally correct for print.

- **Bottle** - Standard 4x5, Longneck 3x4, Large 4.5x6
- **Can** - 12 oz 4x5.2, 16 oz 4x6, Slim 2.6x6
- **Tap handle** - Blade 2x7, Shield 2.6x5, Tall 1.8x8

## Motifs and color

Five motifs, each with its own typographic personality: Hop Crest (emblem and serif), Modern (bold minimal), Vintage (ornate frame and ribbon), Bold Type (slab headline), and Botanical (wheat sprigs and Fraunces). Eight color schemes span warm to cool, and any AI-generated palette joins them as a selectable swatch. A Shuffle button reshuffles motif and scheme for quick exploration.

## AI setup

The AI art-director calls the Anthropic API directly from the browser with your own key. Open Settings, paste your Anthropic API key, and save. The key is stored only in your browser's local storage and is sent only to the Anthropic API when you generate a design. The model is `claude-sonnet-5`.

## Build notes

One self-contained `index.html`: vanilla HTML, CSS, and JavaScript, no build step, no dependencies beyond Google Fonts. The label renders on a single high-resolution canvas and exports via `toBlob`. Layout scales from a small phone to a large desktop, and the current design persists across reloads.

Category: Creative (AI-powered). Part of the [AppADay](https://augustineiacopelli.github.io/appaday/) project by Augustine Iacopelli.
