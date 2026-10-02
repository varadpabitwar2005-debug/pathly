# Pathly

Static site (index.html) connected to the Pathly Supabase project.

## Deploy
Option A (GitHub): push this folder to a new GitHub repo, then import it in Vercel (Framework: Other, no build command).
Option B (CLI): run `npx vercel --prod` inside this folder.

## After the first deploy (Supabase dashboard > Authentication > URL Configuration)
1. Set Site URL to your Vercel URL so confirmation emails link back to the site.
2. Add the same URL under Redirect URLs.
3. Email confirmation: leave it on for the live site. Turn it off under Providers > Email while testing.
4. Supabase's built-in email sender allows only a few emails per hour. Add a custom SMTP provider before launch.

## Make yourself an admin
Create an account, then run in the Supabase SQL editor:
update public.profiles set is_admin = true where username = 'YOUR_USERNAME';
Then open the site and use the Admin link in the top bar to approve mentors.

## Not included yet
Student booking, password reset, Google Sheets sync.
