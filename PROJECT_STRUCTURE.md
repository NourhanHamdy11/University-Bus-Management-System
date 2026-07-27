<div align="center">

# 🗂️ Project Structure

</div>

This document explains what lives in every folder and file of this repository, and why.

```
University-Bus-Management-System/
│
├── README.md                 # Project landing page: overview, features, diagrams, badges
├── LICENSE                   # MIT License
├── .gitignore                 # Ignore rules for common build/OS/IDE artifacts
├── CONTRIBUTING.md            # How to propose changes to this repository
├── CODE_OF_CONDUCT.md         # Community standards for contributors
├── PROJECT_STRUCTURE.md       # This file
├── REQUIREMENTS.md            # Full functional & non-functional requirements (FR-01 … FR-13)
├── USE_CASES.md               # Actors, use cases, and detailed usage scenarios
├── SYSTEM_DESIGN.md           # Class, sequence, activity, state, collaboration diagrams & DFDs
├── CHANGELOG.md               # Version history of the documentation/design deliverables
│
├── docs/
│   └── University Bus Management System.pdf   # Original source specification (Feb 2025)
│
├── diagrams/                  # Every UML / DFD diagram, exported as standalone PNGs
│   ├── use-case.png
│   ├── sequence-1-booking-a-trip.png
│   ├── sequence-2-realtime-tracking.png
│   ├── sequence-3-first-station-notification.png
│   ├── sequence-4-qr-code-validation.png
│   ├── sequence-5-assigning-drivers-buses.png
│   ├── sequence-6-system-update.png
│   ├── class-diagram.png
│   ├── activity-1.png
│   ├── activity-2.png
│   ├── state-1.png
│   ├── state-2.png
│   ├── collaboration-1.png
│   ├── collaboration-2.png
│   ├── collaboration-3.png
│   ├── dfd-level0.png
│   └── dfd-level1.png
│
├── images/                    # Supporting photography referenced from the README
│   ├── campus-bus.jpg
│   └── campus-bus-fleet.jpg
│
└── assets/                    # Non-diagram visual assets (banner, badges source, etc.)
    └── banner.svg
```

---

## Folder-by-folder

### `/` (root)

Root-level files are the ones every visitor and every GitHub feature (Issues templates, license detection, community-profile checklist) looks for first: `README.md`, `LICENSE`, `.gitignore`, `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`. Keeping them at the root — rather than nested in `docs/` — is what makes GitHub auto-detect the license badge, the "Contributing" link, and the community health checklist.

### `docs/`

Holds the **original source of truth**: the specification PDF this entire repository was generated from. Every other Markdown file in the repo is a structured, navigable derivative of this document — if anything here ever looks ambiguous, `docs/` is the tiebreaker.

### `diagrams/`

One PNG per diagram, extracted directly from the source PDF at full resolution. Naming follows a flat, predictable convention (`<type>-<index>.png`) so they can be embedded individually in Markdown (`README.md`, `SYSTEM_DESIGN.md`, `USE_CASES.md`) without any ambiguity about which figure is which. This folder intentionally contains **only** diagrams — no decorative photography or icons.

### `images/`

General-purpose photography used to give the README visual context (e.g., the actual bus referenced in the source deck). Kept separate from `diagrams/` so the two folders can be told apart at a glance: `diagrams/` is technical and diagrammatic, `images/` is photographic.

### `assets/`

Non-photographic visual assets that support the documentation but aren't diagrams — currently the README banner (`banner.svg`). Future additions (a project logo, a favicon, exported badge SVGs) belong here.

---

## Root files at a glance

| File | Purpose |
|---|---|
| `README.md` | Entry point — overview, features, requirements summary, diagrams, tech, team, license |
| `REQUIREMENTS.md` | The 13 functional requirements (FR-01–FR-13) and all non-functional requirement categories |
| `USE_CASES.md` | 4 actors, 16 use cases, and all 16 detailed usage scenarios |
| `SYSTEM_DESIGN.md` | Class diagram, 6 sequence diagrams, 2 activity diagrams, 2 state diagrams, 3 collaboration diagrams, 2 DFDs — each with a short explanation and, where useful, a Mermaid equivalent |
| `CONTRIBUTING.md` | Branch naming, commit style, and the PR process for this repo |
| `CODE_OF_CONDUCT.md` | Expected behavior for anyone participating in this project |
| `CHANGELOG.md` | What changed and when, in [Keep a Changelog](https://keepachangelog.com/) format |
| `LICENSE` | MIT License text |
| `.gitignore` | Ignore rules covering common web, mobile, Python, and IDE artifacts |

> 📎 Return to [`README.md`](README.md).
