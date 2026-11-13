# MillardSEN

A learning app for Tier 3 SEN students working at Kindergarten–Grade 2 level (Alberta curriculum), built for older learners. It avoids babyish design.

## What's in it
- **Home**: a colourful landing page with the four learning areas.
- **Sign-in with approval**: students create an account and ask to join. Mr Millard approves or declines each request on the Teacher tab. Learn and Library open only for approved students. This uses the shared `app_access` table, app `millardsen`.
- **Learn**: 18 short tasks in four groups (Number; Money, time & measuring; Shape & pattern; Reading & life skills), with big buttons, questions read aloud and errorless mode.
- **Library**: about 58 hand-picked free and low-cost resources (videos, manipulatives, books, switch and eye-gaze games), each with a Tier 3 tip.
- **Teacher** (approvers only): approve requests, set each student's level and access settings, see progress.

## Stack
- One static page: `index.html`. There is no build step.
- Data is stored in the Supabase project **Mathsguru** in the tables `public.sen_profiles` (per-student settings) and `public.sen_rounds` (results).
  Row Level Security: students read only their own data and can save rounds only once approved; approvers (`app_admins`, app `millardsen`) see everyone.
  The browser uses the publishable key only.
- Hosted on Vercel and deployed automatically on every push to `main`.

Money tasks use UAE dirhams (1 AED coin; 5, 10, 20 and 50 AED notes).

Live at https://www.millardsen.live
