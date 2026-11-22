# Lowkey

> Spotify, quieter. A native, lightweight desktop player for Spotify Premium.

**[Website and live demo](https://lowkey.ctlx.app)** · **[Download the latest release](https://github.com/whynoctlx/lowkey-build/releases/latest)** · **[Changelogs](changelogs)**

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
- **Paste a link.** Paste a Spotify link into search and Lowkey opens it at once: a song plays, an album, artist or playlist opens.
- **Your sidebar, your order.** Drag any row to reorder it, or up to the top to pin it. Playlists you made get their own section under the pins.
- **A floating player.** The player floats over the page as a glass bar, or sits docked under it, as you like.
- **Ignore an artist.** One press on an artist's page: their songs dim in every list and are skipped when they come up. Press again to skip the songs they're featured on too.
- **Songs into your playlists.** Add a song to your own or collaborative playlists, or take it out, from the save menu next to its name.
- **Yours to tune.** Theme, accent colour, contrast, density, UI scale, motion, glass and page background. On Home, pick which shelves show and how large the cards are.

---

## Spotify vs Lowkey vs Spotatui

| | Spotify | **Lowkey** | Spotatui |
|---|---|---|---|
| **Focus** | Complete music ecosystem | Native feel and user experience | Lightweight playback |
| **Cold start** | Slow | Nearly instant | Slower than Lowkey |
| **Opening a page** | Slower | Nearly instant | — |
| **Resource use** | High | Low, nothing while idle | Low |
| **App size** | Over 430 MB | 8.6 MB | 23.4 MB |
| **Feels like Spotify** | Yes | Yes | Partly |
| **Everything clickable** | Yes | Yes | Some elements aren't |
| **Adapts to window size** | Partly | Fully | Not at all |
| **Resizing** | Stutters | Smooth, tiles glide into place | No rearranging |
| **Card rows** | One row + "Show all" | All cards, as many per row as fit | — |
| **Sidebar** | Sort options, a few pins | Drag to reorder and pin, your playlists in their own section | Plain list |
| **Pasting a link** | — | Opens it right away from search | — |
| **Ignoring an artist** | Only on mobile | Dimmed and skipped, optionally their features too | No |
| **Long text** | Cut off with "…" | Glides so all of it is readable | — |
| **Window** | Its own title bar | Native title bar, macOS vibrancy, Windows 11 Mica | Terminal, or a desktop app without the native feel |
| **Appearance settings** | None | Theme, accent, contrast, density, scale, motion, glass, background | None |
| **Home page** | Yes, with promos | Yes, music only, you pick the shelves | No |
| **Player** | Docked at the bottom | Floating glass bar, or docked | Docked at the bottom |
| **Tracking and ads** | Listening data collected, ads on Free | None of its own; Spotify still sees what you play, through Soloist | None of its own; Spotify still sees what you play |
| **Downloading music** | Offline, inside the app, with Premium | Never, streams only | — |
| **Signing in** | Email and password, in the app | A short code at spotify.com/pair, your password never touches Lowkey; tokens stay encrypted on your computer | A short code at spotify.com/pair |
| **Account** | Free or Premium | Premium | Free or Premium |
| **Setup** | Easiest | Easy, a guided setup explains each step | Harder, no guided setup |
| **Price** | Free with ads, or subscription | Free, forever | Free, open source |
| **Built with** | Chromium (CEF) | Rust, Tauri 2, SvelteKit 5 | Rust, Tauri + terminal UI |
| **Playback** | Spotify's engine | Spotify Soloist (official) | librespot or Soloist |
| **Updates** | Automatic | Automatic and signed, installed when you quit | By hand, through cargo |

[Spotatui](https://github.com/LargeModGames/spotatui) is a great project with a different goal. Lowkey is another independent approach, centred on desktop design.

---

## Free, non-commercial, forever

Lowkey is free for everyone and always will be. No subscription, no paid features, no ads.

It is also built to harm Spotify as little as possible. That's why it **requires your own Spotify Premium** and never works around Spotify's subscription. Playback runs through Soloist, Spotify's official player, so every stream counts as usual.

---

## Streams only, never downloads

Lowkey is a remote control for Spotify's own playback. Music is streamed and played only by Soloist, Spotify's official player, with your Premium account, so every play is a normal Spotify stream that counts for the artist.

Lowkey never touches the audio. It has no download, recording, export or offline feature, does not access or decrypt audio, and does not work without Premium. It never will, and contributions or requests that would add any of this are not accepted.

---

## Private by design

- **No analytics, no tracking.** No telemetry, no crash reporter, no ads. Lowkey records nothing about how you use it. Playback runs through Soloist, so Spotify sees what you play, just as in its own app.
- **No Lowkey account, no Lowkey server.** The app talks to Spotify directly.
- **Your sign-in stays on your computer.** Your Spotify session and Soloist key are stored encrypted (ChaCha20-Poly1305) with a key tied to your computer.
- **One other request: updates.** Lowkey checks GitHub for a newer release and sends nothing about you or your music.

Full details: [Privacy policy](https://lowkey.ctlx.app/privacy.md) · [Terms of use](https://lowkey.ctlx.app/terms.md)

---

## Requirements

- Spotify **Premium**
- Your own **Soloist API key** (entered in Settings)
- **macOS** on Apple Silicon. Windows x64 is coming soon.

Lowkey downloads Soloist from Spotify's servers on first run. It is never bundled.

## Install

1. Download the `.dmg` from the [latest release](https://github.com/whynoctlx/lowkey-build/releases/latest), open it and drag Lowkey to Applications.
2. Lowkey isn't notarized by Apple, so the first launch is blocked. Open **System Settings › Privacy & Security**, scroll down and click **Open Anyway** next to Lowkey. You do this once.
3. Sign in with a short code at spotify.com/pair and add your Soloist key. From then on Lowkey updates itself.

---

## Limitations

These come from Soloist or Spotify, not from Lowkey.

- **Starting a playlist or album at a given track:** Soloist can't. Clicking a track plays only that track.
- **Offline downloads:** not supported, by design (see above).
- **Playlist editing:** you can add songs to your playlists or take them out; other editing is blocked by Spotify Web API restrictions on this client ID.
- **Intel Macs:** Soloist runs only on Apple Silicon.
- **Mac App Store:** window vibrancy uses a private macOS API.

---

## Disclaimer

Lowkey is an unofficial, independent project, not affiliated with, endorsed by or sponsored by Spotify AB. Spotify is a trademark of Spotify AB.

It signs in with Spotify's desktop client ID and reads some undocumented Spotify endpoints. These may change, stop working or be restricted at any time and may not comply with Spotify's terms. Use at your own risk.
