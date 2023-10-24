# Youtube Assistant

Enjoy Youtube with less effort and without nuisances like ads, sponsor segments and streaming issues. **yt-assistant** is a wrapper for [yt-dlp](https://github.com/yt-dlp/yt-dlp/) which helps with storing configuration and automation.

## Use case

- Automate retrieval of videos — or music — from a playlist. 
- Bypass ads, anti-adblock warnings and other nuisances. 
- 

## Usage

### Config

Create a `options.yml` file in the destination path:

*e.g.*

```yaml
video_id: "PLAYLIST_ID"
format: "bestvideo+bestaudio/best/best"
```

_`video_id` is mandatory and additional options from [yt-dlp](https://github.com/yt-dlp/yt-dlp#usage-and-options) are optional._

*e.g.*

```yaml
video_id: "PLAYLIST_ID"
format: "best"
output: "%(playlist_index) - %(channel) - %(title)s.%(ext)s"
restrict-filenames: True
sponsorblock-remove: "all"
write-subs: True
write-auto-subs: True
sub-langs: ["en*"]
write-thumbnail: True
```

### Run

```sh
# run with implict path
cd <path> && yt-assistant

# or with explicit path
yt-assistant -d <path>
```

## Features & Roadmap

- [x] Fetch playlist
- [ ] Fetch channel
- [x] Skip already downloaded
- [x] Load local config file
- [ ] Load global config file
- [ ] Automate with systemd service and timer
