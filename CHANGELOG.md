# Changelog

All notable changes to Nervenet are listed here, newest first. Version numbers follow
[Semantic Versioning](https://semver.org/). Dates are written as YYYY-MM-DD.

## [1.0.0]

The first public version of Nervenet, for **Windows 10 and 11** (x64, and Windows on ARM through emulation), **macOS 14
or later** (Apple silicon and Intel) and **Linux** (x64 and arm64). The release date will be set when the installers
are published.

### Release

- Downloads for Windows, macOS (Apple silicon and Intel) and Linux, all on this repository's releases page.
- **Report a problem** in the profile menu and in Settings › About opens a new issue here, with your version filled in.
- Updates come from nervenet.app. Each daily check also counts the install anonymously: a random number, the version
  and the system, never your files or chats. Turning off automatic update checks turns the count off too.
- The Mac app isn't notarised by Apple: open it once through System Settings › Privacy & Security › Open Anyway.

Nervenet is a desktop AI agent that works in a folder on your computer, with the model you choose. It reads and edits
files, runs commands, searches the web and uses a browser. It asks you before risky steps. You can reach it from your
phone through messaging apps, or from a web browser on another device.

### 2026-11-17

- **Privacy** (Settings › Privacy, off by default) hides personal details from the model: emails, phone numbers, card
  numbers, IP and device addresses, links, and patterns you add. The model sees stable placeholders. Your chat, your
  tools and your history keep the real values.
- **Remote access** (Settings › Remote access, off by default) opens Nervenet in a web browser on another device,
  behind a password. It works on this computer only, or on other devices on your network too. The page counts the
  signed-in browsers and has Sign out everywhere.
- `nervenet --serve` runs Nervenet without a window, for a computer you reach only through a browser, such as a VPS
  through an SSH tunnel.
- ElevenLabs connects with a sign-in or with an API key.

### 2026-11-16

- **Plugins** add skills, subagents, slash commands and connectors as one bundle. You can install them from GitHub, a
  link, a folder, a .zip file or a marketplace. You turn them on and off on the Plugins page, or per chat in the + menu.
- Nervenet comes with **about fifty built-in plugins**, all off until you turn them on. They cover sales, marketing,
  finance, legal, support, product, HR, operations, small business, software development, data, video, voice and music.
- When you turn on a plugin that works with your tools (a CRM, email, a calendar …), it asks you to connect them.
- Ask the agent to make a plugin and it builds the plugin, then gives you a card to install it.
- Schedules choose which plugins their chats get.
- **Browser:** the agent works across tabs, and several agents can browse at the same time. It also scrolls inner
  panels and takes whole-page pictures, and Google's sign-in page accepts it.

### 2026-11-14

- **Speak** reads a finished reply aloud. It uses only voices installed on your computer.

### 2026-11-13

- **Goals:** give Nervenet an outcome and it keeps working on it by itself, in its own chat, until it is done. A goal
  card in the chat, a goal chip in the sidebar and the Goals page show what it is doing. You can Pause, Resume, Check
  now or mark it Done.
- **Voice:** the microphone in the message box types what you say. Voice notes sent through a messaging app are
  understood too. Speech is processed on your computer after a one-time download (about 486 MB), and the recording is
  never sent anywhere.
- You can delete, edit and retry messages.
- A stopped turn keeps a **Continue** card, and Continue never repeats a step that already finished.
- **Exit Nervenet** in the profile menu quits fully. It asks first only when work is still running.
- Finished background jobs show which chat started them.
- In Task Manager, every Nervenet process is named Nervenet.
- Fixed: layouts on small windows, sidebar scrolling, and a cut-off notice in narrow subagent chats.

### 2026-11-12

- **Auto mode:** Nervenet reviews its own actions before they run. It runs what your request covers, stops what it
  shouldn't do, and asks you only about the steps that are yours to decide.
- **Manual** mode asks you as before. **Bypass** runs tools without asking.
- **Browser tool:** the agent uses the built-in browser beside the chat while you watch. It opens pages, clicks, types
  and fills in forms with your sign-ins. For a sign-in or a code, it asks you to do that step yourself.
- **File requests:** the agent can ask you for a file it can't work without, or ask you to pick one of several files,
  with a preview.
- The main agent can read what each of its subagents did.
- You can sign in to Composio instead of pasting an API key.
- The About page links to Nervenet's Instagram.

### 2026-11-11

- **App lock:** a PIN, a pattern, a password or a pet code. It asks when Nervenet opens and when the app has been idle,
  the computer sleeps or the window is hidden. A recovery key gets you back in.
- **Connector suggestions:** the agent finds a connector for the task and shows a card in the chat. You connect it
  from the card and the agent carries on.
- The Connectors page has one search across your connectors, the catalog and Composio's apps.
- Connecting a messaging channel takes fewer steps. Each platform shows its own logo.
- A built-in coding skill gives the agent better habits for software work.
- Keyboard shortcuts show ⌘ on a Mac.
- The greeting no longer says "Good morning" in the middle of the night.
- Fixed: Gemini's usage was counted twice, and its parallel tool calls got mixed up.
- Fixed: a finished chat could still show as running.

### 2026-11-10

- **Folder memory:** for each folder you work in, the agent keeps notes about that project and reads them in every
  new chat there. A folder's own `AGENTS.md` is loaded too.
- The agent runs independent parts of a job in parallel subagents, and it is better at finishing the work it starts.
- **Studio file explorer:** browse the chat's folder in the Studio.
- When a provider limits the number of pictures in a request, Nervenet keeps the newest ones and tries again.
- Notifications are only for new events. Toasts appear at the top of the window.

### 2026-11-09

- **Messaging channels:** talk to Nervenet from Telegram, WhatsApp, Discord, Slack, Signal or SMS (Twilio), or start
  chats with signed webhooks.
  - Messages go into ordinary Nervenet chats.
  - Progress, approval requests, questions, files and results come back to the same conversation.
  - Unknown senders must be paired and approved in the app.
- **Continue** picks up a run that stopped before it finished.

### 2026-11-08

- **Connectors:** connect MCP servers by link or by command. Servers that need a sign-in open their sign-in page in
  your browser. Each tool call asks first unless you choose otherwise.
- **Composio:** choose free actions in apps such as GitHub, Gmail or Slack. Each call asks first.
- **Subagents:** the agent hands parts of a job to helpers (Explore, Plan, general-purpose, fork). Each helper has its
  own chat, which you can open read-only, and the Agent map shows their tokens and time.
- **Scheduled chats** start by themselves:
  - at a set time on chosen days, every few minutes or hours, once, or when you open your computer in the morning,
    afternoon, evening or night
  - with their own instructions, skills and connectors
  - missed runs run when Nervenet is back
- **Cron jobs and wake-ups:** the agent can come back to a chat later by itself.
- **Sign in with OpenRouter** (no key to paste), and **Continue with ChatGPT** to use a ChatGPT plan.
- The computer stays awake while the agent is working.

### 2026-11-04 to 2026-11-06

- **Skills:** folders of instructions that teach the agent a task. Over thirty come built in. You can add your own, or
  ask the agent to write one.
- **Memory:** the agent remembers your preferences across chats. A card shows each note it saves, with View and Undo.
  You can edit or delete notes in Settings › Memory, and one switch turns memory off.
- **Task list:** for multi-step work, a card shows what is done, what is in progress and what is still to do.
- **Widgets:** interactive cards in the chat, such as charts, comparisons, itineraries, recipes with timers, quizzes,
  step-by-step guides and the weather, plus live visuals the agent draws.
- **Branch a chat** to try a different direction.
- **Companions:** animated pets for each chat, in the sidebar, the header and the chat.
- Fixed: a closed video preview could reappear over the chat.

### 2026-11-03

- **Web search works without a key**, with numbered sources, site icons and citations in the reply. Tavily, Brave
  Search and SearXNG are optional.
- **Queue and steer:**
  - type while the agent works, and your message waits above the box and sends by itself when the agent is done
  - **Steer** gives it to the running turn
  - **Edit** takes it back
- **Live writing:** you see a file grow line by line while the agent writes it.
- Attach files by dropping them on the chat or pasting them.
- Usage for each turn, and a time on each message.
- Desktop notifications when a chat needs you or a run finishes.
- **Zoom** the whole app from 50 to 200 %.
- **Layout:** the chat and the Studio sit side by side with a divider, and the Studio can be expanded.
- The jellyfish logo.
- Builds work in Restricted mode on Windows: npm, node, git and Python run in the sandbox.

### 2026-11-02

The first working build.

- **Works in your folder.** Open a project folder, right-click a folder › *Open with Nervenet*, or run
  `nervenet <folder>`. The sidebar groups chats by folder.
- **Restricted mode by default:**
  - file tools reach only the open folder
  - shell commands run in a sandbox on your computer
  - *Allow All* is a per-chat choice that asks you to confirm
- **Asks before risky steps:** overwrites, writes outside the folder, destructive or unclear commands and sandbox exits.
  Each approval card shows the exact arguments, the paths it affects and a diff.
- **Tools:**
  - Read (text, PDF, Word, Excel, PowerPoint, notebooks and images), Write, Edit, Glob and Grep
  - shell commands (PowerShell, and Bash through WSL2)
  - WebSearch and WebFetch
  - AskUserQuestion, with background jobs you can read and stop
- **The Studio:** a panel that opens what the agent touched, formatted or raw:
  - web pages, Word, PowerPoint, Excel, CSV, PDF, Markdown, code, JSON, images, audio and video
  - diffs that are unified or side by side
  - running jobs with their ports
- **Any model:** 70 provider presets, local servers (Ollama, LM Studio and others) and any OpenAI-compatible API.
  - **Test connection** checks the key, the model, streaming, tools, images and reasoning.
  - When a provider rejects a setting, Nervenet offers a one-click fix.
  - Reasoning settings and request parameters are editable, with a request preview.
- **Long conversations:** automatic and manual compaction. A context meter shows the size of the latest request against
  the model's window, with input, output, cached and reasoning tokens.
- **Your keys stay yours:** they are kept in your system's credential store and never written to files or logs.
- Right-to-left text (Urdu, Arabic) in messages, file names and paths.
- A Windows installer, either for all users or for you only, with *Open with Nervenet* on folders, the `nervenet`
  command and automatic updates.

### Known limitations

- **Platforms:** most of the testing was on Windows 11 x64. The macOS and Linux versions are new and have had much less
  testing. There is no native Windows on ARM build; the x64 version runs there through emulation.
- **Providers:** only a few were tested against the real services. The other presets follow their providers'
  documentation. Continue with ChatGPT hasn't been tried against the real service yet.
- **Not yet tried with real accounts:**
  - messaging channels
  - Composio
  - connector sign-ins
  - remote access from other devices
- **WhatsApp linked by QR code** is unofficial and can get a number banned. The official Cloud API is the safe choice.
- **Not yet tested over long runs with real models:** subagents, goals and scheduled chats.
- **Remote access** uses plain http. Beyond your own network, put it behind a tunnel or a VPN.
- **Voice** accuracy depends on noise, accents and language.
- **Privacy** doesn't cover images.
- **The app lock** locks the app. It doesn't encrypt your files.
- **Context sizes** are estimates for providers that don't report usage.

[1.0.0]: https://github.com/Nervenet-AI/nervenet/releases/tag/v1.0.0
