# FourTech LLC — Website & Email Setup Guide

The cheapest reliable setup: **free website hosting on GitHub Pages + one domain you buy (~$11/yr) + free email forwarding.** Total first-year cost is basically just the domain.

Your website file (`index.html`) is already built and ready to publish. Work through the steps below in order. Total time: about 30–45 minutes.

---

## What it costs

| Item | Provider | Cost |
|---|---|---|
| Website hosting | GitHub Pages | **Free** |
| Domain name | Porkbun | **~$11/year** |
| Business email (info@yourdomain) | ForwardEmail (forwarding to your Gmail) | **Free** |
| Contact form | Formspree free plan | **Free** (up to 50 submissions/mo) |
| **Total** | | **~$11 for the first year** |

> Note: The website file currently uses **fourtechconsulting.net** and **info@fourtechconsulting.net**. If you buy a different domain, tell me and I'll swap it everywhere before you publish.

---

## Step 1 — Buy your domain (~$11)

1. Go to **porkbun.com**.
2. Search for **fourtechconsulting.net** (or your chosen name). Porkbun shows live availability — if it's taken, try `fourtechmd.com`.
3. Add it to the cart and create an account. **Leave "WHOIS privacy" ON** (it's free and hides your home address).
4. Skip every upsell — you do **not** need their hosting, email, or SSL add-ons. GitHub gives you hosting and HTTPS for free.
5. Check out. That's your only cost.

---

## Step 2 — Publish the website on GitHub Pages (free)

1. Create a free account at **github.com**.
2. Click **+ → New repository**. Name it exactly:
   **`f4ourtech-lang.github.io`** (this must match your GitHub username exactly). Set it to **Public** and click **Create repository**.
3. On the new repo page, click **uploading an existing file**.
4. Drag in the **`index.html`** file I created. Commit the change.
5. Your site is now live at **`https://f4ourtech-lang.github.io`** within a minute or two.

---

## Step 3 — Connect your domain to GitHub (free)

**In GitHub:**
1. In your repository, go to **Settings → Pages**.
2. Under **Custom domain**, type `fourtechconsulting.net` and click **Save**.
3. Tick **Enforce HTTPS** (may take an hour to become available — that's normal).

**In Porkbun (DNS records):**
1. Open your domain → **DNS** / **DNS Records**.
2. Add these **four A records** (Type: A, Host: blank or `@`), one per line:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
3. Add one **CNAME record**: Host `www`, Answer/Target `f4ourtech-lang.github.io`
4. Save. DNS can take 15 minutes to a few hours to take effect. Once it does, `fourtechconsulting.net` loads your site with a secure padlock.

---

## Step 4 — Set up free business email (info@fourtechconsulting.net)

This lets email sent to **info@fourtechconsulting.net** land in your normal Gmail inbox — for free.

1. Go to **forwardemail.net** and sign up (free).
2. Add your domain **fourtechconsulting.net**.
3. It gives you a few DNS records (an **MX** record and a **TXT** record). Add them in Porkbun's DNS panel, same place as Step 3.
4. Create the alias: **info@fourtechconsulting.net → f4our.tech@gmail.com**.
5. Test it: email info@fourtechconsulting.net from your phone — it should arrive in your Gmail.

**Optional — reply *as* info@fourtechconsulting.net from Gmail:** In Gmail go to Settings → Accounts → "Send mail as" → add the address. (Sending-as needs an SMTP step; ForwardEmail's docs walk you through it, or upgrade to their ~$3/mo plan for one-click sending.)

---

## Step 5 — Turn on the contact form (free)

The website has a working contact form; it just needs a free Formspree endpoint.

1. Sign up at **formspree.io** (free plan).
2. Create a new form; connect it to **f4our.tech@gmail.com**.
3. Formspree gives you a form URL like `https://formspree.io/f/abcdwxyz`.
4. Send me that URL (or open `index.html`, find `YOUR_FORM_ID`, and replace it with your ID). Submissions will then arrive in your inbox.

---

## Quick reference — what to give me next

To finish wiring everything, I just need:
- **Your final domain** (if not fourtechconsulting.net)
- **Your GitHub username** (so I can set the exact CNAME/site URL)
- **Your Formspree form URL** (to activate the contact form)

Send those and I'll update the site file so it's 100% ready to upload.
