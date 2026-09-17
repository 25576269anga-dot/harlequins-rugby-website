# HTML Validation Evidence — A2 HTML5 Website

All three pages of this website were checked using the **Nu Html Checker** (`vnu.jar`), the same validation engine used by the official W3C Markup Validation Service (https://validator.w3.org/nu/).

## How to reproduce this check

1. Open https://validator.w3.org/nu/
2. Choose "Validate by File Upload," select one of `index.html`, `teams.html`, or `register.html`, and click **Check**.
   - Alternatively, once the site is published (GitHub Pages), choose "Validate by Address" and paste the live page URL.
3. Repeat for all three pages.

## Result summary

| Page | Errors | Warnings |
|---|---|---|
| `index.html` | 0 | 0 |
| `teams.html` | 0 | 0 |
| `register.html` | 0 | 1 (informational, explained below) |

**Total: 0 errors across the site.**

## Full raw output

```
"file:/.../register.html":112.13-112.60: info warning: The "date" input type
is not supported in all browsers. Please be sure to test, and consider using
a polyfill.
```

## Explanation of the one warning

`register.html` uses `<input type="date" id="dob" name="dob" required>` for the Date of Birth field in the Membership Registration form. The Nu Html Checker flags this as an **informational warning only** (not an error): `type="date"` is valid, standards-compliant HTML5, but very old browsers may fall back to a plain text field instead of showing a native date picker. This is expected, standard HTML5 behaviour, is explicitly listed as a required HTML5 input type in the assessment brief (section 8.6), and does not affect the validity or functioning of the page in any current browser (Chrome, Edge, Firefox, Safari all support it). No change was made in response to this note, as removing the date input would remove a required HTML5 feature for no real benefit.

## Tooling note

For efficiency during development, validation was run locally with `html5validator` (a Python wrapper around the same `vnu.jar` checker used by validator.w3.org), against all files in the project root, e.g.:

```
html5validator --root . --show-warnings
```

This produced the identical single warning shown above and no errors, confirming the result is consistent with the official online validator.
