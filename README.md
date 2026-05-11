# music-handaduke

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

アルバム「はんだづけはたのしいよ」 (Album: "Soldering is Fun")

This repository contains a web-based music player and the data for the AI-generated music album "はんだづけはたのしいよ". The music was created using [Suno](https://suno.com/).

## ▶️ Live Demo

Listen to the full album on the web player:
**[https://code4fukui.github.io/music-handaduke/](https://code4fukui.github.io/music-handaduke/)**

The player features:
- A complete playlist of the album tracks.
- Display of album art, lyrics, and the original AI generation prompts.
- A blurred background that dynamically updates with the current track's artwork.
- Media Session API integration for lock screen and remote playback controls.

## About the Music

The album was generated from the following public Suno playlist:
- [https://suno.com/playlist/ca3142ba-48ab-411f-b837-44c60c97c1e6](https://suno.com/playlist/ca3142ba-48ab-411f-b837-44c60c97c1e6)

## Download Playlist Data

You can download the original audio files, images, and metadata from Suno using the `music-opendata-fukui` Deno script.

```sh
deno run -A https://code4fukui.github.io/music-opendata-fukui/download.js https://suno.com/playlist/ca3142ba-48ab-411f-b837-44c60c97c1e6
```
This command will create a directory containing the `playlist.json` file and all associated media assets.

## Source Code

This project is a self-contained web application built with vanilla HTML, CSS, and JavaScript. All music data is loaded from the local `playlist.json` file.

- **`index.html`**: The main application file for the music player.
- **`playlist.json`**: Contains all metadata, lyrics, and local paths to the album's audio and image files.
- **`audio/` & `image_large/`**: Directories containing the downloaded media assets.

## Credits

- Music generated via [Suno](https://suno.com/)
- Project by [Code for FUKUI](https://github.com/code4fukui)