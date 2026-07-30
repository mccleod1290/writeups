# Writeups

Public security writeups from authorized challenges and CTFs.

## Intigriti July 2026 (0726)

**Title:** From blank page to flag: dual `package` JSON and authorization split  
**Target:** [challenge-0726.intigriti.io](https://challenge-0726.intigriti.io/)  
**Class:** Authorization bypass via JSON duplicate top-level `package` keys  
**Date:** 2026-07-30

The app (Registry Observatory) builds protected preflight reports from a base64 JSON manifest. Authorization was checked on the **first** `"package"` object while report generation used the **last**. That split let a dual-package document pass ownership checks and still read the platform-protected `@core/security-notes` report (the flag).

### Read the writeup

- **HTML (recommended):** [intigriti-0726/intigriti-0726-first-principles.html](intigriti-0726/intigriti-0726-first-principles.html)
- Open the file locally in a browser, or use GitHub Pages / raw HTML preview if enabled.

Screenshots and diagram figures live under [`intigriti-0726/images/`](intigriti-0726/images/).

### Layout

```text
.
├── README.md
└── intigriti-0726/
    ├── intigriti-0726-first-principles.html
    └── images/
        ├── 01-landing.jpg
        ├── 02-workspace.jpg
        ├── 03-observatory.jpg
        ├── …
        └── 12-403.jpg
```

### Note

These notes are for **authorized** challenge work only. Do not reuse techniques against systems outside explicit scope.

## License

Writeups are provided as educational material. Challenge branding and assets remain with their owners.
