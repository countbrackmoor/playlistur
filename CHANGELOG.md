# Changelog — Playlistur

YouTube playlist builder. No-API URL approach. Repo: `countbrackmoor/playlistur`.

---

## 2026-06-21 — Changelog established

### Added
- This CHANGELOG.md, reconstructed from past work sessions
- Project rule: future changes to this module must be logged here in the same session they're made

---

## ~2026-06-05 — Build session

### Added (initial: API-based prototype)
- OAuth-authenticated build using YouTube Data API v3
- Google Cloud project setup, OAuth consent screen, client credentials
- Hit OAuth verification wall — Google's review process for sensitive scopes blocked public use

### Added (final: no-API approach)
- URL generator using undocumented `watch_videos?video_ids=` endpoint
- Generates a shareable queue link with no login, no backend, no data leaving the browser
- Parses all common YouTube URL formats:
  - `youtube.com/watch?v=`
  - `youtu.be/`
  - `youtube.com/shorts/`
  - `youtube.com/embed/`
  - Bare 11-character video IDs
- Automatic deduplication
- Step-by-step save workaround documented in-tool: add a recommended video to the queue to make the *Save* button appear, save and name the playlist, then remove the added video
- API-based version preserved as "WIP" tab for future use if scope verification clears

### Changed
- Renamed from "Playlist Forge" → "Playlistur"
- Filename set to `playlistur.html`, hosted at `gorgon.live/playlistur/` in `countbrackmoor/playlistur` repo

### Changed (readability)
- `--text-dim` lifted from `#506070` → `#7a9ab0`

### Added (docs)
- `README.md` covering what it does, supported URL formats, the save workaround, and tech stack

### Tech notes
- Single HTML file, vanilla JS, no frameworks
- State not persisted — page resets on reload
