# The Smartass Silencer

> *Automated ego deflation for the modern era.*

The **Smartass Silencer** is a React-based PWA designed to analyze pretentious statements, "LinkedIn thought leadership," and confidently incorrect technical assertions. It uses Google's Gemini AI to generate surgically precise, devastating comebacks in either **British Cynicism** or **German Efficiency** modes.

![Project Preview](public/NewLogo.png)

## Features

- **Dual Personality Engines:**
  - 🇬🇧 **British Mode:** Delivers dry wit, backhanded compliments, and "proper" cynicism.
  - 🇩🇪 **German Mode:** Treats stupidity as an inefficiency that must be corrected.
- **The "Kill Shot" System:** Generates instant, one-line shutdowns tailored to the input.
- **Technical Autopsy:** A detailed breakdown of exactly *why* the target is wrong.
- **Audio & TTS:** features a custom audio engine with distinct voice personas (e.g., "Fenrir") to read the roast back to you.
- **Interactive UI:** Hand-drawn aesthetic using `rough-notation` with haptic feedback and sound effects.
- **Integrated Minigame:** Play a fully functional version of **Pong** while the AI processes your request.
- **PWA Support:** Installable on mobile and desktop for offline-ready verbal violence.

## Tech Stack

- **Core:** React 19, TypeScript, Vite
- **AI:** Google Gemini Flash 2.0 (Text + TTS)
- **Styling:** Tailwind CSS, Lucide React
- **Animation:** Rough Notation, CSS transitions
- **Audio:** Web Audio API (real-time sound generation)
- **Deployment:** GitHub Actions -> GitHub Pages

---

## Quick Start

### Prerequisites
- Node.js (v20+)
- A Google Gemini API Key ([Get one here](https://aistudio.google.com/app/apikey))

### Installation

1. **Clone the repository**
   ```bash
   git clone [https://github.com/yourusername/smartassilencer.git](https://github.com/yourusername/smartassilencer.git)
   cd smartassilencer
Install dependencies

Bash

npm install
Configure Environment Create a .env file in the root directory:

Code snippet

VITE_GEMINI_API_KEY=your_api_key_here
Run Locally

Bash

npm run dev
Deployment
This project includes a pre-configured GitHub Action for automatic deployment to GitHub Pages.

Push your code to a GitHub repository.

Go to Settings > Secrets and variables > Actions.

Create a New repository secret:

Name: GEMINI_API_KEY

Value: (Your actual API key)

Go to Settings > Pages.

Under Build and deployment, select GitHub Actions as the source.

Push a change to the main branch. The site will deploy automatically.

Usage Guide
Input: Type or paste the "cringe" statement into the text area. Alternatively, click the Mic icon to dictate.

Settings: Click the gear icon to adjust:

Brutality Level: From "Mildly Annoyed" (1) to "Nuclear" (5).

Language: Toggle between English and German.

Audio: Adjust volume or toggle auto-play.

Analyze: Hit the big red button.

Pong: While the AI "consults the archives," use your mouse or touch to play Pong.

Receipt: Receive your "Kill Shot" and audio playback.

License
Distributed under the MIT License. See LICENSE for more information.


***

### Option 2: The "No-Cringe" Tutorial Instructions

You asked for better instructions that aren't "fookin cringe." The key here is to be **imperative** and **precise**. Don't make jokes in the instructions; let the code be the joke.

Here is a clean guide you can paste into a `CONTRIBUTING.md` or a `docs/SETUP.md` file, or replace the "Setup" section in the README above.

#### **Local Development Guide**

**1. Environment Setup**
You need an API key from Google to power the AI responses.
* Visit [Google AI Studio](https://aistudio.google.com/).
* Click **Get API key** -> **Create API key**.
* Copy the key string (it starts with `AIza...`).

**2. Project Configuration**
The project uses Vite, which loads environment variables from `.env` files.
* Duplicate the file named `.env.example` and rename the copy to `.env`.
* Paste your API key into the file:
    ```bash
    VITE_GEMINI_API_KEY=AIzaSyD...
    ```
    *Note: The `.gitignore` file is already configured to prevent this file from being uploaded to GitHub, keeping your key safe.*

**3. Running the App**
Execute the following commands in your terminal:

```bash
# Install all required node modules
npm install

# Start the development server
npm run dev
The terminal will provide a localhost link (usually http://localhost:5173). Ctrl+Click to open it.

Deployment Guide (GitHub Pages)
This project uses a CI/CD pipeline. You do not need to manually build or upload files.

Repository Settings:

Navigate to your repository on GitHub.

Click Settings (top bar) → Pages (left sidebar).

Under "Source", change the dropdown from "Deploy from a branch" to GitHub Actions.

Secure your API Key:

Still in Settings, go to Secrets and variables → Actions.

Click New repository secret.

Name: GEMINI_API_KEY

Secret: Paste your Google API Key here.

Click Add secret.

Trigger Deployment:

Any commit pushed to the main branch will now trigger a build.

You can monitor progress in the Actions tab.

Once complete, your live URL will appear in the Settings > Pages section.

Note on Base URL: If you are deploying to a user site (e.g., username.github.io), you may need to update vite.config.ts.

Change base: '/smartassilencer/' to base: '/'.

If deploying to a custom domain, also set base: '/'.