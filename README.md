
# 🎓 EduQuest

### *Level Up Your Learning Journey*

> A full-stack gamified education platform featuring AI-powered coding, multilingual learning, STEM deep-dives, interactive quizzes, and mind games — built for students and teachers.


## 🚀 About

**EduQuest** is a gamified learning platform designed to make education engaging, measurable, and fun. Students earn XP, maintain streaks, unlock certificates, and climb leaderboards — while teachers create and assign quizzes, track student progress, and manage content. An AI-powered chatbot (EduBot) and in-browser compiler make it a complete, self-contained learning environment.

Built as a single-file React application with AI integrations via the **Anthropic Claude API**.

---

## 🌐 Live Demo


---

## ✨ Features

### 🔐 Authentication System
- Email + password login / sign-up
- Separate portals for **Students** and **Teachers**
- Role-based routing and UI

### 👨‍🎓 Student Portal

| Feature | Description |
|---|---|
| 🏠 Home Dashboard | Streak counter, XP bar, quick-access blocks, pending assignments |
| 💻 Coding Lab | 5 languages (Python, JS, C++, Java, SQL), problem set, AI compiler |
| 🌐 Language Learning | 8 world languages with progress tracking |
| 🔬 STEM Hub | Physics, Chemistry, Math, Biology, Engineering with topic breakdowns |
| 🎯 Quizzes & Games | Teacher quizzes + 6 interactive mind games |
| 📊 Full Dashboard | Profile, leaderboard, certificates, badges |
| 🤖 EduBot | AI chatbot powered by Claude for instant academic help |

### 👩‍🏫 Teacher Portal

| Feature | Description |
|---|---|
| 📊 Analytics Dashboard | Student count, average scores, active users |
| ➕ Quiz Creator | Create and publish quizzes with XP rewards and due dates |
| 👨‍🎓 Student Roster | View all students with XP, badges, and streaks |
| 📋 Quiz Management | Track quiz completion rates and pending submissions |

---

## 🛠 Tech Stack

```
Frontend       →  React 18 (Hooks, functional components)
Styling        →  Inline CSS-in-JS (no external dependencies)
AI Layer       →  Anthropic Claude Sonnet 4 API
Compiler Sim   →  Claude API (code execution simulation)
Chatbot        →  Claude API (streaming conversation)
State Mgmt     →  React useState / useEffect / useRef
Icons          →  Unicode Emoji (zero-dependency)
Build Tool     →  Vite / Create React App compatible
```

---

## 📦 Getting Started

### Prerequisites

- Node.js `v18+`
- npm or yarn
- Anthropic API Key → [Get one here](https://console.anthropic.com)

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/eduquest.git
cd eduquest

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.example .env
```

### Environment Variables

Create a `.env` file in the root:

```env
VITE_ANTHROPIC_API_KEY=your_api_key_here
```

> ⚠️ **Note:** For production, proxy API calls through a backend server. Never expose your API key in the browser bundle.

### Run Locally

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Build for Production

```bash
npm run build
npm run preview
```

---

## 📁 Project Structure

```
eduquest/
│
├── src/
│   ├── App.jsx                  # Root component + auth routing
│   │
│   ├── components/
│   │   ├── Auth.jsx             # Login / Sign-up screen
│   │   ├── StudentApp.jsx       # Main student layout + navigation
│   │   ├── TeacherPanel.jsx     # Teacher dashboard + quiz creator
│   │   │
│   │   ├── modules/
│   │   │   ├── CodingLab.jsx    # Problem set + language tabs
│   │   │   ├── LanguageHub.jsx  # 8-language learning module
│   │   │   ├── StemHub.jsx      # STEM subjects + topic drilldown
│   │   │   └── Quizzes.jsx      # Teacher quizzes + mind games
│   │   │
│   │   ├── shared/
│   │   │   ├── Chatbot.jsx      # EduBot AI assistant
│   │   │   ├── Compiler.jsx     # AI-powered code compiler
│   │   │   ├── MemoryGame.jsx   # Memory match mini-game
│   │   │   ├── QuizModal.jsx    # Interactive quiz player
│   │   │   └── Navbar.jsx       # Top nav + hamburger sidebar
│   │   │
│   │   └── dashboard/
│   │       ├── Profile.jsx      # User profile + XP stats
│   │       ├── Leaderboard.jsx  # Global rankings
│   │       └── Certificates.jsx # Earned + locked certificates
│   │
│   ├── data/
│   │   ├── languages.js         # Language database
│   │   ├── stemSubjects.js      # STEM topics database
│   │   ├── codingProblems.js    # Problem set database
│   │   └── mindGames.js         # Games config
│   │
│   └── utils/
│       └── api.js               # Anthropic API helper
│
├── public/
│   └── favicon.ico
│
├── .env.example
├── package.json
├── vite.config.js
└── README.md
```

---

## 📚 Modules

### 💻 Coding Lab
- **5 Language Tabs:** Python · JavaScript · C++ · Java · SQL
- **Problem Set:** Difficulty levels (Easy / Medium / Hard) with XP rewards
- **AI Compiler:** Paste or write code → click Run → get simulated real output powered by Claude
- **Playground Mode:** Free-form editor for any language

### 🌐 Language Learning
Pulls from a curated database of 8 world languages:

| Language | Level | Lessons |
|---|---|---|
| 🇪🇸 Spanish | Beginner | 24 |
| 🇫🇷 French | Beginner | 20 |
| 🇯🇵 Japanese | Intermediate | 30 |
| 🇩🇪 German | Beginner | 18 |
| 🇨🇳 Mandarin | Advanced | 36 |
| 🇸🇦 Arabic | Intermediate | 28 |
| 🇮🇳 Hindi | Beginner | 22 |
| 🇧🇷 Portuguese | Beginner | 20 |

### 🔬 STEM Hub
Engineering-grade subject coverage pulled from structured database:

- **Physics** — Mechanics, Thermodynamics, Electromagnetism, Quantum
- **Chemistry** — Atomic Structure, Bonding, Organic, Electrochemistry
- **Mathematics** — Calculus, Linear Algebra, Statistics, Discrete Math
- **Biology** — Cell Biology, Genetics, Ecology, Human Anatomy
- **Engineering** — Circuits, Mechanics of Materials, Fluid Mechanics, Signal Processing

### 🎯 Quizzes & Mind Games

**Teacher-Assigned Quizzes:** Students see and attempt quizzes created by their teachers with XP rewards and due dates.

**Mind Games:**

| Game | Skill Trained |
|---|---|
| 🧠 Memory Match | Working memory, pattern recall |
| 🔢 Sudoku | Logical deduction |
| 📝 Word Scramble | Vocabulary, spelling |
| 🏁 Math Race | Arithmetic speed |
| 🔷 Pattern IQ | Abstract reasoning |
| 🏆 Trivia Battle | General knowledge |

---

## 🤖 EduBot — AI Chatbot

EduBot is a context-aware academic assistant integrated directly into the platform. It can:

- Explain concepts across all subjects
- Help debug code problems
- Suggest study strategies
- Answer language learning questions
- Guide students through STEM topics

Powered by **Claude Sonnet 4** via the Anthropic API.

---

## 🏆 Gamification System

```
XP (Experience Points)   →  Earned by completing lessons, quizzes, games
Levels                   →  Every 1000 XP = new level
Streaks                  →  Daily login + activity tracking
Badges                   →  Milestone achievements
Certificates             →  Awarded on course completion
Leaderboard              →  Global ranking by XP
```

---

## 🗺 Roadmap

- [x] Student + Teacher auth portals
- [x] Coding lab with AI compiler
- [x] 8-language learning module
- [x] 5 STEM subject hubs
- [x] Teacher quiz creation & assignment
- [x] 6 mind games (Memory Match fully playable)
- [x] Global leaderboard
- [x] Certificate system
- [x] EduBot AI chatbot
- [ ] Real-time multiplayer quiz battles
- [ ] Video lesson integration
- [ ] Parent/guardian portal
- [ ] Mobile app (React Native)
- [ ] Backend with persistent database (Supabase / MongoDB)
- [ ] OAuth (Google / GitHub login)
- [ ] Spaced repetition flashcard system
- [ ] Live classroom mode for teachers

---

## 🤝 Contributing

Contributions are welcome! Here's how to get started:

```bash
# Fork the repo, then:
git clone https://github.com/yourusername/eduquest.git
git checkout -b feature/your-feature-name

# Make your changes, then:
git commit -m "feat: add your feature description"
git push origin feature/your-feature-name
# Open a Pull Request
```

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for code style guidelines and commit conventions.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**David Raj**
- GitHub: (https://github.com/boddudavidraj)
- LinkedIn: (www.linkedin.com/in/david-raj-boddu-8b33b037b)
---

<div align="center">

Made with ❤️ and ☕ by David Raj

⭐ **Star this repo if EduQuest helped you!** ⭐

*"Education is not the filling of a pail, but the lighting of a fire." — W.B. Yeats*

</div>
