# digidigi.ee

Website of Digidigi MTÜ, an Estonian non-profit association promoting cybersecurity
and information security awareness. Live at <https://digidigi.ee/>.

## How it works

Plain HTML and CSS with no build step and no JavaScript. GitHub Pages publishes the
`main` branch on every push, and the `CNAME` file binds the site to digidigi.ee.

| File | Purpose |
|---|---|
| `index.html`, `style.css` | The page and its styles |
| `404.html` | Shown for any address that does not exist |
| `logo.svg` | Temporary "DD" logo |
| `favicon.svg`, `favicon.ico`, `apple-touch-icon.png` | Browser tab and home-screen icons, drawn from the logo |
| `og-image.png` | Preview image shown when the link is shared |
| `robots.txt`, `sitemap.xml` | For search engines |
| `.well-known/security.txt` | Security contact, per RFC 9116 |
| `_config.yml` | Tells GitHub Pages which files to publish |

## Preview locally

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000/>.

## Keep up to date

- `.well-known/security.txt` has an `Expires` date of 1 November 2027. Move it forward
  before then, and change the contact once a domain mailbox exists.
- `sitemap.xml` has a `lastmod` date. Update it when the page content changes.
- The PNG and ICO icons are rendered from the SVG files. Regenerate them if the logo changes.
- GitHub Pages skips folders that start with a dot, except `.well-known`, which
  `_config.yml` allows. Keep it that way so local tool settings are never published.

## Reporting a security issue

See <https://digidigi.ee/.well-known/security.txt>.
