Context: Motsac — Chrome extension (Negotiation Assistant).

Current state:
- v0.1 published (Telegram only).
- Chrome developer account approved.
- Terms of Use v1.1 finalized.
- Privacy Policy v1.1 finalized.
- GA active (standard, no consent wall for MVP).
- Freemium model planned.
- AI suggestions processed server-side.
- No background monitoring of Telegram.

Goal:
Move from legal-ready MVP to working functional v0.2.

====================================================
FULL ROADMAP (PROJECT OVERVIEW)
====================================================

[0] Chrome moderation (DONE)
- Icons 16/48/128
- Landing pages
- Lite version uploaded
- Passed initial release

[1] Legal (DONE)
- Terms of Use v1.1
- Privacy Policy v1.1
- International neutral
- AI liability protected

====================================================
ROADMAP FOR v0.2 (CURRENT TARGET)
====================================================

PHASE 1 — CONSENT + IDENTITY (Core Foundation)

1. Consent screen inside extension
   - Single checkbox
   - Link to Terms
   - Link to Privacy
   - “Continue” button
   - Store consent timestamp locally
   - Log consent on server

2. Telegram bot authentication
   - User clicks “Continue”
   - Redirect to TG bot
   - Bot returns Telegram ID
   - Server binds Telegram ID to extension session
   - Minimal identity layer created

DELIVERABLE:
User identity + legal consent fully integrated.

----------------------------------------------------

PHASE 2 — CHAT PARSING (Manual Trigger Only)

3. Manual parsing only
   - No auto background scraping
   - Button: “Add new messages”
   - Extract selected messages only
   - Mark parsed messages with 🗿

4. Media files handling (optional v0.2)
   - Safe skip if complex

DELIVERABLE:
User-controlled message extraction.

----------------------------------------------------

PHASE 3 — EDIT LAYER

5. “Edit” mode
   - Show parsed messages
   - Allow word deletion → replace with [deleted]
   - Do not alter original Telegram message

6. Store edited version in indexedDB

DELIVERABLE:
User has control before sending to AI.

----------------------------------------------------

PHASE 4 — SERVER PIPELINE

7. Send edited content to server
8. Stream AI response
9. Store summary + tags
10. Delete user content after processing

DELIVERABLE:
Working AI suggestion loop.

----------------------------------------------------

PHASE 5 — UX STRUCTURE (Negotiation Framework)

Five-step interface:

(0) Result approach
(1) Current situation
(2) I want
(3) Best approaches (correct/incorrect)
(4) Forecast
(5) Reinforcement

Minimal UI.
No complexity.
Emoji limited to head + hands.

DELIVERABLE:
Structured negotiation guidance, not just raw AI output.

====================================================
WHAT REMAINS FOR v0.2 (CRITICAL PATH)
====================================================

1. Implement consent screen logic
2. Implement Telegram ID binding
3. Create server endpoint for identity
4. Implement manual message parsing
5. Implement edit layer
6. Connect streaming AI response
7. Ensure data deletion after response
8. Add changelog entry for legal foundation
9. Prepare Chrome update submission

====================================================
SUCCESS CRITERIA FOR v0.2
====================================================

- User gives consent
- User authenticated
- User manually selects messages
- User edits content
- AI returns structured output
- No background monitoring
- No automatic scraping
- No legal inconsistencies

====================================================
Next task:
Help prioritize implementation order and reduce complexity.
Focus only on critical path for v0.2.
Ignore future scaling for now.