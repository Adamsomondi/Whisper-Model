# Video Transcription & Keyword Analysis

A Python tool for transcribing and analyzing video/audio files using OpenAI's Whisper model in Google Colab.

## Features

- Transcribe video and audio files to text
- Search for keywords with timestamps
- Extract phrases and topics
- Save results to Google Drive
- Support for multiple languages

## Installation

```python
!pip install openai-whisper torch torchaudio
!pip install moviepy
```

## Usage

```python
# Mount Google Drive
from google.colab import drive
drive.mount('/content/drive')

# Set video path
video_path = "/content/drive/MyDrive/your-video.mp4"

# Define keywords
keywords = ["investment", "property", "finance"]

# Process video
results = process_local_video(video_path, keywords, model_size="base")
```

## Supported Formats

**Video:** MP4, AVI, MKV, MOV, WMV, FLV, WebM, M4V

**Audio:** MP3, WAV, M4A, FLAC, AAC

## Model Options

- `tiny` - Fastest, least accurate
- `base` - Good balance (recommended)
- `small` - Better accuracy
- `medium` - High accuracy
- `large` - Best accuracy

## Output

Three files are saved to Google Drive:
- `{filename}_transcript.txt` - Full transcript
- `{filename}_keywords.json` - Keyword matches with timestamps
- `{filename}_summary.json` - Analysis summary

## License

Uses OpenAI's Whisper model.
