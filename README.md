# ធៀបអនឡាញ · អ៊ូច ភីធ័រ & នូ ដាលីណា

Static website (HTML + CSS + JavaScript, no build step). Works on Vercel, Netlify or any static host.

```
index.html          the invitation page (all text, sections, inline SVG ornaments and QR for the map)
css/style.css       the whole design: colours, fonts, cover, kbach bands, animations
js/invite.js        guest name links (#g.…), countdown, share / copy link, owner tool (#host)
js/guides.js        starts the gold couple guide animations on scroll
js/content.js       EDIT HERE: photos, song, KHQR image, bank account
js/features.js      Khmer / English, calendar, save-to-calendar, story, gallery, music, wishes
js/gift.js          KHQR wedding-gift section and copy buttons
js/share-qr.js      share QR (draws itself for the address the site is on)
media/              p01.jpg, p02.jpg (photos), khqr.jpg (ABA KHQR), music.mp3 (song)
vercel.json         optional Vercel settings (clean URLs, cache for media)
```

## Deploy on Vercel (no Git needed)

1. Go to https://vercel.com/drop and sign in (or sign up free).
2. Drag the whole `peter-dalina-vercel` folder (or the .zip) onto the page.
3. Choose your team, type a project name such as `peter-dalina`, then **Deploy**.
4. Your link will be like `https://peter-dalina.vercel.app`. The share QR on the page follows that address automatically.

To update later: open the project in the Vercel dashboard and drop the new folder onto it.

## Test on your computer

Open a terminal in this folder and run `python3 -m http.server 8000` (or `npx serve .`), then open http://localhost:8000

## Change content

- Photos: replace `media/p01.jpg`, `media/p02.jpg` (portrait photos look best), or add `media/p03.jpg` and list it in `js/content.js`.
- Song: replace `media/music.mp3`.
- Gift: replace `media/khqr.jpg` (use the original image from the bank app so it scans) and the numbers in `js/content.js`.
- Text: edit `index.html`. Each Khmer text has its English version in the `data-en="…"` attribute next to it.
- Colours: top of `css/style.css` (`--wine` olive, `--wine-deep` dark olive, `--gold`).

## Guest personal links

Open your site with `#host` at the end (e.g. `https://peter-dalina.vercel.app/#host`) to make a link with a guest's name on the cover.
