# Install SilverZAgents on Windows

## 6.7.1 startup error

If 6.7.1 displays `brandIcons is not defined`, install **6.7.2 Preview 1** into the existing application folder and choose **Upgrade**. The previous protected package omitted an interface resource. Do not delete your data, reinstall browser profiles or manually replace signed application files.

## Requirements

- Windows x64 and an existing supported browser with your own Facebook session.
- Internet access for dependencies, browser/Facebook access, and online AI.
- This build uses CPython **3.14.10 or a compatible newer 3.14 patch**, x64, with pip and Tk. Python 3.15/3.13, free-threaded and debug builds are not compatible with these compiled modules.
- The installer detects compatible Python and reuses it. If only an incompatible Python exists, it keeps that installation and can install a private compatible runtime in the chosen application folder after Python-license acceptance.
- WebView2 Runtime is recommended for the main panel; the application has a Tk compatibility fallback.
- Local AI models require additional disk/RAM and may benefit from a GPU. Model weights are downloaded separately during Setup (Qwen by default); start with a small task and measure performance on your PC.

## Download and verify

Get the `.exe` installer and `SHA256SUMS.txt` from [official Releases](https://github.com/silverznet/SilverZAgents/releases). Do not use GitHub's “Source code” ZIP as an installer.

In PowerShell, from the download folder:

```powershell
Get-FileHash -Algorithm SHA256 .\SilverZAgents-6.7.2-preview.1-Setup.exe
```

Compare the complete hash with `SHA256SUMS.txt`. This verifies that your download matches the published asset; it is not Windows publisher certification. Do not disable system protections to install the application.

## Interactive setup

Run the installer and choose a dedicated folder, for example `D:\Program Files\SilverZAgentsClient`. Do not install into the developer source folder. The installer can download pinned libraries into its own `vendor` directory; it does not replace your unrelated Python installation.

The `.exe` is a bootstrap installer, not an offline bundle of Python, every dependency, model and browser. Allow time for downloads. Keep the installation log if setup fails; remove private details before sharing it.

## Upgrade an existing client

Setup is in **English**. Stop active jobs, stop the local model and exit SilverZAgents fully before upgrading. Select the **existing installation folder**. Setup recognizes its publisher-signed installation metadata and shows **Upgrade** after the system check.

Upgrade retains application data, settings and the current model selection. The default **Keep current model · verify / repair files** option checks the existing model files and repairs missing downloads; an explicit different model choice changes the selected local model. **Skip model installation** skips this check. Downloads are separate from the EXE. Back up important data locally before updating.

Do not select the developer source folder, delete the client data folder, or install into a browser profile directory. A missing/invalid installation manifest requires correcting the installation location or restoring the installation files.

## Command-line setup

From Command Prompt, inspect the installer first:

```cmd
SilverZAgents-6.7.2-preview.1-Setup.exe --validate --dir "D:\Program Files\SilverZAgentsClient"
SilverZAgents-6.7.2-preview.1-Setup.exe --diagnose --dir "D:\Program Files\SilverZAgentsClient"
```

For unattended installation, first review the [Python license](https://docs.python.org/3/license.html). The following flag explicitly accepts it if Python must be installed:

```cmd
SilverZAgents-6.7.2-preview.1-Setup.exe --quiet --dir "D:\Program Files\SilverZAgentsClient" --accept-python-license --log "D:\SilverZAgents-setup.log"
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
Management requires extension **3.2.0**. Reload the extension in every participating browser profile, then assign the exact public Page/Profile URL and current actor identity under **Task → Interaction & Page/Profile management**. Start in **draft** mode with a small limit. Inbox remains off until deliberately enabled with the exact permitted inbox URL. The app does not switch Facebook identities. See the [management guide](MANAGEMENT.md) for bounds, privacy, and unsupported layouts.
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


## Offline model installation (6.7.1)

Setup defaults to **Qwen3 4B** and finishes only after required runtime/model files are present and download checksums match. Model setup errors are visible in the installer log and fail installation; they must not appear as successful completion.

| Setup choice | Files downloaded separately |
|---|---|
| Qwen (default) | Qwen3 4B text model and llama.cpp runtime |
| DeepSeek | DeepSeek R1 Distill Qwen 1.5B and runtime |
| Vision | Gemma 3 4B, image projector and runtime |
| None | No model download; existing selection retained |

Use the model selector in graphical Setup, or add `--model qwen`, `--model deepseek`, `--model vision` or `--model none` in CMD. Omitting this flag (or using `--model auto`) selects Qwen on a fresh installation and verifies/repairs the currently selected model on an upgrade, preserving its selection and task settings. For example:

```cmd
start /wait "" SilverZAgents-6.7.2-preview.1-Setup.exe --quiet --dir "D:\Program Files\SilverZAgentsClient" --model qwen --no-shortcut --log "D:\SilverZSetup-6.7.1.log"
echo Exit code: %ERRORLEVEL%
```

Add `--accept-python-license` only after reviewing the Python license, if no compatible runtime is installed. Existing Python 3.15 is preserved; this native build needs compatible CPython 3.14.10+ x64. Setup does not downgrade the system interpreter or change its PATH.

Keep Internet connected and allow several GB for models and dependencies. Verified cached downloads are reused; interrupted downloads can resume. Reload the installed extension **3.2.0** in every intended browser profile. Models can also be installed/repaired later from the Offline panel.

Stop jobs and exit fully before updating an existing client. Personal browser profiles and login sessions remain browser-owned. Automatic client updates are not included.

Setup is a graphical EXE with a command-line mode. Use `start /wait ""` in CMD (or `Start-Process -Wait -PassThru` in PowerShell) when a script must wait for completion and inspect the final exit code. A returned shell prompt by itself is not proof of completed model installation.
