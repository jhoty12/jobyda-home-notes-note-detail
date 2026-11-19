# Notes Portal — Jobyda Akter Jhoty's part

**Jobyda Akter Jhoty** · Student ID `02725105101094` · Member · 66th Batch, Section B
**Pages (points 1, 2, 3): Home, Notes, Note Detail**

This is a runnable mini-app with ONLY Jobyda Akter Jhoty's pages from the City
University Notes Sharing Portal, plus the minimum shared shell needed
to run it (header, footer, login, localStorage demo data, styles and
images). The other members' pages are in their own zips, not here.

## How to open

Serve this folder, then open it in a browser (opening `index.html`
directly with `file://` may work, but serving is the reliable way):

```bash
# from inside this folder (jobyda-home-notes-notedetail/)
python3 -m http.server 8000
```

Then open http://localhost:8000

Or use VS Code Live Server on this folder.

## Always logged in

This mini-app opens **already logged in as Rafiq Ahmed (student, rafiq@city.edu)** — no need to sign in. If you log out, just reload the page and it signs back in automatically.

## Demo logins

| Role | Email | Password |
| --- | --- | --- |
| Admin | admin@city.edu | Admin@123 |
| Student | rafiq@city.edu | Student@123 |
| Student | nusrat@city.edu | Student@123 |
| Student | tanvir@city.edu | Student@123 |
| Moderator | mim@city.edu | Student@123 |

## What is inside

- `index.html` — standalone shell (`#app`, dark-mode pre-paint, fonts)
- `js/app.js` — the app: only Jobyda Akter Jhoty's pages + the shared shell
- `js/data.js` — seed data (`window.PLAIN`): 294 courses, 5 users,
  7 sample notes, ratings, comments, bookmarks, notices
- `css/styles.css` — the portal stylesheet (same design as the full site)
- `assets/` — logo and photos

## Standalone demo — no backend

This build has **NO backend**. All data lives in `js/data.js` as
`window.PLAIN`, and any changes you make while using the site (uploads,
approvals, new accounts) are stored in the browser's **localStorage
under the key `notesPortalPlainV1`**. Clear that key (or clear site
data) to reset the demo back to the seed data.

A small login form is included as part of the shared shell so the
pages can be signed in to — the full Log In / Create an Account /
Forgot Password pages belong to Purnima Maria Palma's part.

## Security note

The demo passwords in `js/data.js` are **plain text ONLY for this
demo**, so the site works with no server at all. The real backend
(`backend-mysql/`) stores passwords as bcrypt hashes only and never
puts a password in any client file. Do not use these demo passwords
anywhere real.
