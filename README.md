# Canvas

Task, Schedule and Note cards on a black canvas. Drag them anywhere.

## What's in this folder

| File | What it does |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | App name, icon and colors, used when someone adds it to a home screen |
| `icons/` | App icons for phones, tablets and browser tabs |
| `vercel.json` | Tells Vercel not to cache old versions, so testers always get your latest update |

## Put it online (GitHub + Vercel)

### 1. Create the GitHub repository
1. Go to github.com and click **+** (top right), then **New repository**.
2. Name it `canvas` (any name works). Choose **Public** or **Private** (both work with Vercel).
3. Leave everything else unchecked and click **Create repository**.
4. On the next page, click the link **uploading an existing file**.
5. Unzip `canvas-web.zip`, open the `canvas-web` folder, select **everything inside it** (including the `icons` folder) and drag it onto the GitHub page. `index.html` must sit at the top level of the repository, not inside a subfolder.
6. Click **Commit changes**.

### 2. Deploy on Vercel
1. Go to vercel.com and click **Add New…**, then **Project**.
2. Under **Import Git Repository**, find your repository and click **Import**. (If it's missing, click **Adjust GitHub App Permissions** and give Vercel access to the repository.)
3. Set **Framework Preset** to **Other**. Leave Build Command and Output Directory empty.
4. Click **Deploy**. After about 30 seconds you get a web address like `canvas-yourname.vercel.app`.
5. Optional: under **Settings → Domains** you can change the name, for example to `ryan-canvas.vercel.app` if it's free.

### 3. Share with testers
Send them the Vercel address. No accounts are needed.

**To install it like an app:**
- **iPhone / iPad:** open the link in **Safari**, tap the **Share** button, then **Add to Home Screen**.
- **Android:** open it in Chrome, tap the **⋮** menu, then **Add to Home screen** or **Install app**.
- **Computer:** in Chrome or Edge, click the install icon at the right end of the address bar.

## Updating the app later
Replace `index.html` in the GitHub repository (open the file, click the pencil icon or **Add file → Upload files**, then commit). Vercel republishes automatically within a minute, and testers get the new version the next time they open or refresh it.

## Good to know
- **Where lists are saved:** each person's lists are saved in their own browser on that device. Testers never see each other's lists. Lists don't sync between a person's phone and computer yet; that would need sign-in and a database (for example Supabase or Firebase).
- **Clearing browser data** (or using a private window) erases the lists on that device.
- **Font:** the app uses Aptos Display where the device has it (Windows, or Macs with Microsoft Office). iPhones and iPads fall back to Apple's system font.
