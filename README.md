# かみずもう

トントン たたいて どひょうの そとへ おしだせ! — a paper-sumo tapping game for kids.

- **ひとりで あそぶ**: play against the CPU (three difficulty levels)
- **ふたりで あそぶ**: two players on one screen
- Tap the 「トン!」 button to push forward. Tapping too fast fills the ぐらぐら gauge, and your rikishi falls over.
- Tap quickly in a row to use special moves (つっぱり・はりて・てっぽう・ぶちかまし).
- Keyboard: A / S / Z / X (1P), K / L / ; / , (2P), Space / Enter in one-player mode.

## PWA

This is an installable Progressive Web App:

- `manifest.webmanifest` — app name, icons, full-screen display
- `sw.js` — service worker that caches the app so it works offline after the first visit
- `icons/` — app icons (regular, maskable, Apple touch icon)

Android / Chrome: open the site and tap 「📲 アプリに する」 on the title screen (or "Add to Home screen" in the browser menu).
iPhone / iPad: in Safari, tap the Share button and choose 「ホーム画面に追加」.

When you change `index.html` or other files, bump `VERSION` in `sw.js` so installed copies pick up the new files.

## Publishing

`.github/workflows/pages.yml` deploys the site to GitHub Pages on every push.
In the repository settings, under **Pages → Build and deployment → Source**, choose **GitHub Actions**.

Local preview:

```sh
python3 -m http.server 8000
# open http://localhost:8000/
```
