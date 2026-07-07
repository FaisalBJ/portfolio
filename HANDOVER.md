# HANDOVER — How to Manage Your Portfolio Images & Holders

Everything lives in one file: `index.html`. Images live in one folder: `images/`.
No build step, no tools needed — edit the HTML, refresh the browser, done.

---

## 1. Plugging photos into the existing holders

Every holder already has a placeholder image wired in. To replace one, you have two options:

### Option A — keep the filename (fastest, zero HTML editing)
Overwrite the file in `images/` with your new image, **keeping the exact same name**.

Current holders and their files:

| Where on the page | File to overwrite |
|---|---|
| Hero slideshow, slide 1 | `images/hero-bg.png` |
| Hero slideshow, slide 2 | `images/vehicle-aston-1.png` |
| Hero slideshow, slide 3 | `images/vehicle-lambo-1.png` |
| 2026 — full-width | `images/pipeline-blender-1.png` |
| 2026 — inset | `images/vehicle-aston-1.png` |
| 2025 — full-width | `images/vehicle-lambo-1.png` |
| 2025 — two-up left | `images/vehicle-mclaren-1.png` |
| 2025 — two-up right | `images/vehicle-jeep-1.png` |
| 2024 — inset | `images/asset-store-1.png` |
| 2024 — full-width | `images/environment-1.png` |
| 2020 — inset | `images/frontlines-1.png` |
| 2015 — full-width | `images/boho-salon-1.png` |

> Note: the Aston and Lambo files appear twice (hero + timeline). Overwriting them changes both spots. If you want different images in the hero, use Option B on the hero slides.

### Expanded section image order

Each year section now has **six** image holders. Replace the files below directly in `images/`, keeping the same filenames. The page order is the same as this table.

Recommended rhythm:
1. Put the strongest wide/cinematic image first.
2. Put the cleanest finished hero/detail images second and third.
3. Put process, wireframe, asset-pack, marketplace, or behind-the-scenes images in the middle.
4. End each year with a strong final image that bridges into the next year.

| Section | Slot | File to replace | Best type of image |
|---|---:|---|---|
| Hero | 1 | `images/hero-bg.png` | Strongest cinematic portfolio image |
| Hero | 2 | `images/vehicle-aston-1.png` | Strong secondary hero image |
| Hero | 3 | `images/vehicle-lambo-1.png` | Strong secondary hero image |
| 2026 | 1 | `images/2026-01-pipeline.png` | Full-width pipeline / automation / strongest 2026 image |
| 2026 | 2 | `images/2026-02-aston.png` | Finished Aston or equivalent hero render |
| 2026 | 3 | `images/2026-03-process.png` | Process, wireframe, node graph, or work-in-progress |
| 2026 | 4 | `images/2026-04-detail.png` | Close-up detail render |
| 2026 | 5 | `images/2026-05-tools.png` | Tools, automation, Blender, Roblox Studio, or MCP work |
| 2026 | 6 | `images/2026-06-final.png` | Final 2026 showcase image |
| 2025 | 1 | `images/2025-01-lambo.png` | Full-width Lamborghini or strongest 2025 vehicle |
| 2025 | 2 | `images/2025-02-mclaren.png` | McLaren or second vehicle render |
| 2025 | 3 | `images/2025-03-jeep.png` | Jeep 6x6 or third vehicle render |
| 2025 | 4 | `images/2025-04-detail.png` | Vehicle surface/detail shot |
| 2025 | 5 | `images/2025-05-wireframe.png` | Wireframe, clay, or viewport shot |
| 2025 | 6 | `images/2025-06-final.png` | Final 2025 vehicle showcase image |
| 2024 | 1 | `images/2024-01-asset-store.png` | Immersed Technologies / asset-store image |
| 2024 | 2 | `images/2024-02-environment.png` | Full-width environment image |
| 2024 | 3 | `images/2024-03-pack.png` | Asset pack or product showcase |
| 2024 | 4 | `images/2024-04-lighting.png` | Lighting, environment, or mood study |
| 2024 | 5 | `images/2024-05-marketplace.png` | Marketplace/storefront/social proof |
| 2024 | 6 | `images/2024-06-final.png` | Final 2024 showcase image |
| 2020 | 1 | `images/2020-01-frontlines.png` | Frontlines or strongest 2020 image |
| 2020 | 2 | `images/2020-02-clearlydev.png` | ClearlyDev / platform / asset-store image |
| 2020 | 3 | `images/2020-03-gameplay.png` | Gameplay or environment shot |
| 2020 | 4 | `images/2020-04-assets.png` | Asset work from this period |
| 2020 | 5 | `images/2020-05-teamwork.png` | Collaboration/project image |
| 2020 | 6 | `images/2020-06-final.png` | Final 2020 showcase image |
| 2015 | 1 | `images/2015-01-boho.png` | Boho Salon strongest/most recognizable shot |
| 2015 | 2 | `images/2015-02-early-map.png` | Early map/build screenshot |
| 2015 | 3 | `images/2015-03-gameplay.png` | Early gameplay screenshot |
| 2015 | 4 | `images/2015-04-awards.png` | Awards, milestone, or proof image |
| 2015 | 5 | `images/2015-05-community.png` | Community/player screenshot |
| 2015 | 6 | `images/2015-06-final.png` | Final early-years image |

### Option B — new filename
1. Drop your image into `images/` (e.g. `images/my-new-render.png`).
2. In `index.html`, find the holder and change the `src` (or `background-image` for hero slides):

```html
<img src="images/my-new-render.png" alt="short description" loading="lazy">
```
```html
<div class="slide" style="background-image:url('images/my-new-render.png')"></div>
```

### Image specs (matters for quality AND speed)
- **Aspect ratio 16:9** — anything else gets center-cropped automatically (`object-fit: cover`), which is usually fine.
- **~1600px wide, exported at ~80% quality, under 500 KB** per image. Hero images can be 1920px.
- PNG or JPG both work. For screenshots with lots of detail, JPG is usually much smaller.

---

## 2. Creating MORE holders

There are three holder types. Copy-paste the block, change the image path and caption, and place it anywhere between year sections.

### Type 1 — Full-width (edge to edge, most cinematic)
```html
<figure class="full reveal">
  <div class="frame">
    <img src="images/YOUR-IMAGE.png" alt="what it is" loading="lazy">
  </div>
  <figcaption>One quiet line about what they're looking at.</figcaption>
</figure>
```

### Type 2 — Inset (has side margins, calmer)
```html
<figure class="inset reveal">
  <div class="frame">
    <img src="images/YOUR-IMAGE.png" alt="what it is" loading="lazy">
  </div>
  <figcaption>One quiet line about what they're looking at.</figcaption>
</figure>
```

### Type 3 — Two-up row (a pair, side by side)
```html
<div class="duo reveal">
  <figure>
    <div class="frame">
      <img src="images/IMAGE-A.png" alt="" loading="lazy">
    </div>
    <figcaption>Caption for the left one.</figcaption>
  </figure>
  <figure>
    <div class="frame">
      <img src="images/IMAGE-B.png" alt="" loading="lazy">
    </div>
    <figcaption>Caption for the right one.</figcaption>
  </figure>
</div>
```

Everything is automatic once pasted: lazy loading, the scroll fade-in (`reveal`), the parallax drift (`frame`), and the hover caption. **Don't remove the `<div class="frame">` wrapper** — the parallax needs it.

### Adding a hero slide
Add another `.slide` div at the top of `<header>`:
```html
<div class="slide" style="background-image:url('images/YOUR-IMAGE.png')"></div>
```
The dots and the crossfade timing adjust automatically. 3–4 slides is the sweet spot.

### Adding a new YEAR section
Paste this between any two sections (order on the page = order the committee sees; keep newest → oldest):
```html
<div class="year-rule reveal"><i></i></div>
<div class="year reveal">
  <h2>2022</h2>
  <div class="year-note">One soft line about this year</div>
</div>
```

### Adding a text passage (the serif "letter" moments)
```html
<section class="letter tight reveal">
  <p>A short personal paragraph in your voice.</p>
</section>
```

### Swapping any image for a looping video
Replace the `<img>` inside a frame with:
```html
<video muted autoplay loop playsinline preload="metadata" style="width:100%;aspect-ratio:16/9;object-fit:cover">
  <source src="images/YOUR-CLIP.mp4" type="video/mp4">
</video>
```
Keep clips short (5–10 s), muted, and under ~5 MB. A gameplay flythrough here is worth a lot.

---

## 3. Testing locally (static HTML)

Just double-click `index.html` — it opens in your browser and everything works (it's fully self-contained; images load from the relative `images/` folder).

If you want it served like a real website (identical to how GitHub Pages serves it):
```
cd portfolio
python -m http.server 8000
```
Then open http://localhost:8000. Press `Ctrl+C` to stop.

**Always test on your phone too** — easiest way: push to GitHub Pages (below) and open the live link on your phone.

---

## 4. Publishing to GitHub Pages

### First-time setup (once)
1. Go to https://github.com/new → name the repo `portfolio` → **Public** → create (add no files).
2. In a terminal, inside the `portfolio` folder:
   ```
   git init
   git add .
   git commit -m "Portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/portfolio.git
   git push -u origin main
   ```
3. On GitHub: repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main**, folder **/ (root)** → Save.
4. Wait ~1 minute. Your live site:
   ```
   https://<your-username>.github.io/portfolio/
   ```

### Every update after that (new photos, new holders, edited captions)
```
git add .
git commit -m "update photos"
git push
```
The live site refreshes itself within a minute or two. If you don't see the change, hard-refresh (`Ctrl+Shift+R`) — your browser may have cached the old image.

> Important: GitHub Pages is **case-sensitive**. `Images/Photo.PNG` ≠ `images/photo.png`. Keep everything lowercase and it will never bite you.

---

## 5. Quick checklist before sending the link

- [ ] Every placeholder image replaced with your real, highest-quality work
- [ ] All captions rewritten in your voice (search `index.html` for `<!-- EDIT -->`)
- [ ] Year groupings match your real timeline
- [ ] Opened on your phone — hero, captions, and year breaks all look right
- [ ] Email the link to **myapplication@aud.edu** before **Thursday 5:00 PM**, AUD ID **2606046047** in the subject
