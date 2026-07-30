# Astro-check-
# AstroLive — Daily Cosmic Check-in

A habit-forming daily engagement prototype built for **AstroHack 2026: Build the Next Universe**.

## Problem

AstroLive retains users through one-off consultations. Once a question is answered, there's no reason to open the app again tomorrow — no daily loop, no reason to return.

## Solution

**Daily Cosmic Check-in** — a once-a-day ritual that gives users:
- A personalized daily reading based on their sun sign
- A **constellation streak**: each day they check in lights up a star and connects it to the last, so their engagement history becomes a unique, growing shape instead of a plain number
- A contextual upsell: on days when the reading flags something significant, a soft prompt nudges the user toward booking a real astrologer — monetization tied to genuine moments, not constant nagging

## Why this approach

Based on the Hook Model (trigger → action → variable reward → investment):
- **Trigger** — daily push/notification moment (not built in this prototype, noted as next step)
- **Action** — one tap to reveal today's reading
- **Variable reward** — the reading and lucky color/number change daily and feel personal
- **Investment** — the constellation grows visually over time, creating a reason not to break the streak

## Tech stack

- React (functional components, hooks)
- lucide-react for icons
- Inline styles (no external CSS framework)
- Client-side persistence via key-value storage (streak and profile survive a page refresh)
- Fonts: Fraunces (display), Inter (body), JetBrains Mono (data/stats)

## Running locally

This is a single-file React component (`AstroCheckin.jsx`) with a default export, built to drop into any React project (Create React App, Vite, Next.js).

```bash
# Example with Vite
npm create vite@latest astro-checkin -- --template react
cd astro-checkin
npm install
npm install lucide-react
# Replace src/App.jsx with AstroCheckin.jsx, update src/main.jsx import accordingly
npm run dev
```

## Deploying (for AstroHack submission)

1. Push the project to a public GitHub repo
2. Connect the repo to [Vercel](https://vercel.com) or [Netlify](https://netlify.com)
3. Deploy — no environment variables or backend required
4. Set the deployed link to public/anyone-with-link, per submission rules

## What's not built (and would come next)

- Real birth-chart calculation (currently sun-sign only, based on date)
- Push notification trigger for the daily reminder
- Real astrologer booking flow (the CTA button is currently a UI mockup)
- A/B testing framework for upsell timing and copy

## Success metrics this prototype is designed to move

- **D1 / D7 retention** — do users come back the next day, and a week later
- **Streak completion rate** — % of users who maintain a 3+ day streak
- **Upsell click-through rate** — % of flagged-day prompts that lead to a booking tap

## AI tools disclosure

This prototype and accompanying documentation were built with assistance from Claude (Anthropic), used for code generation, UX reasoning, and copywriting under human direction and review.
