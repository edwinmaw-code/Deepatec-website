# DeepaTec Website — File Structure Guide

## Folder Structure

```
deepatec/
├── index.html                        ← Main website file (open this in browser)
│
└── assets/
    ├── logos/
    │   ├── logo-horizontal.png       ← Used in NAV bar (icon + "DeepaTec" text, dark)
    │   ├── logo-white-version.png    ← Used in FOOTER (icon + white text)
    │   ├── logo-icon-only.png        ← Used as FAVICON (browser tab icon)
    │   └── logo-stacked.png          ← Reserved (icon above text, dark)
    │
    ├── images/
    │   ├── hero/
    │   │   └── hero-africa-bg.jpg    ← Optional fallback if video is removed
    │   │
    │   ├── about/
    │   │   └── about-team.jpg        ← Photo of your team / office in Tema, Ghana
    │   │                               (Replace Unsplash URL in index.html)
    │   │
    │   ├── services/
    │   │   ├── 01-software-dev.jpg   ← Software Development card image
    │   │   ├── 02-ui-ux-design.jpg   ← UI/UX Design card image
    │   │   ├── 03-ai-data.jpg        ← AI & Data card image
    │   │   ├── 04-it-consulting.jpg  ← IT Consulting card image
    │   │   └── 05-infrastructure.jpg ← Digital Infrastructure card image
    │   │
    │   └── unyplus/
    │       └── unyplus-hero-bg.jpg   ← Background image for UnyPlus hero section
    │                                   Recommended: African students on campus
    │
    └── video/
        └── hero-africa-globe.mp4     ← Self-hosted hero video (optional)
                                        Alternative to YouTube embed
```

---

## How to Swap Images

1. Download your preferred image (JPG or PNG)
2. Rename it to match the filename shown above
3. Place it in the correct folder
4. In `index.html`, find the `<img src="https://images.unsplash.com/...">` tag
5. Change the `src` to the local path, e.g:
   ```html
   <img src="assets/images/about/about-team.jpg" alt="DeepaTec Team" />
   ```

---

## How to Change the Hero Video

### Option A — YouTube Embed (current default)
1. Find a royalty-free "earth zoom africa" video on YouTube
2. Get the video ID from the URL (e.g. youtube.com/watch?v=**XXXXXXX**)
3. In `index.html`, find the `<iframe>` inside `.hero-video-wrap`
4. Replace the video ID in the `src` URL

### Option B — Self-hosted MP4
1. Download a free video from pixabay.com/videos (search "earth africa")
2. Save it as: `assets/video/hero-africa-globe.mp4`
3. In `index.html`, replace the `<iframe>` block with:
   ```html
   <video autoplay muted loop playsinline>
     <source src="assets/video/hero-africa-globe.mp4" type="video/mp4">
   </video>
   ```

---

## Logo Placement Summary

| Location        | Logo File                  | Background |
|-----------------|----------------------------|------------|
| Browser tab     | logo-icon-only.png         | Any        |
| Navigation bar  | logo-horizontal.png        | Light      |
| Footer          | logo-white-version.png     | Dark       |

---

## Notes

- All Unsplash image URLs in the code work online but require internet.
- For offline use, download & replace them with local files as described above.
- The website is a single-page app — all pages are in `index.html`.
- To publish: upload the entire `deepatec/` folder to your web host.
