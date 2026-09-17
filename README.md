# Port Moresby Harlequins Rugby Union Club — Website

**ISO229 Web Design — Assessment 2: Web Design Using HTML5 and Text/Web Editor**
Bachelor of Business in Information Technology | 2026

Student Name: _Ande Gabbii____________
Student ID: ___25576269_______________

A three-page semantic HTML5 website for a fictional/student-project rugby union club, built with hand-written HTML5 and basic CSS3 only — no frameworks, no downloaded templates, per the A2 brief.

---

## 1. Submission checklist (per Assessment Handbook §8.9)

| # | Requirement | Where to find it |
|---|---|---|
| 1 | GitHub repository URL | *Add your repository link here once pushed:* `https://github.com/YOUR-USERNAME/YOUR-REPO` |
| 2 | Published website URL | *Add your GitHub Pages (or other approved host) link here:* `https://YOUR-USERNAME.github.io/YOUR-REPO/` |
| 3 | `README.md` | This file |
| 4 | Complete source code and assets | `index.html`, `teams.html`, `register.html`, `css/style.css`, `images/` (all in this package) |
| 5 | HTML validation evidence | `validation-evidence.md` in this package |
| 6 | Meaningful Git history | Create your repository and commit progressively (see §5 below) — a single final upload will not satisfy this requirement |
| 7 | AI Use Declaration | §6 below |

## 2. Pages (recommended A2 structure)

| File | Purpose |
|---|---|
| `index.html` | **Home** — club introduction, history, "why join," latest news and a photo gallery |
| `teams.html` | **Information / Services** — teams and grades, weekly training schedule table, rugby development content |
| `register.html` | **Contact / Registration** — club contact details table and a substantial membership registration form |
| `css/style.css` | Single external stylesheet for all pages — colour, typography, spacing and basic presentation only |

All three pages share the same header, navigation and footer, and link to one another.

## 3. How to view the site

- **Locally:** double-click `index.html` (or any page) to open it in a browser — no build step or server required.
- **Published:** deploy the whole folder to GitHub Pages (Settings → Pages → deploy from the `main` branch / root) and use the resulting URL.

## 4. Design notes

- **Colour palette:** drawn from the club's crest/jersey — navy (`#14213d`), pink/magenta (`#d6236a`), green (`#1f8a4c`), teal (`#0f7fa8`) and gold (`#e0a629`) — applied as CSS custom properties in `:root`.
- The club crest (`images/logo.png`) appears in the header on every page.
- **Typography:** Georgia for body/headings, Trebuchet MS for navigation and UI labels — both web-safe, no external font loading required.
- Per the assessment's "basic CSS" scope (§8.7), styling covers colour, type, spacing and simple flexbox rows for nav/cards/photo galleries only — no CSS Grid, no animation library, no responsive framework. Advanced/responsive CSS is deliberately left for A3. One `@media` breakpoint stacks navigation and cards on small screens.

## 5. Semantic HTML5 & accessibility features

- Landmark elements throughout: `header`, `nav`, `main`, `section`, `article`, `footer`.
- A "Skip to main content" link for keyboard users.
- Visible focus outlines on all interactive elements.
- Logical heading hierarchy (`h1` in the header, `h2` per section, `h3` in cards/subsections).
- `figure`/`figcaption` used for every photograph, with descriptive `alt` text on all images.
- Data tables use `<caption>` and `<th scope="col">` / `<th scope="row">` (training schedule, contact details).
- Every form control has an associated `<label for="">`; related fields are grouped in `<fieldset>`/`<legend>`.
- Native HTML5 validation: `required`, `type="email"`, `type="tel"` with a `pattern`, `type="date"`, and appropriate `select`/radio/checkbox controls.
- Radio groups use `role="radiogroup"` with `aria-label` for extra clarity.

## 6. Suggested Git workflow (for a meaningful commit history)

The brief requires progressive commits, not one final upload. A suggested minimum sequence once you have this folder:

```
git init
git add README.md
git commit -m "Add README and project plan"

git add index.html css/style.css images/logo.png
git commit -m "Add global structure and Home page"

git add teams.html
git commit -m "Add Teams & Activities page with training schedule table"

git add register.html
git commit -m "Add Contact & Registration page with membership form"

git add validation-evidence.md
git commit -m "Add HTML validation evidence"

git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

Then enable GitHub Pages under **Settings → Pages** and record the live URL above.

## 7. Images

`images/` contains only photos that are actually used on the site: the club crest, current squad and championship-team photos, and match-action shots, each with descriptive filenames and `alt` text.

## 8. Content sourcing & honesty notes

Some club background (founding year, competition, and reported historic titles) is presented as sample content for a student website, **not verified official club copy**. Before any real-world use:

- Confirm founding date, competition name, and historic titles directly with the club.
- Replace the contact email/phone and social links with the club's real ones.
- Confirm training times/venue directly with the club.

## 9. Validation evidence

See `validation-evidence.md`. Summary: **0 errors** across all three pages when checked with the Nu Html Checker (same engine as the W3C validator). One informational note on `register.html` about `type="date"` browser support — expected HTML5 behaviour, not an error.

## 10. AI Use Declaration

**AI Used:** I used generative AI (Claude) throughout the development of this project to:
- Review the HTML against the ISO229 A2 assessment brief and rubric, and identify gaps against the required elements list (semantic structure, forms, tables, figures, validation attributes).
- Help build and iterate the three pages, external stylesheet, and membership registration form, including HTML5 input types and validation attributes.
- Fix specific defects it identified (e.g. a broken stylesheet path, an invalid heading nested inside an inline element).
- Wire in the real club crest and team photographs supplied for this project, and align the CSS colour palette with the club's crest/jersey colours.
- Restructure the third page into a contact-information-plus-registration-form page in line with the brief (§8.4), and remove unrelated merchandise/e-commerce content that fell outside the assessment's scope.
- Run local HTML validation (`html5validator`, the same engine as the W3C Nu Html Checker), summarised in `validation-evidence.md`, and assemble the final submission package.

I reviewed, tested and understand every part of the submitted HTML, CSS and form logic, and can explain and modify any section of it if asked.
