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

## Backups (important)

Data lives only in this app on this phone. Export a backup file from the settings
gear every week or after big entries, and keep it in iCloud Drive. If you delete
the Home Screen app, its data is deleted too.

## Updating the app later

Replace the changed files on GitHub, and change `VERSION` at the top of `sw.js`
(for example `site-ledger-v2`). Open the app twice and the new version loads.
Your data is not affected by updates.
