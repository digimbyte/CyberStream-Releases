# CyberStream Player — Feature List

**CyberStream is a Windows music player that brings together your own music, online music links, Twitch requests, and a customizable OBS overlay.** Use it purely for personal listening, or connect the streaming features when you need them.

[Download for Windows](https://github.com/digimbyte/CyberStream-Releases/releases/latest) · [What's new](https://github.com/digimbyte/CyberStream-Releases/releases)

## 1. A unified music library

Add individual songs, albums, playlists, local files, or folders through one Library input. Supported sources include YouTube, SoundCloud, Spotify, Apple Music, and other compatible public music links.

Titles, artists, and artwork are filled in automatically where available. You can edit display titles and artist names afterward.

**The important nuance:** Spotify and Apple Music links identify the music, while playback uses a matching recording found on YouTube. The version you hear can differ from the original platform's recording.

## 2. Local music that stays in its original location

CyberStream supports local MP3, WAV, FLAC, and OGG files, including music on Windows network shares.

Your files stay in their existing folders. Adding them creates references; removing them from the Library does not delete the originals.

Folder imports can include loose songs and immediate subfolders treated as albums. It does not scan an unlimited number of nested folders.

## 3. Library organization and selective playback

- Drag Library entries into your preferred order.
- Enable or disable an entry without deleting it.
- Open a collection's track list, search within it, and enable or disable individual songs.
- Edit an entry's details or remove it.
- Copy a source link.

Keep a broader collection while choosing a smaller selection for the current listening rotation.

## 4. An active queue you can control directly

The Active Queue shows the current track and scheduled music, with grouped collections where appropriate.

Select a track and play it directly, remove items from the rotation, and see when media is waiting, loading, unavailable, or failed.

Queue membership and current playback are handled separately: taking a playing song out of the rotation can let it finish without keeping it eligible for future playback.

## 5. Playback controls and smoother transitions

The player provides play/pause, stop, next-track control, and seeking within the current song. It displays artwork, title, artist, collection, elapsed time, and duration.

Windows media keys support play/pause, next, and previous.

An optional **Blending** switch smooths track changes and seeking. Between songs, it can briefly overlap the transition when the next track is ready. It is a simple on/off feature.

## 6. Three distinct ways to shuffle

| Mode | What it does |
| --- | --- |
| **Shallow Shuffle** | Shuffles collections and standalone songs while preserving the order inside each collection. |
| **Recursive Shuffle** | Shuffles collections and also shuffles their songs, keeping each collection grouped. |
| **Total Mix** | Mixes individual songs across collections into one combined order. |

**Loop Library** repeats the enabled Library rotation. Choose between an album-oriented experience and a fully mixed soundtrack.

## 7. Twitch chat requests

Link Twitch to receive music requests directly from your channel's chat. The request command is customizable; the starting command is `!request`.

Restrict requests to moderators, subscribers, followers, everyone, or disable requests entirely. Moderator access is included in the broader subscriber and follower settings.

Requests can wait for manual **Accept / Reject**, or be accepted automatically. Duplicate requests already pending or queued are rejected.

Automatic acceptance applies to eligible incoming requests; it is not limited to songs already in your Library. The app receives chat requests without posting confirmation or rejection messages back into chat.

## 8. Control over what happens to accepted requests

Accepting a request adds it to the Active Queue. Separately, choose how the song is retained:

| Setting | Intended use |
| --- | --- |
| **Memory only** | Play a temporary request without automatically adding it to the Library. |
| **Library disabled** | Save it to the Library, but leave it out of the normal rotation. |
| **Permanent** | Save it for future playback as part of the Library. |

Temporary requests also have an **Add to Library** action if you decide to keep one.

**Persist Ephemeral** controls whether eligible temporary request state survives a restart. Acceptance, Library membership, and restart retention are separate decisions.

## 9. Track-length limits

A configurable maximum length helps prevent unexpectedly long new remote additions and requests. The setting ranges from one minute to twelve hours, with a thirty-minute default.

This is an admission check: it does not cut off a playing song when the limit is reached. Local imports and already-known tracks are treated differently from new remote tracks.

## 10. Separate listening and stream volumes

| Control | What it changes |
| --- | --- |
| **Local** | Music heard through your computer's listening output. |
| **Stream** | Music delivered through the OBS overlay. |
| **Master** | Both routes together. |

Listen quietly while keeping stream music louder, or mute local listening without muting the stream.

The OBS integration carries audio through the overlay's Browser Source. The built-in guide explains setup and avoiding duplicate audio capture.

## 11. A live OBS now-playing overlay

The Streamer Overlay provides a copyable link for an OBS Browser Source. It displays the current song, artwork, playback status, and timing.

OBS determines the overlay's canvas size, and the widget fills that space. Playback and appearance changes update live.

The overlay also handles reconnection, displays an offline state when the player is unavailable, and includes automatic refresh behavior when it detects a different app build.

## 12. Extensive overlay appearance controls

- **Backgrounds:** solid colors, gradients, images, transparency, blur, and the current song's artwork.
- **Layouts:** left-first, right-first, top-down, bottom-up, centered, and hero arrangements.
- **Composition:** artwork/text order, alignment, spacing, padding, and compact-layout behavior.
- **Artwork:** visibility, scale, and fallback text.
- **Typography:** font selection and separate visibility, color, and size controls for title, artist/source, status, and time.
- **Progress:** independent bar and time visibility, gradient colors, bar thickness, and width.
- **Edge accents:** individually controlled top, right, bottom, and left edges, with colors and thickness.
- **Branding:** an idle image, image positioning and fit, plus an option to override track artwork.

A generated-style action changes coordinated colors and layout choices, alongside session restoration and default restoration controls. Style changes save automatically.

## 13. Library refresh and optional automatic synchronization

Refresh a Library source to pick up changes. Separate **Auto Sync Local** and **Auto Sync Remote** switches enable automatic synchronization.

Automatic synchronization checks enabled sources at startup and relevant sources as queue selection changes. Repeated manual refresh clicks are combined rather than starting duplicate work.

Remote synchronization reuses completed cached music instead of automatically downloading everything again.

## 14. Managed media storage

CyberStream prepares remote music locally and reuses completed downloads. It also prepares upcoming music in advance to reduce waiting between tracks.

Choose a storage location and select protected Cyber storage or ordinary managed MP3 storage for future acquisitions.

**Existing cached media is retained** when changing encoding settings, finishing requests, or removing Library entries. **Purge Cache** is the explicit deletion action. Original local music files remain outside that managed cache.

Shared temporary media and artwork can also be reused in memory, then released after an hour without access while protecting active playback.

## 15. Optional service sign-in browser

An optional internal browser downloads a dedicated portable Firefox installation for service sign-in and age-verification pages.

It includes controls for Twitch, YouTube, SoundCloud, Spotify, and Apple Music sessions, with distinctions between saved, validated, disconnected, and unavailable session states.

Sessions stay on the computer across player updates. Uninstalling the browser removes its profiles and saved sessions.

Provider acceptance and authenticated playback depend on the service. A saved session does not by itself establish successful authenticated playback.

## 16. Automatic setup, updates, and activity reporting

Required media tools download automatically, are reused across launches, and can be restored if missing.

CyberStream checks for application updates on startup. Choose **Update and restart** or **Later**, with Library and settings retained.

Settings generally save automatically. Session Activity and playback logs expose connection events, refresh results, and acquisition failures. Queue failure indicators provide access to those logs.

## 17. Twitch panel extension: a separate, unfinished integration

A viewer-facing Twitch panel is prepared to show current playback and upcoming songs.

Live updates and viewer requests still require a hosted relay service. This is **prepared extension work**, rather than a fully connected feature of the desktop player today.
