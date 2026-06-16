# NOBSED Engineering Ltd — Website Handover

Built by **Forge Technologies**. Static HTML/CSS/JS site — no build step, no server needed.

**Live site:** https://ramzy-tla.github.io/Nobsed/
**Repository:** https://github.com/ramzy-tla/Nobsed

---

## ⚠️ ONE REQUIRED STEP — Activate the contact form

The contact form is wired to **Web3Forms** (free forever, unlimited submissions). It will
**not deliver emails until an access key is set**. One-time setup:

1. Go to **https://web3forms.com**
2. Enter the company email — `nobsedengineering@gmail.com` — and click **Create Access Key**
3. Confirm via the email Web3Forms sends
4. Open `contact.html`, find line ~217:
   ```html
   <input type="hidden" name="access_key" value="YOUR_WEB3FORMS_KEY">
   ```
   Replace `YOUR_WEB3FORMS_KEY` with the key they email you
5. Commit & push — the form will then deliver every enquiry straight to the Gmail inbox.

Until this is done, the form shows a "sent" state but no email arrives.

---

## Changing the logo

The logo is a **single file**: `images/Logo.png`. Replace that one file (keep the same
name) and it updates the navbar, mobile menu, and favicon across **all pages** automatically.

Notes for the new logo:
- The navbar shows the logo in **white** (via a CSS filter), so a transparent-background PNG
  works best. If the new logo is full-colour and the white filter looks wrong, tell Forge and
  we'll remove the filter for that logo.
- The social-share preview image (`images/og-preview.jpg`) has the old logo baked in — ask
  Forge to regenerate it after a logo change.

---

## Optional polish (not blocking)

- **Social links:** the Facebook and Instagram icons in the footer currently link to `#`
  (placeholders). Send Forge the real page URLs to wire them up. WhatsApp & phone already work.
- **Domain:** the site lives at the GitHub Pages URL above. A custom domain (e.g.
  `nobsedengineering.com`) can be pointed at it any time.

---

## Deploying changes

Every `git push` to the `main` branch auto-publishes to the live site within ~1–2 minutes.
No other steps. Images live in `images/` (logos, service photos) and `images/projects/`
(portfolio). To view locally, open `index.html` in a browser or run any static server.
