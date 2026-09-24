# Foundry releases

## 0.4.0 — 2026-09-24

- **Model presets.** Every action — Clarify, Planner, Simple / Standard / Complex tasks, merges, goal and task reviews, docs, feedback triage, hints, style samples — now has its own model, set by a preset. Max, Production, Balanced and Economy ship built in, each with a table for Code, Docs & research and Media goals. Settings picks one per goal type (Code = Production, Docs & Media = Balanced by default) and the New goal form can pick another for one goal. Built-in presets can be edited and reset; your own can be created, renamed and deleted. Settings that used the old Strong / Worker / Cheap tiers move to the defaults once, with a note listing the old values.
- **Model sync.** Foundry reads every model id your Claude Code knows and resolves fable / opus / sonnet / haiku with one tiny session each — automatically when Claude Code updates, or with *Sync models*. Dropdowns show what each alias resolves to and the newest pinned ids; no ids to type.
- **Task difficulty.** The Clarifier rates each task simple, standard or complex (editable on the Brief); it picks the model the worker runs on. The last attempt of a task and every retry you grant run on the Complex-task model. A model found unavailable is remembered per goal.
- **Faster delivery.** Repositories without CI no longer wait 90 s per PR for checks that never come; checks are polled every 10 s at first; each PR is retargeted once; new goals deliver as one PR by default. Dependencies are installed in the delivery worktree before its checks, so the Acceptance card no longer turns red after a delivery.
- **Effort per goal.** Claude Code's effort level (low … max) is set on the New goal form or in Settings and applies to every session of the goal.
- **Cheaper goal review.** Small goals (≤ 400 diff lines) are reviewed without the expensive sub-agents; large diffs are read from a file instead of being pasted into the prompt.
- Live logs show when a sub-agent is still working; the interview round title no longer suggests four pages; session usage is labelled with the model that did the work.

## 0.3.0 — 2026-09-14

- **Progress folders.** Every goal's work now lives next to your repository as `<repo>-foundry/<goal>/` — open it, run it, read it at any time. Goals in flight are moved there when the engine starts; Settings → Engine → *Progress folders* moves the root (ADR-0011).
- **Milestones.** The Brief marks 1–3 tasks after which the goal pauses for a look: the preview starts, the Inbox and Telegram get the note (with a screenshot when the self-check is on). Continue, or write what you saw and confirm what it becomes — a hint for the remaining tasks, fix tasks (then a second look), or a Decision every later task follows (ADR-0012).
- **Preview.** The engine runs the goal's dev server in its progress folder (ports 4200–4299, Settings → Preview; Docker: publish the range), restarts it after each task lands, stops it when idle. The Brief can name the run command; otherwise package.json is read.
- **Self-check** (off by default). After each task lands, headless Chromium opens the preview, screenshots it and fails a must check on console, page or network errors. Chromium is installed from Settings → Preview.
- **Clarify interviews you** in rounds before writing the Brief: only the decisions the repository cannot settle, each with a recommended answer and the reason it asks; answers become Decisions and Revise resumes the same session. Settings → Workflow chooses auto / always / never (ADR-0013).
- **Goal review.** *Retry with hint* on a goal-level escalation spawns fix tasks from the reviewer's findings instead of re-running the review; a re-review sees the previous verdicts and may flip one only with a cited reason; the review timeout is 30 minutes.
- A model change in Settings reaches goals in flight; the chosen style sample reaches mobile and general tasks and every task worktree; worker permission denials are guarded; the release script resumes after a failed image push.

## 0.2.1 — 2026-09-03

- Fable 5.1: pick `fable` (Claude Code ≥ 2.1.259 resolves it to claude-fable-5-1) or the pinned `claude-fable-5-1` entry in Settings → Models & limits; the Docker image now ships Claude Code 2.1.259
- Self-update under launchd/systemd: set FOUNDRY_SUPERVISED=1 and the updater exits for the service manager instead of respawning itself (fixes a port fight after one-click updates)
- Docker: markitdown is baked into the image (the in-container install could not write the root-owned tool dirs)
- New guides: remote access via Tailscale (keep working from your phone), Telegram/Discord notification setup
- Documentation audited against the code and corrected throughout; Simplified Chinese versions of the README and every guide

## 0.2.0 — 2026-08-28

### Version detection and one-click self-update (#7)
- Foundry knows its own version and checks the release registry daily; a header pill and Settings → About & updates show what is new, with the changelog
- One-click update: docker installs go through a watchtower sidecar (new docker-compose.yml); local installs run git pull → install → rebuild with automatic rollback
- Updates drain first — active agents finish before the restart, with a force option; installs that cannot self-update get the exact guided commands instead
- New-version notifications via Telegram/Discord (own switch)

### Notifications (#6)
- Telegram and Discord push notifications, configured on the Settings page: *Needs you* (an escalation), *Goal finished*, *Delivery* (PR opened / merged / failed) and *Usage pause*, each with its own switch
- Optional link base URL so messages open the right page from a phone; Detect button resolves the Telegram chat id; Send test message per channel

### Agents monitor (#5)
- New Agents page and header pill: every Claude Code session on the machine — Foundry-spawned and external — with source, busy/idle/finished status, model, elapsed time, context-window usage and nested subagents
- Click a session for its live log; Foundry sessions can be stopped from here, external ones are watched only

### Packs, keys and a readable Skills page (#4)
- Image pack adds claude-image-gen (Gemini / OpenAI gpt-image) and taste-imagegen; design pack adds design-taste-frontend; video pack adds the hyperframes kit (HTML+GSAP motion graphics rendered to real video)
- Kimi and Gemini API keys under Settings → Tools & keys, applied without a restart; a missing required key shows as a degraded-mode warning instead of a silent fallback
- Skills page groups sources by manager, folds installed entries away, streams pack installs inline, and offers a real Install button for CLI tools
- Catalog edits now reach the running server; the web app is part of typecheck

### Light mode (#3)
- Sun/moon toggle in the header; first visit follows the system theme
- The consistency pass it exposed: real surfaces for tables, lists and markdown panels, readable dim text, header/tab edges, no layout shift between tabs, one page width everywhere, header no longer overflows at mid widths
- Settings: sticky save bar, section index, seven sections grouped by intent, and a control for the default pace

### Renamed to Foundry (#2)
- The project is Foundry: `@foundry/*` packages, `FOUNDRY_*` environment variables, image `imlouiskhenghao/foundry`; existing installs stay managed via the legacy skill marker
- Deployments must rename their `AI_ENGINE_*` environment variables — there is no legacy fallback

## 0.1.0 — 2026-08-28

### Media goals, style proposals, fast pace, plan UX (#1)
- Goals can produce images, video, research and documents, not only code: goal nature and output folder, image/video skill packs, artifacts generated in the workspace and delivered at done, reviewers that judge the artifacts
- The Clarifier proposes visual style directions for media and UI goals; the chosen direction binds workers and reviewers; on-demand style samples with kept history
- Fast pace per goal skips the engine's own AI reviews; media goals start fast
- Brief plan UX: tasks edit in a modal, stages as numbered groups, Kind / Area / Scenario tags, clickable dependency chips, a readable task graph, live Clarifier output while drafting

### Completion actions
- Post-goal documentation (PRD, README, changelog, confirmation questionnaire) generated by a Documenter and shipped in the same delivery; knowledge-graph refresh after delivery
- Brief questions carry options with the recommendation first; empty repositories get a tech-stack question
- Usage pauses survive restarts and show a banner

### Docker
- Official image with the engine, web UI and every tool it drives; volumes for the event log and the Claude login; repositories mounted at /repos
- Headless sign-in from the web UI in Docker and remote environments (copy-the-code flow)
- autoskills handles symlinked skills correctly (they are never committed)

### Orchestration
- Manual merge resolution page for conflicts the engine cannot settle
- TDD discipline (required / preferred / off) per goal and task; Simple mode with a plain-language Brief and progress view
- Continuations: interrupted or capped sessions resume instead of restarting; per-attempt session tracking and cost
- AI-suggested hints for escalations, with one-click apply
- Brief Areas with per-Area planning and coverage; answered questions and rejected assumptions become Decisions carried into every prompt, with revise-with-answers
- Base-branch sync before a goal starts and between tasks; merges judged on regressions only; conflict avoidance between overlapping tasks
- The foundation: goals → Brief → tasks on isolated worktrees, checks, reviews, stacked per-task PRs, budgets, skills catalog, Settings with file › env › default precedence
