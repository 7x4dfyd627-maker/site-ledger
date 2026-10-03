# Site Ledger

Construction expense tracker for iPhone. Runs from GitHub Pages, installs to the
Home Screen, works offline, and creates PDF reports. Data stays on your phone.

## Put it on GitHub (one time)

1. Go to github.com, tap **+**, then **New repository**. Name it `site-ledger`. Choose **Public** (free GitHub Pages needs a public repo; your expenses are NOT in these files, so nothing private is published).
2. In the new repo, tap **Add file**, then **Upload files**. Upload everything in this folder, keeping the `fonts`, `icons` and `vendor` folders. Do NOT upload your data file (`House-D-18-data.json`).
3. Tap **Commit changes**.
4. Open **Settings**, then **Pages**. Under Source pick **Deploy from a branch**, branch `main`, folder `/ (root)`, tap **Save**.
5. Wait 1 to 2 minutes. Your app is at `https://YOUR-USERNAME.github.io/site-ledger/`.

## Install on iPhone

1. Open that link in **Safari** (not Chrome).
2. Tap **Share**, then **Add to Home Screen**, then **Add**.
3. Open it from the Home Screen icon. It now runs full screen and offline.

## Load the existing D-18 expenses

1. Save `House-D-18-data.json` to the iPhone Files app (AirDrop, iCloud Drive or WhatsApp to yourself, then Save to Files).
2. In the app tap **Import backup file** (on the empty screen, or under the settings gear) and pick the file.

## Daily use

- **Add expense**: type amounts as `52000`, `52k`, `1.6m`, `2 lakh` or `1.5 crore`.
- Tap any row to edit or delete it.
- **PDF**: pick a period and categories, tap **Create PDF**, then share to WhatsApp, Mail or Files.
- **Settings gear**: project name, budget, extra categories, backup, CSV for Excel.

## Money sent and balance

- Open the **Money sent** tab. The first time, type the name of the person you send money to.
- Tap **Record money sent** each time you transfer. Enter the PKR amount that reached him, the date, and optionally the AED you paid (the app shows the rate).
- Balance = money sent minus expenses he paid. A red balance means he has spent more than you sent.
- Every expense is counted against his balance unless you set **Paid by** to **Me directly** on that expense.
- The Statement shows each transfer and expense with the running balance. PDF reports include it, with opening and closing balance for the chosen period.

## Sync across iPhone, iPad and Mac

Your data is saved to a private file (a "secret gist") in your own GitHub account, and every device you connect shows the same data.

**Create the token (once, on the Mac is easiest)**
1. Go to github.com, tap your photo, then **Settings**.
2. Scroll down to **Developer settings**, then **Personal access tokens**, then **Tokens (classic)**.
3. Tap **Generate new token**, then **Generate new token (classic)**.
4. Note: `Site Ledger`. Expiration: **No expiration** (or 1 year, if you prefer to renew).
5. Under scopes, tick **only `gist`**. Nothing else.
6. Tap **Generate token** and copy it (starts with `ghp_`). GitHub shows it only once, so keep it in your Notes or password manager.

**Connect each device**
1. Open the app, tap the **settings gear**.
2. Under **Sync across devices**, paste the token and tap **Connect**.
3. The first device uploads its data. Every later device downloads it and merges anything it already had.

**After that**
- Changes sync by themselves about a second after you save, and whenever you open the app.
- The line under the project name shows **Synced** with the time. If it shows **Not synced**, tap it to retry. Changes made offline sync when you are back online.
- Deletions sync too.
- If a phone is lost, delete the token on GitHub (same Tokens page). Your data stays in GitHub; make a new token for your other devices.
- Do not edit or delete the gist named "Site Ledger data" on GitHub.

## Backups (important)

With sync on, your data is safe in GitHub. Still export a backup file now and then
and keep it in iCloud Drive. Without sync, data lives only on that device, and
deleting the Home Screen app deletes it too.

## Updating the app later

Replace the changed files on GitHub, and change `VERSION` at the top of `sw.js`
(for example `site-ledger-v2`). Open the app twice and the new version loads.
Your data is not affected by updates.
