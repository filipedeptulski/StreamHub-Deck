[![StreamHub Deck banner](https://raw.githubusercontent.com/filipedeptulski/StreamHub-Deck/main/steamgrid/streamhub-deck-header-920x430.png)](https://github.com/filipedeptulski/StreamHub-Deck/releases/latest)

# StreamHub Deck

[![Latest release](https://img.shields.io/github/v/release/filipedeptulski/StreamHub-Deck?label=Latest%20Release&logo=github)](https://github.com/filipedeptulski/StreamHub-Deck/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/filipedeptulski/StreamHub-Deck/total?label=Downloads&logo=github)](https://github.com/filipedeptulski/StreamHub-Deck/releases)
[![SteamOS](https://img.shields.io/badge/SteamOS-Steam%20Deck-1b2838?logo=steam)](https://store.steampowered.com/steamos)
[![Electron](https://img.shields.io/badge/Electron-App-47848f?logo=electron&logoColor=white)](https://www.electronjs.org/)
[![Chrome Flatpak](https://img.shields.io/badge/Google%20Chrome-Flatpak-4285f4?logo=googlechrome&logoColor=white)](https://flathub.org/apps/com.google.Chrome)

Welcome to **StreamHub Deck**, a SteamOS and Steam Deck streaming launcher designed for Gaming Mode. It centralizes streaming platforms, IPTV, and persistent browser profiles in a controller-friendly interface for the Steam Deck.

StreamHub Deck opens DRM-protected streaming services through a real browser profile, while IPTV playback runs inside the app.

## Quick Start

Download the latest Steam Deck package from GitHub Releases:

[Download StreamHub Deck for SteamOS](https://github.com/filipedeptulski/StreamHub-Deck/releases/latest)

In Desktop Mode on the Steam Deck, place the `.tar.gz` file in `~/Downloads`, then run:

```bash
cd ~/Downloads
tar -xzf StreamHub-Deck-vX.X.X-x64.tar.gz
cd StreamHub-Deck-vX.X.X-x64
chmod +x install-streamhub-deck.sh
./install-streamhub-deck.sh
```

The installer creates a Desktop Mode shortcut, adds StreamHub Deck as a Non-Steam Game when possible, applies Steam library artwork, and installs Google Chrome Flatpak when needed for DRM-heavy streaming platforms.

## Features

- Steam Deck friendly main menu with physical controller navigation.
- Streaming launcher for Netflix, Disney+, Max, Prime Video, Crunchyroll, YouTube, Apple TV+, Paramount+, Hulu, Peacock, Plex, Tubi, Pluto TV, Roku, Rumble, ESPN, YouTube TV, and more.
- Persistent browser profiles so each platform can keep its own login session.
- Real Google Chrome Flatpak workflow for Widevine/DRM-heavy streaming services on SteamOS.
- Internal IPTV player with Xtream Codes API and M3U URL support.
- IPTV categories, channel navigation, profile management, and Xtream Codes account expiration display.
- HLS and MPEGTS IPTV playback support with compatibility fallback.
- Steam Deck shortcut support with `F9` for the StreamHub Deck menu.
- Browser back/forward navigation support through `Alt + Left Arrow` and `Alt + Right Arrow` Steam Input subcommands.
- GitHub Releases based automatic updates with SHA256 validation.
- SteamGrid-style artwork for the Steam library.

## Steam Deck Controls

Recommended Steam Input mapping:

- Physical Menu / Start button: `F9`
- `L4`: `Alt + Left Arrow` as a subcommand for browser back
- `R4`: `Alt + Right Arrow` as a subcommand for browser forward
- Directional pad: arrow keys
- `A`: select / confirm
- `B`: back when the active platform or page supports it

## IPTV

StreamHub Deck includes an internal IPTV area for:

- Xtream Codes API login
- M3U URL login
- Live TV, movies, and series categories
- Active IPTV profile display
- Xtream Codes account expiration date
- HLS/MPEGTS playback compatibility

## File Structure

```text
/
|-- docs/
|   |-- ARCHITECTURE.md
|   |-- BRAND_ASSETS.md
|   |-- DEVELOPMENT.md
|   |-- RISKS.md
|   `-- ROADMAP.md
|-- scripts/
|   |-- release/
|   |-- steamos/
|   `-- tests/
|-- src/
|   |-- input/
|   |-- renderer/
|   |-- updater/
|   |-- main.js
|   `-- preload.js
|-- steamgrid/
|-- services.json
|-- package.json
`-- README.md
```

## Development

Requirements:

- Node.js 20+
- npm

Install dependencies and run the app:

```bash
npm install
npm run dev
```

Run syntax checks:

```bash
npm run check
```

Build a Linux release package:

```bash
npm run dist:linux
npm run release:prepare
```

## Further Reading

- [Architecture](docs/ARCHITECTURE.md)
- [Development](docs/DEVELOPMENT.md)
- [Roadmap](docs/ROADMAP.md)
- [Risk Notes](docs/RISKS.md)
- [Brand Assets](docs/BRAND_ASSETS.md)
- [Latest Release](https://github.com/filipedeptulski/StreamHub-Deck/releases/latest)

## Project Topics

Steam Deck streaming launcher, SteamOS streaming app, IPTV launcher, Xtream Codes player, M3U player, Electron Steam Deck app, Non-Steam Game launcher, Google Chrome Flatpak streaming, Widevine streaming workflow.

`#SteamDeck` `#SteamOS` `#StreamingLauncher` `#IPTV` `#XtreamCodes` `#M3U` `#Electron` `#Widevine` `#GamingMode` `#NonSteamGame`

## Notes

StreamHub Deck does not bypass DRM and does not reimplement official streaming apps. DRM-protected services are opened through their official websites in a compatible browser profile. IPTV playback is handled internally by StreamHub Deck.
