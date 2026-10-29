# Gauntlet

Gauntlet takes a list of problems and gives you a printable PDF with one problem on each page. It is one HTML file. It has no build step and no server.

The pages use the black and white print style of [Istari](https://github.com/TheScholium/istari).

## Use it

Open the page, paste your problems into the box on the left, and click **Save as PDF**.
In the print window, choose Save as PDF, set the paper size to match the page, and turn off headers and footers.

`https://thescholium.github.io/gauntlet/`.
You can also download `index.html` and open it in your browser.
It needs an internet connection to load the math library and the fonts.

## Write the problems

A line of three dashes (`---`) starts a new problem.
The first block can be a title page, but that is optional.

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
| Figures | A line that holds only `![description](file.png)`. See [Figures](#figures) |

Short macros are available: `\R`, `\C`, `\N`, `\Z` (number sets), `\vb E` (bold vector), and `\dd` (a thin space and an upright d).
Write `\dd` in front of the variable: `\int E^2\,\dd\tau`.

## Figures

Put a figure on a line of its own:

```
![Circuit with two resistors](circuit.png)
```

Add `{width=50%}` after the line to set the width. Without it, a figure keeps its own size, up to the width of the box and a height of 3.2 in.

The name in the brackets is a file. To give Gauntlet the file:

1. Drop the image files on the page, or click **Add figures**. PNG, JPEG, GIF, WebP and SVG files work.
2. Write the file name in the problem. Upper and lower case do not matter. A folder in front of the name is ignored.

Gauntlet keeps the files in your browser, so they are there when you come back. **Remove** deletes one file. **Remove all** deletes all of them.
If a file is not in the list, the preview shows a red box, and the panel names the missing file.

You can use a web address (`https://...`) or a `data:image/...` address in place of a file name. A web address makes your browser ask that site for the picture.
A figure must be alone on its line. It cannot sit inside a sentence.

## Options

- **Paper**: US Letter or A4.
- **Text size**: 11 to 14 pt.
- **Work area**: blank, ruled, dot grid, or lined grid. The "Pattern at 2/3 scale" option makes the lines or dots 2/3 as far apart.
- **Cover page**: a title page with a table of the problems and the total points. In the saved PDF, each problem on the title page is a link to its page, and each problem page has a Contents link back to the title page.

If a problem is too long for one page, it continues on a second page, and the panel shows a warning.

## Privacy

Your problems stay in your browser. The page does not send them anywhere.
It saves your last text and options in the browser's local storage, so that they are there when you come back.
It saves your figure files in the browser's IndexedDB. Use **Remove all** to delete them.
The page loads the KaTeX library from cdnjs and the fonts from Google Fonts.
A figure with a web address is the one case where the browser contacts another site.

## Limits

- The page does not draw figures. It shows picture files that you give it (see [Figures](#figures)).
- A figure is always centered on its own line. It cannot sit beside text or beside another figure.
- It does not read problems from an image or a PDF. Write them as text, or ask for an image mode.
- Tested in Chromium. Safari and Firefox are not tested.

## Credits

Math is set by [KaTeX](https://katex.org). Fonts are EB Garamond, Cormorant Garamond and JetBrains Mono.

## License

MIT. See `LICENSE`.
