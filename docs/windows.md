# Installing on Windows

Version 1.5.2, for Windows 10 and 11 on 64-bit Intel or AMD. There's no ARM or 32-bit build for Windows right now.

Get `KinodeMediaServer-1.5.2-x64.exe` from https://kinode.tv/download or the [Releases page](https://github.com/KinodeLLC/MediaServer/releases). Run it on the computer that holds your media.

## The unknown publisher warning

The installer isn't signed, so Windows shows a blue SmartScreen box saying it protected your PC. Choose **More info**, then **Run anyway**. The warning is about the missing signature, not about what the installer does.

## What setup asks

1. **What to install.** The server on its own, or the server and the Discord bot.
2. **Port.** 5466 by default. Only change it if something else on the machine already uses it.
3. **Firewall.** It adds a rule for your private network so your phone and TV can reach the server. It doesn't open anything to the internet.

Setup takes about a minute. Your browser opens at `http://localhost:5466` when it's done. Create your account, add your media folders and start watching. The first account you make is the owner of the server, and it only exists on your machine.

## Where things go

- The program: `C:\Program Files\Kinode Media Server`
- Your accounts, history and settings: `C:\ProgramData\Kinode Media Server`
- Logs: `C:\ProgramData\Kinode Media Server\logs`

It runs as a Windows service called Kinode Media Server and starts with the machine. If it crashes it restarts itself.

## Ports

| Port | Used for |
|---|---|
| 5466 TCP | The web app. This is the one you open in a browser. |
| 5467 UDP | Lets apps on your network find the server without typing an address |
| 5468 TCP | The Discord bot, only if you installed it |

## Watching away from home

Sign the server in to a free Kinode account and forward TCP port 5466 on your router to the computer running the server. The apps find it from anywhere, and the connection uses HTTPS with a certificate that's set up for you. The account is optional. Without it everything still works at home.

## If the page won't load

```
sc query KinodeMediaServer
net start KinodeMediaServer
```

If it starts and stops again, the error is in `C:\ProgramData\Kinode Media Server\logs\KinodeMediaServer.err.log`. Please attach it if you [open an issue](https://github.com/KinodeLLC/MediaServer/issues/new/choose).

## Uninstalling

Use Settings, Apps, or the Start menu shortcut. It asks whether to keep your accounts and watch history. Your media files are never touched.

More in the docs: https://kinode.tv/docs
