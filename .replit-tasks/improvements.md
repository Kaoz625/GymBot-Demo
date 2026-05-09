# Replit Agent Task: GymBot-Demo

## Goal
Transform the current single-page HTML stub into a full-featured AI gym assistant web app with real OpenAI gpt-4o integration, workout plan generation, progress tracking, and meal planning — all in one responsive interface.

## Tasks
1. Replace the bare-bones index.html with a polished React (Vite + TypeScript) or vanilla JS app with tabbed navigation: Chat, Workout Plans, Progress, Meal Planner
2. Wire up OpenAI gpt-4o via a backend proxy (Node/Express or Cloudflare Worker) — never expose the API key client-side; read OPENAI_API_KEY from env
3. Build the AI Chat tab: streaming responses, system prompt that makes the bot a certified personal trainer, suggested quick-start prompts ("Build me a 4-week beginner plan", "What should I eat before a morning workout?")
4. Build the Workout Plans tab: form inputs (goal: strength/cardio/weight-loss, days/week, equipment available), calls AI to generate a structured weekly plan, renders it as a printable card grid
5. Build the Progress tab: local-storage-backed log where users record reps/sets/weight per exercise; line chart (use Chart.js CDN) showing volume over time per muscle group
6. Build the Meal Planner tab: inputs for calories/day, dietary restrictions, macro goals; AI returns a 7-day meal plan with macro breakdown per meal
7. Dark gym aesthetic: black/charcoal background, electric orange (#FF6B00) accent, Inter font, mobile-first responsive layout
8. Add a loading skeleton and error toast system so failed API calls degrade gracefully
9. Deploy target: Cloudflare Pages (static frontend) + Cloudflare Worker (API proxy) — include a `wrangler.toml` and deploy instructions in README

## Tech Stack
- React 18 + TypeScript + Vite (frontend)
- Cloudflare Worker (API proxy, OPENAI_API_KEY secret)
- OpenAI gpt-4o with streaming (chat) and single-shot (plans/meals)
- Chart.js for progress charts
- LocalStorage for progress persistence
- Tailwind CSS or plain CSS modules

## Deploy Target
Cloudflare Pages (static frontend) + Cloudflare Worker (backend proxy). Never Vercel.

## Done When
- [ ] App loads with 4 working tabs (Chat, Workout Plans, Progress, Meal Planner)
- [ ] AI Chat streams real gpt-4o responses via the Cloudflare Worker proxy
- [ ] Workout plan generator returns a structured weekly plan from form inputs
- [ ] Progress tab logs and charts at least one exercise over multiple sessions
- [ ] Meal planner returns a 7-day plan with macros
- [ ] No API key is exposed in client-side code
- [ ] App is fully responsive on mobile (375px) and desktop
- [ ] `wrangler.toml` present and README documents deploy steps
