Based Ronin Cyber — Vercel-ready demo project
===============================================

Contents:
- index.html                       (main page)
- public/.well-known/farcaster.json (Farcaster manifest template)
- public/assets/icon.png           (placeholder icon)
- public/assets/og.png             (placeholder og image)
- vercel.json                      (Vercel config)

How to deploy (simple & free):
1. Install Vercel CLI (optional) or use Vercel Dashboard:
   - Dashboard method (recommended):
     - Go to https://vercel.com/new
     - Drag & drop this folder, or import via Git.
     - Deploy. Your site will be available at https://<your-project>.vercel.app

2. Edit `public/.well-known/farcaster.json`:
   - Replace "https://<your-project>.vercel.app" in homeUrl/iconUrl/imageUrl with your actual deployed URL
   - After you generate accountAssociation (header/payload/signature), paste the values into the file and redeploy.

3. To generate Farcaster accountAssociation:
   - Use Farcaster developer tooling or the script your assistant can provide.
   - Sign the payload {"domain":"<your-project>.vercel.app"} with your custody key.
   - Fill header/payload/signature in the manifest file.

Notes:
- No custom domain needed; Farcaster accepts .vercel.app domains.
- If you want, ask the assistant to provide a Node.js script to create the accountAssociation signature.
