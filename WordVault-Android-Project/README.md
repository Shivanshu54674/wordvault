# WordVault — Build Your Android App (no coding needed)

Follow these steps once. At the end you get a real APK installed on your phone.
Total time: about 15 minutes.

## Step 1 — Create a free GitHub account
Go to https://github.com/signup and sign up (free).

## Step 2 — Create a repository
1. After logging in, click the **+** (top right) → **New repository**
2. Repository name: `wordvault`
3. Keep it **Public**, click **Create repository**

## Step 3 — Upload this project
1. On the new repository page, click the link **"uploading an existing file"**
2. Open the unzipped `WordVaultAndroid` folder on your computer
3. Select EVERYTHING inside it and drag into the GitHub upload box
   (the `app` folder, `build.gradle`, `settings.gradle`, `gradle.properties`, this README, the txt file)
4. Click **Commit changes** and wait for upload to finish

## Step 4 — Add the build instruction file
The `.github` folder is hidden and usually does NOT get uploaded, so create it by hand:
1. Click **Add file** → **Create new file**
2. In the filename box type exactly: `.github/workflows/build.yml`
3. Open `WORKFLOW-FILE-CONTENT.txt` (in this folder) and copy everything **below the dashed line**
4. Paste it into GitHub's text box → **Commit changes**

## Step 5 — Download your APK
1. Click the **Actions** tab at the top of your repository
2. A build called "Build WordVault APK" will be running — wait ~5 minutes for the green ✓
3. Click on the finished run → scroll down to **Artifacts** → click **WordVault-APK** to download
4. Unzip it — inside is `app-debug.apk`

## Step 6 — Install on your phone
1. Send `app-debug.apk` to your phone (Google Drive / USB cable / email)
2. Tap the file on your phone → Android will ask to "allow installing unknown apps" → allow it
3. Install → WordVault appears in your app list

Done. The app is fully standalone — all your words are stored inside the app on your phone.
Internet is only used to auto-fetch meanings when you add a word (you can also type them manually offline).

## Troubleshooting
- **Build shows red ✗ in Actions**: click the failed run, screenshot the error, and ask Claude — usually a file landed in the wrong folder. Check that `app/build.gradle` exists (not just `build.gradle` at the top).
- **Phone blocks install**: Settings → Apps → Special app access → Install unknown apps → allow for the app you're opening the APK from (e.g., Files or Drive).
