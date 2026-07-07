# Faisal T.A. Sumak — Portfolio

Single-page portfolio for the AUD Game Design & Development scholarship application (AUD ID 2606046047). Pure HTML/CSS/JS — no build step.

## Deploy to GitHub Pages

1. **Create the repo** — go to https://github.com/new, name it `portfolio` (public), don't add any files.
2. **Push this folder:**
   ```
   cd portfolio
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/portfolio.git
   git push -u origin main
   ```
3. **Enable Pages** — repo → **Settings → Pages** → under *Build and deployment*, set Source to **Deploy from a branch**, branch **main**, folder **/ (root)** → Save.
4. **Wait ~1 minute**, then your live link is:
   ```
   https://<your-username>.github.io/portfolio/
   ```
   (Shown at the top of the Pages settings once deployed.)

To update the site later: replace files, then `git add . && git commit -m "update" && git push`.

## Image checklist (`/images` folder)

All 16:9, ideally ~1600px wide exported at ~80% quality (< 500 KB each). Placeholders are already in place — just overwrite with your best renders, keeping the same filenames:

| File | What to put there |
|---|---|
| `images/hero-bg.png` | Your single most cinematic render (≥1920×1080) |
| `images/boho-salon-1.png` | Boho Salon showcase shot |
| `images/frontlines-1.png` | Frontlines gameplay/environment shot |
| `images/environment-1.png` | Strongest 3D environment render |
| `images/vehicle-aston-1.png` | Aston Martin render |
| `images/vehicle-lambo-1.png` | Lamborghini Aventador SVJ render |
| `images/vehicle-jeep-1.png` | Jeep 6×6 render |
| `images/vehicle-mclaren-1.png` | McLaren render |
| `images/asset-store-1.png` | Immersed Technologies storefront/asset shot |
| `images/pipeline-blender-1.png` | Blender wireframe / MCP automation behind-the-scenes shot |

## Before you send

- Edit the placeholder copy — search `index.html` for `<!-- EDIT -->`.
- Test on your phone.
- Email the live link to **myapplication@aud.edu** before **Thursday 5:00 PM**, with AUD ID **2606046047** in the subject line.
