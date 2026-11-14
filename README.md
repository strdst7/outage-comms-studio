# Outage Comms Studio

[![status](https://img.shields.io/badge/status-stable-green)](https://github.com/strdst7/outage-comms-studio)
[![license](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![built with](https://img.shields.io/badge/built%20with-HTML%2FCSS%2FJS-black)](https://github.com/strdst7/outage-comms-studio)
[![dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)](https://github.com/strdst7/outage-comms-studio)
[![platform](https://img.shields.io/badge/platform-browser%20%7C%20static-lightgrey)](https://github.com/strdst7/outage-comms-studio)
[![language](https://img.shields.io/badge/language-EN%20%7C%20MS-orange)](https://github.com/strdst7/outage-comms-studio)

**Turn a messy outage timeline into clear, consistent customer updates — in minutes, without promising what you can't keep.**

---

## Who it's for

The **outage communications lead / network ops duty manager** — the person who has to press "send" during an incident, under time pressure, with incomplete information.

## Problem it solves

During an outage, the technical timeline is full of jargon, guesses, and half-confirmed causes. Customers hear something different on every channel (SMS, app push, status page, social, email, support, IVR). Support gets flooded with *"when will it be fixed?"* calls. Well-meant ETAs become broken promises.

Teams need **one checked set of facts turned into every channel message — consistently**.

## What you get

A **ready-to-send update pack in under 5 minutes**:

- **Checked facts** — what we know vs what we don't know, listed side by side
- **7 channel-ready messages** from a single source of truth: SMS, app push, status page, social post, email, support script, IVR
- **Live character counts** with over-limit warnings for SMS (160) and push (120)
- **Automatic risk detection** — flags ETA promises ("fixed by…", "we guarantee"), missing next-update time, missing doing/can-do/area, and unconfirmed causes
- **Plain-English jargon check** — flags technical terms with plain replacements
- **Pre-send checklist** — 5 mandatory checks with duty-manager sign-off
- **Update log** — every "mark as sent" is recorded with timestamp, next update time, severity, and approver
- **Export & print** — downloadable Markdown pack (`outage-update-pack.md`) and browser print support
- **Bilingual** — English and Bahasa Melayu message generation
- **Privacy by design** — everything stays in your browser (localStorage); nothing is uploaded
- **Works offline** — single static file, no build step, no external dependencies

---

## How to use

### Step 1 — Incident details
Fill in only what the network team has confirmed:
- **Title**, **area**, **services affected**, **start time**, **severity**
- **Next update time** (required — never promise a fix time; always give a next update commitment instead)
- **Cause** (optional — leave blank if unknown) + confidence (**Confirmed / Likely / Unknown**)
- **What we're doing now** and **what customers can do**
- **Tone** (calm / apologetic / urgent) and **message language** (English / Bahasa Melayu)

Messages refresh automatically as you type.

### Step 2 — Timeline
Log events in order with time, title, optional detail, and confidence tag:
- **Confirmed** — verified by the network team
- **Likely** — strong indication, still verifying
- **Unknown** — still investigating

Add, edit, or delete events anytime. Messages are worded according to confidence (e.g. *"Likely cause: … We're still verifying this"*).

### Step 3 — Facts check
Automatic review before anything goes out:
- **Known vs unknown** facts listed side by side
- **Risk flags** — ETA promises, missing fields, unconfirmed causes, no services selected
- **Jargon detection** — technical terms with plain-English replacement suggestions

Fix all warnings before sending.

### Step 4 — Send pack
- Copy each channel message (character limits shown for SMS & push)
- Tick the **5-point pre-send checklist**
- **Mark as sent** — enter the duty manager approver name; the update is logged with timestamp
- **Download** the Markdown pack or **print** for the incident record

---

## Try the sample

Click **"Load fictional sample"** for a ready-made Kota Bharu fibre disruption scenario (synthetic training data). Edit it, switch languages, export the pack, and see how the workflow flows end to end.

> ⚠ **FICTIONAL SCENARIO — Synthetic data for training only.** No real network data, no provider branding. Do not use for a real outage without verifying every fact.

---

## Tech stack

- **HTML5** — semantic markup
- **CSS3** — custom properties, print styles, responsive grid
- **Vanilla JavaScript** — no frameworks, no build step, no bundler
- **Browser localStorage** — auto-saves state; nothing leaves your device
- **Deployable anywhere** — Vercel, Netlify, GitHub Pages, or any static host

---

## Data & safety

- **Fictional by default** — the sample scenario is synthetic. No real customer data, network telemetry, or provider branding is used.
- **Uncertainty is labelled** — "Likely" and "Unknown" items are worded as such in every message. User reports are never presented as verified coverage data.
- **Your data stays here** — everything is stored only in your browser (`localStorage` key `outage-comms-studio-v1`). Nothing is uploaded. Clear it anytime with **"Clear all"**.
- **Human approval required** — the checklist and duty-manager sign-off are part of the workflow. The tool never auto-sends anything.
- **No ETA promises** — the tool actively blocks fix-time promises and rewrites them as next-update commitments.

---

## Deployment

### Option A — Drag and drop (fastest)
1. Go to [vercel.com/new](https://vercel.com/new)
2. Drag the `outage-comms-studio/` folder onto the upload area
3. Vercel auto-detects the static HTML site and deploys instantly
4. You get a `*.vercel.app` URL — that's your submission link

### Option B — Vercel CLI
```bash
cd outage-comms-studio
vercel
```

### Option C — GitHub Pages
1. Push this repo to GitHub
2. Enable GitHub Pages in repository settings
3. Site publishes automatically

### Option D — Run locally
```bash
cd outage-comms-studio
python3 -m http.server 8000
# open http://localhost:8000
```

No `vercel.json`, `package.json`, or build configuration is required — it's a single static file.

---

## Local development

The project is a single `index.html` file with embedded CSS and JavaScript. No install, no build step.

```bash
# Open directly in browser, or serve locally
python3 -m http.server 8000 --directory outage-comms-studio
```

State persists in `localStorage` during the session. Use **"Clear all"** to reset.

---

## Project structure

```
outage-comms-studio/
├── index.html        # Complete single-file application
└── README.md         # This file
```

---

## Credits

**MI4, INC.** · by **kdmirah lab**

Designed as a tool for connectivity teams — support agents, network operations, and duty managers who own customer communication during outages.

---

## License

MIT License. See [LICENSE](LICENSE) for details.

---

> Built for connectivity teams · Synthetic training data only · Human approval required — never auto-sends
