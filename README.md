# Lowkey

> Spotify, quieter. A lightweight, native desktop player built around user experience.

Lowkey is a new face for Spotify, not a new Spotify. Your account, your library and Spotify's own playback stay exactly as they are. Lowkey only changes the window you look at.

I've been a Premium user for about three years. I built Lowkey because I wanted everyday Spotify to feel calmer, faster and more native. It doesn't compete with Spotify or try to replace it.

---

## Why Lowkey

- **Native, not a website in a window.** System font, native title bar, macOS vibrancy and Windows 11 Mica, platform scrollbars. Everything is clickable, just like in Spotify.
- **Light.** Rust and Tauri instead of Electron. It opens instantly from local cache and uses nothing while paused or hidden.
- **Just your music.** Library, search, playlists, albums, artists and a home page without promos.
- **Nothing cut off.** Where Spotify trims long titles with "…", Lowkey glides the text so you can read all of it.
- **No waiting.** Lowkey loads a playlist, album or artist the moment you point at it, so it's already there when you click. Pages open faster than in Spotify.
- **Every card visible.** No "Show all" on card rows. Home, search and artist pages show every album, playlist and artist, rearranged to fit the window.
- **Smooth resizing.** Spotify stutters while you resize. Lowkey waits until you stop, then glides every tile into place in one smooth move.
- **Yours to tune.** Theme, accent colour, contrast, density, UI scale, motion and glass.

---

## Spotify vs Lowkey vs Spotatui

| | Spotify | **Lowkey** | Spotatui |
|---|---|---|---|
| **Focus** | Complete music ecosystem | Native feel and user experience | Lightweight playback |
| **Feels like Spotify** | Yes | Yes | Partly |
| **Everything clickable** | Yes | Yes | Some elements aren't |
| **Adapts to window size** | Partly | Fully | Not at all |
| **Resizing** | Stutters | Smooth, tiles glide into place | No rearranging |
| **Card rows** (albums, playlists, artists) | One row + "Show all" | All cards, as many per row as fit | — |
| **Long text** | Cut off with "…" | Glides so all of it is readable | — |
| **Appearance settings** | None | Theme, accent, contrast, density, scale, motion, glass | None |
| **Home page** | Yes, with promos | Yes, music only | No |
| **Cold start** | Slow | Fast | Fastest, slightly ahead of Lowkey (no home page to load) |
| **Opening a page** | Loads after you click | Preloaded on hover, opens faster than Spotify | — |
| **Resource use** | High | Low, nothing while idle | Low |
| **Account** | Free or Premium | Premium | Free or Premium |
| **Price** | Free with ads, or subscription | Free, forever | Free, open source |
| **Built with** | Electron | Rust, Tauri 2, SvelteKit 5 | Rust, Tauri + terminal UI |
| **Playback** | Spotify's engine | Spotify Soloist (official) | librespot or Soloist |

[Spotatui](https://github.com/LargeModGames/spotatui) is a great project with a different goal. Lowkey is another independent approach, centred on desktop design.

---

## Free, non-commercial, forever

Lowkey is free for everyone and always will be. No subscription, no paid features, no ads.

It is also built to harm Spotify as little as possible. That's why it **requires your own Spotify Premium** and never works around Spotify's subscription. Playback runs through Soloist, Spotify's official player, so every stream counts as usual.

---

## Requirements

- Spotify **Premium**
- Your own **Soloist API key** (entered in Settings)
- **macOS** on Apple Silicon or **Windows** x64 (Linux builds exist but are unsupported)

Lowkey downloads Soloist from Spotify's servers on first run. It is never bundled.

---

## Limitations

These come from Soloist or Spotify, not from Lowkey.

- **Starting a playlist or album at a given track:** Soloist can't. Clicking a track plays only that track.
- **Offline downloads:** not supported.
- **Playlist editing:** blocked by Spotify Web API restrictions on this client ID.
- **Intel Macs:** Soloist runs only on Apple Silicon.
- **Mac App Store:** window vibrancy uses a private macOS API.

---

## Disclaimer

Lowkey is an unofficial, independent project, not affiliated with, endorsed by or sponsored by Spotify AB. Spotify is a trademark of Spotify AB.

It signs in with Spotify's desktop client ID and reads some undocumented Spotify endpoints. These may change, stop working or be restricted at any time and may not comply with Spotify's terms. Use at your own risk.
