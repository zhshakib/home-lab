# home-lab

A public dev journal of my journey from **CSE student → Junior Backend Engineer (PHP/Laravel)**.

I'm rebuilding my whole setup around Linux, Laravel, and local AI coding agents — and documenting every day in public. No fluff, no over-engineering. Just what I did, what broke, and what's next.

---

## Why this repo exists

- **Remember what I did** — a daily log beats trying to recall last month
- **Build in public** — accountability + proof of work
- **Reuse my own fixes** — errors repeat; the log saves me next time
- **Turn it into a portfolio** — eventually this becomes a Laravel app

---

## The system

One file per day. Three sections. Done in 3 minutes.

```
home-lab/
└── journal/
    ├── 2026-09-24.md
    ├── 2026-09-25.md
    └── ...
```

Each entry has:
- **Did** — what I worked on
- **Broke** — what went wrong and the fix
- **Next** — what's coming

Every entry also includes ready-to-post versions for **X (Twitter)** and **LinkedIn** so I don't write twice.

---

## My setup

**Hardware**
- CPU: AMD Ryzen 5 3600G (Vega iGPU, gfx900)
- RAM: 16GB shared
- GPU: none — iGPU only

**Stack**
| Layer | Choice |
|---|---|
| OS | Fedora KDE Plasma |
| Containers | Podman (Fedora default) |
| Backend | PHP + Laravel |
| Editor | VS Code + Continue.dev |
| Local AI runtime | Ollama |
| Local AI models | Qwen2.5-Coder-1.5B, DeepSeek-Coder-V2-Lite |
| Terminal AI agent | Aider |

**Why these choices:** see [journal/2026-09-24.md](journal/2026-09-24.md)

---

## The roadmap

Toward a **Junior Laravel Backend Engineer** role:

1. **PHP foundations** — OOP, Composer, PSR, PHP 8.3+ features
2. **Laravel fundamentals** — routing, Eloquent, Blade, validation
3. **Production-ready** — APIs (Sanctum), queues, Redis, testing
4. **DevOps** — Dockerize, deploy, CI, basic system design

Portfolio project: rebuild this journal as a **Laravel blog**. Documentation and portfolio in one.

---

## Follow along

- **X:** [@yourhandle](https://x.com/zhshakib)
- **LinkedIn:** [your name](https://linkedin.com/in/zhshakib)

---

## Status

- [x] Day 0 — planning + decisions locked
- [ ] Fedora KDE installed
- [ ] Dev environment ready (PHP, Composer, Podman, VS Code)
- [ ] Local AI agent running
- [ ] First Laravel app deployed

_Last updated: 2026-09-24_
```