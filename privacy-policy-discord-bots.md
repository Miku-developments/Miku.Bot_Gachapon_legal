# Privacy Policy for **Miku.Bot#6889**

**Effective date:** November 13, 2025

This Privacy Policy explains how **Miku.Bot#6889** (the “Bot”), developed and maintained by **benzene.c6h6**, collects, uses, retains, and protects information. By using or inviting Miku.Bot#6889 to your Discord server, you agree to the practices described below.

---

## 1. Data We Collect

**Command data**

* When you run `/setrole type @role`, we collect the **Server ID** and **Role ID** so the bot can ping that role when required.

**Message attachments (images)**

* When an image is sent and moderation is enabled, the Bot processes the **image attachment** to extract text via OCR (currently using a local Tesseract instance; planned migration to AWS within ~1 year).
* The Bot only accesses the image attachment(s) — it does not read or store full chat logs.

**Minimal runtime metadata**

* Transient processing metadata (e.g., timestamp, processing result, cache keys) may be used to perform the moderation check and then deleted. We do not attach this metadata to personal profiles.

---

## 2. How We Use Collected Data

* **Moderation:** Extracted text from images is analyzed for banned, vulgar, or otherwise disallowed content. If violations are detected, the Bot sends an alert to the server’s moderators or configured role(s).
* **Command functionality:** Server ID and Role ID from `/setrole` are used solely to perform role pings requested by server administrators.
* **Operational needs:** Transient data is used only to complete the processing flow (OCR → check → notify) and improve reliability. No profiling or targeted advertising is performed.

---

## 3. Storage & Retention

* We do **not** keep permanent copies of images or extracted text. All processed data is removed from cache and temporary storage immediately after the moderation check and within a short automatic expiry window.
* Role configuration from `/setrole` is retained until you remove it via `/wiperoledata` or until a server admin deletes the bot from the server.
* If required by law or valid legal request, specific data may be retained or disclosed as mandated.

---

## 4. Data Sharing & Third Parties

* We **do not sell, trade, or share** your data with advertisers or unrelated third parties.
* The Bot may transfer data to third-party services strictly for processing if/when we migrate OCR to AWS (e.g., AWS-hosted OCR or logging). Any such transfer will follow applicable security standards and provider terms.
* Data will only be disclosed to law enforcement, courts, or regulators when legally compelled.

---

## 5. Security

* We implement reasonable administrative, technical, and physical safeguards to protect data during processing and storage.
* No method of transmission or storage is 100% secure — while we work to protect your information, we cannot guarantee absolute security.

---

## 6. International Transfers

* If OCR or other processing moves to cloud providers outside your jurisdiction (e.g., AWS), data processing may occur in those locations. We will follow applicable legal requirements for cross-border transfers.

---

## 7. User Rights & Controls

* Server admins can remove stored role configuration at any time with `/wiperoledata`.
* If you need data removed outside of these commands (for example you believe something was retained), contact us (see Contact section) and we will investigate and comply where appropriate.

---

## 8. Children’s Privacy

* The Bot is not intended for use by children under applicable age limits. We do not knowingly collect personal information from children.

---

## 9. Changes to This Policy

* We may update this Privacy Policy. When we do, we will post the revised policy and update the “Effective date” above. Continued use after changes indicates acceptance.

---

## 10. Contact & Support

If you have questions, requests, or concerns about this policy or data handling:

* Join our support server: 🔗 [https://discord.gg/YybFY2uD5p](https://discord.gg/YybFY2uD5p)
* Or contact the developer: **benzene.c6h6**

---
