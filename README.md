<div align="center">

# 🧪 MIT CODE LAB

### The workbench — where ideas become experiments.

**Twelve research and build projects, from shipped systems to confidential work in progress.**

[![Live site](https://img.shields.io/badge/🌍_live-mitcodelab.github.io-8130F1?style=for-the-badge)](https://mitcodelab.github.io/)
[![Checks](https://img.shields.io/badge/browser_checks-160%2F160-2ea44f?style=for-the-badge&logo=playwright)](#-tested)
[![a11y](https://img.shields.io/badge/axe--core-0_violations-2ea44f?style=for-the-badge)](#-tested)
[![Languages](https://img.shields.io/badge/🌐-EN·TL·ES·FR-1f2937?style=for-the-badge)](#-features)

</div>

---

## 👋 What is MIT CODE LAB?

The **workbench** of the ecosystem. It's where experiments are run, prototypes are built, and papers are written, before the finished work is listed in [MITLIVE](https://mitlive.github.io/).

> 🧭 **Ecosystem:** ⚙️ [QSTYX](https://qstyx.github.io/) (the machine) → 🧪 **MIT CODE LAB** (the workbench) → 🌐 [MITLIVE](https://mitlive.github.io/) (the catalog)

## 🔬 The lab

| ID | Project | Status |
|---|---|---|
| LAB-01 | 🏫 Project CUP | ✅ Shipped · 🟢 Live |
| LAB-02 | 🏠 SmartHome Theft Alert | ✅ Shipped · 📝 Paper in progress |
| LAB-03 | 🩺 Specea | 🔨 In progress |
| LAB-04 | 🗣️ AyraTalk | ✅ Shipped · 🟢 Live |
| LAB-05 | 📡 Project Styx | 🔨 In progress |
| LAB-06 | 🔊 Acoustic Shepherd | 🧪 Prototype · 🟢 Demo live · 📝 Paper in progress |
| LAB-07 | ☁️ Project Cloud9 | 🔨 In progress |
| LAB-08 | 🌾 Bannawag Network | ✅ Shipped · 🟢 Live |
| LAB-09 | 👁️ Project Hawkeye | ✅ Shipped · 🟢 Live |
| LAB-10–12 | 🔒 Projects X / Y / Z | Confidential |

*Status source: the owner, 2026-09-29.*

## ✨ Features

- 🎠 **3D coverflow carousel** of animated SVG covers that react on hover
- 🔍 **Explorer** — search, filters, sort and a *Live only* toggle
- 📂 **Project drawer** with shareable deep links (`#project/<id>`)
- 🧬 **Lifecycle view** — 10 stages from idea to archived, plus MITLIVE
- 🕸️ **Technology map** — projects linked by shared themes
- ✉️ **Send chooser** — Gmail, Outlook.com, mail app or copy address
- 🌐 **4 languages** — English, Tagalog, Spanish, French (translations are drafts pending native review)
- 🌗 **Dark and light** themes, mobile-friendly, keyboard accessible

## 🛡️ Security & privacy

- 🔐 Hash-locked **Content-Security-Policy**, no `unsafe-inline`, Trusted Types
- 🖼️ Anti-framing protection
- 🤖 `robots` meta + `robots.txt` blocking ~35 AI and scraper bots, and `noindex`
- 🚫 Deterrents against copy, print, right-click and shortcuts; blur shield when the window loses focus

> ⚠️ **Honest limit:** no website can truly stop screenshots or a determined copier. These measures are deterrents, not guarantees.

## 💥 Impact

- 🔗 **One place for the whole pipeline** — from idea to shipped, every project's stage is visible at a glance.
- 🤝 **Real-world grounding** — four projects are shipped and live: campus network, AAC app, rural internet and community CCTV.
- 📝 **Research output** — two papers in progress (SmartHome Theft Alert, Acoustic Shepherd).
- ♿ **Inclusive by design** — four languages, axe-core audit with 0 violations, keyboard-first navigation.
- 🧭 **Honest reporting** — unknown stays unknown; no invented metrics, users or outcomes.

## 📁 Repo layout

```text
index.html     # the entire site: HTML, CSS, JS, SVG, data, i18n
robots.txt     # crawler policy (must sit next to index.html)
```

Source and tooling (kept in the lab kit):

```text
src/                  # style.css, shell.html, app.js
build.py              # assembles dist/index.html and re-hashes the CSP
tools/rehash_csp.py   # ⚠️ run after ANY script/style edit, or the page goes blank
tools/lab_data.py     # export · check · review · apply · import (projects + translations as JSON)
tools/test_site.py    # 160 Playwright checks (+ --links, --shots)
```

## 🧪 Tested

- ✅ **160 / 160** automated browser checks (Playwright)
- ♿ **0** axe-core violations
- 📱 Desktop and mobile, EN/TL/ES/FR, dark and light

```bash
python3 tools/test_site.py
```

## 🚀 Deploy

1. 📋 Copy `index.html` and `robots.txt` into the repo root
2. ⬆️ Commit and push to `master`
3. ⏳ Wait 1–3 minutes for GitHub Pages

Preview locally with `python3 -m http.server` and open http://localhost:8000. Use `?debug=1` for diagnostics. The page hides itself inside frames — that's the anti-framing protection, so open it directly.

## ✏️ Editing content

Never hand-edit the data blocks in `index.html`:

```bash
python3 tools/lab_data.py export index.html data/
# edit data/projects.json or data/i18n.json
python3 tools/lab_data.py check  index.html
python3 tools/lab_data.py import index.html data/   # also re-hashes the CSP
```

## 📬 Contact

✉️ mmfrigillana.au+mitcodelab@gmail.com

<div align="center">

Made with 💜 and 🩵 by **MIT CODE LAB**

</div>
