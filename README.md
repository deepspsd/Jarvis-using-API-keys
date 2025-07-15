# Jarvis-using-API-keys

🎙️ LiveKit AI Assistant:

This project is an AI-powered voice assistant built using LiveKit, with real-time speech processing, noise cancellation, and large language model integration.

🚀 Features
✅ Real-time LLM inference with Google’s Realtime Model
✅ Text-to-speech using Cartesia Sonic-2
✅ Voice Activity Detection with Silero
✅ Enhanced noise cancellation with LiveKit BVC
✅ Customizable agent instructions
✅ Runs in LiveKit Cloud rooms

📂 Project Structure
.
├── main.py            # Entry point (the code you see here)
├── prompts.py         # Contains AGENT_INSTRUCTION & SESSION_INSTRUCTION
├── .env               # Environment variables (API keys, configs)
└── README.md          # This file

⚙️ Requirements
Python 3.8+
LiveKit Python SDK
python-dotenv

Install dependencies:
pip install -r requirements.txt

🔑 Setup
Clone the repository:
git clone https://github.com/yourusername/livekit-ai-assistant.git
cd livekit-ai-assistant
Create a .env file: env

LIVEKIT_API_KEY=your_livekit_api_key
LIVEKIT_API_SECRET=your_livekit_api_secret
Add any other required keys for Google Realtime Model, Cartesia TTS, etc.

Prepare your prompts:
Edit prompts.py to customize AGENT_INSTRUCTION and SESSION_INSTRUCTION for your assistant’s behavior.

🧩 How it Works
The Assistant class inherits from Agent and defines how your assistant should behave.
entrypoint() sets up a session with LLM, TTS, VAD, and enhanced noise cancellation.
The assistant joins a LiveKit Cloud room, listens for voice input, processes it with the LLM, and responds in real-time.

▶️ Run
Run locally: python main.py

📞 Notes
Noise Cancellation: The BVC() plugin is used for telephony-grade noise cancellation. If you self-host LiveKit, you may skip or customize this.
Voice Model: Change voice="Charon" and tts=model="sonic-2" to your preferred models.
Room Input Options: video_enabled=True allows video streams in addition to audio.

✨ Acknowledgements
LiveKit
Cartesia
Silero VAD

🙌 Contributing
Feel free to open issues and submit pull requests to improve this assistant.

Since this only runs on LiveKit Playground the UI is seen like this
<img width="1918" height="912" alt="image" src="https://github.com/user-attachments/assets/000421d0-b7d3-445e-8006-c0110e2b6ef3" />
