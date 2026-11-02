# Contrast

Opal aims at WCAG 2.2 AA in light and dark: 4.5:1 for text (3:1 for large text), and 3:1 for the parts of a control that
identify it (field borders) and for focus indicators.

## How it is measured

- **The page check** (`npm run check`) loads 24 pages in light and dark, at 1280px and 390px wide, and measures every visible
  piece of text against the colour stacked behind it. On 2026-11-02 against Redmine 7.0.2 with the Rubylode plugins mounted it
  measured about 2,800 text pairs per run at desktop width and 3,000 at phone width, and found none below AA: 96 of 96 gated
  runs clean.
- **The tokens**, one pair at a time, below. The check skips text over a gradient or an image, so the header and the primary
  buttons are measured here, at each end of their gradient, and so are field borders and focus rings, which are not text.
  Chip colours are the mixes the stylesheet makes (`color-mix`), worked out on the row colour they sit on.

## Light

| Pair | Foreground | Background | Ratio |
|---|---|---|---|
| Body text on the page | `#1c2833` | `#f4f6f8` | 13.84 |
| Body text on a panel | `#1c2833` | `#ffffff` | 14.99 |
| Secondary text on the page | `#56636f` | `#f4f6f8` | 5.68 |
| Secondary text on a sunken panel or stripe | `#56636f` | `#f3f6f8` | 5.67 |
| Link on a panel | `#16657a` | `#ffffff` | 6.61 |
| Link on a hovered row | `#16657a` | `#e2f0f2` | 5.66 |
| White on the primary gradient, teal end | `#ffffff` | `#1b6b80` | 6.07 |
| White on the primary gradient, lilac end | `#ffffff` | `#4b5d97` | 6.34 |
| Tinted button text | `#11505f` | `#e3f0f2` | 7.71 |
| Delete button text | `#9c2f37` | `#fbe9ea` | 6.24 |
| Header text on the teal end of the wash | `#1c2833` | `#e6f2f4` | 13.12 |
| Header text on the lilac middle | `#1c2833` | `#efeafa` | 12.72 |
| Header links on the peach end | `#2f4150` | `#fcefe7` | 9.35 |
| Status chip New | `#194365` | `#e1ebf3` | 8.55 |
| Status chip In Progress | `#104e57` | `#dfeef0` | 7.84 |
| Status chip Resolved | `#1c532f` | `#e2efe6` | 7.61 |
| Status or priority chip Feedback / High, on a hovered row (the lowest) | `#79530b` | `#dfe2d3` | 5.22 |
| Status chip Closed | `#404750` | `#eaecee` | 7.93 |
| Status chip Rejected | `#78272d` | `#f7e4e6` | 8.09 |
| Priority Immediate, white on red | `#ffffff` | `#a8323b` | 6.59 |
| Field border on a panel (control) | `#7f8c99` | `#ffffff` | 3.43 |
| Field border on the page (control) | `#7f8c99` | `#f4f6f8` | 3.17 |
| Header field border on the lilac middle (control) | `#75828f` | `#efeafa` | 3.33 |
| Focus ring on a panel | `#24808f` | `#ffffff` | 4.61 |

## Dark

| Pair | Foreground | Background | Ratio |
|---|---|---|---|
| Body text on the page | `#e2e8ed` | `#11171c` | 14.61 |
| Body text on a panel | `#e2e8ed` | `#182027` | 13.34 |
| Secondary text on a panel | `#9aa7b3` | `#182027` | 6.71 |
| Secondary text on a sunken panel or stripe | `#9aa7b3` | `#1c252d` | 6.33 |
| Link on a panel | `#6cc4d1` | `#182027` | 8.20 |
| Link on a hovered row | `#6cc4d1` | `#1d3138` | 6.75 |
| White on the primary | `#ffffff` | `#1b6b80` | 6.07 |
| Tinted button text | `#a3e0e8` | `#18323a` | 9.24 |
| Delete button text | `#f2a7ae` | `#35202a` | 7.84 |
| Header links on the teal end of the wash | `#c9d3db` | `#13262c` | 10.31 |
| Header links on the plum middle | `#c9d3db` | `#1d1d30` | 10.88 |
| Status chip New | `#8ab0cf` | `#1b2e3e` | 6.10 |
| Status chip In Progress | `#82bac3` | `#19323a` | 6.26 |
| Status chip Resolved | `#8dbf9e` | `#1c332e` | 6.45 |
| Status or priority chip Feedback / High, on a hovered row | `#e1bf7d` | `#3c4131` | 6.00 |
| Status chip Closed | `#aeb4bc` | `#273038` | 6.42 |
| Status chip Rejected | `#e1979c` | `#38262d` | 6.14 |
| Code block (kept light) | `#1c2833` | `#eef2f5` | 13.32 |
| Field border on a panel (control) | `#6b7a86` | `#182027` | 3.73 |
| Field border on the page (control) | `#6b7a86` | `#11171c` | 4.09 |
| Header field border on the plum middle (control) | `#6b7a86` | `#1d1d30` | 3.74 |
| Focus ring on a panel | `#6cc4d1` | `#182027` | 8.20 |

## Not covered

- Redmine's own avatar colours with white initials: the three that fall below 4.5:1 (red, orange, pink) are darkened; the rest
  are Redmine's.
- Syntax highlighting inside code blocks is Redmine's, made for a light background, which is why code blocks stay light in dark mode.
- Colour is never the only signal: status and priority chips carry their name, and the priority meter its bar count.
