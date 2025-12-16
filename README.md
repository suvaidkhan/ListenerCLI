# ListenerCLI

A CLI-based speech-to-text tool that records audio from your microphone, transcribes it using Whisper AI, and copies the result to your clipboard.

## Features

- Record audio directly from your microphone
- Transcribe audio using faster-whisper models
- Automatic clipboard integration
- Support for multiple Whisper models (tiny, base, small, medium, large, turbo)
- Language detection and forcing
- Re-transcribe last recording without re-recording

## Installation

Install using uv:

```bash
uv pip install listenercli
```

Or using pip:

```bash
pip install listenercli
```

## Usage

### Basic recording and transcription

```bash
listenercli
```

Press Enter to start recording, speak, then press Enter again to stop. The transcription will be automatically copied to your clipboard and printed to stdout.

### List available models

```bash
listenercli --list-models
```

### Force a specific language

```bash
listenercli --language en
```

### Re-transcribe last recording

```bash
listenercli --last
```

### Custom audio settings

```bash
listenercli --sample-rate 16000 --channels 1
```

## Environment Variables

- `LISTENER_CLI_LANGUAGE`: Set default language for transcription (e.g., `en`, `es`, `fr`)

## Requirements

- Python >= 3.13
- Microphone access

## License

MIT
