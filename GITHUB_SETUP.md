# GitHub Actions Autonomous Scheduler — Setup Guide
## Makes SEO OS run 24/7 without your browser open

═══════════════════════════════════════════════════
STEP 1 — Create GitHub Repository (FREE)
═══════════════════════════════════════════════════

1. Go to github.com → Sign up (free) or login
2. Click "New repository"
3. Name: trio-nexus-website
4. Set to: Public (required for free Actions minutes)
   OR Private (still gets 2,000 free minutes/month)
5. Click "Create repository"

═══════════════════════════════════════════════════
STEP 2 — Upload Your Files
═══════════════════════════════════════════════════

Option A — GitHub Web (easiest from mobile):
1. Open your new repository
2. Click "uploading an existing file"
3. Upload ALL files from the zip:
   - index.html
   - tn-admin-secure.html
   - blog.html
   - sitemap.xml
   - robots.txt
   - README.md
   - .github/workflows/seo-cron.yml  ← IMPORTANT
4. Click "Commit changes"

Option B — Connect Netlify to GitHub:
1. Netlify → Sites → Your Site → Site Configuration
2. Build & Deploy → Link to Git → GitHub
3. Select your repository
4. Netlify will auto-deploy on every push!

═══════════════════════════════════════════════════
STEP 3 — Add GitHub Secrets
═══════════════════════════════════════════════════

In your GitHub repository:
Settings → Secrets and variables → Actions → New secret

Add these 3 secrets:

Secret 1:
  Name:  GEMINI_API_KEY
  Value: AIza... (your Gemini API key)
  Get:   aistudio.google.com/app/apikey

Secret 2:
  Name:  NETLIFY_TOKEN
  Value: Your Netlify personal access token
  Get:   netlify.com → User Settings → Applications → New Access Token

Secret 3:
  Name:  NETLIFY_SITE_ID
  Value: Your site ID (e.g. elegant-dusk)
  Get:   Netlify → Your Site → Site Settings → General → Site ID

═══════════════════════════════════════════════════
STEP 4 — Test the Workflow
═══════════════════════════════════════════════════

1. Go to your GitHub repository
2. Click "Actions" tab
3. Click "Trio Nexus Autonomous SEO Cycle"
4. Click "Run workflow" → "Run workflow"
5. Watch it run live (takes 2-5 minutes)
6. Check your live website — content should update!

═══════════════════════════════════════════════════
AUTOMATIC SCHEDULE
═══════════════════════════════════════════════════

The workflow runs automatically:
  Monday    09:00 AM Pakistan time
  Thursday  02:00 PM Pakistan time

Each run:
  ✓ Researches keywords for all 3 services
  ✓ Rewrites service page content with AI
  ✓ Generates a new blog post
  ✓ Adds 2 new FAQs
  ✓ Deploys everything to Netlify live site
  ✓ Saves data to repository (seo-data.json)

NO BROWSER NEEDED. Runs 100% in the cloud.

═══════════════════════════════════════════════════
FREE TIER LIMITS
═══════════════════════════════════════════════════

GitHub Actions Free:
  2,000 minutes/month on public repos
  500 minutes/month on private repos
  Each SEO run takes ~3-5 minutes
  2 runs/week = ~8 runs/month = ~40 minutes used
  Well within free limits

Gemini API Free:
  1,500 requests/day
  Each run uses ~10-15 requests
  Well within free limits

Netlify Free:
  100GB bandwidth/month
  300 build minutes/month (not used by this method)
  Unlimited deploys via API

TOTAL MONTHLY COST: $0
═══════════════════════════════════════════════════
