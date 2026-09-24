# 2026-09-24 — Day 0: Planning the Journey

## what I learned

**1. "Rolling release or fixed? I want to use it long-term without tweaking."**
→ Learned that "not tweaking" and "rolling release" are almost opposites. Rolling = latest packages but you're the sysadmin. Fixed release = stable but stale. Middle ground: Fedora's 6-month cycle.

**2. "Can I go with Debian or Fedora? I love their snaps."**
→ Big correction: **Snaps are Ubuntu's thing.** Debian, Fedora, and openSUSE don't ship them by default. Debian has the best Snapd integration of the three, but for Laravel dev, **you don't need Snaps at all** — Composer + Docker cover everything.

**3. "If I install Fedora, do I have to reinstall every 6 months?"**
→ No. `dnf system-upgrade` does **in-place upgrades**. All your files, configs, and apps carry over. You can even **skip a release** — F43 → F45 is supported. Each release gets ~13 months of updates, so upgrading **once a year** is fine.

**4. "Which Fedora flavor for Ryzen 5 3600G, 16GB RAM, no GPU?"**
→ **Fedora KDE Plasma.** Lighter than GNOME on the iGPU, now an official Fedora Edition, traditional layout = less friction coming from Windows. More RAM headroom for local LLMs, which matters a lot when everything shares 16GB.

**5. "How do I document this without it becoming a chore?"**
→ Started with a big fancy folder tree. Realized it was over-engineered. **Simple wins:** one repo, one markdown file per day, one post from it. 3 lines in the file, 2 minutes for the post. Same day, every day.

## Decisions locked in

| Decision | Choice | Why |
|---|---|---|
| OS | **Fedora KDE Plasma** | Fresh PHP without third-party repos, Podman + SELinux for backend skills, annual upgrade path |
| Container tool | **Podman** (Fedora default) | Rootless, daemonless, `docker` CLI compatible — resume-friendly |
| Local AI runtime | **Ollama** | Easiest local model runner |
| Local AI models | **Qwen2.5-Coder-1.5B**, **DeepSeek-Coder-V2-Lite** | Only realistic options for Vega iGPU + 16GB RAM |
| Local AI agents | **Continue.dev** (editor) + **Aider** (terminal) | Free, local, git-aware |
| Docs system | One repo, one file/day, one post | Consistency > completeness |

## What I learned about my own hardware
- Vega iGPU (gfx900) needs `OLLAMA_IGPU_ENABLE=1` — newer Ollama drops some iGPUs silently
- Realistic LLM ceiling: 1B–3B comfortable, 8B at ~6 tok/s, 14B+ not worth it
- RAM is the bottleneck. Desktop + IDE + browser + LLM all fight over 16GB
- KDE over GNOME = actual headroom for models

## Laravel roadmap in one glance
1. **PHP + OOP + Composer** — foundations
2. **Laravel fundamentals** — routing, Eloquent, Blade, validation
3. **Production-ready** — APIs (Sanctum), queues, Redis, tests
4. **DevOps** — Dockerize, deploy, CI, basic system design

Portfolio project plan: **build my own journey blog in Laravel** — kills two birds (documentation + portfolio).

## Open questions for tomorrow
- Does `OLLAMA_IGPU_ENABLE=1` still work on latest Ollama?
- Best ROCm version for gfx900 on current Fedora kernel?

## Next session
- Install Fedora KDE, verify hardware
- Post-install: RPM Fusion + codecs + JetBrains Mono
- Install Composer, verify PHP extensions
- First journal post goes live

---

# 📣 Social Posts

## Twitter / X — Thread

**Tweet 1 (hook):**
```
Day 0 of my home-lab journey 🐧

7th-sem CSE student. Goal: Junior Laravel Backend role.
Today I locked in the whole stack.

Thread 🧵
```

**Tweet 2:**
```
OS decision: Fedora KDE Plasma.

Considered Debian, Tumbleweed, Arch.

Picked Fedora because:
• Latest PHP with zero third-party repos
• In-place upgrades — no reinstalls ever
• Podman + SELinux = real backend skills
• Can skip releases → upgrade once a year
```

**Tweet 3:**
```
Fun correction from today:

I thought Debian & Fedora came with "snaps."

Nope — Snaps are Ubuntu's thing. 💀

Debian has the best Snapd support of the three, but for Laravel dev you don't need Snaps at all.
Composer + Docker covers everything.
```

**Tweet 4:**
```
Local AI setup (no GPU, 16GB RAM):

• Ollama for runtime
• Qwen2.5-Coder-1.5B + DeepSeek-Coder-V2-Lite
• Continue.dev in VS Code
• Aider in the terminal

Vega iGPU needs OLLAMA_IGPU_ENABLE=1 or it silently drops support.

Realistic ceiling: ~6 tok/s on 8B. Good enough.
```

**Tweet 5:**
```
The roadmap: PHP → Laravel → APIs & Queues → DevOps.

Portfolio project: build my own journey blog in Laravel.

Documentation + portfolio in one project.

Day 1 tomorrow: install + first post.
```

## LinkedIn — Single Post

```
Day 0: I'm rebuilding my dev setup and documenting the whole thing.

I'm a 7th-semester CSE student aiming for a Junior Backend Engineer role in PHP/Laravel. Over the next few months, I'm going all-in on Linux, Laravel, and local AI coding agents — and I'm doing it in public.

Here's what I locked in today:

🖥️ OS: Fedora KDE Plasma
I considered Debian, openSUSE Tumbleweed, and Arch. Fedora won because it gives me a fresh PHP toolchain without third-party repos, does true in-place upgrades (no reinstalls), and ships Podman + SELinux — both relevant for backend and DevOps work.

🐳 Containers: Podman
Rootless, daemonless, drop-in `docker` CLI compatible. Resume-friendly and Fedora-native.

🤖 Local AI agents: Ollama + Continue.dev + Aider
Running Qwen2.5-Coder-1.5B and DeepSeek-Coder-V2-Lite entirely locally on a Ryzen 5 3600G with 16GB RAM — no GPU. Realistic but workable. The Vega iGPU needs OLLAMA_IGPU_ENABLE=1 to be used at all, which took some digging.

🗺️ The Laravel roadmap:
1. PHP + OOP + Composer
2. Laravel fundamentals (routing, Eloquent, Blade, validation)
3. Production-ready: APIs (Sanctum), queues, Redis, testing
4. DevOps: containerize, deploy, CI, system design basics

Portfolio project: I'll build my own journey blog in Laravel. Documentation and portfolio in one.

Biggest lesson today: rolling release ≠ less work. And "Snaps" aren't a Debian/Fedora thing — that's Ubuntu. 😅

Day 1 tomorrow: install Fedora, set up the dev environment, get the first local AI agent running.

If you've walked this path before — what would you have done differently in your first month of Laravel?

#Laravel #PHP #Fedora #BackendDevelopment #DevJourney #Linux
```