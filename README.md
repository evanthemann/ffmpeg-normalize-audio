# ffmpeg-normalize-audio

A shell script that extracts audio from a video file, lets you adjust the audio externally, and then replaces the original audio track with your adjusted version.

## What It Does

1. Extracts the audio from a video file as a WAV file.
2. Pauses so you can edit the audio in an external editor (e.g., Audacity).
3. Accepts your adjusted audio file (AIFF format) and merges it back into the video, producing a new MP4 with the updated audio track.

## Usage

```
bash normalize_audio.sh
```

The script will interactively prompt you for:

- The path to your source video file.
- The path to your adjusted audio file (AIFF format) after you have made your edits.

Output files are saved in the same directory as the source video:

- `<filename>_audioonly.wav` -- the extracted audio.
- `<filename>_enhanceaudio.mp4` -- the final video with replaced audio.

## Requirements

- ffmpeg
- Bash
