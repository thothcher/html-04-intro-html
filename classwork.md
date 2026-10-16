# H/04 · Classwork

One classwork, 15 minutes, on **your own restaurant page** (a restaurant you invent or pick). Le Bistro is the lecturer's demo — look at it for the pattern, don't copy it.

No AI today. You write every character.

---

## Classwork 1 · Your restaurant's HTML skeleton (slide 23, before break)

Build a valid HTML page for a restaurant you choose. No CSS yet — structure and content only.

### Base (everyone)

1. Create a folder named after your restaurant (no spaces, lowercase), for example `casa-mia/`.
2. Inside it, create `index.html`.
3. Write the document shell from memory — no copying:
   ```
   DOCTYPE declaration
   html with lang attribute
   head with charset meta, viewport meta, and title
   body (empty for now)
   ```
4. Add content to `<body>`:
   - One `<h1>` with the restaurant name
   - Two `<h2>` headings: one for "Menu", one for "About us"
   - Under the Menu heading: a `<ul>` with at least four dishes (name and price)
   - Under the About heading: a `<p>` with two sentences about the restaurant
   - One `<img>` of a dish — use any photo URL from the web. Give it meaningful `alt` text.
   - One `<a>` link to a reservation page (`href="reserve.html"` is fine — the file doesn't need to exist yet)
   - One `<button type="button">` that says "Order now"

### Plus

- Change one list item to also show a short description: use a `<dl>` / `<dt>` / `<dd>` pattern for at least three dishes.
- Add a second page, `reserve.html`, with a heading, a paragraph and a "Back to home" link.
- Add `loading="lazy"` to your image and verify it appears in the HTML source.

### Pro

- Add a second image and write a caption for it using `<figure>` and `<figcaption>`.
- Validate your page at [validator.w3.org](https://validator.w3.org) — zero errors, zero warnings.
- Navigate the page with only the keyboard (Tab, Enter, Space). Can you reach every link and button?

### Done when

- [ ] `<!DOCTYPE html>` on line 1, exact spelling
- [ ] `<meta charset="utf-8">` and `<meta name="viewport" ...>` in `<head>`
- [ ] `<title>` is the restaurant name, not "Document"
- [ ] All four content types are in the body: heading, list, image, link
- [ ] The image has non-empty, descriptive `alt` text
- [ ] No errors in browser DevTools console

### Common problems (for the lecturer)

| Problem | Fix |
|---|---|
| `<!doctype HTML>` (wrong case) | The tag is case-insensitive, but `<!DOCTYPE html>` is the convention |
| `<meta charset>` is in `<body>` | It belongs in `<head>`. The browser stops reading charsets once the body begins |
| `alt=""` left empty | Make them write what the image shows: "Bowl of ratatouille, served with herbs" |
| `<button>` inside `<a>` | A button cannot be inside a link — they are separate interactive elements |
| `<img src="...">` shows broken icon | URL is wrong or the browser blocked a mixed-content image. Try a different URL |
| Page is "display none" because of typo | Usually a missing `>` somewhere. Open DevTools → Elements and look for mismatched nesting |
