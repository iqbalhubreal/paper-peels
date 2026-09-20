# Paper Peels

## Files

```
index.html              the website
.pages.yml              Pages CMS config
content/site.json       all site text, logo, footer links
content/stickers.json   the sticker list
media/                  logo + low-res preview images
```

## Setup

1. Push this folder to a GitHub repo.
2. Deploy it (Netlify, Vercel, or GitHub Pages — it's static, no build step).
3. Go to **pagescms.org**, sign in with GitHub, and add the repo. It picks up `.pages.yml` automatically.

You'll then see two things to edit in the CMS: **Site settings** and **Stickers**.

## Adding a sticker

1. Upload the full-quality file to Cloudinary and copy its URL.
2. For PDFs and raw files, insert `fl_attachment/` right after `upload/` so the browser downloads it instead of opening it:

   ```
   https://res.cloudinary.com/your-cloud/raw/upload/fl_attachment/my-sticker.pdf
   ```

   Images work the same way:
   ```
   https://res.cloudinary.com/your-cloud/image/upload/fl_attachment/my-sticker.png
   ```

3. In Pages CMS → **Stickers** → add an entry. Give it a title, upload a small compressed preview image, and paste the Cloudinary link.

Preview images are the only thing the site loads, so keep them light — around 600px wide and under 200 KB. Everything else comes from Cloudinary only when someone clicks Download.

## What's editable in the CMS

Every visible word, image, and link: brand name, logo, hero headline and subtext, the search placeholder, the download button text, the "no results" message, each sticker's title and preview and link, the footer note, Instagram, Pinterest, email, and the copyright line.

Tick **Show first** on a sticker to pin it to the top of the grid.
