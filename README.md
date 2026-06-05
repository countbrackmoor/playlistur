# Playlistur

A lightweight YouTube playlist builder. Paste a list of YouTube URLs, get a shareable queue link instantly — no login, no backend, no data leaves your browser.

Live at **[gorgon.live/playlistur](https://gorgon.live/playlistur/)**

---

## What It Does

Playlistur extracts video IDs from a list of YouTube URLs and generates a `watch_videos` link that opens all of them as a queue in YouTube. From there, a short workaround lets you save it as a permanent playlist on your account.

Supports all standard YouTube URL formats:
- `youtube.com/watch?v=`
- `youtu.be/`
- `youtube.com/shorts/`
- `youtube.com/embed/`
- Bare 11-character video IDs

Duplicate URLs are detected and removed automatically.

---

## How to Save the Queue as a Playlist

YouTube loads the generated link as an unlisted queue that can't be saved directly. This workaround converts it:

1. **Open the generated link** — your videos load as a queue in YouTube
2. **Add any recommended video to the queue** — hover a video in the sidebar, click ⋮ → *Add to queue*
3. **Save the queue** — a *Save* button appears at the top of the queue panel; click it and name your playlist
4. **Delete the extra video** — go to your new playlist and remove the video you added in step 2

---

## Tech

Single HTML file. No frameworks, no dependencies, no backend. Uses vanilla JS for URL parsing and link generation. State is not persisted — the page resets on reload.

The **API Mode** tab (marked WIP) is a placeholder for a future OAuth-authenticated version that would create playlists directly via the YouTube Data API v3, skipping the manual save steps. Pending Google API scope verification.

---

## Part of gorgon.live

Playlistur is one of several self-contained tools hosted at [gorgon.live](https://gorgon.live). All tools are pure HTML/CSS/JS with no external data dependencies.
