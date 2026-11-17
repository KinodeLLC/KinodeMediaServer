# Kinode Media Server

Kinode is a free home media server. Install it on the computer that holds your movies, shows and music, and watch your personal media library on your phone, your TV or in a browser, at home or away.

There is no paid tier. Remote streaming, hardware transcoding, skip intro, sharing and the apps are all in the free download.

This repo is where you get downloads, report bugs and ask questions. The code itself is not here.

- Website: https://kinode.tv
- Download: https://kinode.tv/download
- Docs: https://kinode.tv/docs
- Report a bug: [open an issue](../../issues/new/choose)

## Get it

The current release is **1.5.0**.

| What you have | Get this |
|---|---|
| Windows 10 or 11, 64-bit (Intel or AMD) | Windows installer |
| Ubuntu, Debian, Mint (Intel or AMD) | `.deb` for amd64 |
| Any other 64-bit Linux with systemd | Linux tarball for x64 |
| 64-bit ARM Linux, like a Raspberry Pi 4 or 5 | `.deb` or tarball for arm64 (see the note below) |
| Docker | Build it yourself from the tarball, see [docs/linux.md](docs/linux.md) |

Get the files from the [Releases page](../../releases/latest) here or from https://kinode.tv/download. They're the same files, and both list SHA-256 checksums.

A few honest notes:

- **The Windows installer is not signed right now.** Windows will show a blue SmartScreen box about an unknown publisher. Choose More info, then Run anyway. Signing is being sorted out.
- **The ARM builds have never been run on real ARM hardware.** They are built from the same code and checked to contain ARM binaries, but nobody has tried them on a Pi yet. If you do, please tell me how it went, good or bad, in an issue.
- **There is no Docker image to pull yet.** There is a Dockerfile and compose file that build one from the Linux tarball. They have not been run end to end.

## Where you can watch

- Any modern web browser, nothing to install
- Android phones, tablets and Google TV (coming to Google Play)
- Roku (coming to the Roku Channel Store, sideload for now)
- Chromecast, from the web player or the Android app

## What it does

- Scans your folders and fills in posters, summaries and cast
- Plays files as they are when the device can, and converts on the graphics card when it can't (NVIDIA, Intel and AMD)
- Skip intro and credits, found by comparing episodes, no setup
- Profiles for everyone in the house, kid profiles with rating limits, bedtimes and time limits
- Share only the libraries you choose with family or friends
- Watch Together rooms with synced playback and chat
- Live channels made from your own library
- Music: lossless and hi-res, gapless, lyrics, queue, playlists, mixes, ListenBrainz
- Remote access over HTTPS with a certificate set up for you, on the port you already forwarded

The full list is on https://kinode.tv/features.

## No lock-in

Your media never leaves your machine. The Kinode hub (the free account on kinode.tv) is optional. It's there so the apps can find your server from anywhere and so you can share with people, and it's on by default because that's what most people want. You don't need it. The server works fully offline with a local account, and if kinode.tv went down your server and apps would keep playing.

## Bugs and questions

- **Bugs:** [open an issue](../../issues/new/choose). Say what device, what OS and what version, and what happened.
- **Questions and ideas:** [Discussions](../../discussions), or the forum at https://kinode.tv/forum
- **Security problems:** please don't post them in public. See [SECURITY.md](SECURITY.md).

## What changed

See [CHANGELOG.md](CHANGELOG.md).
