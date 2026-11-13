# Step Up — SEN Learning Hub

A learning app for Tier 3 SEN students working at Kindergarten–Grade 2 level (Alberta curriculum), built for older learners. It avoids babyish design.

## What's in it
- **Learn**: 18 short tasks in four groups (Number; Money, time & measuring; Shape & pattern; Reading & life skills), with big buttons, questions read aloud and errorless mode.
- **Library**: about 58 hand-picked free and low-cost resources (videos, manipulatives, books, switch and eye-gaze games), each with a Tier 3 tip.
- **Teacher**: sign in, add students (first names only), set each student's level and access settings, and view progress.

## Stack
- One static page: `index.html`. There is no build step.
- Data is stored in the Supabase project **Mathsguru** in the tables `public.sen_students` and `public.sen_rounds`.
  Row Level Security lets each signed-in teacher see only their own students and rounds.
  The browser uses the publishable key only.
- Hosted on Vercel and deployed automatically on every push to `main`.

Without signing in, the app still works and keeps progress in the browser's local storage.
