# agoshsaini.com

Personal portfolio website for Agosh Saini — built with plain HTML/CSS/JS and deployed on Vercel.

## Stack

- **HTML/CSS/JS** — no framework, no build step
- **Vercel** — hosting + analytics
- **Google Fonts** — Space Grotesk, Manrope, Inter (+ Press Start 2P for the game)

## Structure

```
.
├── index.html          # Main site — one-page summary
├── game.html           # AGOSH.EXE — "under construction" placeholder (served at /game)
├── WIP/game.html       # Work-in-progress playable game version (not linked/deployed)
├── Branding/           # Design system & brand guidelines
│   ├── DESIGN.md       # Design tokens, typography, principles
│   └── agosh-brand.html # Visual brand reference
├── Inspiration/        # Design inspiration files
├── vercel.json         # Hosting config (clean URLs, headers)
├── .vercelignore       # Excludes WIP/ from deployment
└── .gitignore
```

## Local development

No build step — serve the folder and open it:

```sh
python3 -m http.server 8765
# → http://localhost:8765/index.html
# → http://localhost:8765/game.html  (/game on Vercel via cleanUrls)
```

## Links

| | |
|---|---|
| Website | https://agoshsaini.com |
| Email | contact@agoshsaini.com |
| LinkedIn | https://www.linkedin.com/in/agosh-saini/ |
| GitHub | https://github.com/agosh-saini |
| X / Twitter | https://x.com/its_agosh |
| Substack | https://substack.com/@agoshsaini |
| Google Scholar | https://scholar.google.ca/citations?hl=en&user=yFrqYN4AAAAJ |
| Resume | https://drive.google.com/file/d/1lmRAQ4jczjBn-2LT8NZ2zeip6X8I0WXH/view?usp=drive_link |

## License

Dual-licensed — see [LICENSE](LICENSE) for details:

- **Code** (HTML/CSS/JS, design system, config) — MIT. Take it and build your own version.
- **Personal content** (name, story, experiences, projects, publications, photos) — © 2026 Agosh Saini, all rights reserved. Swap in your own story; don't republish his.
