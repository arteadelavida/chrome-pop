# CHROME//POP 💿

A Spotify-style music player with a Y2K / Winamp-era interface. Built with React + Vite as a front-end portfolio project.

<!-- Replace with your own screenshot: save it as docs/screenshot.png -->
![Screenshot](docs/screenshot.png)

## Features
- Play, pause, next, previous, shuffle, and repeat (off / all / one)
- Track title, artist, and generated holographic cover art
- Interactive progress bar and volume slider
- Clickable playlist with active-track highlight
- Y2K UI: chrome bevel buttons, pixel LCD readout, wireframe grid and star background, glitch hover
- Keyboard focus styles and reduced-motion support

## Tech stack
React 18 · Vite 5 · Plain CSS (design tokens in `:root`)

## Getting started
```bash
git clone https://github.com/<your-username>/chrome-pop.git
cd chrome-pop
npm install
npm run dev
```
Build for production: `npm run build`

## Project structure
```
src/
├─ components/   Player, Playlist, Cover
├─ hooks/        usePlayer.js (all player state + simulated playback)
├─ data/         tracks.js (demo playlist)
└─ styles/       y2k.css (tokens + all styling)
docs/DESIGN.md   Design guide
```

## Roadmap
- [ ] Real audio via `<audio>`
- [ ] Search and multiple playlists
- [ ] Keyboard shortcuts
- [ ] Deploy to GitHub Pages

## License
MIT
