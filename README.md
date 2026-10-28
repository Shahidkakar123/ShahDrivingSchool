# Shah Driving Center

Bilingual (Urdu default / English) static website for Shah Driving Center, Soan Garden, Islamabad.
Plain HTML, CSS and JavaScript. No framework and no build step.

## Structure

```
shah-driving-center/
├── package.json        scripts and the local dev server
├── vercel.json         Vercel config (serves ./public, cache and security headers)
├── .gitignore
├── README.md
└── public/             everything that gets deployed
    ├── index.html      page markup
    ├── css/style.css   styles (light/dark themes, RTL support)
    ├── js/app.js       packages data, Urdu translations, interactions
    └── assets/
        ├── favicon.svg
        └── map-soan-gardens.webp
```

## Run locally

```bash
npm install
npm run dev        # http://localhost:3000
```

## Deploy on Vercel

**Dashboard:** push this folder to a GitHub repository, then in Vercel choose
*Add New > Project*, import the repository and click *Deploy*. No settings need changing.

**CLI:**

```bash
npm i -g vercel
vercel            # preview deployment
vercel --prod     # production deployment
```

## Editing content

All in `public/js/app.js`:

- `C` is the list of course packages (name, price, lessons, features).
- `U` maps each English string to its Urdu translation. A new text with `data-t` in
  `index.html` needs a matching entry here.
- WhatsApp number: search for `923315340282` in `index.html` and `js/app.js`.
- Default language: the `lang` variable near the top of `app.js` (`'ur'` or `'en'`).

## Notes

- Forms open WhatsApp with a pre-filled message. There is no backend or database.
- Fonts load from Google Fonts.
