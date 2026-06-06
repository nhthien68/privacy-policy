# Multi-App Privacy Policy Website (GitHub Pages)

## Objective

Build a GitHub Pages website to host Privacy Policy pages for multiple mobile applications.

Repository name:

```text
privacy-policy
```

Deployment target:

```text
https://<github-username>.github.io/privacy-policy/
```

---

## Directory Structure

```text
privacy-policy/
│
├── index.html
├── assets/
│   ├── css/
│   │   └── style.css
│   └── images/
│
├── app-quay-so/
│   └── index.html
│
├── app-can-lua/
│   └── index.html
│
├── app-battery-alert/
│   └── index.html
│
│
└── README.md
```

---

## Homepage Requirements

URL:

```text
https://<github-username>.github.io/privacy-policy/
```

Purpose:

* Display all applications.
* Allow users to navigate to each app's Privacy Policy page.
* Responsive design.
* Mobile friendly.
* Clean and professional appearance.

Example:

```text
Privacy Policies

- Quay So
- Can Lua
- Battery Alert
```

Each item links to its own privacy policy page.

---

## Privacy Policy Page Requirements

Each application must have its own page:

Examples:

```text
https://<github-username>.github.io/privacy-policy/app-quay-so/

https://<github-username>.github.io/privacy-policy/app-can-lua/

https://<github-username>.github.io/privacy-policy/app-battery-alert/
```

Each page should contain:

### Header

```text
Application Name
Privacy Policy
Last Updated
```

### Sections

1. Introduction
2. Information Collection
3. Advertising Services
4. Analytics Services
5. Third-Party Services
6. Data Retention
7. Children's Privacy
8. Security
9. Changes to This Policy
10. Contact Information

---

## Template Variables

The page generator should support:

```text
{{APP_NAME}}
{{CONTACT_EMAIL}}
{{LAST_UPDATED}}
{{PLAY_STORE_URL}}
```

Example:

```text
App Name: Quay So
Contact Email: support@example.com
Last Updated: 2026-06-06
```

---

## Design Requirements

Style:

* Modern
* Lightweight
* Fast loading
* Pure HTML/CSS
* No framework required

Colors:

```text
Primary: #2563eb
Background: #ffffff
Text: #111827
```

Features:

* Responsive layout
* Mobile friendly
* Clean typography
* SEO friendly

---

## Google Play Compliance

Each application must have a dedicated URL.

Valid examples:

```text
https://<github-username>.github.io/privacy-policy/app-quay-so/

https://<github-username>.github.io/privacy-policy/app-can-lua/

https://<github-username>.github.io/privacy-policy/app-battery-alert/
```

These URLs will be used in:

Google Play Console
→ App Content
→ Privacy Policy

---

## Future Expansion

The structure must support:

```text
20+
50+
100+
applications
```

without requiring additional repositories.

All new applications should only require:

```text
/new-app-name/index.html
```

to be added.

---

## README Requirements

README should include:

### Local Development

```bash
# open index.html directly
```

### GitHub Pages Deployment

Settings
→ Pages
→ Deploy from branch

```text
Branch: main
Folder: /(root)
```

Result:

```text
https://<github-username>.github.io/privacy-policy/
```

---

## Deliverables

Generate:

* index.html
* style.css
* sample app page
* README.md

Ready for GitHub Pages deployment without modification.
