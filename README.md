# StreamHub Deck

StreamHub Deck is a SteamOS and Steam Deck streaming launcher built for Gaming Mode. It centralizes streaming platforms in a controller-friendly interface and opens each service through a real browser profile so logins can remain persistent per platform.

This repository is the official release and automatic update channel for StreamHub Deck.

## Features

- Steam Deck friendly main menu with physical controller navigation.
- Persistent browser profiles for streaming platforms such as Netflix, Disney+, Max, Prime Video, Crunchyroll, YouTube, Apple TV+, Paramount+, Hulu, Peacock, Plex, Tubi, Pluto TV, Roku, Rumble, ESPN, YouTube TV, and others.
- Real Google Chrome Flatpak workflow for DRM/Widevine-heavy streaming services on SteamOS.
- Internal IPTV area with Xtream Codes and M3U support.
- IPTV profile management, active profile display, and Xtream Codes account expiration display.
- HLS/MPEGTS IPTV playback support with compatibility fallback.
- Steam Deck shortcut support using F9 for the app menu and Alt + Left/Right Arrow for browser back/forward navigation.
- Steam library artwork, desktop shortcut, and Non-Steam Game installer support.
- GitHub Releases based automatic updates.

## Download

Download the latest Steam Deck package from the official GitHub Releases page:

https://github.com/filipedeptulski/StreamHub-Deck/releases/latest

The release includes:

- `StreamHub-Deck-vX.X.X-x64.tar.gz`
- `INSTALL.txt`
- `REMOVAL.txt`
- SHA256 checksum
- `latest.json` for the automatic updater

## Install On SteamOS

In Desktop Mode on the Steam Deck, download the latest `.tar.gz` release to `~/Downloads`, then run:

```bash
cd ~/Downloads
tar -xzf StreamHub-Deck-vX.X.X-x64.tar.gz
cd StreamHub-Deck-vX.X.X-x64
chmod +x install-streamhub-deck.sh
./install-streamhub-deck.sh
```

The installer creates a Desktop Mode shortcut, adds StreamHub Deck as a Non-Steam Game when possible, applies Steam artwork, and installs Google Chrome Flatpak when needed for DRM-heavy platforms.

## Remove From SteamOS

From the extracted release folder:

```bash
chmod +x uninstall-streamhub-deck.sh
./uninstall-streamhub-deck.sh
```

## Development

Requirements:

- Node.js 20+
- npm

```bash
npm install
npm run dev
```

Syntax check:

```bash
npm run check
```

Build Linux release package:

```bash
npm run dist:linux
npm run release:prepare
```

## Notes

StreamHub Deck does not attempt to bypass DRM or reimplement official streaming apps. DRM-protected platforms are opened through their official websites in a compatible browser profile. IPTV playback is handled internally by StreamHub Deck.
