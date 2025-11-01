# GitHub Repository Setup Instructions

Your privacy policy repository is ready to push to GitHub!

## Manual Setup Steps

Since GitHub CLI is not available, follow these steps:

### Step 1: Create Repository on GitHub

1. Go to: **https://github.com/thegrovelabs** (or your organization)
2. Click the **"+"** button in the top right → **"New repository"**
3. Repository settings:
   - **Name**: `timeletters-privacy`
   - **Description**: Privacy policy for Time Letters mobile app
   - **Visibility**: Public ✅
   - **Initialize**: ❌ DO NOT check "Add a README", ".gitignore", or license
4. Click **"Create repository"**

### Step 2: Add Remote and Push

After creating the repository, GitHub will show you commands. Run these:

```bash
cd /Users/henryye/Dev/timeletters-privacy

# Add the GitHub remote
git remote add origin git@github.com:thegrovelabs/timeletters-privacy.git

# Push to GitHub
git branch -M main
git push -u origin main
```

Or copy the exact commands GitHub provides you!

### Step 3: Enable GitHub Pages

1. Go to your repository: **https://github.com/thegrovelabs/timeletters-privacy**
2. Click **Settings** tab
3. Scroll to **Pages** section (left sidebar)
4. Under **Source**:
   - Select **Branch**: `main`
   - Select **Folder**: `/` (root)
5. Click **Save**
6. Wait 1-2 minutes for deployment

### Step 4: Verify

Visit your privacy policy at:
**https://thegrovelabs.github.io/timeletters-privacy/**

You should see your styled privacy policy page.

### Step 5: Update Your App

The app already points to the new URL! Just verify the URL in Settings.tsx is:
```
https://thegrovelabs.github.io/timeletters-privacy
```

If it needs updating, change line 401 in `src/components/Settings.tsx`

## Done! ✅

Your privacy policy is now hosted in its own dedicated repository at:
- **Repository**: https://github.com/thegrovelabs/timeletters-privacy
- **Public URL**: https://thegrovelabs.github.io/timeletters-privacy/

## Future Updates

To update the privacy policy:
1. Edit `/Users/henryye/Dev/timeletters-privacy/index.html`
2. Commit and push:
   ```bash
   cd /Users/henryye/Dev/timeletters-privacy
   git add .
   git commit -m "Update privacy policy"
   git push
   ```
3. GitHub Pages will auto-deploy in 1-2 minutes

## Benefits of Separate Repository

✅ Isolated from main codebase
✅ Version history specific to legal documents
✅ Can share with legal team without codebase access
✅ Cleaner separation of concerns
✅ Professional appearance
✅ Easy to update independently


