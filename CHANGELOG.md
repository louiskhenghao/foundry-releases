# Foundry releases

## 2.15.0 — 2026-10-25

Adjust the result (beta): a finished goal's page takes your words on its result — what should change, with pictures or files — and the goal carries them out itself: the session that did the work picks up where it left off (a goal of one task), or a task is added after the finished ones, or a failed goal's failed tasks run again with your words. The adjustment lands as a commit of its own, so a pushed branch is never rewritten; the checks and reviews run again; the output folder and an open pull request get the new result; the result as it was is kept under artifacts/.history and listed under each adjustment. A merged goal is not adjusted (start a follow-up). Switch it on under Settings → Beta → Adjust the result (ADR-0078).

## 2.14.0 — 2026-10-25

- docs(adr): the motion-studio record is ADR-0077 (0076 went to figure goals on main)
- fix(review): scores a reviewer wrote in its notes count
- fix(checks): a command check gets the engine's Playwright like a session does
- fix(server): the Beta filter of the skills overview tolerates a manager that returns no catalog
- docs(guide): the Motion studio page tells how a film is made
- feat(engine): the motion-studio engine on a video goal
- feat(skills): the motion-studio skill, bundled with Foundry
- feat(review): a verdict carries scores on the rubric's axes
- feat(web): a clip in the artifacts strip plays in place, with its poster
- feat(attachments): audio and video up to 200 MB, and files the browser can seek in
- docs(adr): ADR-0076, the motion-studio video engine
- build(docker): ffmpeg in the image
- feat(doctor): ffmpeg and Chromium for the motion-studio engine
- feat(skills): a catalog entry can be bundled with Foundry
- feat(engine): sessions learn where the engine's Playwright lives
- feat(engine): a video goal carries its own engine and its own session cap
- feat(settings): beta.motionStudio, the switch for the motion-studio video engine
- fix(skills): an install moves a shared cache to the pinned commit
- feat(catalog): Hyperframes pack on the Herk Edit Kit at 10511e5
- feat(skills): a catalog git source can pin a commit id

## 2.13.0 — 2026-10-24

Figure goals (beta): a kind of goal of its own for interactive isometric figures of everyday objects and machines, one self-contained HTML page each, drawn by the new Figure pack — April Zhu's Colorfigures (hand-inked colour, working buttons, a see-through) or iso-glow (dark glowing line art), both bundled with Foundry as snapshots of their author's archives and installed by copying. The page is committed in the repository (figures/<name>.html, its source beside it); Foundry opens every delivered page headless when a task lands, fails the task on script errors, screenshots it for the Have a look card and the task drawer, and shows pages in a sandboxed frame that can never act as Foundry. A goal may pick the other installed style; figure sessions get at least 45 minutes; the doctor checks Chromium, python3 and a Chrome; the Docker image gains python3 and a google-chrome shim. Switch it on under Settings → Beta → Figure goals (ADR-0076).

## 2.12.0 — 2026-10-24

- **The Explainer proposes, the person applies.** Ask the Conversation for a change — add a task, fix this, from now on do that, here are the files for the request, open a follow-up — and the answer ends with a card: Add the task, Record the decision, Add the note, Open the New goal form, or Hand it over. Nothing changes before the press; applying is recorded once, with who and what came of it. (Conversation beta, ADR-0075)
- A proposed task lands after the tasks it names, with the goal's must commands and its own checks; a decision goes on the Brief and into the hint of every task not yet started; a note goes on a Brief awaiting approval; a follow-up opens the New goal form prefilled; a hand-over gives files from the Conversation to an open Request or a promised material — the goal gets copies of its own, marked with the Request.
- The Explainer's records gain `materials.md` (promised materials with keys, open Requests with ids) and the ids of the files attached to a question. `foundry ask` lists what was proposed, with ids, and keeps the proposal block itself off the terminal.
- Fixed: a Request answered with files that could not be taken in was recorded as answered with nothing done; now the files come first and a Request that cannot take them stays open.
- Fixed: a question's uploads stayed registered as staged after they were claimed.
- Fixed: words in angle brackets in Markdown (`<p>`, `<title>`) were dropped on the page; they are shown as written now, with HTML comments still hidden.

## 2.11.0 — 2026-10-24

A goal can ask for what only you can give. A worker that cannot finish without a private asset, a key or a decision that is yours stops and asks: an Inbox item says what, why and where to get it, and takes your words, files and links — the same session then goes on with them (or without, if you say there is none). Materials you promise during Clarify are listed on the Brief under You will provide, each with the tasks that need it and a choice: wait for it (Foundry asks when a task is ready) or build with a placeholder first and swap it in when it arrives; hand things over on the Brief page or the goal page whenever you have them. An attachment you add while the goal runs is announced to the tasks not yet started.

## 2.10.2 — 2026-10-24

Conversation (beta): a question can carry pictures and files (the clip in the box, a paste, or a drop; up to eight), which the Explainer opens; the composer is one box with the files, the words and the send button; the window sits above the bubble instead of over it; New Conversation only becomes a row of the list once its first question is sent.

## 2.10.1 — 2026-10-24

Conversation (beta) polish: on the Conversation tab the thread reads as a column in the middle of the card, an empty Conversation offers three questions to start from, the composer grows with what you type, the list has a New Conversation row and the thread is titled by its first question in normal case.

## 2.10.0 — 2026-10-23

Conversation (beta): a bubble on the goal page and the Brief page opens a Conversation with the goal's Explainer, a read-only session of the goal's coding agent that answers your questions about the goal's code and Foundry's records of it (why a task was done that way, where something lives, what went wrong), on the preset's new Conversation row; it never changes anything, and when asked to it points the way and drafts the words. Answers stream, Stop keeps what was said, and questions queue. A Conversation tab (Expert view) lists every Conversation of a goal; from the terminal, foundry ask <goalId> "question". Its cost counts in the goal's total but not against the Budget. Switch it on under Settings → Beta.

## 2.9.1 — 2026-10-23

- feat(install): Memory's Hindsight can run on your Codex sign-in — with `--with hindsight`, answer `openai-codex` as the provider (no key) and the installer signs the server in by device code, into a folder of its own beside the compose file; the Hindsight card and the guide say so.

## 2.9.0 — 2026-10-23

- feat(memory): Memory — an optional Hindsight server you run keeps everything a folder's goals did, decided, were refused and wrote, and answers each stage of a goal before it starts (Clarify and the planner, every attempt, a replan, the task and goal reviews) under "What Memory recalls", beside the folder's Learnings. Set up on Extensions → MCP servers (the Memory · Hindsight card) or with the Docker installer's --with hindsight; one bank per repository (coding-agent::<folder>), shared with your own Claude Code or Codex sessions there and given the five knowledge pages Hindsight's own integration keeps, plus a bank of your own decisions across folders. The server can run on the Claude Code or Codex sign-in you already have: the wait for its answer is a setting, and the memories themselves stand in when the answer is late (ADR-0072).
- fix(roles): a role's answer is not refused for a field its schema does not name (ADR-0071).
- fix(web): a long commit subject stays inside the repository card; a check's result and a goal's state are each said in one set of words; expand all and collapse all reach every fold of the Goals list.

## 2.8.0 — 2026-10-23

- perf(web): ask the goals before the doctor, load pages at once
- perf(engine): concurrent doctor runs share one run
- perf(skills): the doctor reads a skill's bytes once
- feat(install): update a coding agent's CLI that has a newer release
- feat(install): choose Antigravity as a coding agent

## 2.7.0 — 2026-10-22

- feat(skills): a workflow suite (Matt Pocock's skills, pstack) can move to a later release from the Extensions page, and back to the pin. A forecast comes first: which skills that release removes, deprecates and adds, the ones Foundry's workflow uses on top (ADR-0068).
- fix(skills): a skill folder that links into another folder (another tool's install, your own clone) is listed under Linked from another folder and left to where it links: no Adopt, never a stale copy of a plugin skill that shares its name, and installing a bundle keeps it (ADR-0069).
- feat(web): empty and loading look designed. An empty page, tab or list shows a placard with its kind's icon, how something comes to be there and the action that puts it there; a page that loads shows the same placard with a spinner and what it is loading.
- feat(web): a goal's tabs stay at the top while a tab scrolls, and every tab is at least a screen tall, so switching to a short one never moves the page.
- feat(web): the Brief's section menu starts with Back to goal (on a phone, a Goal chip pinned at the start of the row).
- feat(web): every group on the Extensions pages starts closed; a search or a filter opens every group with a match, and a closed group says when a source in it has an update.
- fix(web): the time ruler's estimate stands on a row of its own instead of running into the limit's label, and the Agents count sits filled on its link's corner instead of pushing Extensions aside.
- upgrade: no migration.

## 2.6.0 — 2026-10-22

- feat(web): a new look, Wayfinding: Foundry read as a sign system. Every page is rebuilt on one kit: large page titles, a goal's five stages as plates, the Goals page as Needs you signs over Working and Finished boards, Budget & time on a goal's Overview, and a menu of sections beside the Brief, New goal and Settings.
- feat(web): themes. Settings → Appearance picks a theme and light or dark, for each browser: Wayfinding (the default), Ledger (paper and ink, serif titles, a column down the left) or Classic (the look Foundry had before themes). A theme sets the layout as well as the colours: where the navigation sits, how titles, stages, labels and signs look, raised or flat cards.
- feat: themes of your own. Make a copy writes a theme as a JSON file in the data folder's themes/, Open in your editor opens it, and the page shows each saved change at once; a theme of your own can be renamed, exported or deleted, and a theme file imported. A file with a mistake is listed with what to fix, and the theme keeps its last good look.
- feat(web): colour says one thing each: yellow only for what waits for you; how something stands in its signal colour on its small mark (done green, at work blue, in review violet, failed red); things of a kind (the Brief's sections, Areas, extension sources) in eight category colours.
- fix(web): phones. The stages, the section menus (a row of chips), the Brief's actions (docked at the foot of the screen), dialogs and the sign-in steps fit a phone's width, and the app no longer scrolls past the end of a page.
- upgrade: no migration. The theme is chosen per browser, and Classic keeps the old look.

## 2.5.2 — 2026-10-22

- fix: Netlify deploys stay on one site. The deploy folder's clean-up deleted Netlify's link to its site wherever the project does not ignore .netlify (Netlify's CLI does not add it to .gitignore), and Netlify then made a new site, <name>-<suffix>, with a new address on every deploy after the first. The hosts' links now stay between deploys.
- upgrade: no migration. A Netlify site duplicated this way before 2.5.2 stays in your Netlify account; delete it there.

## 2.5.1 — 2026-10-22

- fix: Netlify — a team slug the token cannot reach (Netlify answers it with a bare "Failed to create site: 404") is named in the failure, with where to set it; npm's own warnings and the CLIs' colours no longer hide a host's error. Settings says the Netlify and Vercel team fields take the team's slug, not its name.
- fix: Cloudflare Pages — a new project stays on Pages. Wrangler 4 had started handing new projects to Workers, which rewrote the app's files and failed without a Workers permission; what that hand-over left behind no longer breaks later deploys, and a production deploy records the project's own pages.dev address.
- fix: Vercel — a new project's first deploy, which Vercel always puts in production, is recorded as production with a note, and a smoke asked for the preview is not run on it.
- fix: the smoke no longer runs its scripts against an address behind the host's login (Vercel protects previews by default; a Netlify team can let only its members in); it says which setting asks for the login.
- feat: what a deploy adds to the project (Vercel's .gitignore line, for example) goes to GitHub the way the goal did: onto the goal's branch while its pull request is open, else in a small pull request of its own. The hosts' own folders (.vercel, .netlify, .wrangler) are added to .gitignore and never committed; a Local only goal keeps nothing.
- feat(web): the Deploy card starts on the host the goal last deployed to.
- upgrade: no migration.

## 2.5.0 — 2026-10-22

- docs: the Usage page per account, in the guide and ADR-0065
- feat(web): the Usage page lists each account's windows or quota
- feat(engine): the usage summary follows the current account and lists every account
- feat(core): each account's own rate-limit windows are kept
- feat(web): the Accounts page leads with each coding agent, and signing in shows its steps
- docs(guide): several accounts, Switch and continue, and the log lines they add
- docs(adr): ADR-0065, several accounts per coding agent, and the glossary's Account words
- fix(engine): an added account never signs in with the machine's OAuth token
- feat(web): the Accounts page holds several accounts per coding agent
- feat(notify): a usage pause offers Switch and continue from the chat, and an automatic switch is told
- feat(server): routes for a coding agent's accounts, and Switch and continue
- feat(engine): sessions run on the coding agent's current account, and a usage limit can move them to the next
- feat(runner): a session can run in an added account's home
- feat(core): a coding agent's accounts and the one its sessions run on
- feat(engine): a session that cannot be resumed hands its work to a new one
- fix(engine): a session a usage limit stops resumes instead of costing an attempt
- fix(engine): every coding agent's usage-limit stop pauses its sessions
- Not yet tested on real accounts: resuming a session on another account. When the coding agent refuses, a new session takes over with a handoff (tested).

## 2.4.1 — 2026-10-22

- feat(web): the ⚙ menu now puts each page's name on the first line and what it is for on a smaller second line (Transfer, Ports, Learnings, Schedules, Reports, Help). Before, both were in one label that wrapped unevenly. The guide names Transfer and Ports as the menu shows them.

## 2.4.0 — 2026-10-22

- feat: the Antigravity CLI as a third coding agent. You choose it per goal on New goal, and it has its own account, model and effort. The Usage page shows its weekly quota per model group, its skills are linked into each workspace, and its model carries over to follow-ups, delegated parts and scheduled runs. It reports no dollar figures, and Foundry manages no plugins or MCP servers for it (ADR-0064). It needs agy 1.1.15 or newer on a local install; the Docker image does not ship it.
- feat: the Goals list folds a goal and its follow-ups into one entry. The entry opens by itself while one of them is under way, and expand all / collapse all open or close every group.
- feat: Open source credits, a page reached from Settings → About & updates. It credits the projects Foundry is built on and gives the license notices of everything the image ships. The image also carries the notices in /app/THIRD-PARTY-NOTICES.txt.
- upgrade: no migration.
- not yet checked against the real service: what agy reports when a model group's quota runs out. Until then, a session that hits it fails and is retried instead of pausing Antigravity.

## 2.3.0 — 2026-10-21

- feat: a goal from a GitHub issue — the New goal form reads the issue into the goal, and the goal's pull request closes it (ADR-0052)
- feat: review comments on a goal's pull request are picked up by the delivery and addressed in a fix task, with a reply under each, within the policy's review rounds (ADR-0053)
- feat: Schedules — a goal recipe that runs daily, weekly or monthly on its own; its Brief can be approved by the engine, a blocking question still waits for you (ADR-0054)
- feat: an everywhere notebook — Learnings of your own that go with you into every folder's goals and their exported skill (ADR-0055)
- feat: the Brief's estimate is read with how far earlier goals ran from theirs (ADR-0056)
- feat: browser QA — the finished app tried in Chromium against the acceptance checks before the final review; a failed must check becomes a fix task (ADR-0057)
- feat: smoke after a deploy — the goal's milestone scripts run against the deployed address (ADR-0058)
- feat: Revert — a merged goal undone through a pull request from its page (ADR-0059)
- feat: Reports — what Foundry cost and did over a window, by project and session kind, on a page of its own and in the CLI (ADR-0060)
- feat: Access — a token per person for a shared Foundry, and who created a goal, approved its Brief and answered (ADR-0061)
- feat: companion repositories — a goal that also changes other folders; each part is done by a delegated goal in its own repository and delivered with the goal (ADR-0063)
- dev: a role-prompt regression set — fixed small goals run against the real coding agent, judged and compared with a baseline (ADR-0062)
- fix: goals created before this release no longer crash their page or the pull-request watch, and a background check that fails is logged instead of ending the server
- fix: stopping the engine closes its database, so test runs on macOS no longer die with exit 137; work still in flight then reads and writes an in-memory copy
- fix: install.sh updates an older Bun, and a skipped sign-in question no longer ends the installer
- upgrade: Bun 1.4 or newer — Bun 1.3 can end a browser Foundry opened for a self-check or a walkthrough (oven-sh/bun#33828). The image ships Bun 1.4.3, install.sh updates Bun, and Doctor warns below 1.4.
- upgrade: migration 0008 adds the schedules table; the engine applies it on first start. Back up the data folder first: going back to 2.2 needs that backup, since 2.2 does not read the new events.
- not yet checked against the real services (covered by tests with fakes): issues, review comments and revert pull requests on a live GitHub repository; smoke against a live Vercel, Netlify or Cloudflare Pages deploy; browser QA with a real session. The regression set has not been run against a real agent yet.

## 2.2.1 — 2026-10-20

The second opinion on the Brief has the room of a goal review (60 turns, a worker session's budget never under $6, twenty minutes, one nudge for the answer) and is written in the background: the Brief page follows it through the goal detail, a reload or another tab finds it, and one that could not finish says why until the next comes in. The server's idle timeout is Bun's maximum. Also since v2.2.0: the Extensions page marks the installed skills no session invoked over the last goals (an unused chip, an "unused only" filter, a note under the Skills heading; GET /api/skills carries the usage), and the New goal form prefills its workflow suite, TDD and Ponytail from the newest goal in the same folder.

## 2.2.0 — 2026-10-20

- Workflow suites: a goal fixes whose skills its roles follow — mattpocock (default), pstack or plain — on the New goal form (Powered by), with a Settings default; follow-ups start from the earlier goal's choice, delegated goals take their main goal's; every prompt names the suite (ADR-0049)
- pstack as a suite: Foundry keeps one pinned release (v0.9.93) as its own hook-less copy and loads it per session; a bug task starts from pstack's tdd, feature and refactor tasks get deslop and blast-radius, the final review runs thermo-nuclear-review (thermos for a large branch), the merger fix-merge-conflicts, the documenter technical-writing; one Setup card installs it, the Extensions page shows it as one source with Re-sync, Codex goals get its skills linked into the workspace
- Learnings shared with your own sessions: each folder's Learnings are written into the repository as the project skill foundry-learnings (kept out of git, rewritten whenever they change); on the pstack suite the Learnings session reflects with reflect's lenses (ADR-0050)
- A second opinion on the Brief: a reviewer that did not write it reads it against the repository, on the goal reviewer's model, and proposes what to change as a checklist on the Brief page — on demand, or on every Brief with the new Settings switch (ADR-0051)
- gstack is no longer known to Foundry: no catalog entry, no provenance family, no special cases (ADR-0048)
- Extensions page: catalog entry details open in a window, side panels pin only when they fit, the Agents badge sits on the link's corner, the pr skill joins the catalog

## 2.1.0 — 2026-10-20

- Notes: a note from you is a Decision whether the interview asked for it or not — add one in the interview or on the Brief page; Revise and Re-run honour it (ADR-0044)
- Revise can ask you back before it proposes; a proposal is a review checklist with word-level before/after and one Apply button; every Brief section has its own colour (ADR-0045)
- Skeleton-first Brief: the page opens as soon as the understanding is in and fills in while the planner works; it can be edited during planning; Clarify shows its stage, queue position and per-step timings (ADR-0046)
- Interactive sessions (Clarify, planner, Revise) no longer queue behind work sessions at the concurrency limit; cancelling a goal kills its queued or running Clarify session
- Codex: a worker's next attempt is no longer told that every mandated skill was "not invoked"
- The mattpocock skills pinned to v1.3.1: writing-for-agents mandated by the files a task touches, the Learnings session opens with retro, and PR bodies follow the pr template — Summary, Decisions, Evidence, Merge Danger (ADR-0047)
- Extensions page: a catalog entry's details open in a window, side panels pin under the top bar only when they fit, the Agents badge sits on the link's corner, gstack's own retro is no longer mistaken for the mattpocock one, and the pr skill joins the catalog
- Migration 0007 adds the Brief skeleton column; the engine applies it on first start

## 2.0.1 — 2026-10-19

- feat: the Timeline reads like a Gantt chart — quiet stretches fold, the chart fits while it reads well and otherwise slides beside the fixed row names, with a rail showing the whole goal; a bar or a row's name opens its details, with Open task and Open delegated goal
- feat: a session cut before it reported its cost shows an estimate (≈) at its model's measured rate, never counted in a total or a budget; the cost meter puts cut sessions behind a dot
- feat: open pages reload themselves into a new version after an update, and a page with an unsaved edit asks first (pages left open from 2.0.0 need one reload by hand)
- feat: Learnings laid out like Agents and Extensions — a chip per kind with its count, search, folding folder cards; each learning added, changed or removed on its own, in a window
- fix: the Inbox is an icon button with its count, beside New goal
- fix: pictures and clips open in one lightbox — evidence four to a row, the arrows under a stage of one height, a swipe on a phone; a task's file preview steps the same way
- fix: on a phone, Open delegated goal sits in the delegated goal's box, and the timeline's rows and small buttons keep their height
- fix: on iOS, a dialog no longer focuses its first field, and a field no longer zooms the page
- upgrade: no database changes; going back to 2.0.0 needs no backup

## 2.0.0 — 2026-10-18

- feat: Deliverables and Replan — a task promises the files it makes, and the planner touches up the steps that follow a Delegated goal
- feat: Delegated goals run side by side within the goal's parallel limit, each with a share of the budget
- fix: a session cut before its result line is unmeasured — its turns and tokens are counted and its cost shows as unknown, not zero
- feat: Telegram takes answers — buttons and replies under the messages that wait for you, /inbox, and a Brief ready message
- feat: Discord takes answers through a bot beside the webhook, read over the gateway
- feat: Learnings — what a folder's goals taught, written when a goal ends and given to the next goals there
- feat: Deploy — a finished goal's web app to Vercel, Netlify or Cloudflare Pages, on your click; workers and backends are never deployed
- feat: Subjects — pictures of the real things a goal depicts, found while the Brief waits, that workers build from and reviews compare against, with a Likeness review of each milestone
- feat: a Timeline tab — where a goal's time went, with its delegated goals, on one time axis
- upgrade: the database is migrated when the new version starts (session cost status, learnings). Back up the data folder first: going back to 1.x needs that backup.
- not yet checked against the real services (covered by tests with fakes): Telegram and Discord answers, deploys to Vercel, Netlify and Cloudflare Pages, and the Subject picture search and Likeness review.

## 1.10.3 — 2026-10-18

- docs: record how unverified merge commits and re-deliveries are handled
- fix(delivery): the after-merge tidy-up keeps what a copy, a restart or a busy folder still needs
- fix(delivery): deliver artifacts again after a restart, replacing only the copies made there
- fix(engine): a manual resolution's checks and baseline read one copy of the goal's exports
- fix(engine): nothing builds on a merge attempt's commit that did not land

## 1.10.2 — 2026-10-18

- docs: record the CAD review follow-ups in ADR-0033, the architecture and the guide
- fix(web): say why evidence media cannot show, and list only the other artifacts
- fix(web): say that the CAD Viewer opens only on Foundry's computer
- fix(web): left-align Brief option buttons, with a fixed radius
- test(notify): pin that Discord's plain-links retry pings nobody either
- fix(transfer): leave behind only the clip copies an output folder received
- fix(engine): undo leftover overlays at start, run no goal before that, and bound stop()'s waits
- fix(delivery): hold the after-merge tidy-up only for files that exist nowhere else
- fix(delivery): treat a PR merged or closed on GitHub as such at every merge step
- fix(engine): land a task's exports with its commit and take back merge attempts that do not land
- fix(engine): skip merge baselines without must checks and key them by export contents
- fix(engine): keep newer exports and the goal's saved copies safe across landings, retries and overlays
- refactor: share the CAD Viewer key and the style-sample folder name
- fix(engine): copy artifacts safely and digest them as a stream
- fix(core): record settled landing failures, a delivery's start and a waiting tidy-up
- docs: ADR-0033 and the notifications guide describe the review follow-ups
- fix(merge): a squash that conflicts at integration is checked with the task's exports
- fix(checks): a baseline is keyed by what the exports hold, not their sizes and times
- fix(transfer): a finished goal leaves its milestones' clip copies behind
- perf(artifacts): artifact copies run off the event loop
- perf(preview): the CAD Viewer's model is not searched for on every status poll
- fix(delivery): cleanup after a merge keeps files that exist nowhere else
- fix(artifacts): files a landing missed are copied again before delivery
- fix(preview): the CAD Viewer is never put on the tailnet
- fix(web): a paused milestone of files does not list the goal's artifacts again
- fix(delivery): a conflict found while settling a merge is re-synced, not failed
- fix(notify): refused pictures go as files and Discord pings nobody

## 1.10.1 — 2026-10-17

- docs(adr): ADR-0033 records rename-over copies, recorded landing failures and stale resolution sessions
- fix(delivery): a PR closed during the merge settle fails as closed
- fix(engine): a baseline that cannot be measured leaves a note
- fix(engine): a manual resolution ignores untracked leftovers, starts over on the task's newer work, and refuses after a skip
- fix(engine): a landing records the files it could not copy, and the milestone says so
- fix(engine): an artifact copy replaces the file by rename, and a folder it cannot read counts as a failure
- docs(adr): ADR-0033 says which exports a manual resolution lands
- fix(engine): a manual resolution lands exports that match the code it kept, and a Finish whose commit already landed only finishes up
- docs(adr): ADR-0033 records landing, baseline and manual-resolution safety
- fix(delivery): the merge settle stops as soon as the PR is merged or closed
- fix(preview): a tailnet name a URL cannot hold no longer fails the preview status
- fix(notify): files reach Telegram with the content type of their format
- fix(engine): milestone copies are reused only when whole, large images are linked, and a task that changed nothing shows what its milestone names
- fix(engine): baselines run one at a time per goal, are keyed by their exports, and are strict when the exports cannot be copied
- fix(engine): a manual resolution keeps the person's work, and a Finish cut short is completed
- fix(engine): a landing skips tracked files and keeps the worktree when a copy fails; copies never write through a link
- docs(adr): ADR-0033 records landed artifacts, safer check-worktree copies and the viewer link that follows
- fix(prompts): a CAD decorator's out= is relative to the model script, and the CAD review and Clarifier rules are tested
- test(delivery): the merge settle proves its wait, its conflict and branch protection; a PR merged meanwhile is merged
- fix(web): the preview card names the CAD Viewer when it is the goal's only app
- fix(web): a milestone of files shows snapshots whole, says what the task produced, and links its files
- fix(notify): a milestone of files speaks of what the task produced, and a refused picture no longer drops the message
- fix(preview): the CAD Viewer's link follows the newest assembly and keeps its model on the tailnet
- fix(engine): a milestone of files shows the task's own files, each under its own copy
- fix(engine): the artifacts listing follows no symbolic link
- fix(engine): finishing a manual resolution anyway lands it, and a resolution without its merge starts over
- fix(engine): artifacts copied for checks skip what git tracks and never stop them; a merge is judged with its own exports
- fix(engine): a manually resolved task's exports reach the goal, and every landing records its files
- fix(server): a milestone's JPEG, WebP, GIF, MP4 and MOV copies are served
- fix(delivery): a merge refused as not mergeable right after a push waits for GitHub to settle
- fix(engine): a milestone of files shows first the images its text and manifest name
- fix(engine): the worktrees that run the goal's checks get its artifacts
- docs(adr): ADR-0033 records the export layout override, the viewer link and file milestones
- fix(cad): Foundry's export layout overrides the cad skill's, and nothing committed points into the plugin folder
- fix(engine): a milestone of files shows the files, and the CAD Viewer opens the goal's model

## 1.10.0 — 2026-10-16

## CAD goals with text-to-cad
- A new goal nature, **CAD**: 3D parts and assemblies (STEP always; STL, 3MF or GLB on request), engineering drawings, DXF cut profiles and URDF/SRDF/SDF robot files, made with text-to-cad's skills (build123d and OpenCASCADE through cadgen). Code model presets, the default view, TDD preferred, Ponytail on; the Clarifier asks about the manufacturing process and the key dimensions; one task per part with Python geometry checks; sources are committed, exports and front/top/right/isometric snapshots are delivered as artifacts; reviewers read the snapshots.
- **Setup → 3D models — text-to-cad (CAD)**: one card installs the plugin for the selected coding agent (a bundle of twelve skills and the `cad` viewer server), allows the server for sessions under the prefix the agent gives it, and downloads the CAD runtime once while you watch; the install runs in the background. A **CAD tools** check reports uv and the slicer or printer apps found. A CAD goal created before the install waits on its page with an install button.
- **CAD Viewer** (text-to-cad's own viewer) is a preview app of every CAD goal, started only by you.
- Every session runs cadgen with usage statistics and update checks off; your own use of text-to-cad keeps its settings.

## Settings → Safety → Desktop apps & printers
- Off by default: the boundary guard refuses commands that open desktop apps or hand files to printers (`open …`, `xdg-open`, `osascript`, `Start-Process`, the slicers' windows) and text-to-cad's Bambu hand-off skill; headless slicing, preflight reports and part lookups stay available. A refused command comes to the Inbox with its own wording; a refused skill is noted on the goal.

## Also
- Bundle installs are background operations the Setup and goal pages follow.
- A plugin's shipped MCP servers carry their deny lists in the skills catalog, under the prefix each coding agent gives them.

## 1.9.0 — 2026-10-16

- docs: review fixes in the guide, CONTEXT and ADR-0032; the investigation caps under Limits
- fix(web): the Brief waits for the investigation, references need Clarify, audit rows name their fix task
- fix(catalog): pin rea-agents 6.5.0, deny the evidence bundle, ponytail-review preferred for task reviews
- fix(delivery): a stacked delivery ships the reference report; a PR body clips long review notes
- fix(engine): the discipline's scope decides Plan lean, the plain profile's hint and the audit default
- fix(engine): the investigation commits its report alone, the audit stays in the goal's files, an unreadable MCP catalog fails closed
- fix(core): goal rows from an older Foundry read with the new fields' defaults
- fix(engine): an unreadable MCP catalog denies nothing instead of failing the session
- docs(guide): screenshots with the Ponytail switch and the reference row
- docs: Ponytail, the audit, references and REA in the guide, CONTEXT and ADR-0032
- feat: a goal can learn from a reference, investigated with REA before Clarify
- feat: REA, reverse engineering, as an optional MCP server with its tools that run things kept off
- feat(engine): an optional audit of the finished branch before the goal review
- fix(delivery): a task's review notes reach its pull request
- feat: Ponytail, the lazy senior dev, as a per-goal discipline next to TDD

## 1.8.0 — 2026-10-14

- fix(engine): an engine error mid-attempt closes the attempt and gives it back
- fix(engine): recordings stay out of the way of work, and the final walkthrough only counts when nothing overtook it
- fix(engine): tell the worker a webServer command must keep running
- fix(engine): a milestone script's check and its recording run it the same way
- docs: feature milestones, their scripts and the final walkthrough
- feat(web): milestones show whether they were shown, with Rerun and the final walkthrough
- feat(server): rerun a milestone, and say which milestones are being recorded
- feat(notify): a failed or fake-data milestone says so, and the final walkthrough sends one message
- feat(engine): the planner gives every feature a milestone, and its task writes the script
- feat(engine): feature milestones go on, are repaired once, and end in a final walkthrough
- feat(engine): record a milestone by running its script, one recording after another
- feat(core): a milestone can carry a Playwright script, and a goal a final walkthrough
- test(engine): the Start now test uses a goal state that exists

## 1.7.0 — 2026-10-14

- docs(guide): Start now can start a ready task past the scheduler's caution
- feat(web): Start now on a ready task held back only by the scheduler, after a confirmation
- feat(server): the goal view says whether a ready task's wait can be overridden
- feat(engine): Start now can override the scheduler's caution on a ready task

## 1.6.0 — 2026-10-14

- feat(web): install optional skills in one click (+ optional), or a whole tier from its heading (Install N)
- feat(web): side panels — Extensions' Catalog, the Ports and Agents overviews — stay in view while their list scrolls
- feat(web): the "waiting for you" card is laid out like the rest of the app: a heading with the reason's icon and colour, the details and your answer, the actions in a footer
- feat(web): the merge conflict page colours code with line numbers and tints ours, theirs and the conflict markers in the editable result
- fix: a task that runs alone (not parallelizable) says it waits for the running task to finish, not that it depends on it, and the task graph marks it runs alone
- fix: times show in your computer's time zone instead of UTC (Activity, imported goals, usage notifications, foundry usage)
- fix(web): everything clickable shows the pointer cursor

## 1.5.0 — 2026-10-12

- feat(web): New folder in the folder picker; Choose with Finder… is left out when Foundry is opened from another device; the picker keeps one height instead of jumping
- feat(web): the Agents page is laid out like Extensions and Ports — cards per goal and per folder that fold, live only, an Overview, a red Stop, and subagents that fold under their session
- feat(web): coloured action buttons on Ports (Open, Stop & release) and Extensions (View, Update, Adopt, Uninstall); Ports cards fold, and a port that cannot be stopped says why in place of the button
- fix(web): a running skills operation shows beside its source's status instead of on a line of its own

## 1.4.0 — 2026-10-10

- feat: the Ports page (⚙ → Ports) — every port in use on Foundry's computer and what holds it: Foundry's server, previews, VS Code (web), what a task started, the Docker services Foundry runs, tailscale serve forwards, Docker containers, other programs and holders only sudo can see
- feat: stop & release a port from the page after a confirmation that says what stops; Foundry itself, the serve that carries it, system and other users' programs are never offered
- feat(web): a preview that fails with EADDRINUSE names the holder of that port on its card, with stop & release and a link to the page
- feat(cli): foundry ports lists the same (--all, --json)
- fix(web): Stop and retry in the task panel confirms in a dialog

## 1.3.2 — 2026-10-10

- fix(preview): a preview no longer fails with EADDRINUSE on a port lsof shows as free — a port held on another address (tailscale serve --https=<port>, which loopback does not see) is skipped and the app gets the next free port

## 1.3.1 — 2026-10-10

- fix(tailnet): preview, VS Code (web) and notification links no longer fall back to localhost when Foundry runs as a launchd service on a Mac without `tailscale` on PATH — the Tailscale app's binary is now called through a shell, so it answers as the CLI

## 1.3.0 — 2026-10-09

- fix(engine): a task no longer hangs in observing when a check's dev server keeps its output open — checks, installs, docker compose and timed git commands run in their own process group and are killed whole on a timeout
- feat(engine): unstick a task without restarting Foundry — Start now on a ready task nothing holds back, Stop and retry on a running task with no live session; a waiting task says why
- feat(preview): open Docker when it is installed but not running, before a preview's services start
- feat(milestone): the walkthrough opens the app the task is about, leaves screenshots of error pages out, takes missing env keys from your checkout, and falls back to the app's mock command (new Mock command in How to run it, or a dev:mock script)
- feat(notify): bold titles; a localhost link is written out as copyable code on Telegram; a stacked delivery is told in a few messages instead of one per pull request
- fix(web): a session stopped by its cost or turn cap reads amber and names the per-session cap, not the goal budget
- feat(web): milestones open independently, goal review notes open full, the file preview steps through a task's files, and the check dialog shows runs first with formatted output

## 1.2.0 — 2026-10-08

- feat: Transfer — carry settings, keys and goals to another Foundry, typically on a new computer (⚙ menu → Transfer, or `foundry export` / `foundry import`)
- feat: import merges — goals already here are skipped, settings are taken section by section, credentials one by one
- feat: imported goals arrive as history; map their repository to restore their branch, and Reattach an unfinished one to carry it on here
- feat: Keys & secrets travel sealed with a password (scrypt + AES-256-GCM)
- feat(cli): foundry export, import and reattach, with or without a running server
- feat(web): the ⚙ menu shows the running version and flags a newer one
- fix(core): keep the newest rate limit sighting when older usage arrives
- docs(guide): Moving to a new computer

## 1.1.3 — 2026-10-08

- docs(guide): retake the screenshots
- docs(guide): describe Codex plugin skills, the Codex sign-in code and the wider setup check
- fix(skills): show skills installed outside Foundry on the next Skills page load
- fix(codex): put back the AGENTS.md autoskills writes, as it does the other guidance file
- fix(setup): flag a Codex CLI that cannot run Foundry's sessions
- perf(codex): load no configured MCP servers into Codex's Clarify and planner
- fix(codex): continue a Codex session that ran out of tool calls
- fix(codex): pause Codex until its used-up quota window resets, not five minutes
- fix(codex): show the Codex sign-in code plainly and wait as long as it lasts
- fix(web): check every agent in use for setup, and show setting sources on its own tab
- fix(codex): name the goal's own agent, and drop instructions Codex cannot follow
- fix(codex): tell Codex sessions to read skills, not call a Skill tool
- fix(settings): say a pack option has nothing for this agent instead of 0 missing
- fix(skills): list Codex plugin skills and count plugin packs as installed on Codex
- fix(web): give every header control one height
- fix(restart): restart a task that is waiting in the Inbox, and review it against its new base
- fix(review): tell the task reviewer which files a long diff leaves out

## 1.1.2 — 2026-10-08

- feat(usage): resume paused sessions by hand, and show the retry date
- fix(usage): stop pausing for a month on an extra-usage window that stopped nothing

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
