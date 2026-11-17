# Nervenet public repository: notes for coding agents

This is Nervenet's **public** face on GitHub (`Nervenet-AI/nervenet`). It holds no source code: the app is proprietary
and its source is private. Everything here is read by users, so write for them.

## What lives here
- `README.md`: what Nervenet is, the download table per system, first start on a Mac (Open Anyway), the anonymous
  install count, and links.
- `CHANGELOG.md`: one section per version, newest first, in plain words for users. Each release's GitHub text is that
  version's section.
- `.github/ISSUE_TEMPLATE/`: the issue forms.
  - `bug_report.yml` is what the app's "Report a problem" opens: `issues/new?template=bug_report.yml&version=…&system=…`.
    Its field ids `version` and `system` must stay as they are, or change together with the app's
    `desktop/src/renderer/lib/report.ts`.
  - `feature_request.yml` is "Suggest an idea".
  - `config.yml` adds the business contact.
- **Releases**: every download is an asset of a release `v<version>`, and `releases/latest` is what the website and
  the app link to. Asset names must stay exactly as they are, because the app's update feed and the README use them:
  - `Nervenet-Setup-<version>-x64.exe`
  - `Nervenet-<version>-macos-arm64.dmg` and `Nervenet-<version>-macos-x64.dmg`
  - `nervenet-<version>-linux-x64.tar.gz` and `nervenet-<version>-linux-arm64.tar.gz`
  - `SHA256SUMS.txt`

## The other repositories
- **The app's source:** private, `MuhammadNoman76/NerveNet`, local `D:\Nervenet`. Its AGENTS.md is the main project
  memory. Its docs/packaging.md › Releases is the release process; it builds the files above and the update feed.
- **The website:** private, `MuhammadNoman76/Nervenet-app`, local `D:\Nervenet-website`. Its AGENTS.md covers Cloudflare
  Pages, the update feed and the privacy policy.
- This repository's local clone is `D:\Nervenet\nervenet-public`. The source repository ignores it through
  `.git/info/exclude`.

## Rules for what is written here
- Never name other AI agents or assistants (model providers such as OpenAI or Anthropic are fine), never name the
  libraries the app is built on, and never describe internals ("backend", "server").
- Every claim must match the app. Say what is untested, for example a platform with little testing.
- Never ask people for keys, passwords or private files in issues: issues are public.
- **Free only:** the owner pays for nothing but the domain.
  - The Mac app isn't notarised: people use System Settings › Privacy & Security › Open Anyway.
  - The Windows installer isn't code-signed: SmartScreen shows More info › Run anyway.

  Keep both explained in the README.
- Commit as `Muhammad Noman <muhammadnomanshafiq76@gmail.com>`, with no AI attribution.
