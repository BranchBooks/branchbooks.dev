---
title: Install
weight: 1
---

## Windows

Download `BranchBooks-win-Setup.exe` from the
[latest release](https://gitlab.com/branchbooks/branchbooks/-/releases/permalink/latest) and run it. It installs for
your user alone, with no admin prompt, into `%LOCALAPPDATA%\BranchBooks`. It also installs Microsoft's
WebView2 runtime if Windows doesn't already have it.

> [!NOTE]
> The app isn't code-signed yet, so Microsoft Defender SmartScreen may say it is unrecognized the first
> time you open it. If you downloaded it from the BranchBooks repository, choose **More info**, then
> **Run anyway**.

## Updates

Each time it starts, BranchBooks asks `branchbooks.dev` for a newer release, which forwards to the latest
release on GitLab, and downloads it in the background.
**Restart to update** then appears beside the book switcher. If you ignore it, the update applies the next
time you open the app. Offline, the app just runs as it is. To check again without restarting, use
**Check for updates** in [Settings](settings).

That check is the only network traffic BranchBooks makes apart from syncing your books with the remote you
chose. It carries the app's version and a random id kept on your device.

## Where your books are

Books are kept in `%APPDATA%\BranchBooks\books`, one git repository each; **Settings → Data and
backups** opens the folder. Uninstalling the app from Windows' **Installed apps** leaves them where they
are.

## Android

Planned, not yet available.
