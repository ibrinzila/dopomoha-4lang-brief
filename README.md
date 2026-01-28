# Dopomoha — Multilingual One‑Pager (RO / EN / UKR / RU)

A single‑file static site with a language switcher and print‑ready A4 layout.

## Quick start (local)
- Open `index.html` directly in a browser, or
- Serve locally:
  ```bash
  python3 -m http.server 8080
  ```
  then visit http://localhost:8080

## Deploy to Cloudflare Pages
1. Create a new Pages project.
2. Choose **Direct Upload** and upload the contents of this folder (or connect a repo).
3. **Framework preset:** None  
   **Build command:** (leave empty)  
   **Build output directory:** `/` (root)
4. Publish. The page is fully static.

## Deploy to Replit
- Create a new Repl using the **HTML, CSS, JS** template.
- Replace the template `index.html` with the one in this project (or upload the whole folder).
- Click **Run** to preview and get a live URL.

## Customize
- Change brand colors in the `:root` CSS vars at the top of `index.html`:
  ```css
  :root{
    --brand-primary:#005BBB;
    --brand-secondary:#FFD500;
    --ink:#111111;
    --ink-2:#555;
    --line:#E6EEF9;
  }
  ```
- Replace the logo placeholder by swapping the `.logo-box` div with an `<img>`:
  ```html
  <!-- Replace this ... -->
  <div class="logo-box">LOGO<br/>PLACEHOLDER</div>
  <!-- ...with: -->
  <img src="assets/logo.svg" alt="Dopomoha logo" width="120" height="120" style="border-radius:12px" />
  ```

## Notes
- The selected language is saved in `localStorage` so visitors return to the last view.
- Printing (to PDF) hides the language pills and locks the acronym grid to 4 columns for a tidy one-pager.
