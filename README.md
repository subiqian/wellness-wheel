# wellness wheel ♥

A retro-vaporwave spider chart for mapping your wellness across life's pillars — score them in hearts, color your wheel, jot a note, then copy the image and share it with someone.

**▶ Use it here: [subiqian.github.io/wellness-wheel](https://subiqian.github.io/wellness-wheel)**

No install, no account, no data stored. It's one HTML file.

## How to use it

1. **Score your pillars.** Every wheel starts with five: Mental, Physical, Productivity, Sociability, Energy. Click the hearts (0 = struggling, 5 = thriving), or click/drag directly on the chart — anywhere inside the grid snaps that pillar to the value you point at.
2. **Add your own pillars** — up to two extra, named whatever you like (Finances? Creativity? Cat time?). Remove them with the × button.
3. **Pick a color.** Nine swatches; the wheel, hearts, title bars, and copy button all follow along. Every fresh visit deals you a random one.
4. **Name it and note it.** The chart window's title is editable, and the note cell below the chart holds a short two-line message.
5. **Copy & share.** The pulsing button beside the chart copies a framed PNG — title bar, scores, wheel, your note, and a datetime + location stamp — straight to your clipboard. Paste it to whoever should see it. ♥

### The two scores

- **average wellness** — a straightforward arithmetic mean of your pillar scores.
- **estimated functionality** — a range, because a spider chart's shaded area doesn't track the mean: area compounds, each pillar scaling its neighbors, so the same scores can shade more or less of the wheel depending on how they're arranged. The range spans the worst possible arrangement to the best, measured against a steady all-3s wheel — 100% means baseline functional, and scores above 3 push past 100%. Hover either score on the page for the full explanation.

## Sharing a live wheel

Your wheel is encoded in the URL as you edit (everything after the `#`). Copy the address bar and send it — the link opens your exact wheel, scores, note, color and all. Opening the bare URL always starts a fresh, empty wheel.

## Privacy

- Nothing is saved anywhere — no cookies, no localStorage, no server. Close the tab and it's gone (unless you kept the URL).
- The stamp shows your time zone by default. A real city appears only if you click the 📍 and grant permission; your coordinates are sent once to a geocoding service to be turned into a city name, and only the name is kept, in your browser.

## Running it yourself

It's a single self-contained `index.html` — no build, no dependencies.

```
git clone https://github.com/subiqian/wellness-wheel.git
open wellness-wheel/index.html
```

One caveat: the copy-to-clipboard button needs a secure context (HTTPS or `localhost`). From a plain `file://` open it falls back to downloading the PNG instead — for the full experience, serve it:

```
cd wellness-wheel && python3 -m http.server 8000
# then visit http://localhost:8000
```

---

*♥ 0 = struggling · 5 = thriving ♥*
