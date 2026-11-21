# Install SilverZAgents on Windows

## Requirements

- Windows x64 and an existing supported browser with your own Facebook session.
- Internet access for dependencies, browser/Facebook access, and online AI.
- This build uses CPython **3.14.10 or a compatible newer 3.14 patch**, x64, with pip and Tk. Python 3.15/3.13, free-threaded and debug builds are not compatible with these compiled modules.
- The installer detects compatible Python and reuses it. If only an incompatible Python exists, it keeps that installation and can install a private compatible runtime in the chosen application folder after Python-license acceptance.
- WebView2 Runtime is recommended for the main panel; the application has a Tk compatibility fallback.
- Local AI models require additional disk/RAM and may benefit from a GPU. Models are not bundled; start with a small task and measure performance on your PC.

## Download and verify

Get the `.exe` installer and `SHA256SUMS.txt` from [official Releases](https://github.com/silverznet/SilverZAgents/releases). Do not use GitHub's “Source code” ZIP as an installer.

In PowerShell, from the download folder:

```powershell
Get-FileHash -Algorithm SHA256 .\SilverZAgents-6.0.0-preview.1-Setup.exe
```

Compare the complete hash with `SHA256SUMS.txt`. This verifies that your download matches the published asset; it is not Windows publisher certification. Do not disable system protections to install the application.

## Interactive setup

Run the installer and choose a dedicated folder, for example `D:\Program Files\SilverZAgentsClient`. Do not install into the developer source folder. The installer can download pinned libraries into its own `vendor` directory; it does not replace your unrelated Python installation.

The `.exe` is a bootstrap installer, not an offline bundle of Python, every dependency, model and browser. Allow time for downloads. Keep the installation log if setup fails; remove private details before sharing it.

## Command-line setup

From Command Prompt, inspect the installer first:

```cmd
SilverZAgents-6.0.0-preview.1-Setup.exe --validate --dir "D:\Program Files\SilverZAgentsClient"
SilverZAgents-6.0.0-preview.1-Setup.exe --diagnose --dir "D:\Program Files\SilverZAgentsClient"
```

For unattended installation, first review the [Python license](https://docs.python.org/3/license.html). The following flag explicitly accepts it if Python must be installed:

```cmd
SilverZAgents-6.0.0-preview.1-Setup.exe --quiet --dir "D:\Program Files\SilverZAgentsClient" --accept-python-license --log "D:\SilverZAgents-setup.log"
```

Use `--python "D:\path\python.exe"` to nominate a compatible existing runtime. `--no-shortcut` skips the desktop shortcut. A zero exit code indicates successful setup; check the log for diagnosis or errors.

## Connect browser profiles

1. Open the browser's extension management page yourself.
2. Enable Developer mode and load the installed application's `extension` folder as an unpacked extension.
3. Repeat for each intended browser profile. Use the same folder; do not copy a separate extension tree for every browser.
4. Check **extension 3.1.0**. After an update, Reload it in each profile where it was already running.
5. Keep your existing Facebook login in the browser. Open the intended tab and start a small test task from the panel.

The application does not import/export cookies, passwords or browser profiles. When idle/finished, the extension removes its own overlays and detaches debugging while retaining readiness for the next explicit run. Manual debugger cancellation requires a new start; restrictions/login/CAPTCHA may require you to intervene.

## Configure Page/Profile management
Management requires extension **3.1.0**. Reload the extension in every participating browser profile, then assign the exact public Page/Profile URL and current actor identity under **Task → Interaction & Page/Profile management**. Start in **draft** mode with a small limit. Inbox remains off until deliberately enabled with the exact permitted inbox URL. The app does not switch Facebook identities. See the [management guide](MANAGEMENT.md) for bounds, privacy, and unsupported layouts.
## Updates and troubleshooting

- Stop active jobs and exit fully before updating. Do not delete `data` to update. Back up important application data locally first; never upload it to a public issue.
- Install new versions manually from Releases. This preview does not auto-update from GitHub.
- **No tab:** verify browser/profile selection, an open Facebook tab, extension folder/version and local connection. Starting a new browser profile is not required.
- **Python exists but setup selects another:** the compiled modules require the compatible 3.14 x64 ABI described above. A higher major/minor version is not automatically compatible.
- **API error:** check the configured provider/model, credentials, quota and connectivity. Do not include keys in reports.
- **Slow local AI:** measure the model time separately from browser actions; reduce concurrent jobs. Multiple workers share a local inference service and do not automatically increase model throughput.
- **Unknown send result:** inspect Facebook manually; do not repeatedly submit the same item. Submitted counts do not confirm publication/approval.
- **Close button:** X minimizes to the taskbar. Use Settings → Exit application for a full exit.

See [Support](../SUPPORT.md) for a sanitized bug-report checklist.
