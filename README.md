# mpv-clip

Extract clips from videos in mpv using ffmpeg.

## Installation

```bash
git clone https://github.com/gustavomoura628/mpv-clip ~/.config/mpv/scripts/mpv-clip
```

## Usage

1. **Set start point**: Press `c` to mark where the clip begins
2. **Set end point**: Press `C` (Shift+c) to mark where the clip ends
3. **Encode**: Press `Ctrl+e` to start encoding

The clip will be saved in the directory where mpv was launched.

## Default Settings

| Setting | Default | Description |
|---------|---------|-------------|
| `key_set_start_frame` | `c` | Key to set clip start |
| `key_set_stop_frame` | `C` | Key to set clip end |
| `key_start_encode` | `Ctrl+e` | Key to start encoding |
| `audio_codec` | `libopus` | Audio codec |
| `audio_bitrate` | `192k` | Audio bitrate |
| `video_codec` | `libx265` | Video codec |
| `video_crf` | `24` | Video quality (lower = better) |
| `video_pixel_format` | `yuv420p10` | Pixel format |
| `output_directory` | `.` | Output directory (current dir) |
| `encoding_preset` | `medium` | ffmpeg encoding preset |

## Configuration

Create `~/.config/mpv/script-opts/clip.conf` to override defaults:

```
key_start_encode=Ctrl+c
output_directory=/tmp
video_crf=20
```

## Requirements

- mpv
- ffmpeg

## License

GPL-3.0
