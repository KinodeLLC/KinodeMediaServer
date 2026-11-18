# What changed

## 1.5.2 (17 November 2026)

Windows only so far. Linux 1.5.2 is coming.

New
- Missing files: if a movie, episode or song file goes missing, its title stays in your library with a FILE MISSING mark on the poster, and the dashboard opens with a list of what's missing and what to do about each one
- Every file in your library is recorded twice, in the server's database and in dated copies kept outside it, and checked after each scan and every few hours
- A drive or share that can't be reached shows once as offline, instead of as thousands of missing files
- Age ratings on the top right of every poster, and optional parental controls for each profile and account, with a parent PIN to unlock a single title
- Private libraries locked with a PIN that stay completely out of sight until unlocked
- Live TV: add M3U playlists, Xtream accounts or HDHomeRun tuners and watch with a TV guide
- TVs without a Kinode app can play your library on your home network through DLNA. It's on by default and you can switch it off in Settings
- Every setting is reworded in plain words, with a short hint under each one

Fixed
- A library scan no longer takes titles out of your library when their file can't be found. You decide what happens to them

The installer is unsigned, like 1.5.0.

## 1.5.1 (17 November 2026)

Not released on its own. Its changes are in 1.5.2.

- Music: every format plays (converted when needed), full-screen Now Playing with synced lyrics, an editable queue that's still there next time, Liked songs and mixes, volume leveling with ReplayGain, M3U import and export, ListenBrainz, a sleep timer, and Hi-Res and Lossless badges

## 1.5.0 (13 November 2026)

New
- A new look for the web player, with a light and dark switch
- Hundreds of settings, with search, export and import
- Link a phone, TV or streaming box by typing its code at kinode.tv/link or scanning the code on screen
- Pick the streaming services you use and browse what's on each one from the sidebar
- A cast row under the player, which follows the scene when scene data is there
- A full editor for any title, with a lock on every field and editing many titles at once
- Download subtitles from a title's menu as VTT or SRT, and edit a subtitle's text and timing (your copy is kept separately, the original is never changed)
- Ask for subtitles in a language and see where the request is
- Folders are watched for new files, with extras, NFO files and artwork beside your media
- Credits are detected so the next episode can start sooner
- Bandwidth limits, PINs on guest links, an audit log, and automatic updates
- Gapless playback and crossfade for music
- Share a server by ticking its libraries, or all of them including ones added later
- People you share with see your server by the name you give it, never its address
- Your Kinode account lists every signed-in device, with rename, remove and sign out everywhere else
- Removing a device or a share stops it playing within about a minute

Fixed
- Folder watching on Windows no longer rescans neighbouring folders
- Intro detection timing
- The tray app stayed closed after an automatic update
- A share saved with no libraries gave the person an empty Home

Linux: .deb and tarball packages for x64 and arm64.
Windows: x64 only for this release, and the installer is unsigned.

## 1.4.0 (5 November 2026)

New
- Decoding and encoding on NVIDIA, Intel and AMD graphics cards, so converting uses the GPU instead of the processor
- Hardware transcoding settings and health checks

Fixed
- Steadier streams on NVIDIA
- Sign-in limits and security fixes

## Older

Earlier versions are listed at https://kinode.tv/download.
