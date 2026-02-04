![Title card](https://cms.protoqol.nl/assets/6942cfbd-13b3-4a6c-9d85-fd67697295a8)

![NPM](https://img.shields.io/npm/v/%40protoqol%2Fdirectus-extension-formatted-numbers)
![NPM](https://img.shields.io/github/actions/workflow/status/protoqol/directus-extension-formatted-numbers/publish.yml)

## Features

- **Smart Abbreviations**: Automatically scales large numbers using standard signifiers (k, M, B, T, P, E, Z, Y).
- **Localisation Support**: Correctly formats abbreviations based on the selected language (e.g., `Mrd.` for German
  Billions, `億` for Japanese). Configure via the "Localisation" field option.
- **Full Value Tooltip**: Hover over any abbreviated number to see the exact, unformatted value in a tooltip.
- **Customisable Appearance**: Add custom prefixes (like currency symbols) and suffixes.

## Installation

In your Directus installation root:

```bash
npm install @protoqol/directus-extension-formatted-numbers
```

or via Directus Marketplace (when available).

## Configuration Options

When configuring a field to use the "Formatted numbers" display, you can customise the following options:

- **Decimals**: Set the maximum number of decimal places to display (default: 2). This controls how accurate the
  displayed number is.
- **Localisation**: Choose the formatting rules for a specific language. Supported languages:
    - English (en)
    - French (fr)
    - German (de)
    - Spanish (es)
    - Japanese (ja)
    - Chinese (zh)
- **Prefix**: Add text or symbols before the number (e.g., `$`, `€`).
- **Suffix**: Add text or symbols after the number (e.g., ` units`, ` EUR`).

## Examples

![Preview](https://cms.protoqol.nl/assets/b368be2b-2acb-4e2a-be9e-228873ea651f)

| Raw Value             | Config            | Output      |
|:----------------------|:------------------|:------------|
| `1,234,567`           | `en`, 2 decimals  | `1.23M`     |
| `123,456,789,000`     | `de`, 1 decimal   | `123,5Mrd.` |
| `5,000`               | `en`, prefix: `$` | `$5K`       |
| `100,000,000,000,000` | `en`              | `100T`      |

## Supported Scales

The extension supports values from thousands up to septillions. Do you require more? Open an issue and we'll add
it!

- **K**: Kilo (10³)
- **M**: Mega (10⁶)
- **B / G**: Giga / Billion (10⁹)
- **T**: Tera / Trillion (10¹²)
- **P**: Peta / Quadrillion (10¹⁵)
- **E**: Exa (10¹⁸)
- **Z**: Zetta (10²¹)
- **Y**: Yotta (10²⁴)

---

Developed by [Protoqol](https://protoqol.nl/).
