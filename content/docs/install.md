---
title: Install
weight: 1
---

## Windows

Download `BranchBooks-setup.exe` from the
[latest release](https://gitlab.com/branchbooks/branchbooks/-/releases/permalink/latest) and run it. Setup first asks
who BranchBooks is for:

- **Only for me** (the default): no admin prompt. It installs into `%LOCALAPPDATA%\Programs\BranchBooks`, and only
  your Windows user sees it.
- **For all users**: Windows asks for an administrator. It installs into Program Files, and everyone on the computer
  gets it in their Start menu. Each person still has their own books.

BranchBooks needs Windows 10 (version 1809) or later, 64-bit. It brings its own .NET, so there is nothing else to
install.

> [!NOTE]
> The app isn't code-signed yet, so Microsoft Defender SmartScreen may say it is unrecognized the first
> time you open it. If you downloaded it from the BranchBooks repository, choose **More info**, then
> **Run anyway**.

## Updates

Each time it starts, BranchBooks asks `branchbooks.dev` for a newer release, which forwards to the latest
release on GitLab, and downloads it in the background. Before offering it, the app checks the download against
the release's checksum.
**Restart to update** then appears beside the book switcher: it closes the app, installs the update, and opens
the app again. If BranchBooks is installed for all users, Windows asks for an administrator first; say no and
nothing changes. If you ignore the button, it's back the next time you open the app. Offline, the app just runs
as it is. To check again without restarting, use **Check for updates** in [Settings](settings.md), where you can
also turn off the check at start.

That check is the only network traffic BranchBooks makes apart from syncing your books with the remote you
chose, and it carries nothing about you or your books.

## Where your books are

Books are kept in `%LOCALAPPDATA%\BranchBooks Data\books`, one git repository each; **Settings → Data and
backups** opens the folder. That folder is your Windows user's own on this computer: a roaming profile never
copies it to another computer, because two computers sharing one copy of a git repository can damage it. To use
a book on more than one computer, give it a remote and sync.

Books that an earlier version kept in `%APPDATA%\BranchBooks` move there the first time the app starts.

## Uninstalling

Uninstall from Windows' **Installed apps**. If BranchBooks was installed only for you, Setup then asks whether to
delete your books and settings too. **No** keeps them, and is the default. Books you sync to a remote are still
on the remote either way; books only on this computer are gone for good if you choose **Yes**. Uninstalling a
copy installed for all users never deletes anyone's books.

## Android

Planned, not yet available.
