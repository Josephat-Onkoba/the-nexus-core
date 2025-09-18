# The Nexus Core — Static Site

A single-file, responsive, futuristic-themed static website for The Nexus Core newsletter.

## Project structure

- `index.html` — Main static page with inline CSS and minimal JS (modals, mobile menu, mailto form, toast)
- `vercel.json` — Vercel configuration for static hosting
- `robots.txt` — Basic robots policy
- `THE NEXUS CORE (2).png` — Logo (ensure this file exists)
- `pexels-kindelmedia-8566636.jpg` — Media image

## Deploy to Vercel

You have two easy options: GitHub integration or Vercel CLI.

### 1) GitHub integration (recommended)
1. Create a new repository `nexuscore` on GitHub if it doesn't exist (or use the existing empty repo).
2. Initialize Git locally and push:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Nexus Core static site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/nexuscore.git
   git push -u origin main
   ```
3. In Vercel, click "New Project" → Import Git Repository → select `nexuscore`.
4. Framework Preset: "Other" (static). Root directory: repository root.
5. Build & Output settings: no build command needed; output is `/`.
6. Deploy. Vercel will host `index.html` at your project URL.

### 2) Vercel CLI (optional)
1. Install CLI and login:
   ```bash
   npm i -g vercel
   vercel login
   ```
2. From this project folder, run:
   ```bash
   vercel
   # For production
   vercel --prod
   ```

## After deploy
- Update Open Graph/Twitter meta image URLs in `index.html` to your live domain for best link previews.
- Verify the YouTube embed renders and the local images (logo and pexels image) resolve.
- Confirm mailto opens your email client; switch to a hosted form service if you need server-side capture.

## Troubleshooting
- If routing doesn’t land on `index.html`, ensure `vercel.json` exists at repository root.
- If images don’t load, confirm `THE NEXUS CORE (2).png` and `pexels-kindelmedia-8566636.jpg` are committed.
- If sharing previews don’t look right, the OG/Twitter images may need absolute URLs on your domain.
