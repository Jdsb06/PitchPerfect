# PitchPerfect-AI

**AI-powered mock interview & pitch practice platform**

Built for **COMSOC HackX 2025** by **Team CodeDiLassi**.

---

## 🎯 Project Overview

PitchPerfect is an interactive EdTech prototype designed to simulate realistic mock interviews and investor pitches using cutting-edge AI. Our MVP delivers:

* **Resume-Based Question Generation**: Automatically parse user resumes and generate tailored interview questions using OpenAI.
* **Adaptive AI Interviewers**: Simulate different personas (Tough, Friendly, Distracted) via GPT-driven chat.
* **Real-Time Speech Feedback**: Analyze audio (Whisper) to provide live coaching on pace and tone.

> 🚀 **Demo Flow**: Upload resume → Browse generated questions → Start AI mock interview → Receive live feedback tips

---

## 📂 Repository Structure

```text
pitchperfect-ai/
├── README.md            # Project overview & instructions
├── .gitignore           # Exclude node_modules, env files, etc.
├── .env.example         # Template for environment variables
│
├── frontend/            # React + Tailwind front-end application
├── backend/             # Node.js (Express) + FastAPI back-end services
├── ai-services/         # AI integrations: GPT prompts, Whisper, feedback logic
├── assets/              # Logos, images, demo videos, sample resumes
├── docs/                # Hackathon docs: pitch script, slides, diagrams
├── scripts/             # Dev scripts (deployment, cleanup, utility)
└── .github/             # GitHub workflows & issue/PR templates
```

---

## ⚙️ Setup & Installation

> **Prerequisites**: Node.js (v16+), Python (3.8+), Yarn or npm, Git

1. **Clone the repo**

   ```bash
   git clone https://github.com/CodeDiLassi/pitchperfect-ai.git
   cd pitchperfect-ai
   ```

2. **Create environment files**

   ```bash
   cp .env.example frontend/.env
   cp .env.example backend/.env
   ```

   * Update API keys (OpenAI, Firebase) in `.env` files.

3. **Install dependencies**

   * Frontend:

     ```bash
     cd frontend
     npm install      # or yarn install
     ```
   * Backend:

     ```bash
     cd backend
     npm install      # or yarn install
     pip install -r requirements.txt
     ```
   * AI Services (if separate):

     ```bash
     cd ai-services
     pip install -r requirements.txt
     ```

4. **Run development servers**

   * Frontend: `npm run dev` ([http://localhost:3000](http://localhost:3000))
   * Backend API: `npm start` or `node app.js` ([http://localhost:4000](http://localhost:4000))
   * FastAPI (Whisper): `uvicorn fastapi_service:app --reload` ([http://localhost:8000](http://localhost:8000))

---

## 👥 Team & Roles

| Member      | Responsibilities                                     | Branch Prefix             |
| ----------- | ---------------------------------------------------- | ------------------------- |
| Frontend    | UI components, pages, styles                         | `feature/frontend-...`    |
| Backend     | API routes, controllers, database integration        | `feature/backend-...`     |
| AI/ML       | GPT prompts, persona simulation, question generation | `feature/ai-question-gen` |
| Audio       | Whisper integration, speech feedback analysis        | `feature/audio-feedback`  |
| Integration | Glue code, deployment scripts, end-to-end testing    | `feature/integration`     |

> 📌 **Branching Model**: Create feature branches off `main`, complete small PRs (<1 day), request 1 peer review, then merge to `main`. Keep `main` deployable.

---

## 🛠️ Development Workflow

1. **Plan tasks** in GitHub Issues & Project Board (Kanban: To Do → In Progress → Done).
2. **Assign** issues to team members and label (`frontend`, `backend`, `ai`, `audio`, `integration`).
3. **Branch & Code**: `git checkout -b feature/issue-<ID>-short-desc`
4. **Commit** frequently with clear messages (`feat:`, `fix:`, `chore:`).
5. **Push & PR**: Open Pull Request targeting `main`. Link the issue, assign reviewer.
6. **Review & Merge**: After approval, merge via GitHub UI. Delete feature branch.
7. **Deploy** (if applicable): Run `scripts/deploy.sh` or manually push to Vercel/Render.

---

## 🗓️ Timeline & Milestones (July 14–19)

* **July 14**: Repo & board setup, env config, basic scaffolding
* **July 15**: Stage 1 complete – resume upload & question list demo
* **July 16**: Stage 2 start – interview UI scaffolding; midday demo Stage 1
* **July 17**: Stage 2 complete – persona-driven mock interview demo
* **July 18**: Stage 3 implement – real-time feedback demo
* **July 19**: Polish, bug-fix, final demo rehearsal, submission

---

## 📚 Additional Resources

* **React Docs**: [https://reactjs.org/docs/getting-started.html](https://reactjs.org/docs/getting-started.html)
* **OpenAI API**: [https://platform.openai.com/docs/introduction](https://platform.openai.com/docs/introduction)
* **Whisper**: [https://github.com/openai/whisper](https://github.com/openai/whisper)
* **FastAPI**: [https://fastapi.tiangolo.com/](https://fastapi.tiangolo.com/)

---

> *Happy coding, Team CodeDiLassi! Let’s get PitchPerfect ready for COMSOC HackX!*
