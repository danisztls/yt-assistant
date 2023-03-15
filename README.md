# Youtube Assistant

Enjoy Youtube with less effort and without nuisances like ads, sponsor segments and streaming issues.

## Use case

Automate retrieval of videos — or music — from a playlist.

## Usage

Create a `options.yml` file in the destination path:

*e.g.*

```yaml
---
video_id: ""
format: "bestvideo+bestaudio/best/best"
```

_`video_id` is mandatory and additional options from [yt-dlp](https://github.com/yt-dlp/yt-dlp#usage-and-options) are optional._

Run script:

```shell
yt-assistant <path>
```

## Features & Roadmap

- [x] Fetch playlist
- [x] Skip already downloaded
- [x] Load options from local config file
- [ ] Fetch channel
- [ ] Systemd service and timer
