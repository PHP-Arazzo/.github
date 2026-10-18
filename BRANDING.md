# php-arazzo Brand Guidelines

How to present the **php-arazzo** organisation and its repositories consistently. This file lives in the org's `.github` repository so every project can link to it.

> **Name:** php-arazzo (lowercase, hyphenated, in code and in running text)
> **One-liner:** Arazzo workflow descriptions for PHP
> **Idea behind the mark:** *arazzo* is Italian for "tapestry". The logo is a woven grid of threads. Each thread is a step, and an amber thread runs through the weave as the workflow.

---

## 1. Files

```
.github/
├── BRANDING.md
├── brand/
│   ├── php-arazzo-avatar-dark.svg / .png     (1024 × 1024)
│   ├── php-arazzo-avatar-light.svg / .png    (1024 × 1024)
│   ├── php-arazzo-logo-dark.svg / .png       (mark + wordmark, for dark backgrounds)
│   ├── php-arazzo-logo-light.svg / .png      (mark + wordmark, for light backgrounds)
│   └── social-preview.png                    (1280 × 640)
└── profile/
    └── README.md                             (org profile page)
```

| File | Use it for |
| --- | --- |
| `php-arazzo-avatar-dark` | Org avatar and dark backgrounds. **Default.** |
| `php-arazzo-avatar-light` | White or paper backgrounds: docs sites, slides, print. |
| `php-arazzo-logo-dark` | Wordmark lockup where the page background is dark. |
| `php-arazzo-logo-light` | Wordmark lockup where the page background is light. |
| `social-preview` | Repository social preview image (GitHub requires PNG or JPG, 1280 × 640). |

The wordmark lockups have the text converted to outlines, so they render correctly without the fonts installed. Always use the exported files. Do not redraw, stretch, recolour or crop the mark.

---

## 2. Colour

| Name | Hex | Role |
| --- | --- | --- |
| Loom Indigo | `#1B1942` | Dark backgrounds, primary text on light |
| Thread Violet | `#777BB4` | Main brand colour |
| Lavender | `#B9BEF2` | Secondary text and accents on dark |
| Amber Thread | `#F5A524` | The single accent: highlights, links, badges |
| Paper | `#F4F3FA` | Light backgrounds |

Supporting thread tones used inside the mark: `#8892D6`, `#9AA3E8`, `#A5ABEA`, `#8D93D8`, `#6A6FA8`.

**Rules**
- Amber is an accent. Use it for one or two things per page, never as a background.
- On dark backgrounds use Paper or Lavender for text. On light backgrounds use Loom Indigo for text.
- Don't put Violet text on Indigo or Amber text on Paper. Both pairings are low-contrast.
- The light variants use a darker amber (`#E8890C`) for legibility on Paper.

---

## 3. Typography

| Role | Font | Notes |
| --- | --- | --- |
| Headings and wordmark | **Bricolage Grotesque**, Bold | Wordmark is lowercase: `php-arazzo` |
| Body and docs | **DM Sans**, Regular / Medium | |
| Code, package names, CLI | **JetBrains Mono** | |

All three are free on Google Fonts. GitHub itself doesn't allow custom fonts, so these apply to the docs site, slides, social images and other external material.

---

## 4. Logo usage

- **Clear space:** keep at least a quarter of the logo's width free on every side.
- **Minimum size:** 20 px on screen. Below that, use the avatar only, never the wordmark lockup.
- **Do:** use the dark variants on dark or neutral backgrounds and the light variants on white or Paper.
- **Don't:** rotate it, add shadows or outlines, recolour the threads, change the amber thread, or place it on busy photos.
- **Original mark:** it does not use the PHP elephant or the PHP logo. php-arazzo is an independent implementation of the Arazzo Specification. Say so in READMEs unless the project gains official status.

---

## 5. GitHub setup checklist

- [ ] **Org avatar:** Org Settings → Profile → upload `brand/php-arazzo-avatar-dark.png`
- [ ] **Org profile README:** `profile/README.md` in this repo (already written; the repo must be public)
- [ ] **Repo social preview:** Repo Settings → Social preview → upload `brand/social-preview.png`
- [ ] **Repo description:** short, plain, starts with the project's purpose
- [ ] **Topics:** `php`, `arazzo`, `openapi`, `api-workflows`, `workflow`, `composer`
- [ ] **Org description and website:** set under Org Settings → Profile
- [ ] **Pin** the main repositories on the org profile

---

## 6. README header for each repository

````markdown
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/PHP-Arazzo/.github/main/brand/php-arazzo-avatar-dark.svg">
    <img alt="php-arazzo" src="https://raw.githubusercontent.com/PHP-Arazzo/.github/main/brand/php-arazzo-avatar-light.svg" width="96">
  </picture>
</p>

# [package-name]

[One sentence: what it does and for whom.]

```bash
composer require [vendor/package]
```
````

**Badges:** keep them to one row and at most 4–5: CI status, latest release, PHP version, license. Use the default shields.io colours so they stay recognisable.

---

## 7. Voice

- Plain, practical, friendly. Explain complex ideas simply and avoid jargon where a normal word works.
- Lead with what the thing does, then how to use it.
- Short sentences. Show a code example early.
- Use "workflow", "step" and "thread" consistently. Don't mix in synonyms.

**Repository naming:** lowercase, hyphenated, descriptive, for example `php-arazzo`, `arazzo-runner`, `arazzo-validator`.

---

## 8. Quick reference

```
Name        php-arazzo
Dark bg     #1B1942      Light bg    #F4F3FA
Primary     #777BB4      Secondary   #B9BEF2
Accent      #F5A524      (light mode accent #E8890C)
Fonts       Bricolage Grotesque / DM Sans / JetBrains Mono
Avatar      brand/php-arazzo-avatar-dark.svg  (default)
```
