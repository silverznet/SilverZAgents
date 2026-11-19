# Data and privacy

SilverZAgents uses browser connection metadata to direct user-started tasks to the intended Facebook tab/profile. It does not import/export browser profiles, cookies, passwords or Facebook accounts, or scan browser history/account databases.

Task data can include user-provided content, selected post text/comments/images, task configuration, local action reservations, history and logs. Local application data is stored on the user's PC. API keys and local connection credentials use Windows user-bound encryption where supported by the application.

Online inference sends the necessary context to the AI service configured by the user; that provider's policies, retention and fees apply. Offline inference uses the installed local model. Facebook/browser traffic and software/model downloads still use the network. This is not a claim that Windows, browsers and third-party providers send no telemetry.

The optional shared-knowledge feature is disabled by default. When deliberately configured, it exchanges signed guidance and allowed aggregate workflow statistics; it is not automatic training of a shared model. No hosted knowledge endpoint is included with this preview.

Reset/cache cleanup acts on application-owned files only. It does not erase browser logins, content folders, models or task history/memory. Reset removes task/connection settings and UI preferences; cache cleanup preserves settings.

Do not publish API keys, credentials, browser exports, raw task memory/databases, full logs or unredacted personal content in GitHub issues. Contact **hello@silverz.net** for private support arrangements.
