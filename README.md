# Two Friends Fishing — Website

## Quick Setup (15 minutes)

### Step 1: Create a GitHub Account
1. Go to github.com and sign up (free)
2. Click "New Repository"
3. Name it `twofriendsfishing-site`
4. Make it **Public**
5. Click "Create Repository"

### Step 2: Upload These Files
1. In your new repo, click "Upload files"
2. Drag the ENTIRE contents of this folder into the upload area:
   - `index.html`
   - `.pages.yml`
   - `data/` folder (contains all JSON content files)
   - `images/` folder (contains all photos)
3. Click "Commit changes"

### Step 3: Connect to Cloudflare Pages
1. Log into your Cloudflare dashboard
2. Go to **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
3. Authorize GitHub and select `twofriendsfishing-site`
4. Build settings: leave everything blank (it's a static site)
5. Click **Deploy**
6. Add custom domain: twofriendsfishing.com

### Step 4: Set Up Pages CMS
1. Go to app.pagescms.org
2. Sign in with your GitHub account
3. Install the GitHub App when prompted
4. Select the `twofriendsfishing-site` repo
5. The CMS will detect your `.pages.yml` config automatically
6. You'll see sections for: Site Settings, Episodes, Gear, Weather, Fish Wall, Fish Map, Social Grid

### Step 5: Start Editing!
From the CMS dashboard you can:
- **Update the weather/bite forecast** → Weather & Bite Forecast
- **Add a new episode** → Episodes → add entry
- **Add a new fish wall photo** → Fish Wall → add entry  
- **Add a map pin** → Fish Map Pins → add entry
- **Change any text on the site** → Site Settings
- **Upload new images** → use the media manager

Every save triggers an automatic rebuild on Cloudflare Pages (~30 seconds).

---

## File Structure

```
/
├── index.html          ← The website (don't edit directly — use CMS)
├── .pages.yml          ← CMS configuration
├── data/
│   ├── site.json       ← Site settings, about text, social links
│   ├── episodes.json   ← Episode cards
│   ├── gear.json       ← Gear gallery items
│   ├── weather.json    ← Weather report & bite forecast
│   ├── fishwall.json   ← Community fish wall photos
│   ├── fishmap.json    ← Map pin data
│   └── social.json     ← Social grid images
├── images/             ← All site images
└── README.md           ← This file
```

## How It Works

The site is a static HTML page that loads content from JSON files via JavaScript. 
Pages CMS provides a visual editor for those JSON files through GitHub. When you 
save a change in the CMS, it commits to GitHub, which triggers Cloudflare Pages 
to rebuild and deploy. Total cost: $0/year (domain registration separate).
