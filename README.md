# 🌿 MindGreen — Mental Wellness & Eco Habit Tracker

> **Team Name:** GreenMind Labs  
> **Developer:** Dhanush  
> **Course:** Web Application Development  
> **Deployment:** [Live on GitHub Pages](https://your-username.github.io/mindgreen)

---

## 📖 About the Project

**MindGreen** is a full-featured web application that bridges two of the most pressing challenges of our time: **mental health** and **climate change**. The app allows users to log their daily mental wellness (mood, sleep, stress, energy) alongside their eco-friendly habits (cycling, plant-based eating, plastic-free days), and visualises the correlation between the two on an interactive dashboard.

**The core insight:** research shows that sustainable living actively improves mental wellbeing. MindGreen makes this visible.

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔐 User Registration | Full sign-up form with validation, password strength meter, wellness goal selection |
| 🧠 Daily Wellness Check-in | Mood picker, sleep/stress/energy sliders, journal entry, gratitude field |
| 🌍 Eco Habit Logger | Select from 8 eco habits, real-time CO₂ counter, weekly targets |
| 📊 Dashboard | Live charts (Chart.js), streak tracker, mood/eco correlation visualisation |
| 📚 Resources & Tips | Filterable articles on mental wellness, eco living, and the science connecting them |
| 🔒 Login / Auth | Email + password login with localStorage session management |
| 🏅 Streak System | Daily streak counter updated on each check-in |
| 📱 Responsive Design | Mobile-friendly layout across all pages |

---

## 📋 Forms with Validation (3 Required)

### Form 1 — User Registration (`register.html`)
- **Fields:** First name, last name, email, age range, password, confirm password, wellness goal, referral, terms checkbox
- **Validation:**
  - Required field checks on all mandatory fields
  - Email regex validation (`/^[^\s@]+@[^\s@]+\.[^\s@]+$/`)
  - Password regex: min 8 chars, one uppercase, one number
  - Password confirmation match
  - Terms of Service checkbox required
  - Real-time password strength meter (4 bars: Weak / Fair / Good / Strong)

### Form 2 — Daily Wellness Check-in (`checkin.html`)
- **Fields:** Mood picker (emoji), mood slider (1–10), sleep hours, stress level, energy level, journal entry, activity type, social level, gratitude entry
- **Validation:**
  - Gratitude field required (cannot submit empty)
  - Sliders enforce numeric range (built into range input)
  - Duplicate check — shows "already checked in" banner if submitted twice in one day

### Form 3 — Eco Habit Logger (`eco.html`)
- **Fields:** Habit checkboxes (8 options), transport mode, diet type, notes, weekly habits target, weekly CO₂ target
- **Validation:**
  - At least one habit must be selected (custom checkbox validation)
  - Transport mode required (dropdown validation)
  - Weekly habits: numeric, 1–56
  - Weekly CO₂ target: numeric, 100–50,000
  - All errors shown inline with red field highlighting

---

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, CSS3, Vanilla JavaScript (ES6+) |
| Charts | Chart.js 4.4 (via CDN) |
| Fonts | Google Fonts — DM Serif Display + DM Sans |
| Data Storage | Browser `localStorage` (no backend required) |
| Deployment | GitHub Pages |

---

## 📁 Project Structure

```
mindgreen/
├── index.html          # Landing page + login modal (Form: Login)
├── register.html       # User registration (Form 1 — full validation)
├── dashboard.html      # Main dashboard with Chart.js visualisations
├── checkin.html        # Daily wellness check-in (Form 2)
├── eco.html            # Eco habit logger (Form 3)
├── resources.html      # Articles and tips page
└── README.md           # This file
```

---

## 🚀 Setup & Running the Application

### Option 1 — Run locally (zero dependencies)

```bash
# Clone the repository
git clone https://github.com/your-username/mindgreen.git

# Navigate to the project folder
cd mindgreen

# Open in browser (any of the following)
open index.html                          # macOS
start index.html                         # Windows
xdg-open index.html                      # Linux

# Or serve with Python (recommended to avoid CORS issues)
python3 -m http.server 8000
# Then open: http://localhost:8000
```

### Option 2 — GitHub Pages (live deployment)

1. Push this repository to GitHub
2. Go to **Settings → Pages**
3. Set source to `main` branch, root `/`
4. Your app will be live at `https://your-username.github.io/mindgreen`

---

## 📦 Dependencies

All dependencies are loaded via CDN — **no npm install required**.

| Library | Version | CDN |
|---------|---------|-----|
| Chart.js | 4.4.0 | `cdn.jsdelivr.net` |
| Google Fonts | DM Serif Display + DM Sans | `fonts.googleapis.com` |

---

## 🧪 How to Use the App

1. **Visit `index.html`** — landing page with feature overview
2. **Click "Get started free"** → goes to `register.html`
3. **Fill in the registration form** (Form 1) with all required fields
4. **You'll be redirected to `dashboard.html`** after successful registration
5. **Click "+ Check-in"** → `checkin.html` to log your daily wellness (Form 2)
6. **Click "+ Log Eco Habit"** → `eco.html` to log today's eco actions (Form 3)
7. **Return to dashboard** to see updated charts, streak, and scores
8. **Browse Resources** for wellness and eco tips

> **Note:** All data is stored in your browser's `localStorage`. Clearing browser data will reset the app. No data is sent to any server.

---

## 👥 Role Distribution

| Role | Responsibilities |
|------|----------------|
| Frontend Developer | HTML/CSS layout, responsive design, component structure |
| UI/UX Designer | Color system, typography, interaction design, form UX |
| JavaScript Developer | Form validation logic, localStorage data layer, Chart.js integration |
| Project Manager | Feature scoping, GitHub commits, documentation |

---

## 🌿 Design Decisions

- **Color palette:** Deep forest green (`#1a7a4a`) with cream (`#f9f6f0`) backgrounds — calm, natural, health-forward
- **Typography:** DM Serif Display (headings) + DM Sans (body) — editorial but approachable
- **No backend:** localStorage chosen for simplicity and GitHub Pages compatibility
- **Chart.js:** Line chart for mood/eco trend correlation; radar chart for wellness breakdown
- **Mobile-first:** Sidebar hidden on mobile; form layouts collapse to single column

---

## 📜 License

This project was created for academic purposes. All content is original.

---

*Built with 🌿 by GreenMind Labs*
