# ALI AZHAAN — DIGITAL WORLD

A starter personal portfolio + Gemini-powered AI chat + private password-only admin area.

## 1. What is included
- Responsive public portfolio homepage
- AI chat using Gemini API through a server-side Next.js route
- Mini calculator and session-only notes
- Private admin login using an HTTP-only signed cookie
- Vercel-ready Next.js project

## 2. Before you start
Install Node.js (LTS) on your computer. Open this folder in a terminal.

```bash
npm install
```

Copy `.env.example` to `.env.local` and fill in:
- `GEMINI_API_KEY`: create a key in Google AI Studio
- `GEMINI_MODEL`: use a model currently available to your API key
- `ADMIN_PASSWORD`: choose a long, unique password
- `ADMIN_SESSION_SECRET`: use a random secret of at least 32 characters

Never commit `.env.local` to GitHub. Never share API keys, passwords or OTPs in chat or screenshots.

## 3. Run locally
```bash
npm run dev
```
Open http://localhost:3000

Before deploying:
```bash
npm run build
```

## 4. Push to GitHub
Create a new EMPTY repository on GitHub. In this folder run:
```bash
git init
git add .
git commit -m "Create Ali Azhaan Digital World"
git branch -M main
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```
Replace the URL with your own repository URL. Do not upload `.env.local`.

## 5. Deploy to Vercel
1. Sign in to Vercel.
2. Choose Add New → Project.
3. Import your GitHub repository.
4. Add the environment variables from `.env.local` in Vercel Project Settings → Environment Variables.
5. Deploy. When you change environment variables, redeploy the project.

## 6. Admin
Open `/admin/login`. The admin password is set only in the server environment variable `ADMIN_PASSWORD`; there is no public username field. Keep the password private. This starter login is a learning implementation, not a substitute for a managed identity provider or rate-limiting service on a high-traffic production site. Add rate limiting / Vercel Firewall protections before public launch.

## 7. Important limitations in this starter
- The AI chat uses Gemini. Google Search grounding, ChatGPT/OpenAI API, voice, image uploads and chat history are not connected yet.
- The admin area is protected, but content editing and database-backed project management are not built yet.
- Notes are not permanently saved.
- Contact form does not send messages yet.
- Do not publish private contact details, account passwords, OTPs or personal gaming credentials. Use only public gaming usernames/profile links. Ask a parent/guardian before publishing contact information.

## 8. Useful official documentation
- Gemini API: https://ai.google.dev/api
- Gemini generateContent: https://ai.google.dev/api/generate-content
- Supabase + Next.js: https://supabase.com/docs/guides/getting-started/quickstarts/nextjs
- Vercel deployment: https://vercel.com/docs
