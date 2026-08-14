# Mwanza Mumba — portfolio site

Plain HTML, CSS and JavaScript. No build step, no framework, no dependencies.
Open `index.html` in a browser and it runs.

## Structure

```
portfolio/
├── index.html          all the page content
├── css/styles.css      all styling; colours and fonts are variables at the top
├── js/main.js          mobile menu toggle and footer year
├── assets/
│   ├── hero.png        hero image
│   └── Mwanza_Mumba_CV.docx   file served by the "My Resume" button
└── README.md
```

## Editing

**Colours and fonts** — the `:root` block at the top of `css/styles.css`.
Change `--accent` in one place and the whole site follows.

**Adding a project** — copy one `<li class="card">` block in `index.html` and
edit the text. The grid reflows on its own; you do not need to touch the CSS.

**Contact details** — the `.contact-list` block in `index.html`.

## Before you publish

- [ ] Replace `assets/Mwanza_Mumba_CV.docx` with a **PDF** version. A .docx
      download opens badly on phones and lets anyone edit it. Export to PDF
      and update the `href` in the "My Resume" button.
- [ ] Check the GitHub URL in the contact list — `github.com/mwanzamumba` is a
      guess based on your CV. Fix it if it is wrong.
- [ ] Confirm both project links still load: laisheni.web.app and
      elect-project-d4c29.web.app. A dead link on a portfolio is worse than no
      link.

## Deploying

Since you already use Firebase Hosting for your other projects:

```bash
firebase init hosting     # set public directory to the folder holding index.html
firebase deploy
```

GitHub Pages also works — push this folder to a repo named
`mwanzamumba.github.io` and it serves automatically.

## Accessibility notes

Keyboard focus is visible, there is a skip link, the hero image has alt text,
and `prefers-reduced-motion` is respected. If you add animation later, keep it
inside that media query so it stays switchable.
