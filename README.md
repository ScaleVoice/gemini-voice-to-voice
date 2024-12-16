# Gemini Voice-to-Voice Chat

A Python implementation of real-time voice conversation with Google's Gemini AI model. This project enables natural, bidirectional voice communication with Gemini, supporting multi-turn conversations. This is an improved version of [philschmid's Gemini Voice implementation](https://gist.github.com/philschmid/cb8c98f0781e4e52e5d364ff39e2ccd2) with fixes for turn handling and other improvements.

## Features

- 🎤 Real-time voice input capture
- 🔊 Real-time voice response playback
- 💬 Multi-turn conversation support
- ⚡ Low-latency audio streaming
- 🎯 WebSocket-based communication with Gemini API

## Prerequisites

- Python 3.11 or higher
- A Google Gemini API key
- PortAudio (required for PyAudio)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/gemini-voice-to-voice.git
cd gemini-voice-to-voice
```

2. Install the required packages:
```bash
pip install -r requirements.txt
```

3. Create a `.env` file in the project root and add your Gemini API key:
```env
GEMINI_API_KEY=your_api_key_here
```

## Usage

1. Run the script:
```bash
python main.py
```

2. Wait for the "Connected to Gemini, You can start talking now" message

3. Start speaking - Gemini will respond with voice in real-time

4. The conversation will continue naturally, with support for:
   - Multi-turn dialogue
   - Natural pauses

## How It Works

The application uses three main components running concurrently:

1. **Audio Capture**: Continuously captures audio from your microphone and streams it to Gemini
2. **Response Processing**: Handles Gemini's responses and manages conversation turns
3. **Audio Playback**: Plays back Gemini's voice responses in real-time

The WebSocket connection ensures low-latency communication for natural conversation flow.

## Technical Details

- Audio Format: 16-bit PCM
- Sample Rate: 16kHz (input), 24kHz (output)
- Chunk Size: 512 samples
- API: Gemini 2.0 Flash Experimental
- Protocol: WebSocket streaming

## License

MIT License - feel free to use and modify as needed.

## Contributing

Contributions are welcome! Feel free to submit issues and pull requests.
