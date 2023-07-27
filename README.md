# Cloudflare Stream Video Downloader

## Supports
- Downloading videos of a user-selected resolution
- Downloading individual segments of a user-selected resolution

## Usage
```sh
./stream-download <HLS_MANIFEST_URL>
```

For building the binary, see section below on `Builds & Releases` or [download latest release here.](https://github.com/Schachte/cloudflare-stream-downloader/releases)

You can grab the HLS manifest from the Cloudflare Dash as shown in the image below:

![](./assets/dashboard.png)

## Example Output
```
./stream-download https://.../manifest/video.m3u8

Use the arrow keys to navigate: ↓ ↑ → ←
? Cloudflare Stream Downloader::
  ▸ Download video and segments
    List available resolutions
    Count number of segments
    🚫 Exit

✔ Download video and segments
📋 Listing all available resolutions for video UID: f92743594bb2d9471c8ef80b9437c1ff

0) 766x360
1) 510x240
2) 🚫 Exit

📼 Select resolution: 0
🌱 Beginning download for [766x360]
10% complete
20% complete
30% complete
40% complete
50% complete
60% complete
70% complete
80% complete
90% complete
Complete!
---------------------------------------------
Video output:
./f92743594bb2d9471c8ef80b9437c1ff/766x360/f92743594bb2d9471c8ef80b9437c1ff.mp4

Segments output:
./f92743594bb2d9471c8ef80b9437c1ff/766x360/segments/

Playback:
ffplay ./f92743594bb2d9471c8ef80b9437c1ff/766x360/f92743594bb2d9471c8ef80b9437c1ff.mp4
---------------------------------------------
```

## Builds & Releases

### Releases 

[Download latest release here.](https://github.com/Schachte/cloudflare-stream-downloader/releases)

or 

You can also run the latest builds for all operating systems by running: `make all`. 