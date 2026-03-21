# Ultravox Web Quickstart

A simple web interface for voice conversations using the Ultravox API. This is a quickstart project for creating a web-based Voice AI Agent on Ultravox with all the key parts in a single file.

## Features

- 🎤 Voice-based chat with AI assistant
- 🐱 Example tool integration (cat facts)
- 🎨 Clean Tailwind CSS UI
- ⚡ Real-time transcripts

## Tech Stack

- **FastHTML**: Lightweight Python web framework
- **Ultravox Client**: Voice AI library
- **Tailwind CSS**: Modern styling
- **Python 3.x**

## Local Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/Eswari2225/ultravox-web-quickstart.git
   cd ultravox-web-quickstart
   ```

2. Create a virtual environment:
   ```bash
   python -m venv .venv
   .venv\Scripts\Activate.ps1  # Windows PowerShell
   # or
   source .venv/bin/activate  # macOS/Linux
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up your API key:
   ```bash
   cp .env.example .env
   # Edit .env and add your ULTRAVOX_API_KEY from https://app.ultravox.ai
   ```

5. Run the app:
   ```bash
   python main.py
   ```
   Open your browser to `http://127.0.0.1:8000/`

## Deployment

### Render (Recommended - Free)

1. Ensure your code is pushed to GitHub (done).
2. Go to [render.com](https://render.com) and sign in with GitHub.
3. Click **New +** → **Web Service**.
4. Select your `ultravox-web-quickstart` repo.
5. Render will auto-detect from `render.yaml`.
6. Add environment variable:
   - Key: `ULTRAVOX_API_KEY`
   - Value: your Ultravox API key from https://app.ultravox.ai
7. Click **Create Web Service**.

Your app will be live in 2–3 minutes!

### Other Platforms

Railway, Fly.io, and Heroku also support this setup via `Procfile` and `requirements.txt`:

1. Connect your GitHub repo
2. Add `ULTRAVOX_API_KEY` as an environment variable
3. Deploy

## API Endpoints

- `GET /` – Home page with call UI
- `POST /start` – Initiate a voice call with AI assistant
- `GET /end` – End the current call

## Environment Variables

- `ULTRAVOX_API_KEY` (required) – Your Ultravox API key

## Looking for React?

For a more advanced example using React, see: [https://github.com/fixie-ai/ultravox-demo-template-vercel](https://github.com/fixie-ai/ultravox-demo-template-vercel)
