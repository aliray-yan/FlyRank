# FlyRank — AI-Assisted Development Capstone

FlyRank is a capstone repository built to demonstrate professional, AI-assisted
software development workflows. Across three weeks, the project moves from
basic AI-tooling conventions, to a controlled experiment on prompt quality, to
a full production-style React application built entirely through a
structured, phased prompting workflow.

## Repository structure

```
FlyRank/
├── Week 1/                      Git & AI-assistant tooling setup (GitHub Copilot)
│   ├── README.md
│   ├── COPILOT.md                AI-assistant rules & project conventions
│   ├── LICENSE                    MIT License
│   ├── .gitignore
│   ├── Commits Screenshot.jpg
│   └── Task Completion By GitHub Copliot.jpg
│
├── Week 2/                      Vague vs. Structured AI-prompting experiment
│   ├── README.md
│   ├── vague/                     Settings page built from a single one-line prompt
│   └── structured/                Same feature, built with a full spec + plan + tests
│       ├── WORKFLOW.md            Side-by-side comparison write-up
│       └── docs/Screenshots/      Evidence (branches, test runs, planning, prompts)
│
└── Week 3/                      AnimeVerse — full React + Firebase application
    ├── README.md
    └── React Project one/          Complete anime discovery app
        ├── README.md                 App docs + full AI prompt plan used to build it
        └── src/                      React 19 + Vite + Firebase + Jikan API source
```

## Weekly breakdown

| Week | Focus | What was produced | Details |
|---|---|---|---|
| **Week 1** | Environment & AI-assistant conventions | Repo scaffold, `COPILOT.md` rules file, Conventional Commits, license/ignore setup, screenshot evidence of Copilot-assisted work | [`Week 1/README.md`](./Week%201/README.md) |
| **Week 2** | Prompt-quality experiment | Two implementations of the same Settings page — one from a vague one-line prompt, one from a fully structured spec — compared on architecture, testing, and accessibility | [`Week 2/README.md`](./Week%202/README.md) |
| **Week 3** | Full application build | AnimeVerse, a complete anime discovery React app (search, details, auth, favorites) built feature-by-feature from a 15-prompt development plan | [`Week 3/README.md`](./Week%203/README.md) |

## Tools & tech used across the capstone

- **AI assistants:** GitHub Copilot (Week 1), structured AI-prompting workflow (Weeks 2–3)
- **Frontend:** React (19 in Week 3), Vite, React Router DOM, TypeScript (Week 2)
- **Backend/services:** Firebase Authentication, Firestore, Jikan REST API (Week 3)
- **Tooling:** Git (Conventional Commits, feature branches), ESLint, Vitest/Jest-style tests, Axios

## How to explore this repo

1. Start with **Week 1** to see the baseline tooling/AI-assistant conventions the rest of the project follows.
2. Read **Week 2** to see how prompt structure affected code quality on an identical task — the `WORKFLOW.md` file there has the full write-up.
3. Explore **Week 3** for the complete application. Its README includes the exact Master Project Prompt (PRD) and the phase-by-phase prompt plan used to build it, so the whole AI-collaboration process is reproducible.

## License

MIT — see [`Week 1/LICENSE`](./Week%201/LICENSE).
