# Changelog

## 6.7.3 Preview 1 — 2026-11-28 · Reply hotfix

- Fix selected-comment grounding: the selected comment is now supplied as a comment source rather than post body while preferring a comment anchor.
- Always finalize optional Reply surfaces, including rejected drafts or no eligible targets.
- Restore the configured feed from the known post only, using verified navigation; preserve unrelated-page, draft, authentication and account-restriction guards.
- Keep Like-before-Reply, no-replay receipts, per-comment limits and durable primary-post counts.
- Agent-side fix; extension remains 3.2.0. Includes the previous protected-interface startup hotfix.
- Live stop logs did not contain the actual changed URL; do not interpret synthetic regression coverage as full live-browser certification.


## 6.7.2 Preview 1 — 2026-11-27 · Startup hotfix

- Fix protected-client startup error `brandIcons is not defined`: include the omitted brand_icons.js in the encrypted resource vault.
- Include the existing third-party browser-logo attribution notice in the actual payload.
- Require compiled-interface browser rendering/navigation checks, including real settings and browser/reaction badges.
- Validate HTML/CSS/image dependencies and reject incomplete/obsolete input or module catalogs before packaging.
- Preserve the English Upgrade installer, existing client settings/data and selected-model repair behavior.
- Extension remains 3.2.0. No business workflow or interface redesign added.


## 6.7.1 Preview 1 — 2026-11-27

- English installer and runtime diagnostics, with an explicit Upgrade action for signed installations at the chosen destination.
- Fresh Qwen default; upgrade verifies/repairs the selected offline model while preserving existing configuration. Explicit model selection and skip remain available.
- Preflight replacement-file checks ask users to close an active client before program files are replaced.
- Reply discovery refreshed after the primary comment; broader accessible Reply/Like recognition and bounded discussion expansion.
- Random/count/all-loaded Reply selection (maximum 100), per-comment receipts, uncertain-send guards and independent main-post counting.
- Approved 6.7.1 interface refinements: reaction/browser badges, intrinsic control sizing, alignment and professional explanatory copy.
- Extension remains 3.2.0. Manual updates; no hosted service or commercial activation added.


## 6.7.0 Preview 1 — 2026-11-25 · Big Update

- Approved desktop presentation from 6.7.0-dev.4; existing business workflows retained.
- Compact workspace/session overview and live-job selection using actual job counters.
- Central Play/Stop action, truthful disabled/stopping states and reduced-motion-safe activity feedback.
- Revised navigation, semantic hardware icons/meters, clock, light/dark appearance and compact About.
- Source autosave, frozen profile settings, module execution and browser-owned sessions preserved.
- Qwen remains the default separate model download; optional DeepSeek/Vision/None and compatible-runtime detection retained.
- Extension 3.2.0. No automatic client updater, account/login management or new business workflow added.


## 6.4.0 Preview 1 — 2026-11-23 · Big Update

- Modular workflow execution with versioned registration, isolated options, normalized module counters and shared phase/deadline handling.
- Manage → Groups → Home routine; Business Suite comment handling; default-off Inbox.
- Shared Gemini rotation/admission and verified local-runtime ownership across worker stops.
- Autosave/chooser recovery, missing scope fingerprints, isolated form status and bounded/redacted worker output.
- Default Qwen model installation and optional DeepSeek/Vision/None choices; model setup output/error propagation fixed for unattended setup.
- Latest desktop UI: session overview ring, independent cursor/text colors and segmented hover/focus feedback with reduced-motion support.
- Extension 3.2.0. Existing browser profiles remain user-owned. No auto-updater or hosted brain is included.
- Protected Windows installation and artifact checks are described in the release notes; live Facebook/Messenger and clean-PC coverage remain limited.


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
