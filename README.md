# Vipin Choudhary — Elite Inner Circle

A single-page fitness coaching website. Plain HTML and CSS in one file, no build step,
no dependencies. Google Fonts is the only external resource.

## Files

- `index.html` — the whole site
- `README.md` — this file

## Run locally

Open `index.html` in a browser. That's it.

Or serve it:

```bash
python3 -m http.server 8000
# visit http://localhost:8000
```

## Deploy on GitHub Pages

1. Create a new repository on GitHub.
2. Upload `index.html` and `README.md` (or push from the terminal — see below).
3. Go to **Settings → Pages**.
4. Under **Source**, pick branch `main` and folder `/ (root)`, then save.
5. The site goes live at `https://<your-username>.github.io/<repo-name>/`.

Pushing from the terminal:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## What to edit before going live

Everything below is a placeholder in `index.html`. Search for it and replace.

| What | Where to look |
|---|---|
| Testimonials | The `<section id="results">` cards — replace name, handle and story |
| Coach photo | The `<div class="photo">` block in `<section id="about">` — swap for `<img src="vipin.jpg" alt="Vipin Choudhary">` |
| Bio | `<section id="about">` paragraphs |
| Prices | `<section id="pricing">` — the `.amt` spans and the lines under them |
| WhatsApp / Join links | Every `href="#"` on a Join Now button. Use `https://wa.me/91XXXXXXXXXX?text=Hi%20Vipin` |
| Contact email | Add to the FAQ section or footer |
| Year in footer | Bottom of the file |

## Changing the colours

All colours are CSS variables at the top of the `<style>` block:

```css
--bg:      #0c0c0e;   /* page background */
--panel:   #141417;   /* cards */
--line:    #26262b;   /* borders */
--ink:     #f5f5f4;   /* text */
--mute:    #a2a2a8;   /* secondary text */
--accent:  #e8b73a;   /* gold highlights and buttons */
```

Change `--accent` alone and the whole site re-themes.

## Adding images

Put image files next to `index.html` and reference them by name:

```html
<img src="transformation-1.jpg" alt="Client transformation">
```

Keep images under about 300 KB each so the page loads fast on mobile.

## Notes

- Responsive down to small phones; layout uses CSS grid and flexbox.
- Respects the visitor's light/dark system setting.
- The copy is original. Replace the placeholder stories with real client
  testimonials you have permission to publish.
