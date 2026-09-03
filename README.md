# IFL Madrid — static site

A single-page static site for IFL Madrid, the non-profit international futsal league
running in Madrid since 1988. It covers what the league is, how the Sunday league works,
the full rulebook, the Wednesday kickabout WhatsApp group, and the contact address.

Anything that changes week to week — fixtures, tables, teams, results, Pichichi — lives on
a different platform. This site is deliberately static and is not intended to be updated.

## Files

```
index.html          the whole site
src/input.css       Tailwind entry + design tokens (@theme)
css/style.css       built output — committed, this is what index.html loads
img/ifl-logo.png    club logo, taken from iflmadrid.com
```

## Working on it

```sh
npm install
npm run dev      # rebuild css/style.css on change
npm run build    # one-off minified build
npm run serve    # http://localhost:4000
```

`index.html` references `css/style.css` directly, so **you must run `npm run build`
after editing any class names in the HTML** or the change won't show up.

## Deploying

Upload `index.html`, `css/` and `img/` to any static host. There is no server-side
component, no JavaScript, and no build step at request time.

## Design

Colours are sampled from the club logo and the original site:

| Token    | Hex       | Used for                          |
| -------- | --------- | --------------------------------- |
| `brick`  | `#c22d18` | Nav bar, contact section          |
| `flame`  | `#e54028` | Logo red — headline accents       |
| `amber`  | `#e99300` | Logo gold — eyebrows, rule numbers |
| `ink`    | `#17161a` | Dark sections, footer             |
| `bone`   | `#f6f3ef` | Page background                   |

Type is Archivo Black for display and Open Sans for body — Open Sans is what the original
site uses. The recurring `-9°` skew (`.slant` / `.unslant` in `src/input.css`) echoes the
italic "IFL" in the logo.

## Content

The rules are paraphrased from the IFL Madrid rulebook rather than copied. If the
Committee's version and this page ever disagree, the Committee's version wins.

Contact: iflmadrid1988@gmail.com
