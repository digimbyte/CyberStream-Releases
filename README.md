# CyberStream Player

CyberStream Player is a Windows desktop request and private-listening player for Twitch and OBS workflows.

## Download

Download `CyberStreamPlayer.exe` from the latest GitHub Release. Place it in a stable folder where your Windows account has write access, then launch it.

CyberStream checks this repository once when it starts. When a newer stable version is available, it displays **New version detected** and asks before downloading anything. Choosing **Update and restart** downloads the new executable from this repository, verifies GitHub's SHA-256 release digest, replaces the installed executable after the current process closes, and relaunches CyberStream automatically.

## Requirements

- Windows 10 or Windows 11
- WebView2 Runtime
- `yt-dlp` and FFmpeg available on `PATH` for media acquisition and playback

Application settings, Twitch credentials, library state, and protected media cache remain in the user's local CyberStream storage when the executable updates.

The application source is maintained in a private repository. This public repository contains only distribution documentation and compiled release assets.
