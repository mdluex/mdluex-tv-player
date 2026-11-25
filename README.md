# Mdluex TV Player

A tiny web page that hosts the YouTube player for the **Mdluex IPTV** Samsung TV app.

YouTube refuses to play videos embedded directly inside TV apps (they load from local files, so YouTube
returns *error 153*). The app instead loads this page from GitHub Pages — a real web address — and the
page plays the video and reports progress back to the app with `postMessage`.

`https://mdluex.github.io/mdluex-tv-player/?v=VIDEO_ID&start=0&mode=full`

| Parameter | Meaning |
|---|---|
| `v` | YouTube video id |
| `start` | start position in seconds |
| `mode` | `full` (sound, controlled by the app) or `preview` (muted, loops) |
| `random` | `1` = preview jumps to a random moment every 8 s |

No data is collected; the page only talks to YouTube and to the app that opened it.
