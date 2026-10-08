# Foundry releases

## 1.1.1 — 2026-10-08

- feat(setup): sign the GitHub CLI in from the Setup page
- feat(github): run the GitHub sign-in as a session a page can follow
- fix(install): sign in through the terminal's own device, not /dev/tty

## 1.1.0 — 2026-10-08

- docs(guide): retake the screenshots
- fix(brief): do not ask again for a style the interview already settled
- feat(goal): show the preview, milestones and verdict in Simple view
- feat(milestones): show a walkthrough as same-size tiles and go through it in a window
- feat(budget): count a goal's time while Foundry works on it, Clarify included
- fix(clarify): keep the planner's task keys unique and its dependencies real
- fix(server): answer only to this computer's names, and keep other sites off the live feed
- fix(ui): wrap a card's actions below its title before squeezing them
- chore(interview): drop a doc comment left without its function
- fix(settings): follow the code-server install until it is done
- fix(checks): say when a check's whole output fails to load
- fix(milestones): show every milestone's walkthrough however long the goal ran
- fix(ui): keep a dropdown reachable by keyboard and inside the window
- fix(diff): read a cut, binary or empty file right in the diff viewer
- fix(brief): keep milestones through Revise and scope 'no tasks' to Clarify
- fix(clarify): give the planner the rules for cutting a plan, not the Clarifier's
- fix(clarify): keep the goal's interview depth through Re-clarify
- fix(clarify): start the shown Clarify step afresh with each session
- fix(clarify): ask for what is missing, plan a repaired skeleton, and stop after a kill
- fix(tailnet): take down serves a crashed run left on the tailnet
- fix(server): refuse changes another website makes the browser send
- fix(server): open a resolve worktree only for a task of the goal
- fix(editor): put VS Code in the browser behind a password and keep workspace trust
- fix(sessions): book a resume the CLI did not restore at its own cost
- docs(guide): retake the screenshots
- feat(open): open a repository or a goal's folder in VS Code in the browser
- fix(web): drop the four-round limit from the interview card
- feat(web): show which Clarify step runs and for how long
- fix(clarify): give the turn that writes the Brief time to finish
- perf(clarify): write the task plan once, in a planner session of its own
- fix(clarify): stop the Brief schema tripping the model into rewriting the Brief
- perf(clarify): load no MCP servers into Clarify sessions
- fix(sessions): book a resumed session for what the run added
- docs(self-check): say what the self-check costs and how it differs from Have a look
- feat(web): list a goal's milestones with their recordings on the Overview
- feat(web): show a changed file's diff in a window, highlighted
- feat(web): open an acceptance check in a window, with every run
- fix(web): keep dropdown menus inside the window
- fix(web): keep the task panel's close button in its top-right corner
- docs(guide): retake the screenshots
- chore(demo): plan a milestone walkthrough in the seeded demo
- fix(milestones): say in words why no walkthrough was planned
- docs(context): say where a notification's links point now
- feat(clarify): choose how deep the interview goes, from 1 to 5
- docs(guide): name the Have a look switch in the Acceptance card's description
- feat(web): show the goal review's verdict right under the goal
- feat(notify): send clickable links, on this computer and on the tailnet
- feat(milestones): record a walkthrough of the preview and send it with the milestone
- feat(milestones): make Have a look a setting, per goal
- fix(sessions): keep image tools' output folder out of goals that make no images
- fix(context): build no graph for repositories without code
- fix(completion): keep gitnexus guidance out of goal folders and task commits
- fix(docs): write a goal's docs when it is accepted as-is, and after its folder is gone
- feat(preview): keep an app's usual port and point env addresses at the port it got
- feat(preview): run a finished goal's preview in the person's checkout when it fits
- fix(preview): stop pnpm handing a literal -- to the dev server

## 1.0.1 — 2026-10-06

- docs: describe the guided install and sharing the host's Docker (ADR-0024)
- feat(install): one installer for source and Docker that starts Foundry
- fix(docker): keep the updater sidecar running on Docker 29, and let the port be chosen
- feat(fs): start the folder picker at the shared projects folder in the image
- feat(preview): start a preview's services on the host's Docker from the image
- fix(web): say why Create is disabled on the New goal form, whatever the reason
- fix(engine): set CLAUDE_CONFIG_DIR only for a non-default home

## 1.0.0 — 2026-10-05

- docs: describe Workspace & preview, the Brief line on the Overview and the Brief's section list
- feat(web): list the Brief's sections beside it, each with its state
- feat(web): show the Brief as one line under the timeline
- feat(web): merge the progress folder card into the preview as Workspace & preview
- feat(web): describe the preview's branch under its menu
- docs: describe the preview branch menu, the environment dialog and the reworked Overview cards
- feat(web): edit the preview environment in a dialog with a note per variable
- feat(web): pick the branch a finished goal's preview runs
- feat(web): move the self-check switch to the Acceptance card
- feat(web): show each completion action as a row with its details and Re-run
- feat(web): group project skills by what they cover
- feat(web): put the Simple | Expert switch in the goal header
- feat(engine): preview another branch of a finished goal
- feat(engine): explain each preview environment variable
- feat(engine): re-run a completion action that failed
- feat(core): record the branch a finished goal's preview runs and the docs commit
- docs(adr): note that stacked branches are reconciled with the remote before a replay
- fix(engine): reconcile a stacked branch with its remote copy before syncing it
- docs: describe resumable stacked delivery (ADR-0023) and the new Delivery tab controls
- feat(web): edit delivery settings any time and label each PR
- feat(engine): save, resume and start over a delivery
- fix(engine): call the local base up to date once it holds the last merged PR
- feat(engine): resume a stacked delivery instead of rebuilding it
- feat(core): record saved policies, branch syncs and deleted branches per delivery PR
- docs: refresh Goals and Usage screenshots for paging and the grouped breakdowns
- docs(guide): describe the shared Models panel layout for Codex
- feat(web): give the Codex Models panel the same layout as the other agent
- refactor(web): extract the Models panel's preset building blocks
- feat(web): choose how many goals a page shows, and always see the count
- feat(web): show all three usage breakdowns at once as grouped rows
- feat(web): compare usage by time and tokens, with cost for the agent that has it
- feat(usage): report time and tokens for every usage breakdown
- fix(web): keep the shared usage numbers still when switching coding agents
- feat(skills): uninstall shared Codex skills without touching the Anthropic CLI's
- fix(skills): stop reporting another tool's skill as a stale copy
- fix(preview): keep a preview the person started on a finished goal
- docs: record why the preview environment stays outside the goal's folder
- feat(web): preview card shows where it runs, what it serves, failures and its environment
- feat(preview): show what a preview serves and why it failed, and give it its environment
- feat(preview): keep per-repository preview variables outside the repository
- feat(preview): find the ports a start command's processes listen on
- docs: refresh guide screenshots for the header logo
- docs: show the Foundry logo at the top of both READMEs
- feat(web): add the Foundry logo as favicon and header mark
- docs: point readers to the changelog for what a release contains
- feat: one-line install for macOS and Linux
- build(docker): enable corepack for pnpm and yarn repositories
- feat(preview): install missing dependencies before apps start
- feat(setup): install a coding agent's CLI from Setup without npm
- docs: record several-app previews and their services
- feat(web): show each preview app and its services
- feat(preview): run every app of a goal side by side
- feat(preview): bring up the compose services the apps need
- feat(preview): detect workspace apps and compose dependency services
- feat(core): let a Brief list several apps to preview
- docs: refresh Goals and Usage screenshots for the stacked layouts
- feat(web): show Foundry activity for both coding agents together
- fix(usage): stop showing a usage-window signal after its window reset
- feat(web): stack Goals rows and page the list
- feat(web): stack Agents rows and mark each coding agent
- feat(agents): name each Foundry session's task and attempt
- docs: refresh guide screenshots for the Open full icon and attachments placement
- feat(web): open goal and Brief text in full with one icon button
- feat(web): show a goal's attachments right under its description
- docs: refresh guide screenshots for the coding agent label and goal badges
- fix(web): explain the usage-window rate-limit signal in plain words
- feat(web): show each goal's coding agent in the list and header
- feat(web): group Foundry agent sessions by goal
- refactor: rename Agent backend to Coding agent
- docs: refresh shared workflow guides and demo screenshots
- feat(web): unify account, usage and session views
- fix(agents): recognize native client-name version handshakes
- fix(skills): select native recipes and remove obsolete workflow dependency
- fix(auth): refresh native CLI discovery for account actions
- docs: align guides with native backend support
- test(plugins): wait for native process readiness
- fix(engine): honor native skill and repository instructions
- fix(usage): report pauses for each backend
- fix(web): unify backend selectors and dropdown spacing
- docs: capture the complete desktop recovery view
- docs: document provider recovery and native shutdown guarantees
- fix(web): scope recovery actions to the goal backend
- fix(runtime): reap native descendants and retain denied tool names
- fix(models): preserve explicit overrides in follow-up goals
- fix(auth): discard stale account status after sign-in changes
- fix(usage): derive quota windows from the signed-in account
- docs: explain native plugins and account command ownership
- fix(cli): honor provider scope and server-owned accounts
- feat(extensions): manage native plugins through the host cli
- docs: document provider extensions and native account status
- fix(cli): preserve follow-up presets and default reasoning
- feat(web): expose provider setup quota and captured models
- feat(engine): isolate provider services and native session history
- feat(engine): add native account quota and mcp adapters
- docs: explain captured presets and model compatibility
- feat(web): expose independent presets and model controls
- feat(engine): add per-role presets and native model discovery
- test(skills): keep update fixtures independent of network
- docs: explain multi-provider accounts and integration limits
- feat(web): add independent accounts and provider-aware goal controls
- feat(engine): route goals through isolated agent providers
- docs(install): document and package the optional codex backend
- feat(web): adapt authentication settings and usage for the selected backend
- feat(engine): select agent backend with isolated data and native authentication
- feat(runner): add native codex execution with guarded tools and session recovery

## 0.7.2 — 2026-09-29

- feat(web): full-height task panel with columns that scroll separately
- fix(web): center dialogs on small screens instead of pinning them to the bottom

## 0.7.1 — 2026-09-29

- docs(guide): a finished task's files come from its commit
- feat(web): open a task's files wherever they now live
- fix(server): a finished task's files are read from its commit
- docs(readme): each How it works step opens its guide page
- docs(guide): the ⚙ menu, task difficulty and openable files
- feat(web): Settings, Setup, Help and the theme move to one menu
- fix(web): the preset name and description line up
- feat(web): task cards show their difficulty and model
- feat(web): a task's spec opens full and its relevant files open
- feat(web): code in the file preview is coloured by language
- feat(server): more source files open as code in the preview
- docs(guide): a task's files, the JSON tree and the file preview
- chore(demo): tasks log absolute paths and one makes an image
- feat(web): a task shows the files it made
- feat(web): JSON in the live log reads as a searchable tree, and file paths open
- feat(server): a merged task's file paths still open
- fix(web): the goal page stays in view behind an open task
- feat(server): serve a goal's files by path, and list the files a task made
- docs(guide): a screenshot for every tab of the goal page
- chore(demo): seed goals whose every tab has real work to show

## 0.7.0 — 2026-09-28

- **MCP servers.** A new MCP servers tab (Extensions page) lists every MCP server Claude Code loads for your account: yours, those plugins bring, and claude.ai connectors. Install Foundry's recommendations (Context7, Playwright; Exa or Brave Search for web search) or your own, change a server's key, remove one, and run a health check. Connect claude.ai connectors (Gmail, Google Drive…) and sign in to servers that need an account, with the terminal command as a fallback.
- **Allowed in goals.** Goals now use only the MCP servers you allow, and only in the sessions that do the work. A refused server can be allowed from its Inbox item with one click.
- **The Skills page is now Extensions**, with Skills and MCP servers tabs.
- **More keys.** MiniMax, ElevenLabs and Groq keys in Settings → Tools & keys reach sessions (MiniMax through mmx). A skill that lacks its key says so where you pick it, and what it loses without it.
- **MiniMax quota** on the Usage page, with an amber dot in the header when it runs low.
- **Keys stay put.** Saved keys and tokens are no longer sent back to the browser, and settings.json is readable by its owner only.
- **Agents page.** A session's log shows one line per entry; click one to read it in full.
- **Sign-in** uses a Pro or Max subscription only.
- **Fixes:** the sign-in, update and restart dialogs were cut off or hidden; stray scrollbars on tab rows; "ago ago" on the Agents page; the header now fits phones; the escalation card keeps its state across screens.
- **Docs:** the README shows the product in pictures, and each docs folder opens on GitHub.

## 0.6.1 — 2026-09-26

- **Command-line tools no longer stuck at PARTIAL.** ffmpeg, mmx and autoskills count as installed as soon as their command is found (only tools that also ship a skill need both), so their rules and hints reach sessions again — as a command-line tool to run, not a skill to invoke.
- **Honest plugin updates.** When a plugin's author changes files without raising its version number, the Skills page now says *unreleased changes* and explains why, instead of an *update available* that the Update button could never clear. Plugin skills show the exact commit they were installed from, a difference only in a README or changelog is no longer an update, and a plugin can be removed as a whole with **Uninstall plugin**.
- **Adopt that works — or says why not.** Adopt is only offered when Foundry can install the skill itself, and a failed adopt reports the reason instead of a false "adopted". gpt-image-2 and kb-retriever now install from their repository.
- **An Operations bar on the Skills page.** Every install, update, adopt or uninstall gets its own tab with its own full-size log; several can run at once, finished ones stay until you close them, and the logs survive a page reload.

## 0.6.0 — 2026-09-26

- **Commits are yours.** Settings → Git & delivery → *Commit author* decides who Foundry's commits are written by: **you, with Foundry as co-author** (default — your git identity, from the project's or your global git config or your GitHub account, plus a `Co-authored-by: Foundry` line), **you only**, or **Foundry only**. Deploy integrations that only accept commits from members of their team (Vercel teams, for one) no longer block Foundry's pull requests. Applies to commits made from now on.
- **A stopped delivery says why.** Each pull request lists the checks failing on it with their own description (for example "Deployment was blocked") and a link, and a *Delivery stopped* item appears in the Inbox with the same reason. A failing check Foundry has no CI log for is no longer handed to a fix task that can only fail, and a fix that changes nothing no longer pushes the same commit again.
- **…and can be finished.** **Retry delivery** continues from the first pull request that is not merged, with a fresh budget for fixing CI; **Re-check** reads one pull request again and carries on when it passes; **Mark as delivered** finishes a delivery you completed yourself. A pull request you merge by hand after a failure is now noticed and finishes the delivery.
- **Read any long message in full.** Every live-log entry is one line; click it for the whole message, read back from the session's transcript, with Markdown preview, raw view and copy. The session's final message now shows too. Shortened rows in the Activity tab, a task's commit message and long Inbox reports open the same way, and Inbox reports are no longer cut when they are raised.

## 0.5.0 — 2026-09-25

- **Merged work reaches your own checkout.** When a goal's pull request merges, Foundry fetches and fast-forwards your local base branch — only when that is safe (no uncommitted changes, no commits of your own on it) — and then removes the goal's progress folder, worktrees and local branches; screenshots and the goal's history stay. If anything could be lost, nothing is removed and the goal page says why, with **Pull into my checkout** and **Clean up anyway**. Settings → Git & delivery → *Update my local base branch after a merge* (on by default) turns it off.
- **Late merges are noticed.** A PR that auto-merges after Foundry stopped waiting, or one you merge yourself on GitHub, is picked up within a few minutes (and whenever you open the goal); a PR closed without merging is shown as such. Delivered goals show three lines: merged on GitHub, your local branch up to date, workspace cleaned up.
- **Follow-up goals.** *Continue with a follow-up…* on any finished goal opens a New goal form prefilled from it; the new goal's Clarify gets the earlier goal's understanding, decisions, task outcomes and review as background, and it starts from the base branch when the earlier work is merged, otherwise from the earlier goal's branch. Attachments and the chosen style direction come along (each can be unticked). The Goals list shows "↳ follows …", both goal pages link to each other, *Mark as follow-up of…* links existing goals, and the CLI takes `goal new --follows <id>`.

## 0.4.2 — 2026-09-25

- **Docker: previews and the self-check work.** Dev servers in the container now listen on every interface, so a milestone preview opens from your computer (the compose file publishes ports 4200–4299 on 127.0.0.1). Chromium's system libraries are in the image, so the self-check can launch; the browser downloads once into a `playwright-browsers` volume and survives updates. Stopping a preview stops the dev server itself, and the container runs with an init process. Re-create the container with the new compose file to get the ports and the volume.
- **Chromium matches Foundry's Playwright.** *Install Chromium* uses the Playwright version Foundry ships instead of the newest one, so the self-check keeps working after Playwright releases.
- **Self-check from the Brief.** The Brief's *How to run it* section has the goal's self-check switch, so the first tasks can be checked too.
- **Top bar fits every screen** from phones to wide monitors; the e-mail address shows only where there is room.
- **Clearer goal pages.** The interview names earlier questions by number and says what happened to unanswered ones; the work-in-progress card says what the goal's delivery setting will do; *Deliver…* in the Simple view opens the Delivery tab; task graph cards show each task's total cost.
- Fixes: the final review's live log belongs to its goal and, like the Brief's Draft log, survives a page refresh; a resumed release pushes a changelog an earlier failed run left behind.

## 0.4.1 — 2026-09-24

- **User guide, in English and 中文, inside Foundry.** A **Help** link in the top bar opens ten plain-language pages — your first goal, the interview, the Brief, while it runs, when Foundry needs you, getting the result, every Settings section, costs and a FAQ — with an EN / 中文 toggle. Small **?** icons on the New goal form, the Brief, the interview, milestones, the Inbox, Settings and Usage open the matching section in a new tab.
- **Documentation reorganised by reader:** `docs/guide` for people using the web UI, `docs/operate` for installing, updating, remote access, notifications and troubleshooting (with configuration and CLI references generated from the code), `docs/develop` for contributors (architecture, roles, testing, releasing, ADRs). Everything was checked claim by claim against the code.
- **New goal form.** Effort, Models and TDD are button groups — every option visible, one click. The form now starts from Settings → New goal defaults (view, fast mode, TDD, delivery mode) instead of the browser's last choice; the Default models button names the preset it will use.
- **CLI.** `goal new` takes `--models <preset>` (an unknown preset is refused with the valid ids), `--nature`, `--pace`, `--interview`, `--effort` and `--self-check`. The retired Strong / Worker tier settings and `FOUNDRY_MODEL_STRONG`, `FOUNDRY_MODEL_WORKER`, `FOUNDRY_GOAL_REVIEWER` are gone; a line in the log says so if one is still set.
- Fixes: the Clarifier's task difficulty was dropped when the Brief was built or revised; changing only the housekeeping model no longer triggers the old-tier migration; the goal Overview shows the model preset; the Delete goal dialog, the Models note and the TDD hint now say what the engine actually does.

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
