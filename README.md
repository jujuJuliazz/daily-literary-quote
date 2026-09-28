# Daily Literary Quote

A calm, mobile-friendly static site that shows **one public-domain classical literature quote per day**.

Live site: [https://jujujuliazz.github.io/daily-literary-quote/](https://jujujuliazz.github.io/daily-literary-quote/)

## What it is

- Vanilla HTML, CSS, and a small bit of JavaScript — no build step.
- Quotes live in [`quotes.json`](quotes.json).
- The calendar day is taken in **Asia/Shanghai (UTC+8)**. Quote index is `(day-of-year − 1) mod N`, so every visitor sees the same quote on a given Shanghai calendar day.

## Copyright approach

**Only public-domain English classical literature** is included — for example Austen, the Brontës, Mary Shelley, Melville, Thoreau, Whitman, Shakespeare, Dickens, George Eliot, early Conan Doyle Holmes stories (public domain in the US), and older public-domain English translations of works such as Marcus Aurelius, Homer, or Hugo.

- Short excerpts only (roughly one to four sentences).
- Each entry records text, book title, author, and a note such as `Public domain — Project Gutenberg`.
- **No** modern copyrighted translations and **no** contemporary bestsellers.
- The site footer repeats this disclaimer.

If you are unsure whether a passage is free of copyright where you live, do not add it.

## How to add quotes

1. Open `quotes.json`.
2. Append an object with this shape:

```json
{
  "text": "Your short excerpt here.",
  "book": "Book Title",
  "author": "Author Name",
  "note": "Public domain — Project Gutenberg"
}
```

3. Keep excerpts short and clearly public domain.
4. Commit and push to `main`. GitHub Pages serves from the repository root; the new quote joins the daily rotation automatically (`N` is the array length).

## Local preview

Open `index.html` in a browser, or serve the folder with any static server so `quotes.json` loads over HTTP:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## Deploy

GitHub Pages is configured to publish from the `main` branch root.
