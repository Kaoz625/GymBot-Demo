# Replit Agent Task: GymBot-Demo

## Goal
Transform GymBot-Demo into a full-featured gym assistant web app with AI-powered workout plan generation, progress tracking, and a conversational AI coach powered by OpenAI.

## Tasks
1. Build a clean landing page with hero: "Your AI Gym Coach" — bold, dark athletic aesthetic, neon green or electric blue accents
2. Create an onboarding flow: collect user's fitness goal (lose weight / build muscle / endurance), current fitness level (beginner/intermediate/advanced), available equipment, and days per week available
3. Build an AI Workout Plan generator: on form submit, call OpenAI GPT-4o with the user's profile to generate a structured weekly workout plan — display in a card-based weekly schedule UI
4. Implement a Workout Tracker: users can log sets, reps, and weight for each exercise — store in Supabase `workout_logs` table
5. Build a Progress Dashboard: weekly volume chart (Chart.js or Recharts), personal records table, streak counter
6. Add an AI Coach chat widget (OpenAI GPT-4o): floating button, conversational interface — coach has context of the user's workout plan and recent logs
7. Implement Supabase auth (email magic link or Google OAuth) so data persists per user
8. Create a Exercise Library page: searchable list of exercises with muscle groups, instructions, and difficulty rating — seed with 30+ exercises
9. Add push notification / reminder system (browser Notifications API) — remind users of their next scheduled workout
10. Mobile-first design — the app must be fully usable on a phone
11. Set up Supabase schema: `users`, `workout_plans`, `exercises`, `workout_logs`, `personal_records` tables with RLS
12. Deploy to Cloudflare Pages (frontend) + Coolify (if Express/Node backend needed for OpenAI calls)

## Tech Stack
- React 18 + TypeScript
- Vite
- Tailwind CSS
- OpenAI GPT-4o API (workout generation + AI coach)
- Supabase (auth + database)
- Recharts or Chart.js (progress charts)
- Cloudflare Pages (frontend) + Coolify (backend API)

## Deploy Target
Cloudflare Pages for the frontend. If an Express proxy for OpenAI is needed, deploy it on Coolify. Never Vercel.

## Done When
- [ ] Onboarding flow collects user profile and generates a workout plan via OpenAI
- [ ] Workout plan displays in weekly card schedule UI
- [ ] Users can log sets/reps/weight — data saves to Supabase
- [ ] Progress dashboard shows a chart with real logged data
- [ ] AI Coach chat widget is functional (sends/receives messages from OpenAI)
- [ ] Supabase auth works (user can sign up, log in, see their own data)
- [ ] App is fully mobile-responsive
- [ ] All changes pushed to `Kaoz625/GymBot-Demo` main branch
