<div align="center">

# A-Z Downloader

**A fast, free download manager for Windows — with one-click video downloads from your browser.**

[![Download for Windows](https://img.shields.io/badge/Download-Windows%20installer-0b5cd5?style=for-the-badge&logo=windows)](https://github.com/Yousha1011/A-Z-Downloader/releases/latest)
&nbsp;
[![Latest release](https://img.shields.io/github/v/release/Yousha1011/A-Z-Downloader?style=for-the-badge&label=Latest)](https://github.com/Yousha1011/A-Z-Downloader/releases/latest)
&nbsp;
[![Report a problem](https://img.shields.io/badge/Report-a%20problem-cf222e?style=for-the-badge&logo=github)](https://github.com/Yousha1011/A-Z-Downloader/issues/new/choose)

</div>

---

## Contents

1. [What is A-Z Downloader?](#what-is-a-z-downloader)
2. [Screenshots](#screenshots)
3. [Features](#features)
4. [System requirements](#system-requirements)
5. [Download and install](#download-and-install)
6. [Add the browser extension](#add-the-browser-extension)
7. [How to use it](#how-to-use-it)
8. [Updating and uninstalling](#updating-and-uninstalling)
9. [Frequently asked questions](#frequently-asked-questions)
10. [Report a problem or suggest an idea](#report-a-problem-or-suggest-an-idea)
11. [Privacy and security](#privacy-and-security)
12. [Credits and licenses](#credits-and-licenses)

---

## What is A-Z Downloader?

A-Z Downloader is a download manager for Windows, in the spirit of Internet Download Manager (IDM). It
speeds up file downloads by using several connections at once, lets you pause and resume at any time, and
downloads videos from YouTube and over a thousand other websites.

Its companion **browser extension** (Chrome, Edge, Brave, Opera, Firefox) puts a **Download this video**
button on videos you watch. Click it, pick a quality, and the download starts in the app. Downloads you
start in the browser are handed to the app automatically.

It's free, has no ads, needs no account, and installs without administrator rights.

---

## Screenshots

**Download this video** — the button on a video lists every quality. One click starts the download.

![The "Download this video" button on a YouTube video, listing qualities from 1080p down to 214p with their sizes](docs/screenshots/download-button.png)

**The main window** — all your downloads, sorted into categories, with progress, speed and time left.

![The A-Z Downloader main window with a list of completed downloads and category folders](docs/screenshots/main-window.png)

**The download window** — live speed, time left, resume support and per-connection progress.

![A download window showing a 1.66 GB video downloading at 7.71 MB/s with 3 minutes 37 seconds left](docs/screenshots/download-progress.png)

---

## Features

### ⚡ Fast, reliable downloads
- **Multi-connection downloads** — starts with one connection and adds more (up to 32) only while they make
  the download faster. Servers that limit connections are respected.
- **Pause and resume** — after pausing, closing the app, a crash, or even a restart of the computer.
- **HTTP, HTTPS, FTP and FTPS**, including FTP logins (`ftp://user:password@host/file`).
- **Queue** — downloads wait their turn; choose how many run at the same time.
- **Speed limiter**, **scheduler** (start and stop downloads at set times), and **shut down when done**.
- **Automatic categories** — Video, Music, Documents, Programs and Compressed files each get their own folder.
- **Clipboard monitoring** — copy a download link and the app offers to download it.

### 🎬 Video downloads
- **YouTube and 1000+ other sites** — YouTube (including Shorts), Facebook, Instagram, TikTok, X (Twitter),
  Reddit, Dailymotion, Vimeo, Twitch, Pinterest, LinkedIn, Bluesky, TED, the Internet Archive, and news sites
  such as BBC, CBC, CBS, NBC, ABC News, MSN, The Guardian and Al Jazeera.
- **Choose your quality** — from 144p up to 4K, or **audio only** as MP3 or M4A, with the size shown for each.
- **Streaming formats** — HLS (`.m3u8`) and DASH (`.mpd`) streams, including AES-128 encrypted HLS.
- **Picture and sound joined automatically** into one MP4 (or MKV) file.
- **Clean file names** — the video's real title, without view counts or hashtag clutter.

### 🔄 Audio and video converter
- **40 formats** — MP4 (H.264 / H.265), MKV, AV1, WebM, MOV, AVI, WMV, FLV, MPG, TS, 3GP, GIF and more,
  plus MP3, M4A, AAC, WAV, FLAC, OGG, Opus, WMA, AC3 and more for audio.
- Video to audio, audio to video (with a waveform picture), resize, choose quality, or a fast lossless
  container change.
- Right-click any audio or video file in File Explorer and choose **Convert with A-Z Downloader**.

### 🧩 Browser extension
- **Download this video** button on videos, with every available quality.
- **Takes over browser downloads** and passes them to the app (if the app isn't running, the browser simply
  downloads as usual).
- **Detects video streams** a page is playing, and adds **Download with A-Z Downloader** to right-click menus.

---

## System requirements

| | |
|---|---|
| **Operating system** | Windows 10 or Windows 11 (64-bit) |
| **Framework** | .NET Framework 4.8 — already included in Windows 10 (since May 2019) and Windows 11 |
| **Disk space** | About 450 MB (the app plus its bundled video tools) |
| **Browser (for the extension)** | Microsoft Edge, Google Chrome, Brave, Opera, or Firefox |
| **Administrator rights** | Not needed — it installs for your Windows account only |

---

## Download and install

1. Go to the **[latest release](https://github.com/Yousha1011/A-Z-Downloader/releases/latest)** page.
2. Under **Assets**, click **`AZDownloader-Setup-1.1.1.exe`** to download it (about 183 MB).
3. Open the downloaded file.
4. **Windows may show "Windows protected your PC."** This appears because the installer isn't signed with
   a paid code-signing certificate yet. Click **More info**, then **Run anyway**.
5. Choose the install folder (the default is fine) and click **Install**.

When it finishes you'll have:
- **A-Z Downloader** in the Start menu (and on the desktop, if you chose that),
- a **Convert with A-Z Downloader** entry when you right-click audio and video files,
- an entry in **Settings → Apps** to uninstall it.

The installer already includes the video tools it needs (yt-dlp, FFmpeg, Deno), so there's nothing else to
download.

<details>
<summary><b>Check that your download is genuine (optional)</b></summary>

Each release lists the installer's **SHA-256 checksum**. To compare, open PowerShell in your Downloads folder
and run:

```powershell
Get-FileHash .\AZDownloader-Setup-1.1.1.exe -Algorithm SHA256
```

The result should match the checksum on the release page exactly.
</details>

<details>
<summary><b>Silent install (for IT administrators)</b></summary>

```text
AZDownloader-Setup-1.1.1.exe /S                       install with default settings
AZDownloader-Setup-1.1.1.exe /S /D=C:\Apps\A-Z Downloader   install to a chosen folder (/D= must come last)
"%LOCALAPPDATA%\Programs\A-Z Downloader\uninstall.exe" /uninstall /S   uninstall silently
```
</details>

---

## Add the browser extension

The extension gives you the **Download this video** button and sends browser downloads to the app. It's
installed together with the app, in this folder:

```text
%LOCALAPPDATA%\Programs\A-Z Downloader\extension
```

> **Tip:** In the app, **Tools → Browser integration** shows these steps and opens the folder for you.

### Microsoft Edge
1. Open Edge and go to **`edge://extensions`**.
2. Turn on **Developer mode** (the switch in the left-hand panel).
3. Click **Load unpacked**.
4. In the folder window, paste this into the address bar, press **Enter**, then click **Select Folder**:
   ```text
   %LOCALAPPDATA%\Programs\A-Z Downloader\extension\chrome
   ```

### Google Chrome, Brave and Opera
1. Go to **`chrome://extensions`** (Brave: `brave://extensions`, Opera: `opera://extensions`).
2. Turn on **Developer mode** (top-right corner).
3. Click **Load unpacked**.
4. Choose the same folder:
   ```text
   %LOCALAPPDATA%\Programs\A-Z Downloader\extension\chrome
   ```

### Firefox
Regular Firefox only installs add-ons signed by Mozilla. You can:
- **Try it for one session:** go to **`about:debugging`** → **This Firefox** → **Load Temporary Add-on…** and
  choose `extension\azdownloader-firefox.xpi` from the folder above. (It is removed when Firefox closes.)
- **Use Firefox Developer Edition or Nightly**, set `xpinstall.signatures.required` to `false` in
  `about:config`, then install the `.xpi` file.

### Connect the extension to the app (first time only)
1. Make sure A-Z Downloader is running (it can stay in the notification area near the clock).
2. Click the A-Z Downloader icon in your browser's toolbar.
3. The app asks **"A browser extension wants to connect…"** — click **Yes**.

You only do this once per browser. The extension's popup then says **Connected to A-Z Downloader**.

> **After updating the app:** open your browser's extensions page and click **Reload** on A-Z Downloader,
> then refresh any open tabs.

---

## How to use it

### Download a video
1. Open a video in your browser and start playing it.
2. Click **Download this video** at the top-right of the player.
3. Pick a quality, or **Audio only (MP3)**.
4. The download window opens in front of your browser, and the file is saved to **Downloads\Video**.

Some players (for example on news sites) only load the video after you press **play** — the button appears
once the video starts.

### Download a file or a link
- Click any download link in your browser — the app takes it over automatically, or
- In the app, click **Add URL** (or press **Ctrl+N**), paste the link and click **Start Download**, or
- Right-click a link in your browser and choose **Download with A-Z Downloader**.

### Manage downloads
- **Pause / Resume** a download from its window or the main list; **Pause All** and **Resume All** are on
  the toolbar.
- **Download Later** in the Add URL window queues a download for the **Scheduler** (Tools → Scheduler).
- Files are sorted into category folders under your Downloads folder. Change the folder, the number of
  simultaneous downloads, connections and the speed limit in **Tools → Options**.

### Convert a file
- In the app: **Tools → Audio & Video Converter** (Ctrl+K), add files, pick a format and click **Convert**, or
- In File Explorer: right-click an audio or video file → **Convert with A-Z Downloader**.

---

## Updating and uninstalling

- **Update:** download the newest installer from the
  [Releases](https://github.com/Yousha1011/A-Z-Downloader/releases) page and run it. It installs over the old
  version and keeps your settings and download list. Then click **Reload** on the extension in your browser.
- **Update the video tools only:** in the app, **Tools → Components**. New versions are installed only if they
  match the publisher's official checksum.
- **Uninstall:** **Settings → Apps → Installed apps → A-Z Downloader → Uninstall**. You can choose to keep or
  remove your settings and download list. Your downloaded files are never deleted.

---

## Frequently asked questions

<details>
<summary><b>Windows says "Windows protected your PC". Is it safe?</b></summary>

The installer isn't signed with a code-signing certificate yet, so Windows SmartScreen doesn't recognise it.
Click **More info → Run anyway**. You can compare the file's SHA-256 checksum with the one on the release page
(see [Download and install](#download-and-install)).
</details>

<details>
<summary><b>The "Download this video" button doesn't appear.</b></summary>

- Check the extension is loaded and turned on (see [Add the browser extension](#add-the-browser-extension)).
- Press **play** on the video — some sites only create the video when it starts playing.
- If you just installed or reloaded the extension, **refresh the page (F5)**.
- In the extension's popup, make sure **Show "Download this video" button on videos** is ticked.
</details>

<details>
<summary><b>Clicking the button says "A-Z Downloader isn't running".</b></summary>

Start A-Z Downloader from the Start menu. It can keep running in the notification area: closing the window
doesn't quit it. To have it start with Windows, tick **Start with Windows** in **Tools → Options**.
</details>

<details>
<summary><b>A site says the video is only for signed-in users.</b></summary>

Use the **Download this video** button in your browser while signed in to that site — the extension passes
your browser session to the app for that site only. For links pasted into the app, you can choose a browser to
read sign-ins from in **Tools → Options → Browser** (Firefox works best).
</details>

<details>
<summary><b>Can it download Netflix, Disney+, Prime Video or Spotify?</b></summary>

No. These services protect their videos with DRM copy protection, and A-Z Downloader does not bypass it.
</details>

<details>
<summary><b>Where are my files and settings?</b></summary>

| What | Where |
|---|---|
| Downloaded files | Your **Downloads** folder, in category subfolders (Video, Music…) — changeable in Options |
| The app and its tools | `%LOCALAPPDATA%\Programs\A-Z Downloader` |
| Settings and download list | `%LOCALAPPDATA%\AZDownloader` |
</details>

---

## Report a problem or suggest an idea

Found a bug, a site that doesn't work, or have an idea? Please open an issue — it only takes a minute and
helps everyone.

1. Go to **[Issues → New issue](https://github.com/Yousha1011/A-Z-Downloader/issues/new/choose)**
   (you need a free GitHub account).
2. Choose **Bug report**, **Site not working**, or **Feature request**.
3. Fill in the short form. For problems, these details help most:
   - your **A-Z Downloader version** (Help → About) and **Windows version**,
   - the **link** you tried (if it's public) and **what happened**, including any error message,
   - for button problems, your **browser** and the lines starting with `[A-Z Downloader]` in the page's
     console (press **F12** → **Console**).

Before opening a new issue, please
[search existing issues](https://github.com/Yousha1011/A-Z-Downloader/issues?q=is%3Aissue) — someone may
already have reported it.

> Please don't post passwords, cookies or links to private content in an issue — issues are public.

---

## Privacy and security

- **No tracking, no ads, no account.** A-Z Downloader doesn't collect or send any information about you.
- The app talks to your browser **only on your own computer** (`127.0.0.1`). Websites can't send it
  downloads, and other browser extensions can't control it — each browser must be approved by you once.
- Your browser's cookies are only used for the site they belong to, and only for the download you started.
- Video tools are updated only from their official sources, and only when the file matches the publisher's
  published checksum.

Please respect copyright and each website's terms of use: download only content you have the right to save.

---

## Credits and licenses

A-Z Downloader includes these free, open-source programs, unmodified, in its `tools` folder:

| Program | Used for | License |
|---|---|---|
| [yt-dlp](https://github.com/yt-dlp/yt-dlp) | Reading video pages and qualities | The Unlicense (public domain) |
| [FFmpeg](https://ffmpeg.org) (Windows build by [BtbN](https://github.com/BtbN/FFmpeg-Builds)) | Joining video and audio, converting | GPL-3.0 |
| [Deno](https://deno.com) | JavaScript runtime yt-dlp uses for YouTube | MIT |

Full license texts and versions are in `tools\THIRD-PARTY-NOTICES.txt` and `tools\GPL-3.0.txt` in the install
folder. The source code of the bundled FFmpeg build is available from
[BtbN/FFmpeg-Builds](https://github.com/BtbN/FFmpeg-Builds) and [git.ffmpeg.org](https://git.ffmpeg.org/ffmpeg.git).

**A-Z Downloader** © 2026 Yousha1011. All rights reserved. You're welcome to download and use the app for
free. The A-Z Downloader program itself may not be redistributed or modified without permission.
