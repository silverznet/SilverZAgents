<p align="center"><img src="assets/silverz-brand.png" width="112" alt="SilverZ logo"></p>
<h1 align="center">SilverZAgents</h1>
<p align="center">A Windows desktop workspace for supervised Facebook workflows.</p>
<p align="center"><strong>Windows x64 · Online & on-device AI · Public Preview</strong></p>
<p align="center"><a href="https://github.com/silverznet/SilverZAgents/releases">Download</a> · <a href="docs/INSTALL.md">Installation</a> · <a href="docs/README.vi.md">Tiếng Việt</a> · <a href="https://silverz.net">Website</a></p>

## About

SilverZAgents helps you configure and supervise repeatable Facebook tasks using browser profiles you already use. Choose prepared content or contextual AI, define run limits, and follow each profile's activity in one desktop panel.

**This is the official distribution and documentation repository.** The proprietary application source is not published here. Download the protected Windows installer from **Releases**. GitHub's automatically generated “Source code” archives contain this repository's public documentation, not the application.

## Big Update · 6.0.0 Preview 1

Page/Profile management now runs independently or after a successful interaction cycle. Assign the exact target to each connected browser profile; choose inspect, draft or auto-reply separately for comments and optional inbox handling. Inbox is **off by default**. [Management guide](docs/MANAGEMENT.md).

Approved FAQ can be reused without AI calls. Generated replies use an asset-scoped encrypted local cache; private conversations are not shared between accounts. The conservative inbox adapter is not verified against every live Facebook layout and will block uncertain sends.

## Capabilities

| Area | Available workflows |
|---|---|
| Reactions & comments | Like, alternating Like/Love, or selected random reactions; prepared text or contextual AI comments |
| Page / Profile management | Explicit per-connection assignments, relevant notifications, owned-post comment replies, optional inbox, encrypted drafts and uncertain-send review |\n| Group publishing | Status, images, multiple images, text + images, website/Facebook URLs, and Facebook Share workflows |
| Multiple profiles | Concurrent connected profiles across Chrome, Edge, Brave and Cốc Cốc; independent job details and limits |
| Run control | One run or loops, time/item limits, scheduled breaks, total stop limits, independent Home or Groups interaction scope and refresh |
| AI options | Configured online providers with fallback, or local Qwen/DeepSeek Distill/text-and-image model options |
| Visibility | Activity log, per-job counters, timing, model metrics, browser cursor labels and optional completion notification |
| Local state | Persistent task memory, optional local knowledge assistance, settings reset and cache cleanup |
| Interface | Vietnamese/English, light/dark appearance, reduced motion and saved window placement |

Browser/website behavior may vary by version, account, permissions and Facebook UI changes. A submitted item is not proof that Facebook published it or that a group administrator approved it.

## Get started

1. Download **SilverZAgents-6.0.0-preview.1-Setup.exe** and **SHA256SUMS.txt** from the [6.0.0 Preview 1 release](https://github.com/silverznet/SilverZAgents/releases/tag/v6.0.0-preview.1).
2. Verify the download and run the installer. Internet access is required for missing Python/dependencies. See [installation](docs/INSTALL.md).
3. Enable the included extension in each browser profile you intend to use. All profiles on that PC can use the same installed `extension` folder.
4. Open a supported Facebook tab in your existing signed-in profile, configure a small task, and start the session yourself.

There are no bundled accounts or API keys. Facebook browser sessions remain in the user's browser. Closing the panel with **X** minimizes it; use **Settings → Exit application** to exit fully.

## AI and privacy

- **Online:** Gemini multi-key → DeepSeek → Grok → OpenAI, using only providers configured by the user and the selected starting point. Provider fees, limits and availability apply.
- **Offline:** local inference after the chosen model/runtime is installed. Models are separate downloads; CPU/GPU/RAM determine speed. Facebook and initial downloads still require Internet.
- Prepared text and image-only publishing do not need an AI call for content generation.
- When optional inbox management is enabled, the necessary customer-message context may also be sent to the selected online provider.\n- Selected post text, comments or images needed for a task may be sent to the chosen online AI provider. Task history, memory and logs are stored locally. See [privacy](docs/PRIVACY.md).
- Shared-knowledge synchronization is optional and disabled by default; this preview does not include a hosted service.

## Preview status

6.0.0 Preview 1 is a **public preview**, not a production certification. Automated and simulated-browser tests have been run; complete validation on clean customer PCs and every real Facebook/browser combination is still pending. No claims of guaranteed reach, account safety, or uninterrupted compatibility are made.

Core Python modules are compiled and selected resources are encrypted; browser extension code remains inspectable. Code protection is not a guarantee against reverse engineering. Internal payload signatures are not a Windows Authenticode certificate; Windows may display publisher/reputation warnings. Confirm the source and checksum according to your organization's installation policy.

Automatic client updates and commercial license activation are not included in this preview. Updates are installed manually from Releases.

## Support & ownership

[Installation & troubleshooting](docs/INSTALL.md) · [Support](SUPPORT.md) · [Security reports](SECURITY.md) · [Changelog](CHANGELOG.md)

Use only accounts and content you are authorized to manage, respect group rules and platform terms, and review AI-generated content. Do not use the software for spam or to bypass account restrictions.

© 2026 **SilverZ.Net** · Developed by **Phạm Hồng Quang**  
Contact: **hello@silverz.net** · [silverz.net](https://silverz.net)

Proprietary software. Public availability does not make the application open source. See [LICENSE.txt](LICENSE.txt) and the third-party notices included with the installer.
