<img width="678" height="563" alt="rip_asset" src="https://github.com/user-attachments/assets/0abf0725-f3f9-40bc-9dbf-bc0c7eb127a0" />
#-- Rip Studio --

**Rip Studio** is an all-in-one media management, disc ripping, web video downloading, torrent downloading, and media transcoding desktop tool.

---

## Key Features

### Optical Media Ripping & Scanning
- **DVD & Blu-ray Processing**: Automated disc scanning and 1:1 track extraction using **MakeMKV** (`makemkvcon`).
- **Audio CD Ripping**: Direct digital extraction of Audio CD tracks.
- **Transcoding Engines**: Integrated post-processing via **FFmpeg** and **HandBrake CLI** for high-quality MP4/MKV conversion.

### Web Video Downloader
-for downloading media from YouTube and supported web video streaming platforms.
- Multi-format extraction options: **MP4**, **MP3**, and **FLAC**.

### Torrent Manager
- Integrated magnet and `.torrent` downloader leveraging **aria2c** for fast asynchronous downloads.

### Intelligent Metadata & Entertainment
- **TMDb Integration**: Automatic movie metadata matching, release date resolution, and poster thumbnail loading via The Movie Database API.
- **Built-in Video Preview**: Live playback widget and log console.
- **Movie Trivia Game**: Embedded interactive trivia widget (`MovieTriviaWidget`) to play while waiting for rips.
- **Custom UI Themes**: Switch seamlessly between **Obsidian Dark**, **Slate Glass**, and **Cyber Neon** themes.

---

##  Prerequisites & Dependencies

### Python Environment
- **Python 3.9+** (64-bit recommended)

### Python Libraries
Install requirements using `pip`:
```bash
pip install -r requirements.txt
```

Key dependencies:
- **PySide6**: Qt for Python GUI framework
- **requests**: Network calls & TMDb API integration
- **yt-dlp**: Web video extraction
- **Pillow**: Image processing for icons and poster art

### External Tools
- **MakeMKV** (`makemkvcon64.exe`): Required for DVD/Blu-ray optical disc scanning and extraction.
- **FFmpeg** (`ffmpeg.exe`): Required for media format conversions and audio extraction.
- **HandBrake CLI** (`HandBrakeCLI.exe`): Optional, required for high-quality HandBrake video encoding profiles.
- **aria2c** (`aria2c.exe`): Included in the project directory for torrent operations.


### Basic Workflow
1. **Optical Media**: Insert a DVD/Blu-ray or Audio CD, select your optical drive from the dropdown, choose **Scan Video Disc** or **Rip Audio CD**, and click **Start Processing**. Select target titles and encoding format, then click **Rip Disc**.
2. **Web Downloader**: Switch to the **Web Downloader** tab, paste a media URL, pick your desired format (MP4/MP3/FLAC), and click **Download Media**.
3. **Torrent Manager**: Switch to the **Torrent Manager** tab, enter a magnet link or `.torrent` file path, and start downloading.

##  Configuration (`config.json`)

Settings are stored in `config.json` and editable through the in-app **Settings** menu:

```json
{
    "makemkv_path": "C:/Program Files (x86)/MakeMKV/makemkvcon64.exe",
    "ffmpeg_path": "C:/Users/<User>/AppData/Local/Microsoft/WinGet/Links/ffmpeg.exe",
    "handbrake_path": "C:/Program Files/HandBrake/HandBrakeCLI.exe",
    "output_dir": "C:/Media_Rips",
    "tmdb_api_key": "YOUR_TMDB_API_KEY",
    "theme"top": true,
    "notif_sound: "Slate Glass",
    "read_passes": 1,
    "notif_desk": true,
    "notif_sound_file": "Notification_Sound.m4a",
    "force_rip": true,
    "debug_mode": false,
    "keep_raw_on_failure": false
}
```

##  License

This project is intended for personal media backup and archival purposes. Please respect copyright laws and terms of service for any external platforms or media processed.
