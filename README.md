<div align="center">
  <img src="./assets/rlgo_logo_no_tagline.png" alt="RL:GO" width="420" />

  <h3>Optimize. Compete. Win.</h3>
  <p><strong>RL:GO</strong> is a Windows utility for Rocket League players who want faster setup, safer config changes, and competitive-focused input and graphics tuning.</p>

  <p>
    <a href="https://github.com/chrallaz/rlgo/releases/latest"><strong>Download latest installer</strong></a>
    ·
    <a href="https://github.com/chrallaz/rlgo/releases">Release notes</a>
  </p>

  <p>
    <img alt="Platform" src="https://img.shields.io/badge/platform-Windows-2F8CFF?style=for-the-badge" />
    <img alt="Rocket League" src="https://img.shields.io/badge/game-Rocket%20League-FF7A00?style=for-the-badge" />
    <img alt="Status" src="https://img.shields.io/badge/status-MVP-43E079?style=for-the-badge" />
  </p>
</div>

---

## Download

Download the latest Windows installer from the Releases page:

**Recommended:** [RL:GO latest release](https://github.com/chrallaz/rlgo/releases/latest)

Use the installer asset named like:

```text
RLGO_<version>_x64-setup.exe
```

The raw app executable is not distributed here. Releases include installer files and SHA256 checksums.

---

## What RL:GO does

RL:GO helps manage Rocket League configuration files without manually digging through `.ini` files.

Current focus:

- Competitive graphics values for `TASystemSettings.ini`
- Fast input/deadzone values for `TAInput.ini`
- Stall button creation and cleanup
- Backup creation before config writes
- Restore from previous backups
- Rocket League process safety checks
- Built-in update page powered by GitHub Releases
- TimerResolution bundled under the Pro tab

---

## Safety

RL:GO is designed to avoid risky writes:

- Creates backups before changing config files
- Restores read-only state after writes
- Blocks config writes while `RocketLeague.exe` is running
- Keeps original binds when adding a stall button
- Shows release checksums for installer verification

If Rocket League is running, RL:GO will ask you to close the game before applying changes.

---

## Default config path

RL:GO looks for Rocket League config files in:

```text
C:\Users\<user>\Documents\Rocket League\TAGame\Config
```

If the folder is not found automatically, the app lets you select the correct `TAGame\Config` folder manually.

---

## Windows SmartScreen note

Windows may show a warning such as **"not commonly downloaded"** because RL:GO is new and not code-signed yet.

To verify a download, compare the installer SHA256 hash with the checksum listed in the release notes or `SHA256SUMS.txt`.

Example PowerShell command:

```powershell
Get-FileHash .\RLGO_<version>_x64-setup.exe -Algorithm SHA256
```

---

## Project status

RL:GO is currently in MVP development. The goal is a clean, safe, Rocket League-inspired Windows app for competitive config management.

Planned polish:

- Better controller/input diagnostics
- More config safety checks
- Cleaner installer trust flow and signing
- More guided recovery tools for backups and config setup

---

## Author

Built by [chrallaz](https://github.com/chrallaz) for Rocket League players who like their config clean, fast, and recoverable.