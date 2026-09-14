# Suno — Real-Time Conversational Voice AI Assistant

> **Suno** is a real-time conversational AI assistant designed for natural voice interaction, intelligent chat, emotional awareness, and optional local system control.

Suno combines **real-time voice conversation**, **AI-powered chat**, **streaming responses**, **emotion and sentiment analysis**, and **local AI capabilities** into a single modern interface.

---

## Overview

Suno is built to provide a more natural way to interact with an AI assistant.

Instead of relying only on traditional text-based conversations, Suno supports hands-free voice interaction with real-time speech recognition, audio visualization, streaming AI responses, and text-to-speech.

The project can operate using cloud-based AI models and can optionally use a local AI model through Ollama.

### Core Capabilities

* Real-time conversational voice interaction
* Hands-free voice mode
* Speech-to-text recognition
* Text-to-speech responses
* Streaming AI responses
* Interactive 3D neural orb interface
* Live microphone level monitoring
* Microphone selection
* Barge-in / voice interruption support
* Multiple AI engine support
* Local Ollama AI fallback
* Emotion and sentiment analysis
* Emotional wellness assistance
* Optional Windows system controls
* Modern web interface
* Optional native Windows desktop interface

---

# Features

## 1. Real-Time Voice Mode

Suno includes a hands-free conversational voice mode designed for continuous interaction.

### Voice features

* Browser-based speech recognition
* Real-time microphone input
* Live audio level visualization
* Microphone selection
* Streaming AI responses
* Text-to-speech playback
* Barge-in interruption
* Continuous conversational flow
* Interactive visual feedback

The interface includes a dynamic **3D neural orb** that reacts to the assistant's state during conversation.

---

## 2. AI Intelligence Engines

Suno supports multiple intelligence backends.

### Google Gemini

Cloud-based AI inference can be used for fast conversational responses and streaming output.

Supported Gemini configurations depend on the API/model configuration provided in the project.

### OpenAI

Suno can also be configured to use an OpenAI model through the application's settings/environment configuration.

### Ollama — Local AI

Suno can optionally use **Ollama** for local inference.

Example model:

```text
qwen3:4b-instruct
```

Local inference provides an option for:

* Offline operation
* Local processing
* Reduced cloud dependency
* Privacy-focused conversations
* No per-request cloud API cost

> Local model availability and performance depend on the user's hardware and installed Ollama model.

---

# 3. Emotional Awareness

Suno includes an emotion and sentiment analysis layer designed to identify conversational emotional signals.

Possible detected states include:

* Anxiety
* Stress
* Sadness
* Anger
* Joy
* Calm

Based on the detected conversational state, Suno can adapt its responses and provide appropriate supportive techniques.

Examples include:

* Grounding techniques
* Breathing exercises
* Calm conversational responses
* Stress-management suggestions

> **Important:** Suno is an AI assistant and is not a replacement for a licensed mental-health professional, emergency service, diagnosis, or medical treatment.

---

# 4. Interactive Neural Orb

The web interface includes a dynamic 3D-style neural orb visualization.

The orb provides visual feedback during interaction, including states such as:

```text
Idle
Listening
Processing
Speaking
Interrupted
```

The visualization is designed to make voice interaction feel more natural and responsive.

---

# 5. Microphone System

Suno provides microphone controls directly inside the voice interface.

Features include:

* Available microphone detection
* Microphone selection
* Default microphone support
* Live input level monitoring
* Voice activity detection
* Continuous voice interaction

The exact microphone capabilities depend on the browser and operating system.

---

# 6. Streaming Responses

Suno is designed around low-latency conversational interaction.

Instead of waiting for an entire response before displaying it, supported AI backends can stream generated output progressively.

Conceptually:

```text
User speaks
     ↓
Speech recognition
     ↓
Suno receives text
     ↓
AI inference
     ↓
Streaming response
     ↓
Text-to-speech
     ↓
User hears response
```

This reduces the perceived response latency during conversations.

---

# 7. System Action Tools

The optional local assistant layer can interact with the Windows system.

Depending on configuration, Suno can perform tasks such as:

* Opening applications
* Checking CPU usage
* Checking RAM usage
* Inspecting running processes
* Executing supported PC actions

System-level functionality should only be enabled when you trust the code and understand the commands being executed.

---

# 8. Web Application

Suno provides a browser-based interface.

Default development address:

```text
http://localhost:3000
```

The interface is designed around:

* Conversational chat
* Voice interaction
* AI status feedback
* Settings
* Microphone controls
* Streaming responses
* Neural visualization

---

# 9. Windows Desktop Interface

The project also contains an optional native Windows interface built with Python/Tkinter.

Main file:

```text
app_gui.py
```

The desktop interface can work alongside the local assistant components.

---

# Technology Stack

## Frontend

* HTML5
* CSS3
* JavaScript
* Canvas-based visualization
* Web Speech APIs

## Backend

* Node.js
* Express.js
* WebSocket / streaming communication
* Server-side AI integration

## AI

* Google Gemini
* OpenAI-compatible integration
* Ollama
* Qwen local models

## Voice

* Speech recognition
* Text-to-speech
* Voice activity detection
* Microphone monitoring

## Desktop

* Python
* Tkinter

---

# Project Structure

```text
Suno/
│
├── server.js
│
├── public/
│   ├── index.html
│   ├── style.css
│   ├── app.js
│   └── voice-live.js
│
├── app_gui.py
├── assistant.py
├── tool_dispatcher.py
├── voice_engine.py
│
├── package.json
├── requirements.txt
├── .env.example
├── start.bat
└── README.md
```

### Important Files

| File                 | Purpose                                 |
| -------------------- | --------------------------------------- |
| `server.js`          | Node.js backend and AI/streaming server |
| `index.html`         | Main Suno web interface                 |
| `style.css`          | UI styling and animations               |
| `app.js`             | Chat and application controller         |
| `voice-live.js`      | Real-time voice interaction             |
| `assistant.py`       | Local assistant logic                   |
| `tool_dispatcher.py` | System action handling                  |
| `voice_engine.py`    | Local voice processing                  |
| `app_gui.py`         | Optional Windows desktop interface      |
| `package.json`       | Node.js dependencies and scripts        |
| `requirements.txt`   | Python dependencies                     |
| `.env.example`       | Environment configuration template      |
| `start.bat`          | Windows quick-start script              |

---

# Requirements

## Required

* Node.js 18 or newer
* Modern web browser
* Working microphone for voice features

## Optional

* Python 3.10+
* Ollama
* Compatible local AI model
* Windows system tools

---

# Installation

## 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Suno.git
cd Suno
```

Replace `YOUR_USERNAME/Suno` with your actual GitHub repository.

---

## 2. Install Node.js Dependencies

```bash
npm install
```

---

## 3. Install Python Dependencies

If you want to use the Python desktop/local assistant components:

```bash
pip install -r requirements.txt
```

---

# Environment Configuration

Create your environment file from the example:

### Windows PowerShell

```powershell
Copy-Item .env.example .env
```

### Windows CMD

```cmd
copy .env.example .env
```

### macOS / Linux

```bash
cp .env.example .env
```

Then open `.env` and configure the required settings.

Example:

```env
PORT=3000
GEMINI_API_KEY=your_gemini_api_key_here
```

Depending on your implementation, additional API keys or configuration variables may be required.

> **Never commit your `.env` file or API keys to GitHub.**

Add `.env` to `.gitignore`:

```gitignore
.env
node_modules/
__pycache__/
*.pyc
```

---

# Running Suno

## Option 1 — Windows Quick Start

Run:

```text
start.bat
```

The script starts the application and opens the web interface.

---

## Option 2 — Terminal

Run:

```bash
npm start
```

Then open:

```text
http://localhost:3000
```

---

# Using Ollama

If you want to use a local AI backend, install Ollama and download the model configured by your project.

Example:

```bash
ollama pull qwen3:4b-instruct
```

Then start Ollama according to your operating system.

Verify that the model is available:

```bash
ollama list
```

The exact model name must match the model configured in Suno.

---

# Voice Mode

To use Suno's real-time voice functionality:

1. Open Suno in a supported browser.
2. Allow microphone permission.
3. Select your microphone.
4. Activate Live Voice Mode.
5. Speak naturally.
6. Suno processes the speech and generates a response.
7. The response is converted to speech and played back.

For the best experience, use a modern Chromium-based browser with microphone access enabled.

---

# API Keys & Security

Suno may use third-party AI APIs.

API keys should be stored securely.

### Never do this:

```javascript
const API_KEY = "your-secret-api-key";
```

Do not publish secret API keys inside:

* `server.js`
* `app.js`
* HTML files
* GitHub repositories
* Screenshots
* Public frontend code

Use environment variables instead.

---

# Architecture

A simplified Suno architecture looks like this:

```text
                  ┌────────────────────┐
                  │       User         │
                  └─────────┬──────────┘
                            │
                       Voice / Text
                            │
                            ▼
                  ┌────────────────────┐
                  │   Suno Web Client  │
                  │ HTML/CSS/JavaScript│
                  └─────────┬──────────┘
                            │
                            ▼
                  ┌────────────────────┐
                  │    Node.js Server  │
                  │      Express       │
                  └─────────┬──────────┘
                            │
             ┌──────────────┼──────────────┐
             │              │              │
             ▼              ▼              ▼
        Gemini API      OpenAI API      Ollama
             │              │              │
             └──────────────┼──────────────┘
                            │
                            ▼
                  ┌────────────────────┐
                  │   Suno Response    │
                  └─────────┬──────────┘
                            │
                            ▼
                  ┌────────────────────┐
                  │    Voice Engine    │
                  │       TTS/STT       │
                  └─────────┬──────────┘
                            │
                            ▼
                         Speaker
```

---

# Privacy

Suno can be configured to use different AI backends.

When using cloud AI services, conversation data may be transmitted to the corresponding service according to that provider's API terms and privacy policies.

When using a local Ollama model, inference can be performed locally on the user's machine.

Users should review the configuration and third-party provider policies before using Suno with sensitive information.

---

# Performance

Suno's performance depends on:

* Internet connection
* Selected AI provider
* AI model
* CPU
* GPU
* Available RAM
* Microphone hardware
* Browser
* Text-to-speech engine
* Local Ollama model performance

Cloud models generally provide stronger performance without requiring local AI hardware, while local models provide greater control and can operate without sending prompts to a cloud AI provider.

---

# Troubleshooting

## Suno does not respond to my voice

Check:

```text
1. Microphone permission
2. Correct microphone selected
3. Browser microphone access
4. Browser console for errors
5. Node.js server status
6. API configuration
```

---

## Server does not start

Try:

```bash
npm install
npm start
```

Check whether port `3000` is already being used.

---

## Ollama does not work

Check:

```bash
ollama list
```

Then verify that the configured model exists.

---

## Python components do not start

Check your Python version:

```bash
python --version
```

Then reinstall dependencies:

```bash
pip install -r requirements.txt
```

---

# Development

Create a new branch:

```bash
git checkout -b feature/your-feature
```

Make your changes, then:

```bash
git add .
git commit -m "Add your feature"
git push origin feature/your-feature
```

Then open a Pull Request on GitHub.

---

# Roadmap

Potential future improvements include:

* Improved wake-word detection
* More advanced voice activity detection
* Lower voice latency
* More AI model providers
* Better local model support
* Persistent conversation memory
* Custom voice personalities
* Multilingual voice interaction
* Advanced emotion recognition
* Mobile support
* Improved desktop integration
* Better system automation controls
* User authentication
* Production deployment improvements

---

# Disclaimer

Suno is an experimental/general-purpose AI assistant project.

Its emotional wellness features are intended for supportive conversational purposes only and should not be considered professional medical or psychological care.

System-action features can interact with the user's computer. Users should review and understand the implementation before enabling or exposing those features.

---

# Contributing

Contributions are welcome.

If you would like to improve Suno:

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test your changes.
5. Commit your work.
6. Push the branch.
7. Open a Pull Request.

Please keep contributions focused, documented, and tested.

---

# License

Add your preferred open-source license here.

For example:

```text
MIT License
```

If the repository does not currently have a license, choose one before presenting the project as open source.

---

# Suno

**A conversational AI assistant built for natural interaction.**

```text
Voice.
Conversation.
Intelligence.
Suno.
```
