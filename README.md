# CHROME//POP 💿

A Spotify-style music player with a Y2K / Winamp-era interface. Built with React + Vite as a front-end portfolio project.

<!-- Replace with your own screenshot: save it as docs/screenshot.png -->
![Screenshot](docs/screenshot.png)

## Features
- Real audio playback: play, pause, next, previous, shuffle, repeat (off / all / one)
- Track title, artist, and generated holographic cover art
- Seekable progress bar, volume slider, and mute
- Playlist with search and a "liked" tab (likes are saved in `localStorage`)
- Keyboard shortcuts and media keys / lock-screen controls (Media Session API)
- Loading and error states (`BUFFERING...`, `SIGNAL LOST`)
- Y2K UI: chrome bevel buttons, pixel LCD readout, wireframe grid and star background, glitch hover
- Accessible focus styles and reduced-motion support

## Keyboard shortcuts
| Key | Action |
|---|---|
| Space | Play / pause |
| N / P | Next / previous |
| S / R | Shuffle / repeat |
| M | Mute |
| L | Like current track |
| ← / → | Seek 5 seconds |
| ↑ / ↓ | Volume |

## Tech stack
React 18 · Vite 5 · Plain CSS (design tokens in `:root`) · HTML5 Audio

## Getting started
```bash
git clone https://github.com/<your-username>/chrome-pop.git
cd chrome-pop
npm install
npm run dev
```
Production build: `npm run build`

## Using your own music
Edit `src/data/tracks.js`. Each track needs `title`, `artist`, `hue`, and `src`.
`src` can be a URL or a local file, e.g. put `song.mp3` in `public/audio/` and use `"/audio/song.mp3"`.

Open-source / free-license sources to look at (always check the license and give credit):
- [Free Music Archive](https://freemusicarchive.org)
- [Jamendo](https://www.jamendo.com)
- [Internet Archive Audio](https://archive.org/details/audio)
- [Incompetech](https://incompetech.com/music/royalty-free/)

## Deploy to GitHub Pages
1. Push to the `main` branch.
2. In the repo: **Settings → Pages → Source: GitHub Actions**.
3. The workflow in `.github/workflows/deploy.yml` builds and publishes on every push.

## Project structure
```
src/
├─ components/   Player, Playlist, Cover
├─ hooks/        usePlayer (audio + state), useLikes (localStorage)
├─ data/         tracks.js
└─ styles/       y2k.css
docs/DESIGN.md   Design guide
.github/workflows/deploy.yml
```

## Credits
Demo audio: example songs by [SoundHelix](https://www.soundhelix.com). Track titles are placeholders.
Pixel font: [VT323](https://fonts.google.com/specimen/VT323) (SIL OFL).

## Roadmap
- [ ] Multiple playlists
- [ ] Queue view and drag-to-reorder
- [ ] Audio visualizer (Web Audio API)

## License
MIT
