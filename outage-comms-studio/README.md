# Outage Comms Studio

**Turn a messy outage timeline into clear, consistent customer updates — in minutes, without promising what you can't keep.**

## Who it's for
The **outage communications lead / network ops duty manager** — the person who has to press "send" during an outage, under time pressure, with incomplete information.

## Problem it solves
During an outage the technical timeline is full of jargon, guesses and half-confirmed causes. Customers hear something different on every channel (SMS vs app vs status page vs support), support gets flooded with "when will it be fixed?" calls, and well-meant ETAs become broken promises. Teams need one checked set of facts turned into every channel message, consistently.

## What you get (outcome)
A **ready-to-send update pack** in under 5 minutes:
- Checked facts (what we know / what we don't know)
- 7 channel-ready messages from the same facts: SMS, app push, status page, social, email, support script, IVR
- Automatic jargon + risky-promise checks
- Pre-send checklist + update log + exportable pack

## How to use
1. **Incident** — Fill in area, services, next update time (always — never a fix time), tone, language (English / Bahasa Melayu). Leave cause blank if unknown.
2. **Timeline** — Log events in order and tag confidence honestly: Confirmed / Likely / Unknown. Messages are worded accordingly.
3. **Facts check** — Review automatic flags: jargon to replace, ETA promises, missing fields. Fix warnings first.
4. **Send pack** — Copy each channel message (character limits shown for SMS/push), tick the 5-point checklist, mark as sent (logged), download the pack (.md) or print.

Try it: click **"Load fictional sample"** for a ready-made Kota Bharu fibre scenario, then edit and export.

## Data & safety
- **Fictional by default:** sample scenario is synthetic. No real customer data, network telemetry, or provider branding.
- **Uncertainty labelled:** Likely/Unknown items are worded as such in every message. User reports are never presented as verified coverage data.
- **Privacy:** everything stays in your browser (localStorage). Nothing is uploaded.
- **Human approval:** checklist + duty-manager sign-off are required. The tool never auto-sends.

## Tech
Single-file static app (`index.html`) — no build step, no external dependencies, works offline. Deployable to any static host (Vercel, Netlify, GitHub Pages).

## Branding / themes
- Brand: **MI4, INC.** · by **kdmirah lab**
- Theme: Light / Dark / System (respects OS preference, saved in browser)

## Files
- `index.html` — the complete tool
- `README.md` — this file
