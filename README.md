# Gauntlet

Gauntlet makes trial sheets: a printable PDF with one problem on each page.
You paste a list of problems, and it sets each one in a titled box with room to work below it.
The pages use the black and white print style of [Istari](https://github.com/TheScholium/istari).

It is one HTML file. It has no build step and no server.

## Use it

Open the page, paste your problems into the box on the left, and click **Save as PDF**.
In the print window, choose Save as PDF, set the paper size to match the page, and turn off headers and footers.

If this repository has GitHub Pages turned on, the page is at
`https://thescholium.github.io/gauntlet/`.
You can also download `index.html` and open it in your browser.
It needs an internet connection to load the math library and the fonts.

## Write the problems

A line of three dashes (`---`) starts a new problem.
The first block can be a header. It is optional.

```
title: Trial 3
course: PHYS 311
date: 30 October 2026
note: Closed book. Show all of your work.
---
# Gauss's law
points: 10
A sphere of radius $R$ carries the charge density $\rho(r)=kr$.
(a) Find $\vb E$ inside and outside the sphere.
(b) Find the energy in the field:
$$U=\frac{\epsilon_0}{2}\int E^2\,d\tau$$
---
# Next problem
...
```

| Part | How to write it |
| --- | --- |
| Header | Lines `title:`, `course:`, `date:`, `note:` in the first block |
| Problem title | A first line that starts with `#` |
| Points | A line `points: 10` after the title |
| Parts | Lines that start with `(a)`, `(b)`, `(i)`, and so on |
| Lists | Lines that start with `-` or `1.` |
| Emphasis | `**bold**`, `*italic*`, `` `code` `` |
| Math | `$inline$` and `$$display$$`, rendered with KaTeX |

Short macros are available: `\R`, `\C`, `\N`, `\Z` (number sets), `\vb E` (bold vector), and `\dd` (a thin space and an upright d).

## Options

- **Paper**: US Letter or A4.
- **Text size**: 11 to 14 pt.
- **Work area**: blank, ruled, or dot grid.
- **Cover page**: a title page with a table of the problems and the total points.

If a problem is too long for one page, it continues on a second page, and the panel shows a warning.

## Privacy

Your problems stay in your browser. The page does not send them anywhere.
It saves your last text and options in the browser's local storage, so that they are there when you come back.
The page loads the KaTeX library from cdnjs and the fonts from Google Fonts.

## Limits

- The page does not draw figures. Add a figure by hand after you save the PDF.
- It does not read problems from an image or a PDF. Write them as text, or ask for an image mode.
- Tested in Chromium. Safari and Firefox are not tested.

## Credits

Math is set by [KaTeX](https://katex.org). Fonts are EB Garamond, Cormorant Garamond and JetBrains Mono.

## License

MIT. See `LICENSE`.
