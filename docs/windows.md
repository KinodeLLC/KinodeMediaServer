# Installing on Windows

For Windows 10 and 11 on 64-bit Intel or AMD. There's no ARM or 32-bit build for Windows right now.

Get the current installer and SHA-256 checksum from [kinode.tv/download](https://kinode.tv/download). Install it on the computer that holds your media.

## Verify the installer

Before running the installer, right-click the downloaded file, choose **Properties → Digital Signatures**, then select the signature and open **Details**. Confirm that the signer is **KINODE LLC** and Windows says the signature is valid. If the signature is missing or invalid, or Windows lists an unknown or different publisher, don't run the file. Download a fresh copy from the official page and check it again.

## What setup asks

1. **Port.** 5466 by default. Only change it if something else on the machine already uses it.
2. **Firewall.** It adds a rule for your private network so your phone and TV can reach the server. It doesn't open anything to the internet.

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

## Watching away from home

Sign the server in to a free Kinode account and forward TCP port 5466 on your router to the computer running the server. The apps find it from anywhere, and the connection uses HTTPS with a certificate that's set up for you. The account is optional. Without it everything still works at home.

## If the page won't load

```
sc query KinodeMediaServer
net start KinodeMediaServer
```

If it starts and stops again, the error is in `C:\ProgramData\Kinode Media Server\logs\KinodeMediaServer.err.log`. Please attach it if you [open an issue](https://github.com/KinodeLLC/KinodeMediaServer/issues/new/choose).

## Uninstalling

Use Settings, Apps, or the Start menu shortcut. It asks whether to keep your accounts and watch history. Your media files are never touched.

More in the docs: https://kinode.tv/docs
