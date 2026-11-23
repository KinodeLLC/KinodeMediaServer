# Installing on Linux

Version 1.5.0. Downloads and checksums are on https://kinode.tv/download.

The packages carry their own Node runtime and the same full ffmpeg as the Windows installer, so nothing else needs installing for playback to work. They set up a systemd service called `kinode-media-server` that starts with the machine. When it's running, open `http://localhost:5466`, or the machine's address on port 5466 from another device, and create the first account.

## What you need

- 64-bit Linux, x64 or arm64. No 32-bit build.
- systemd
- glibc 2.28 or newer: Debian 10, Ubuntu 20.04 and anything later
- The server runs as its own `kinode` user, which needs to be able to read your media folders

Tested on Ubuntu 24.04 with an NVIDIA card.

## Ubuntu, Debian, Mint

```
sudo apt install ./kinode-media-server_1.5.0_amd64.deb
```

Use the `arm64` file on 64-bit ARM. To update, install the next `.deb` the same way.

## Any systemd distribution

```
tar xzf kinode-media-server-1.5.0-linux-x64.tar.gz
cd kinode-media-server-1.5.0-linux-x64
sudo ./install.sh
```

Add `--open-firewall` to open the port in ufw or firewalld. The tarball install updates itself from Settings, Updates.

## Raspberry Pi and other ARM boards

The arm64 builds have **not** been run on real ARM hardware yet. If you try one, please [open an issue](https://github.com/KinodeLLC/KinodeMediaServer/issues/new/choose) and say how it went, even if it just worked.

What should matter:

- You need the **64-bit** Raspberry Pi OS (or another 64-bit OS). The 32-bit one won't run it. `uname -m` should say `aarch64`.
- A Pi 4 or Pi 5. Older Pis are 32-bit or too slow.
- Files that play as they are should be fine. Converting video on a Pi will be slow, so it's best with files your devices can already play.

## Docker

There is no image to pull yet. The download page has a `Dockerfile`, `docker-compose.yml` and `docker-entrypoint.sh` that build one on your machine from the tarball. They haven't been run end to end, so treat them as a starting point.

1. Put the three Docker files and the tarball for your machine in one folder.
2. Edit `docker-compose.yml` and point `/path/to/your/media` at your media.
3. `docker compose up -d`

Your accounts and library live in `./data` next to the compose file. Your media is mounted read-only at `/media`. For an NVIDIA card you need the NVIDIA Container Toolkit; without one, delete the `deploy:` block. For Intel or AMD, uncomment the `devices:` lines.

## Uninstalling

```
sudo apt remove kinode-media-server        # .deb, keeps your library
sudo /opt/kinode-media-server/uninstall.sh  # tarball, keeps your library
```

Your media files are never touched. The server only reads them.

More in the Linux section of the docs: https://kinode.tv/docs#linux
