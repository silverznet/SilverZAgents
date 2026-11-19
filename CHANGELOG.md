# Changelog

## 5.5.1 Preview — 2026-11-19

First public GitHub distribution preview; extension **3.0.3**.

### Reliability
- Wait for the worker output reader before finalizing counters and completion notification.
- Apply Groups/Home navigation consistently to Like-only workflows.
- Serialize legacy publication database migrations across concurrent workers.
- Isolate and serialize atomic JSON writes, with bounded retries for transient Windows file locks.
- Serialize recovery-log rotation and writes across workers.
- Include window, appearance and progress preferences in full settings reset; preserve them during cache cleanup.
- Clear the debugger cleanup error once detach succeeds, while preserving other/manual-stop states.

### Browser and desktop lifecycle
- Restore extension-owned debugger state after service-worker restarts; retry failed detach without attaching while idle.
- Recognize browser branding through user-agent/client hints; support depends on browser behavior/version.
- Minimize to taskbar on X; provide an explicit full-exit action.
- Save window placement separately from task configuration and fit restored bounds to available screens.

### Distribution
- Compiled first-party Python modules, encrypted selected UI/engine resources and signed payload integrity manifests.
- Windows installer with compatible-Python detection, pinned dependency setup and command-line options.
- Public documentation, installation instructions and download checksums.

### Known limits
Public preview: clean-PC installation and all real Facebook/browser combinations are not fully certified. No automatic client updates, hosted knowledge service or commercial license activation. No Windows Authenticode certificate. Prepared/AI submission counts do not guarantee publication or group approval.
