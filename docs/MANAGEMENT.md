# Page / Profile management

Available in **6.0.0 Preview 1**, requiring extension **3.1.0**.

## Set up

1. Open a public Facebook tab in your existing signed-in browser profile. Reload the installed extension after an update.
2. In Task → Interaction & Page / Profile management choose interaction only, management only, or interaction → management. Combined mode enters management after a successful interaction cycle; errors and session stops take priority.
3. Assign the selected connection, or use the management button on each multitasking profile row. Enter its Page/Profile root URL, stable asset ID where known and exact current actor name. Switch Facebook identity manually beforehand if needed. Do not assign one asset to multiple simultaneous jobs.
4. Enable comments, relevant notifications and/or inbox. Choose inspect, draft or auto-reply independently for comments and messages. Start with **draft** and a small time/item cap.
5. Select a shared approved knowledge group and optionally provide the exact post URLs to monitor, one per line. Otherwise the adapter uses attributable rendered posts.

## Optional inbox

Inbox is **off by default**, requires a verified actor name and an explicit permitted URL. Page inbox uses `https://business.facebook.com/latest/inbox?asset_id=YOUR_PAGE_ID`; the ID must match the assigned Page. Profile inbox uses `https://www.facebook.com/messages/`. Do not paste login links or credentials.

The conservative adapter requires stable message IDs and explicit incoming/outgoing direction, verifies the active actor and thread, and ignores a last outgoing message. If this evidence is unavailable, it reports unsupported rather than guessing. This preview has simulated-browser coverage; the inbox adapter has not been validated against every real Facebook or Business Suite layout.

## Shared knowledge and token use

Enter approved business information only. FAQ lines use `Question | Answer`. An exact normalized question match uses the approved answer verbatim without AI generation. Other questions retrieve a bounded selection of relevant information for the configured model. AI follows the customer language; the interface language does not select reply language.

Knowledge groups can be reused by related assigned assets on the PC. Customer conversations are not a shared training set. Generated cache is encrypted, expires after 24 hours and is scoped by asset, channel, context and knowledge version. No automatic cross-PC upload or hosted knowledge service is included.

## Review and limits

Management-only respects its phase cap and applicable cycle limit. Combined mode has its own bounded management phase; global Stop and session deadlines remain active. Processed-item totals include inspections, saved drafts and Enter submissions. The activity log separates these; they are not confirmed Facebook deliveries.

Draft view is read-only/copy for manual review. Switching to auto does not automatically send previous drafts. Uncertain submissions are shown separately: inspect Facebook before a manual resend. The app reserves an event before sending and will not automatically replay an interrupted send. It leaves existing user drafts untouched.

Only attributable rendered posts/comments and recognized controls are processed. Hidden/unloaded content, insufficient approved facts, changed actor/thread/context, account restrictions and unsupported layouts can require manual handling. Do not use auto-reply for cases requiring human judgment without review.

[Installation](INSTALL.md) · [Privacy](PRIVACY.md) · [Support](../SUPPORT.md)
