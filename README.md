# Smart Bookmark

A full-stack bookmark manager built with Next.js (App Router), Supabase (Auth, Database, Realtime), and Tailwind CSS. Deployed on Vercel.

## Features Implemented

✅ Google OAuth authentication

✅ Added bookmarks (URL + title)  
✅ Private bookmarks per user  
✅ Real-time updates across tabs  
✅ Delete own bookmarks  
✅ Responsive Tailwind CSS styling  
✅ Deployed on Vercel  

## Tech Stack

- **Frontend**: Next.js 15 (App Router), Tailwind CSS
- **Backend**: Supabase (Auth, PostgreSQL, Realtime)
- **Deployment**: Vercel

## Challenges Faced & Solutions

### OAuth Redirect Configuration
Initially, Google OAuth was not redirecting correctly after login due to misconfigured callback URLs.  
**Solution:** Updated the correct redirect URL in Supabase Auth settings and ensured it matched the deployed Vercel domain.

### Environment Variables in Production
The application failed to connect to Supabase after deployment because environment variables were not configured in Vercel.  
**Solution:** Added `NEXT_PUBLIC_SUPABASE_URL` and `NEXT_PUBLIC_SUPABASE_ANON_KEY` in Vercel project settings.

### User Data Security
At first, bookmarks were accessible without proper user-level restriction.  
**Solution:** Implemented Supabase Row Level Security (RLS) policies to ensure users can only access their own bookmarks.

