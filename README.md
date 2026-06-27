# CookMate AI

> AI-powered personal cooking planner built for **PromptWars Warm-Up Challenge** (Google + Hack2Skill)

Generate personalized meal plans with AI, complete with grocery lists, cooking steps, timers, budget analysis, and smart ingredient substitutions.

**[Live Demo](https://108tsrenukesh.github.io/CookMateAI/)**

---

## Features

- **AI Meal Generation** - Gemini (Google) primary, Groq (Llama 3.3) fallback
- **Installable PWA** - Add to home screen, works offline
- **Age-Based Personalization** - Nutrition targets auto-adjusted per age group
- **Smart Grocery List** - Auto-scaled quantities for your group size
- **Ingredient Substitutions** - Vegan, gluten-free, dairy-free swaps
- **Budget Analysis** - Real-time cost tracking with visual budget bar
- **Cooking Timers** - Per-meal timers with start/pause/reset
- **Step-by-Step Instructions** - Interactive checklist for cooking flow
- **Share & Print** - Copy to clipboard or print your meal plan

---

## Quick Start

### Option 1: Just open the file

1. Open `index.html` in any browser
2. Enter your name & age
3. Click "Start Planning Meals"

### Option 2: Deploy to GitHub Pages (recommended)

1. Create a new repo: `CookMateAI`
2. Push this folder to it
3. Go to **Settings > Secrets and variables > Actions**
4. Add two repository secrets:
   - `GEMINI_API_KEY` = your Gemini key
   - `GROQ_API_KEY` = your Groq key
5. Go to **Settings > Pages > Deploy from branch > main**
6. GitHub Actions auto-injects your keys at deploy time

**Live at:** `https://108tsrenukesh.github.io/CookMateAI/`

---

## Install as App (PWA)

### Android (Chrome)
Tap the **Install** button in the app header, or Chrome menu > "Install app."

### iPhone (Safari)
Tap **Share** > **Add to Home Screen** > Add.

### Desktop (Chrome/Edge)
Click the install icon in the address bar.

---

## How It Works

1. **Enter name & age** on the onboarding screen
2. **Set preferences** - dietary needs, cuisine, budget, people count
3. **Click "AI Generate"** - app calls Gemini/Groq for a personalized plan
4. **Get your plan** - meals, grocery list, steps, timers, budget analysis

### AI Fallback Chain

```
Gemini API (primary) → Groq API (fallback) → Smart Algorithm (offline)
```

---

## API Keys

API keys are stored in `.env` (not committed to git). GitHub Actions injects them into `index.html` during deployment via the workflow in `.github/workflows/deploy.yml`.

**Get your free keys:**
- **Gemini**: https://aistudio.google.com/apikey
- **Groq**: https://console.groq.com/keys

---

## Tech Stack

- **Frontend**: Vanilla HTML/CSS/JS (single file, zero dependencies)
- **PWA**: Service Worker + manifest.json
- **AI**: Google Gemini API + Groq API
- **CI/CD**: GitHub Actions
- **Hosting**: GitHub Pages

---

## License

MIT - Built for PromptWars Warm-Up Challenge
