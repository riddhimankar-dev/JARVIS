# JARVIS

JARVIS is a small voice assistant built in Python. It listens for the wake word "jarvis", then responds to simple commands like opening websites, playing songs from a built-in library, reading news, or sending the prompt to OpenAI for a short reply.

## Features

- Wake-word based voice activation
- Open common websites like Google, YouTube, GitHub, LinkedIn, and Facebook
- Play mapped songs from `musicLibrary.py`
- Read top headlines from NewsAPI
- Fall back to OpenAI for general responses

## Files

- `main.py`: main voice assistant loop and command handling
- `client.py`: simple OpenAI example script
- `musicLibrary.py`: song name to URL mapping

## Setup

1. Create and activate a virtual environment.
2. Install the dependencies used by the project:

```bash
pip install speechrecognition pyttsx3 requests openai gTTS pygame pyaudio pocketsphinx
```

3. Set your API keys as environment variables:

```bash
set OPENAI_API_KEY=your_openai_key
set NEWS_API_KEY=your_newsapi_key
```

4. Update `main.py` to read `NEWS_API_KEY` if you want news to work without editing the source.

## Run

```bash
python main.py
```

Say `jarvis` to wake the assistant, then speak a command.

## Notes

- The assistant uses Google speech recognition, so an internet connection is required for voice input.
- `main.py` currently hardcodes a placeholder NewsAPI value, so news requests will only work after that is replaced with a real key.
