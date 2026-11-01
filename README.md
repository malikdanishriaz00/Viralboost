# ViralBoost — Free Creator Tools

A responsive starter website for creator planning, captions, hashtag ideas, and a local content planner.

## What's included
- Responsive dark/neon landing page
- Four browser-based creator tools
- Login and sign-up UI
- Optional Supabase Auth integration (secure account authentication)
- Content planner saved in the current browser only
- No fake views, bots, or artificial engagement

## Important before publishing
The login screen will **not create real accounts until Supabase is configured**. Do not publish this as a working account system without completing the steps below. The content planner in this starter saves data in the current browser only; it is not yet synced across devices.

## Free deployment: GitHub Pages
1. Create/sign in to a GitHub account at https://github.com/
2. Create a new public repository named `viralboost`.
3. Upload `index.html`, `styles.css`, `app.js`, and `README.md` from this folder to the repository root.
4. Open repository **Settings → Pages**.
5. Under Build and deployment, choose **Deploy from a branch**, select `main` and `/ (root)`, then Save.
6. Wait for GitHub Pages to publish. The website URL will be shown in Settings → Pages.
7. Test the site on mobile and desktop.

GitHub Pages hosts static sites; it does not provide a secure user database or server-side authentication by itself.

## Enable real email/password accounts with Supabase
1. Create a project at https://supabase.com/ (check the current free-plan limits).
2. In the Supabase dashboard, open **Project Settings → API** (labels may change).
3. Copy the **Project URL** and the **publishable/anon key** only.
4. In `app.js`, replace:
   - `YOUR_SUPABASE_PROJECT_URL`
   - `YOUR_SUPABASE_ANON_KEY`
5. In Supabase **Authentication → URL Configuration**, add your deployed website URL to the allowed redirect/site URLs. For local testing, add `http://localhost:...` only if you use a local server.
6. Configure email confirmation as you prefer, then test sign-up and login.
7. Never put a `service_role` or secret key in `app.js`, GitHub, or any public website.
8. Review Supabase Auth rate limits and policies before collecting real user data.

## Current feature notes
- Idea generator, caption drafts and hashtag helper use local templates, not AI or live trend data.
- Hashtag suggestions are starting points, not a guarantee of reach.
- Planner uses this browser's local storage. Clearing browser data may erase plans.
- This site is not affiliated with TikTok and does not generate or sell artificial views/likes/followers.

## If you want AI generation later
Connect a server-side function/API that keeps the provider API key secret. Never put a paid AI API key directly in browser JavaScript.
