# M3U Play Pro

A modern, browser-based IPTV player that supports M3U playlists, HLS/MPD streams, and **ClearKey DRM** with automatic detection from `#KODIPROP` tags in M3U files.

![M3U Play Pro](https://img.shields.io/badge/IPTV-Player-blue) ![DRM](https://img.shields.io/badge/DRM-ClearKey-orange) ![License](https://img.shields.io/badge/license-MIT-green)

## Demo
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Click Here to Open in New Tab</a>
[Click Here to Open in New Tab](https://ex3mpli.github.io/m3u-play-pro/index.html){:target="_blank"}
[Click Here to Open in New Tab](https://external.ink)

## Features

- 🎬 **JW Player 8 Integration** – HLS & MPEG-DASH support
- 🔐 **ClearKey DRM Support** – Auto-detects `#KODIPROP` tags in M3U playlists
- 📁 **M3U Playlist Loading** – Import .m3u / .m3u8 with embedded DRM
- ✅ **Link Verification** – Batch test streams; DRM checked via `fetch()`
- 🔑 **DRM Key Display Bar** – Shows `kid:key` with a Copy button
- 📋 **Copy Stream Link** – One-click copy of the active URL
- 🔍 **Channel Search** – Filter loaded channels
- 🏷️ **DRM Badge** – ClearKey channels show a 🔒 badge
- 📱 **Responsive Design**
- 🎨 **Modern UI**

## Usage

### Quick Play
1. Enter stream URL (.m3u8 / .mpd)
2. (Optional) Enter ClearKey ID & Value
3. Click **Launch Stream**

### Load M3U Playlist
1. Click **Load M3U File**
2. Select .m3u / .m3u8 file
3. Click any channel — DRM applied automatically

### Verify Links
- 🟢 working · 🔴 broken · 🟡 unknown (CORS-blocked DRM)

## M3U Format

```m3u
#EXTM3U
#EXTINF:-1 tvg-logo="https://example.com/logo.png",Channel Name
https://example.com/stream.m3u8
```

### ClearKey DRM

```m3u
#EXTINF:-1 tvg-logo="https://example.com/logo.png",DRM Channel
#KODIPROP:inputstream.adaptive.license_type=clearkey
#KODIPROP:inputstream.adaptive.license_key=0123456789abcdef0123456789abcdef:fedcba9876543210fedcba9876543210
https://example.com/stream.mpd
```

## Configuration

Replace the JW Player license in `<head>`:

```javascript
jwplayer.key = "YOUR_LICENSE_KEY_HERE";
```

## Known Limitations

- ClearKey only (no Widevine/PlayReady)
- CORS restrictions may block playback or verification
- 5s verification timeout per channel

## Disclaimer

This tool does not host or provide streaming content. Users are responsible for ensuring they have the legal right to access any streams they play.

---

**© 2026 M3U Play Pro**
