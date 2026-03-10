# Compass AI

AI Governance & Regulatory Consulting tool by Ryan Vasquez.

## Local Development

1. Install dependencies:
   ```bash
   npm install
   ```

2. Set up your API key:
   ```bash
   cp .env.example .env.local
   # Edit .env.local and add your Anthropic API key
   ```

3. Run the dev server:
   ```bash
   npm run dev
   ```

4. Open [http://localhost:3000](http://localhost:3000)

## Deploy to Vercel

1. Push this repo to GitHub

2. Go to [vercel.com](https://vercel.com) and import the repo

3. In the Vercel dashboard, add this environment variable:
   - Key: `ANTHROPIC_API_KEY`
   - Value: your Anthropic API key (from console.anthropic.com)

4. Deploy. Vercel will auto-deploy on every push to main.

## Custom Domain

In the Vercel dashboard, go to Settings > Domains and add your domain.
Point a CNAME record from your domain to `cname.vercel-dns.com`.

## Project Structure

```
compass-ai/
├── app/
│   ├── layout.tsx          # Root layout + metadata
│   ├── page.tsx            # Entry point
│   ├── CompassApp.tsx      # Main client component
│   └── api/
│       └── analyze/
│           └── route.ts    # Anthropic API call (server-side)
├── public/
│   └── logo.png            # Compass AI logo
├── .env.example            # Copy to .env.local
└── next.config.js
```
