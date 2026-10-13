# test-manager-library-3145556-page

> **Technical test · ADSO group 3145556**: static public site that presents *Manager Library* (T-23).

## Rules it follows

| Rule | How |
|---|---|
| Never talks to the API | Plain HTML and CSS: no JavaScript and no `fetch` |
| Exposes no personal data | No member or librarian data (`data-model.md` §7) |
| Works on phone and desktop | `auto-fit` grid and `clamp()` typography; checked at 375 px and 1280 px |

The site content is in Spanish because it is shown to users (ADR-015).

## How to open it

- Locally: open `index.html` in the browser, with no server and no API.
- Publishing: GitHub Pages → *Settings → Pages → Deploy from a branch → `main` / root*.

## Evidence (T-23)

```bash
grep -c "fetch\|<script" index.html   # 0: it never calls the API
```
