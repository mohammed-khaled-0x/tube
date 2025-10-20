# Modern YouTube Downloader

A sleek, feature-rich GUI application for downloading YouTube videos and playlists, built with Python and powered by `yt-dlp` and `ffmpeg`.

## ✨ Features

This application provides a comprehensive set of tools to make video downloading simple and powerful.

### Smart URL Fetching

Paste any YouTube video or playlist URL and click **Fetch Info**. The app will quickly retrieve all necessary data, identify playlist contents, and prepare for download.

### Powerful Playlist Support

When you paste a playlist URL, the app fetches all videos in that list. A selection dialog appears, allowing you to **choose exactly which videos** you want to download (e.g., select 6 out of 444 videos).

### Advanced Download Queue

All selected videos are added to the **Downloads Queue** for easy management.

  * **Prioritize Downloads:** Use the **Up** and **Down** buttons to reorder videos and decide which ones download first.
  * **Full Control:** **Pause**, **Resume**, or **Cancel** any download at any time.
  * **Visual Status Indicators:** The border of each video card changes color to reflect its current status:
      * 🔵 **Blue:** Actively downloading
      * 🟢 **Green:** Download successful
      * 🟡 **Yellow:** Queued / Waiting
      * 🔴 **Red:** Canceled or Failed

### Advanced Conversion & Audio Options

Click the **Advanced...** button before downloading to access powerful conversion settings:

  * **Video Conversion:** Keep the original format, or convert to **MP4** or **MKV**.
  * **Audio Extraction:** Keep the original audio, extract to **MP3**, **M4A (AAC)**, or **Opus**.
  * **Subtitles:** Download subtitles for a specific language or all available languages.
  * **Thumbnail:** Embed the video thumbnail into the downloaded file.

### Comprehensive Settings

Customize the app's behavior from the **Settings** menu.

  * **General Tab:**

      * **Download Path:** Set your preferred folder for all downloads.
      * **Parallel Downloads:** Enable concurrent downloads and set the max number (e.g., download 1-by-1, 3-by-3, or 5-by-5).
      * **Filename Template:** Use metadata tags (like `%(title)s`, `%(id)s`, `%(ext)s`) to create your perfect file naming scheme.
      * **Cookies File:** Use a cookies file for downloading private or age-restricted content.

  * **Dependencies Tab:**

      * View the status and version of `yt-dlp` and `ffmpeg`.
      * **Check for Updates** or **Download/Update** `yt-dlp` directly from the app.

### Download History

Keep track of your completed downloads in the **History** window. You can search, filter by status, open files, or re-download any item.

## 📦 Requirements

  * **Python 3.x**
  * **[yt-dlp](https://github.com/yt-dlp/yt-dlp):** The core engine for fetching and downloading.
  * **[FFmpeg](https://ffmpeg.org/):** Required for merging video/audio, file conversions, and thumbnail embedding.

The app can manage `yt-dlp` for you, but **FFmpeg must be installed separately** and available in your system's PATH.

## 🔧 Installation

To run the application with its full feature set, you must install `yt-dlp` and `FFmpeg` on your system.

### 1\. Installing `yt-dlp`

`yt-dlp` is the core engine for fetching and downloading videos. While the app can manage and update it, it's best to install it beforehand.

Open a Terminal or Command Prompt and run the following command to install it via `pip`:

```bash
pip install --upgrade yt-dlp
```

### 2\. Installing `FFmpeg`

`FFmpeg` is essential for merging audio/video, converting formats, and embedding thumbnails. **It must be installed separately and added to your system's PATH.**

#### Windows

1.  Download the latest release from **[FFmpeg builds](https://www.gyan.dev/ffmpeg/builds/)** (choose the `ffmpeg-release-full.7z` archive).
2.  Extract the archive to a permanent location on your computer (e.g., `C:\ffmpeg`).
3.  Add the `bin` folder path (inside the `ffmpeg` directory) to your system's environment variables:
      * Search for "Edit the system environment variables" in the Start Menu and open it.
      * Click the **Environment Variables...** button.
      * In the "System variables" section, find the `Path` variable and click **Edit**.
      * Click **New** and paste the full path to the `bin` folder (e.g., `C:\ffmpeg\bin`).
      * Click **OK** on all windows to save the changes.
4.  To verify the installation, open a **new** Command Prompt window and type `ffmpeg -version`. If it displays version information, the installation was successful.

#### macOS

The easiest way to install is with **[Homebrew](https://brew.sh/)**. Open your Terminal and run:

```bash
brew install ffmpeg
```

#### Linux

Use your distribution's package manager. Open a Terminal and run the appropriate command:

  * **On Debian/Ubuntu-based distros:**

    ```bash
    sudo apt update && sudo apt install ffmpeg
    ```

  * **On Arch Linux:**

    ```bash
    sudo pacman -S ffmpeg
    ```

  * **On Fedora:**

    ```bash
    sudo dnf install ffmpeg
    ```

## 🚀 How to Use

1.  Paste a YouTube video or playlist URL into the top bar and click **Fetch Info**.
2.  If it's a playlist, select the videos you want to download.
3.  (Optional) Choose a format from the **Available Formats** dropdown or click **Advanced...** for specific conversion options.
4.  Click the **Download** button.
5.  Manage your active downloads in the **Downloads Queue**.
