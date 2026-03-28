# Analytics Setup — Landing Page

**Status:** ✅ Infrastructure Ready — Awaiting GA4 ID

---

## What's Done

GA4 tracking code has been added to `index.html` with:
- Pageview tracking (automatic)
- CTA click tracking (Calendly, Gumroad links)
- Event categorization for conversion analysis

---

## What Simon Needs to Do (2 minutes)

### Step 1: Get Your GA4 Measurement ID

1. Go to https://analytics.google.com
2. Sign in with your Google account
3. If you don't have a property yet:
   - Click **Admin** (gear icon, bottom left)
   - Under **Property**, click **Create Property**
   - Name it "Agentic Commerce" or similar
   - Follow the setup wizard (select web, enter URL)
   - Create a **Data Stream** for web
4. Copy your **Measurement ID** (looks like `G-XXXXXXXXXX`)

### Step 2: Replace Placeholder in index.html

1. Open `/home/simonso1224/.openclaw/workspace/landing-page/index.html`
2. Find `G-XXXXXXXXXX` (appears 2 times)
3. Replace BOTH with your actual ID (e.g., `G-ABC123XYZ`)
4. Save the file

### Step 3: Deploy to Vercel

```bash
cd /home/simonso1224/.openclaw/workspace/landing-page
vercel --prod
```

Or push to Git if connected to Vercel.

---

## Verification

After deployment:
1. Visit your landing page URL
2. Go to GA4 → **Reports** → **Realtime**
3. You should see your own visit within 30 seconds

---

## What's Tracked

| Event | Category | Label | Use Case |
|-------|----------|-------|----------|
| Pageview | — | — | Total visitors, traffic sources |
| CTA Click | CTA | Link URL | Conversion rate, which CTAs work |

---

## Next Steps (Optional)

Once GA4 is working, we can add:
- Scroll depth tracking
- Form submission tracking
- Outbound link tracking
- Custom funnel analysis

---

**Added:** 2026-03-28 05:04 UTC (CEO Proactive Action)
**Time Required:** ~2 minutes
**Priority:** Medium (needed for conversion tracking once traffic starts)
