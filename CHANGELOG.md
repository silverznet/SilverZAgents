# Changelog

## 6.0.0 Preview 1 — 2026-11-21 · Big Update

Includes Core management and the subsequent 6.0.0-dev.2 UI refinements; extension **3.1.0**.

### Page / Profile management
- Interaction-only, management-only and interaction → management modes.
- Explicit Page/Profile assignment for each connected browser profile, with frozen job settings and per-asset processing leases.
- Owned-post comment handling, attributable notification links, and optional inbox checks; inbox defaults off.
- Separate inspect, draft and auto-reply delivery choices for comments and messages.
- Durable event reservations and no automatic replay after an uncertain send; existing user drafts are preserved.
- Read-only encrypted draft and uncertain-send review.

### Content and efficiency
- Built-in contextual-comment rules: source language, AI minimum 50 characters, persistent duplicate protection and media/discussion grounding; literal prepared content is preserved.
- Shared, explicitly approved FAQ/knowledge groups. Exact FAQ reuse avoids AI calls; generated cache remains scoped to the assigned asset.
- Local hardware acceleration choices and one shared local model runtime across jobs.
- Independent Home/Groups interaction scope, optional Follow and random reply handling.

### Interface and privacy
- Grouped management settings, localized friendly choices, retained drafts through in-app selectors and correct processed-item units.
- Private inbox capability is bound to one active pinned connection and removed on idle/stop; no browser account/profile import or automatic identity switching.
- Fresh settings copies prevent assignment changes from mutating factory defaults.

### Known limits
This is a preview, not a guarantee of compatibility with all Facebook layouts. The inbox adapter requires explicit actor, thread and message-direction evidence; unsupported layouts require manual review. Check/draft/Enter counts do not confirm Facebook delivery. No automatic client updates, hosted knowledge service, commercial activation or Windows Authenticode certificate.

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
