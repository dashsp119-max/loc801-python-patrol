# Python Patrol: Localización Web con una herramienta TAC

**Loc801: Web Localization — Topic 7: Translation Technology Options**

---

## Context

You have been hired to localize a conservation awareness page for **The Nature Conservancy Florida**. The target audience is Spanish-speaking residents of South Florida, many of whom are Colombian, Cuban, or from other Latin American backgrounds. Your target variety is **Miami Spanish** — a contact variety that is heavily influenced by Colombian and Caribbean Spanish and is the dominant Spanish of the Greater Miami area.

The goal: get local Spanish-speaking communities involved in reporting Burmese python sightings before the invasion spreads further.

---

## Repo Structure

```
python-patrol/
├── index.html              ← English source page (do not modify)
├── inicio.html             ← YOUR DELIVERABLE (you will create this)
├── styles.css              ← Shared stylesheet (do not modify)
├── PythonPatrol-base.js    ← Shared logic + UI strings (see Step 3)
└── images/
    ├── python-hero.jpg
    ├── python-capture.jpg
    ├── lionfish.jpg
    ├── seabird-nest.jpg
    └── tallow-tree.jpg
```

---

## Your Tasks

### Step 1: Translate `index.html` Using a CAT Tool

Load `index.html` into the CAT tool of your choice and translate it into Miami Spanish (`es-US`). Save your output as `inicio.html` in the repo root.

**Translate:**
- All visible text content (headings, paragraphs, lists, button labels, form placeholders, image `alt` and `title` attributes, footer links)
- `<meta name="description">`, `<meta name="keywords">`, and Open Graph tags (`og:title`, `og:description`)
- The `<title>` element

**Do not translate:**
- HTML tag names or attribute names
- CSS class names or IDs
- File paths (`src` and `href` values for local files and stylesheets)
- The phone number `1-888-IVEGOT1` — this is a real hotline; keep it as-is

**Set in `inicio.html`:**
- `<html lang="es-US">`
- `og:locale` → `es_US`
- `og:url` → `inicio.html`
- Language switcher: the `class="active"` should move to the Español link

---

### Step 2: Localize External Links

For each external link in `index.html`, check whether a Spanish-language equivalent page exists. If it does, update the `href` and link text in `inicio.html` accordingly.

Check these links at minimum:

| English link | What to look for |
|---|---|
| [IveGot1.org](https://www.eddmaps.org/florida/report/index.htm) | Check the site for a language toggle or Spanish URL |
| [Florida Fish & Wildlife Conservation Commission](https://myfwc.com/wildlifehabitats/nonnatives/python/) | Look for an `es` subdomain or Spanish page |
| [UF IFAS Extension guide](https://edis.ifas.ufl.edu/uw336) | Check for a Spanish PDF or alternate page |
| [New York Times article](https://www.nytimes.com/2019/04/08/us/python-florida.html) | Check NYT en Español |
| [Donate link](https://preserve.nature.org/page/80910/donate/1) | Check for a Spanish version of the donation page |

If no Spanish equivalent exists for a given link, keep the English link but note it in your reflection.

---

### Step 3: Handle the JavaScript String

Open `js/PythonPatrol-base.js`. Near the top you will find a `STRINGS` object with an `en-US` key and an `es-US` key. The `es-US` value is currently a placeholder — the same English text as the source.

**Your task:** Replace that placeholder with your Spanish translation.

This string does not appear in `index.html`, so your CAT tool will not pick it up automatically when you import the HTML file. Think about how you would handle this. Could you enter it into your translation memory manually? Could you create a simple plain-text file containing just this string, run it through your CAT tool first, and add the resulting translation to your TM before tackling the HTML? There is no single right answer, but you should be prepared to explain your approach in your reflection.

---

### Step 4: Publish to GitHub Pages

1. Push your completed repo (including `inicio.html`) to your GitHub account.
2. Go to **Settings → Pages → Deploy from branch → `main` → `/ (root)`**.
3. Wait a minute, then confirm both pages load at your GitHub Pages URL:
   - `https://[your-username].github.io/python-patrol/index.html` → English page
   - `https://[your-username].github.io/python-patrol/inicio.html` → Spanish page
4. Confirm the language switcher in the header links correctly between the two pages.
5. Share your GitHub Pages URL with your instructor.

---

## Deliverables

- `inicio.html` committed to the repo root
- The `es-US` string in `js/PythonPatrol-base.js` translated
- External links updated where Spanish equivalents were found
- A short reflection (see the [assignment page](https://loc801.locessentials.com/t-7/python-patrol-project.html) for the full prompts)
- Your GitHub Pages URL shared with your instructor

---

## Acknowledgements

The webpage for localization here is inspired by this Nature Conservancy article: [https://www.nature.org/en-us/about-us/where-we-work/united-states/florida/stories-in-florida/stopping-a-burmese-python-invasion/](https://www.nature.org/en-us/about-us/where-we-work/united-states/florida/stories-in-florida/stopping-a-burmese-python-invasion/)
