Yash — Python Voice Assistant

A desktop voice assistant built in Python that listens to spoken commands, converts them to text, and responds with synthesized speech. It can look things up, open apps and websites, play music, tell the time, crack jokes, and send emails — all hands-free.

Features
Speech in, speech out — captures microphone audio, converts it to text with Google Speech Recognition, and replies using text-to-speech.
Wikipedia search — speaks a short summary of any topic.
Web browsing — opens YouTube, Google, and other sites on command.
App launching — opens local apps like Notepad, Spotify, and VS Code.
Music playback — plays songs from a local folder or streams from YouTube via pywhatkit.
Time queries — tells the current time.
Jokes — delivers a random joke with pyjokes.
Email — sends emails through Gmail's SMTP.
Time-based greeting — greets you with "Good morning/afternoon/evening" on startup.
Tech stack
Purpose	Library
Speech-to-text	speech_recognition
Text-to-speech	pyttsx3
Microphone access	PyAudio
Wikipedia lookups	wikipedia
YouTube / web playback	pywhatkit
Jokes	pyjokes
Web browsing	webbrowser
App / system control	subprocess, os
Email	smtplib
Time	datetime
Requirements
Python 3.8+
A working microphone and speakers
Internet connection (for speech recognition, Wikipedia, and YouTube)
Installation
bash
pip install SpeechRecognition pyttsx3 pyaudio wikipedia pywhatkit pyjokes

If pyaudio fails to install:

Windows: pip install pipwin then pipwin install pyaudio
macOS: brew install portaudio then pip install pyaudio
Linux: sudo apt-get install python3-pyaudio
Setup

Email sending uses Gmail SMTP. Before using that feature:

Open VoiceAssistant_project.ipynb and find the sendEmail() function.
Replace the placeholder email and password with your own.
Use a Gmail App Password, not your real account password (Google requires this for SMTP).

Security note: Never commit your real email address or password to GitHub. Keep credentials out of the notebook — load them from environment variables or a separate ignored file instead.

Usage
Open the notebook:
bash
   jupyter notebook VoiceAssistant_project.ipynb
Run all cells.
When it greets you, speak a command into your microphone. Examples:
"Wikipedia Albert Einstein"
"Open YouTube"
"Play <song name>"
"What's the time"
"Tell me a joke"
Key functions
wishMe() — time-based greeting on startup
takeCommand() — records the microphone and returns recognized text
speak(text) — converts text to speech
sendEmail(to, content) — sends an email via Gmail SMTP
Main loop — matches keywords in the spoken command and triggers the right action
Notes
Speech recognition accuracy depends on your microphone and background noise.
Some commands (opening Notepad, Spotify, VS Code) use Windows-style paths and may need adjusting on macOS/Linux.
Author

Yash (@YashasviSah)
