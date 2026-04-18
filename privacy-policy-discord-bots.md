# Privacy Policy for **Miku.N**

**Effective date:** April 19, 2026

This Privacy Policy explains how **Miku.N** (the "Bot"), application ID `876139135507763280`, developed and maintained by **benzene.c6h6** ("we," "us," or "our"), collects, uses, retains, and protects information. By using or inviting Miku.N to your Discord server, you agree to the practices described below.

---

## 1. What the Bot Does (Context for Data Use)

Miku.N is a companion bot for the **Gachapon** Discord game. Its core functions are:

* **Drop detection:** It watches messages from the Gachapon bot (user ID `815289915557675118`) that match a card-drop pattern.
* **Image OCR:** When Gachapon posts a drop image, the Bot downloads the image and runs local OCR (Tesseract) to read character names, series, rarity/global-wishlist numbers, and print IDs from the card art.
* **Wishlist matching:** Extracted card info is compared against a **global wishlist database** (aggregated character/series data), and users who have wished those characters are pinged in the channel where the drop occurred.
* **Mission & statistics display:** Provides aggregate bot-wide statistics (`/botinfo`, `/mission`).
* **Optional token/premium features:** Tracks server- and user-level token balances and premium status for servers/users who opt in via Ko-fi or are granted premium by the bot owner.

Processing is performed only on messages that match the Gachapon drop pattern. The Bot does not read, log, or store general chat messages.

---

## 2. Data We Collect

### 2.1 Discord IDs

To **provide premium/token features**, the Bot stores the following in local JSON files:

* **User ID** — only for users who:
  * Have a non-zero token balance,
  * Have an active monthly plan,
  * Have been granted premium by the bot owner, or
  * Have toggled personal token spending.

  Associated fields: token balance, monthly-plan expiry timestamp, premium flag, personal token-spending toggle, lifetime token totals.

* **Server (Guild) ID** — only for servers that:
  * Have a non-zero token balance,
  * Have been granted premium by the bot owner, or
  * Have the server token-spending toggle changed from default.

  Associated fields: token balance, premium flag, server token-spending toggle.

No usernames, display names, emails, avatars, or other profile data are stored.

### 2.2 Card-drop processing (transient)

When a Gachapon drop is detected:

* The Bot temporarily downloads the drop image to disk to run OCR.
* Extracted text (character names, series, rarity numbers, print IDs) is held in memory only long enough to match the wishlist, format the ping message, and send it.
* Temporary images are automatically deleted by a cleanup task (runs every hour) and are not retained long-term.

The Bot does **not** store extracted card text, per-user drop history, or who owned/claimed which card.

### 2.3 Aggregate statistics (non-personal)

The Bot maintains anonymous aggregate counters (e.g. total drops scanned, total cards scanned, per-rarity counts, total wishes matched). These contain no user or server identifiers.

### 2.4 Wishlist / character database

The Bot maintains a global database of Gachapon characters, series, and emoji mappings. This is reference data about the game and does **not** contain personal Discord data.

### 2.5 Runtime metadata

Transient data such as timestamps, latency metrics, shard status, and in-memory caches are used only to operate the Bot and are not tied to identifiable users.

---

## 3. How We Use Collected Data

* **Core functionality:** Detect Gachapon drops, OCR card images, match cards against the wishlist, and ping users whose wishes matched.
* **Premium & tokens:** Track balances, consume tokens for drops that cost tokens, apply monthly plans, and enforce premium entitlements.
* **Bot health & debugging:** Log errors and operational events to the developer's private logging webhooks. Logs do not include chat content.
* **Public listings:** Server count (not member data) may be posted to **top.gg** for bot-listing purposes.

We do **not** use collected data for advertising, profiling, or resale.

---

## 4. Storage & Retention

* **User & server records (`premium/users.json`, `premium/servers.json`):** Retained while the user/server has an active balance, plan, premium flag, or non-default toggle. Records are automatically purged when all fields return to default (no balance, no plan, no premium, default toggle).
* **Card drop images:** Stored only on the Bot's host during processing, then deleted by the hourly cleanup task.
* **Aggregate statistics:** Retained indefinitely in anonymized form.
* **Wishlist / character database:** Retained indefinitely as reference data.
* **Logs and webhook notifications:** Retained according to Discord's own data retention for the webhook channels.

You may request earlier deletion of your user or server record via the support server listed below.

---

## 5. Data Sharing & Third Parties

We do **not** sell, trade, rent, or share personal data with advertisers or unrelated third parties. Data is processed by the following services only to the extent needed to run the Bot:

* **Discord** — hosts messages, attachments, and slash-command traffic the Bot sees.
* **Tesseract OCR** — runs **locally** on the Bot's host; card images are not sent to any third-party OCR service.
* **Ko-fi** (`ko-fi.com`) — used for optional token and premium purchases; payment processing occurs entirely on Ko-fi's platform under Ko-fi's own privacy policy. The Bot only learns of purchases through Ko-fi's standard mechanisms and does not receive payment-card data.
* **top.gg** — receives only the Bot's total server count for listing purposes.
* **GitHub** — the Bot's source code is managed in a Git repository; operational data (user/server JSON files, wishlist data) may be committed to a private repository by scheduled maintenance tasks. No chat content or card drop images are committed.

Data will only be disclosed to law enforcement, courts, or regulators when legally compelled.

---

## 6. Security

We implement reasonable technical and administrative safeguards to protect data during processing and storage (scoped file access, restricted owner-only admin commands, no public exposure of JSON stores). No method of transmission or storage is 100% secure; we cannot guarantee absolute security.

---

## 7. International Transfers

The Bot may be hosted in regions different from your own. By using the Bot you acknowledge that the limited data described above (primarily Discord IDs and token balances) may be processed in those regions in accordance with applicable law.

---

## 8. User Rights & Controls

* **View your balance/status:** Use `/balance` or `M.balance`.
* **Toggle personal token spending:** Available on the `/balance` message (green = on, red = off).
* **Toggle server token spending:** Available to members with **Manage Server** or **Administrator** permission, on the `/balance` message.
* **Remove the Bot:** Kicking the Bot stops all future processing for that server. Existing server records can be deleted on request.
* **Data deletion request:** Contact us via the support server to have your user ID or server ID removed from persistent storage. Aggregate counters cannot be reversed because they contain no identifiers.

---

## 9. Children's Privacy

The Bot is intended for users who meet Discord's minimum age requirements in their jurisdiction. We do not knowingly collect personal information from children below those ages. If you believe a child has submitted data to the Bot, please contact us for removal.

---

## 10. Changes to This Policy

We may update this Privacy Policy as the Bot evolves. When we do, we will update the "Effective date" above. Continued use after changes indicates acceptance.

---

## 11. Contact & Support

If you have questions, requests, or concerns about this policy or data handling:

* Support server: [https://discord.gg/d8wah6chGs](https://discord.gg/d8wah6chGs)
* Developer: **benzene.c6h6**

---
