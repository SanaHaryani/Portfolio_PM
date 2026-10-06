# Sana Haryani Portfolio

Static site — no build step. Open `index.html`, or deploy the folder to GitHub Pages, Netlify or Vercel.

## Add your videos

Put two files in a `videos/` folder next to `index.html`:

```
videos/sana-en.mp4   ← English
videos/sana-de.mp4   ← Deutsch
```

- Export as **MP4 (H.264 + AAC)** so it plays on every browser and phone. 1080p is plenty; aim for under ~50 MB each (HandBrake or `ffmpeg -i in.mov -c:v libx264 -crf 24 -c:a aac -movflags +faststart out.mp4`).
- `+faststart` lets the video start playing before it has fully downloaded.
- Optional captions (recommended for accessibility and silent autoplay viewers): `videos/sana-en.vtt` and `videos/sana-de.vtt`.
- Until the files exist, visitors see a friendly "Video coming soon" panel instead of a broken player.
- Different file names or a YouTube/Vimeo host? Edit `CONFIG.videos` at the top of the `<script>`.

## Language toggle

- EN / DE switch in the top bar; a second switch sits next to the video. Both stay in sync.
- Switching language translates the whole page **and** swaps the video.
- The choice is remembered; first-time visitors with a German browser see German automatically.
- English text lives in the HTML; German text is the `DE` object in the script. Edit either to adjust wording.

## CV download button

Drop your CV at `cv/Sana-Haryani-CV.pdf`. The "Download CV" button appears automatically once the file is on the server (and stays hidden until then).
Note: your current CV PDF includes your phone number and home address, which would become public. Consider exporting a version without them.

## GitHub

Once your repo/profile exists, paste the URL into `CONFIG.github`. An "All assignments & code on GitHub" link then appears under the Academic work, plus a GitHub button in Contact.

## Before publishing

1. Check the email and LinkedIn link in `CONFIG` at the top of the script (taken from your CV).
2. Add the videos.
3. Skim the German text and adjust anything that doesn't sound like you.
