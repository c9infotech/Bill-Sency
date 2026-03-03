# GitHub Repository Setup Guide

Step-by-step instructions to create and publish your Bill-Sency releases repository.

---

## Prerequisites

- [ ] GitHub account ([Create one](https://github.com/join) if needed)
- [ ] Git installed on your computer ([Download](https://git-scm.com/downloads))
- [ ] All release files ready:
  - `BillSency-Setup-1.0.0-beta.exe` (installer)
- [ ] This `releases-repo` folder complete with all documentation

---

## Step 1: Create GitHub Repository

### Option A: Via GitHub Website (Recommended)

1. Go to [GitHub](https://github.com)
2. Click **"+"** in top-right → **"New repository"**
3. Fill in details:
   - **Owner:** Your username or organization (e.g., `c9infotech`)
   - **Repository name:** `bill-sency-releases`
   - **Description:** "Bill-Sency Business Management System - Releases and Support"
   - **Visibility:** **Public** ✅
   - **Initialize:** Leave unchecked (we'll push existing files)
   - Don't add README, .gitignore, or license (we have them)
4. Click **"Create repository"**

### Option B: Via GitHub CLI

```powershell
# Install GitHub CLI first: winget install GitHub.cli
gh repo create bill-sency-releases --public --description "Bill-Sency Business Management System - Releases and Support"
```

---

## Step 2: Upload Files to Repository

### Navigate to releases-repo folder

```powershell
cd C:\Projects\winapp\bill-sency\releases-repo
```

### Initialize Git (if not already done)

```powershell
git init
```

### Configure Git (first time only)

```powershell
git config --global user.name "Your Name"
git config --global user.email "your.email@c9infotech.com"
```

### Add all files

```powershell
git add .
```

### Commit files

```powershell
git commit -m "Initial release documentation for v1.0.0-beta"
```

### Add remote repository

Replace `c9infotech` with your GitHub username/organization:

```powershell
git remote add origin https://github.com/c9infotech/bill-sency-releases.git
```

### Push to GitHub

```powershell
git branch -M main
git push -u origin main
```

**Note:** You may be prompted for GitHub credentials. Use a Personal Access Token if using HTTPS.

---

## Step 3: Create Personal Access Token (If Needed)

If you're using HTTPS and get authentication errors:

1. Go to GitHub → **Settings** → **Developer settings** → **Personal access tokens** → **Tokens (classic)**
2. Click **"Generate new token (classic)"**
3. Name it: "Bill-Sency Releases"
4. Select scopes:
   - ✅ `repo` (all)
   - ✅ `workflow`
5. Click **"Generate token"**
6. **Copy the token** (you won't see it again!)
7. Use this token as your password when pushing

---

## Step 4: Create First Release

### Via GitHub Website (Easier)

1. Go to your repository: `https://github.com/c9infotech/bill-sency-releases`
2. Click **"Releases"** (right sidebar)
3. Click **"Create a new release"**
4. Fill in details:
   - **Tag:** `v1.0.0-beta`
   - **Target:** `main`
   - **Release title:** `Bill-Sency v1.0.0-beta`
   - **Description:** Copy from [CHANGELOG.md](CHANGELOG.md) → [1.0.0-beta] section
   - **Attach binaries:**
     - Click "Attach binaries by dropping them here or selecting them"
     - Upload: `BillSency-Setup-1.0.0-beta.exe` (recommended)
     - Upload: `bill-sency.exe` (optional, portable version)
   - **Pre-release:** ✅ Check this box (it's a beta)
5. Click **"Publish release"**

### Via GitHub CLI

```powershell
# Navigate to where your installer is
cd C:\Projects\winapp\bill-sency\bin\Release\net8.0-windows\win-x64\publish

# Create release
gh release create v1.0.0-beta `
  --repo c9infotech/bill-sency-releases `
  --title "Bill-Sency v1.0.0-beta" `
  --notes "See CHANGELOG.md for details" `
  --prerelease `
  BillSency-Setup-1.0.0-beta.exe
```

---

## Step 5: Update README Download Links

After creating the release, update the download links in README.md:

1. Go to your release: `https://github.com/c9infotech/bill-sency-releases/releases/tag/v1.0.0-beta`
2. Right-click the installer → **Copy link address**
3. Edit `README.md` in your repository
4. Replace placeholder links with actual release URLs:

```markdown
<!-- Before -->
[Download Bill-Sency Installer](https://github.com/c9infotech/bill-sency-releases/releases)

<!-- After -->
[Download Bill-Sency Installer](https://github.com/c9infotech/bill-sency-releases/releases/download/v1.0.0-beta/BillSency-Setup-1.0.0-beta.exe)
```

5. Commit the change:

```powershell
git add README.md
git commit -m "Update download links with actual release URLs"
git push
```

---

## Step 6: Configure Repository Settings

### Enable Features

1. Go to repository **Settings**
2. Scroll to **Features** section
3. Ensure these are enabled:
   - ✅ Issues
   - ✅ Projects (optional)
   - ✅ Discussions (optional, for community Q&A)
   - ❌ Wikis (not needed, we have docs in repo)
   - ❌ Sponsorships (unless you want to accept donations)

### Add Topics (Tags)

1. Go to repository main page
2. Click **"⚙️"** next to **About**
3. Add topics:
   - `pos`
   - `business-management`
   - `inventory-management`
   - `retail`
   - `windows`
   - `point-of-sale`
   - `inventory`
   - `business-software`
4. Click **"Save changes"**

### Set Repository Image

1. Still in **About** settings
2. Click **"Choose an image"**
3. Upload your logo or app icon
4. Click **"Save changes"**

---

## Step 7: Test Everything

### Check Release

- [ ] Go to: `https://github.com/c9infotech/bill-sency-releases/releases`
- [ ] Verify v1.0.0-beta is visible
- [ ] Click installer link → Should download
- [ ] Verify "Pre-release" badge is shown

### Check Documentation

- [ ] README.md displays correctly
- [ ] INSTALLATION.md has proper table of contents
- [ ] CHANGELOG.md formats correctly
- [ ] Links work (not all will work until you replace placeholders)

### Check Issues

1. Click **"Issues"** tab
2. Click **"New issue"**
3. Verify templates appear:
   - Bug Report
   - Feature Request
   - Contact links (Documentation, Security, Support, Website)

### Test Download

1. Download the installer from GitHub
2. Verify file size matches (should be ~75 MB)
3. **Optional:** Install on a test machine to verify

---

## Step 8: Announce the Release

### Update Your Website

Add to https://c9infotech.com:

```html
<h2>Bill-Sency</h2>
<p>Business Management System</p>
<a href="https://github.com/c9infotech/bill-sency-releases/releases/latest">
  Download Now
</a>
```

### Social Media (Optional)

Share on LinkedIn, Twitter, Facebook:

```
🎉 Excited to announce Bill-Sency v1.0.0-beta!

A comprehensive business management system featuring:
✅ Point of Sale (POS)
✅ Inventory Management
✅ Financial Reports
✅ Multi-user Support
✅ Fully Customizable

Download now: https://github.com/c9infotech/bill-sency-releases

#POS #BusinessManagement #SoftwareRelease
```

---

## Future Releases Workflow

When releasing v1.0.1 or later:

### 1. Update Code

- Change version in `bill-sency.csproj`
- Update features/fixes in code

### 2. Build

```powershell
dotnet publish -c Release -r win-x64 --self-contained true /p:PublishSingleFile=true
& "C:\Program Files (x86)\Inno Setup 6\ISCC.exe" installer.iss
```

### 3. Update Documentation

- Add version to `CHANGELOG.md`
- Update version references in `README.md`
- Document new features in `INSTALLATION.md` (if needed)

### 4. Commit Documentation Updates

```powershell
cd releases-repo
git add .
git commit -m "Documentation for v1.0.1"
git push
```

### 5. Create GitHub Release

```powershell
gh release create v1.0.1 `
  --title "Bill-Sency v1.0.1" `
  --notes-file release-notes.txt `
  BillSency-Setup-1.0.1.exe
```

Or use GitHub website as in Step 4.

---

## Troubleshooting

### Authentication Failed

**Problem:** `git push` fails with authentication error

**Solution:**
- Use Personal Access Token instead of password
- Or use SSH instead of HTTPS: `git remote set-url origin git@github.com:c9infotech/bill-sency-releases.git`

### Large File Warning

**Problem:** Git warns about large files (installer is 75MB)

**Solution:**
- Don't commit installers to the repo! Only upload to Releases
- Add `*.exe` to `.gitignore` (already done)
- Installers should only exist in GitHub Releases, not in commits

### Push Rejected

**Problem:** `git push` rejected - updates were rejected

**Solution:**
```powershell
git pull --rebase origin main
git push
```

### Wrong Remote URL

**Problem:** `git push` pushes to wrong repository

**Solution:**
```powershell
git remote -v  # Check current remote
git remote set-url origin https://github.com/c9infotech/bill-sency-releases.git
```

---

## Checklist

Before going public, verify:

- [ ] Repository created and public
- [ ] All documentation files pushed
- [ ] README.md displays correctly
- [ ] v1.0.0-beta release created
- [ ] Installer uploaded to release
- [ ] Release marked as pre-release
- [ ] Issues enabled
- [ ] Issue templates working
- [ ] Topics/tags added
- [ ] About section filled
- [ ] Download link tested
- [ ] Website updated
- [ ] Announcement posted (optional)

---

## Resources

### Git Basics

- **[Git Documentation](https://git-scm.com/doc)**
- **[GitHub Docs](https://docs.github.com)**
- **[Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)**

### GitHub Features

- **[About Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)**
- **[Issue Templates](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/configuring-issue-templates-for-your-repository)**
- **[Repository Topics](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics)**

### Markdown

- **[Markdown Guide](https://www.markdownguide.org/)**
- **[GitHub Flavored Markdown](https://github.github.com/gfm/)**

---

## Need Help?

- **Git Issues:** Ask on [Stack Overflow](https://stackoverflow.com/questions/tagged/git)
- **GitHub Issues:** Contact [GitHub Support](https://support.github.com/)
- **Project Issues:** Email dev@c9infotech.com

---

## Quick Command Reference

```powershell
# Clone repository
git clone https://github.com/c9infotech/bill-sency-releases.git

# Check status
git status

# Add files
git add .

# Commit
git commit -m "Message"

# Push
git push

# Pull latest
git pull

# View remotes
git remote -v

# Create and switch to branch
git checkout -b feature-branch

# View commit history
git log --oneline

# Tag a commit
git tag v1.0.1
git push --tags
```

---

**Good luck with your release! 🚀**

---

*This guide created: March 3, 2026*
