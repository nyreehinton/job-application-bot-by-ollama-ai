## Repository research digest

**Repo:** `job-application-bot-by-ollama-ai` (workspace root)  
**Nature:** This checkout is **documentation and static assets only**. There is **no application source code**, dependency manifests, tests, CI, or server code in the tree.

---

### 1) Purpose and high-level summary

- **Stated purpose (from docs):** Marketing and user-facing documentation for **JobHuntr** (jobhuntr.fyi) — a desktop product that automates job applications (e.g. LinkedIn), with optional **local Ollama** vs **cloud AI** positioning in `PRICING.md` / `USER_LETTER.md` / `README.md`.
- **User-specific layer:** `NYREE_*.md` files are **personal job-search configuration** (filters, FAQ answers, profile text, targets) meant to be copied into the **installed app**, not executed from this repo.
- **Mismatch with repo name:** The name suggests an Ollama-based bot codebase; **no Ollama integration code** lives here — only prose references (e.g. `NYREE_TARGETS.md`, `PRICING.md`).

---

### 2) Directory tree (depth 3) and language / ecosystem

```
.
├── .gitignore
├── FAQ.md
├── MAC_SETUP.md
├── NYREE_FAQ.md
├── NYREE_PROFILE.md
├── NYREE_TARGETS.md
├── PLATFORM_LETTER.md
├── PRICING.md
├── README.md
├── USER_LETTER.md
├── WIN_SETUP.md
└── src/
    ├── demo.gif
    ├── flow_chart.png
    ├── history.png
    ├── installer_image.png
    ├── login.png
    ├── logo-large.png
    ├── mac_download.png
    ├── queue.png
    ├── sample_cover_letter.pdf
    ├── setup_page.png
    ├── slack-logo.png
    ├── star_repo.gif
    ├── where_find_it.png
    ├── where_to_subscribe.png
    ├── windows_download.png
    ├── windows_finish_install.png
    ├── windows_ui.png
    └── windows_unknown_publisher.png
```


| Layer                                                                       | Ecosystem                                   |
| --------------------------------------------------------------------------- | ------------------------------------------- |
| Root                                                                        | **Markdown** only (11 `.md` files)          |
| `src/`                                                                      | **Binary assets** (PNG, GIF, PDF) — no code |
| **No** `package.json`, `pyproject.toml`, `requirements.txt`, `go.mod`, etc. | **N/A**                                     |


---

### 3) Entrypoints (CLI, main scripts, servers, scheduled jobs)


| Type                                            | In repo?                      |
| ----------------------------------------------- | ----------------------------- |
| **CLI**                                         | None                          |
| **Python / Node / shell scripts**               | None                          |
| **HTTP server / webhooks**                      | None                          |
| **Scheduled jobs (cron, GitHub Actions, etc.)** | None (no `.github/workflows`) |


**Documented “entry” for end users:** Install **GUI app** from releases / jobhuntr.fyi (`MAC_SETUP.md`, `WIN_SETUP.md`, `README.md` links) — **not** something you run from this clone.

---

### 4) Key “modules” (all meaningful files; fewer than 30)

Importance is **documentation / asset role**, not code complexity.


| Path                          | Role                                                                               |
| ----------------------------- | ---------------------------------------------------------------------------------- |
| `README.md`                   | Product overview, changelog-style updates, links to setup, FAQ, pricing, demo      |
| `MAC_SETUP.md`                | macOS install (DMG from GitHub releases), login flow, first run                    |
| `WIN_SETUP.md`                | Windows install (`JobHuntr-Setup.exe`), login flow                                 |
| `FAQ.md`                      | End-user FAQ (e.g. History / Q&A)                                                  |
| `PRICING.md`                  | Plans, Ollama vs premium AI comparison                                             |
| `USER_LETTER.md`              | Product positioning, competitor table, Ollama cost note                            |
| `PLATFORM_LETTER.md`          | Responsible use / partnership / API interest (prose)                               |
| `NYREE_TARGETS.md`            | Personal bot filters, Ollama URL **example** `http://localhost:11434`, job targets |
| `NYREE_PROFILE.md`            | Resume-style profile for applications                                              |
| `NYREE_FAQ.md`                | FAQ-style answers for the bot                                                      |
| `.gitignore`                  | Ignores `.DS_Store` only                                                           |
| `src/*.png`, `src/*.gif`      | README / setup screenshots and branding                                            |
| `src/sample_cover_letter.pdf` | Sample asset                                                                       |


---

### 5) HTTP routes, API surfaces, webhooks

- **None in repository code** (no server).
- **External URLs referenced in markdown:** `https://jobhuntr.fyi`, GitHub releases (`lookr-fyi/job-application-bot-by-ollama-ai/releases/...`), Slack invite, TikTok, YouTube demo — **outbound links only**, not routes defined here.

---

### 6) CLI commands

- **None** documented as shell/CLI for this repo. Setup docs describe **GUI** steps only.

---

### 7) Dependencies from manifests

- **No** `package.json`, `requirements.txt`, `pyproject.toml`, `Pipfile`, `Cargo.toml`, `go.mod`, `Gemfile`, etc.  
- **Versions:** N/A for this tree.

---

### 8) Environment variables (code patterns)

- Searched for `os.environ`, `getenv`, `process.env`, `dotenv` in the repo: **no matches** (no code).
- **Prose / config examples:** `NYREE_TARGETS.md` documents a literal **Ollama base URL** for the installed app (`http://localhost:11434`) — not `os.environ`-style usage.

---

### 9) Tests and coverage

- **No** `tests/`, `test_*.py`, `*.test.ts`, `pytest.ini`, `jest.config.`*, coverage config, or CI test jobs.
- **Coverage hint:** Not applicable; nothing to measure in this tree.

---

### 10) Config files


| File                                                                                                           | Notes                 |
| -------------------------------------------------------------------------------------------------------------- | --------------------- |
| `.gitignore`                                                                                                   | Minimal (`.DS_Store`) |
| **No** `docker-compose`*, `Dockerfile`, `*.toml` (app), `editorconfig`, `pre-commit`, `tsconfig`, ESLint, etc. |                       |


---

### 11) Data stores / DB / migrations

- **None** in repository.

---

### 12) Security-sensitive patterns

- **No secrets or API keys** in files scanned; no credential placeholders like `sk-...` in markdown grep results.
- **Third-party / identity flows described:** LinkedIn email + browser login; note that **Google OAuth is discouraged** in embedded Chromium (`MAC_SETUP.md` / `WIN_SETUP.md`).
- **Risk (process):** `NYREE_*.md` can contain **PII / career details** suitable for job apps — treat as sensitive if published; not “secrets” in the API-key sense.

---

### 13) Notable gaps and risks


| Gap / risk                  | Detail                                                                                                                                                                         |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Name vs contents**        | Repo suggests an Ollama bot **source** project; actual clone is **docs + images** only.                                                                                        |
| **No reproducible build**   | Cannot audit behavior, security, or data handling from this tree — real app is **closed binary** (per `USER_LETTER.md` “Open Source: ❌” for JobHuntr in the comparison table). |
| **README asset paths**      | `README.md` references `src/logo-large.png`, etc. — present in `src/`; OK.                                                                                                     |
| **Automation / compliance** | `PLATFORM_LETTER.md` discusses responsible use and interest in official APIs — **policy**, not implementation here.                                                            |
| **Fork / clone confusion**  | Contributors expecting Python/Node/Ollama code will find **zero** runtime.                                                                                                     |


---

**Bottom line:** Static analysis of **this** repository describes a **small documentation and asset bundle** (JobHuntr + personalized `NYREE_`* notes), not a runnable bot or Ollama service. Any real entrypoints, HTTP APIs, env handling, DB, and tests live **outside** this tree (distributed app / other repos).