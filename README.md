# Conchshell for Scoop

The official [Scoop](https://scoop.sh/) bucket for
[Conchshell](https://conchshell.app/): an SSH terminal, an SFTP and FTPS file
manager, an RDP client and a VNC viewer in one app. The bucket is maintained
by the publisher of Conchshell, DeveloperEva.

## Install

```powershell
scoop bucket add conchshell https://github.com/DeveloperrEva/scoop-conchshell
scoop install conchshell/conchshell
```

Start it from the Start menu (Scoop Apps > Conchshell) or type `conchshell`
in a terminal.

## Update

```powershell
scoop update
scoop update conchshell
```

Update Conchshell with Scoop. Conchshell also looks for a new version at
launch, but it sees that Scoop installed it and does not install new versions
itself: when one is out, it says so and leaves the update to Scoop. To stop
the check at launch, switch off Settings > Advanced > Check for Updates.

## What the package does

- Downloads the official 64-bit `.msi` from `https://conchshell.app/updates/`
  and checks it against the SHA-256 published with the release.
- Unpacks the program files into Scoop's own directory. It does not run the
  Windows installer, so there is no entry in Apps & features.
- Adds a Start menu shortcut and the `conchshell` command.

Conchshell keeps its settings, saved connections and the vault in
`%APPDATA%\app.conchshell` and `%LOCALAPPDATA%\app.conchshell`. They survive
updates, and `scoop uninstall conchshell` leaves them in place; delete those
two folders to remove them as well.

## Requirements

64-bit Windows 10 or 11 and the Microsoft Edge WebView2 Runtime. Windows 11
includes WebView2. If Conchshell does not start on Windows 10, install the
runtime from https://developer.microsoft.com/microsoft-edge/webview2/.

## Price and licence

The application is free, with no account and no subscription. One feature is
paid: Sync, which carries saved connections between your own machines, for a
one-time $19.

Conchshell is proprietary software; its terms are the
[User Agreement](https://conchshell.app/legal/agreement/). This bucket is the
publisher's own; please do not copy the manifest into other buckets.

## Support

Write to **support@conchshell.app** about the package or the application:
a failed install or update, a wrong hash, anything else. Issues are turned off
in this repository, so e-mail is the way to reach the publisher.
