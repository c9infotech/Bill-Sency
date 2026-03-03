# Installation Guide

Complete installation instructions for Bill-Sency Business Management System.

---

## Table of Contents

- [System Requirements](#system-requirements)
- [Download](#download)
- [Installation](#installation)
- [First-Time Setup](#first-time-setup)
- [Installing Demo Apps](#installing-demo-apps)
- [Troubleshooting](#troubleshooting)
- [Uninstallation](#uninstallation)
- [Upgrading](#upgrading)

---

## System Requirements

### Minimum Requirements
- **Operating System:** Windows 10 (64-bit) or later
- **Processor:** Intel Core i3 or equivalent
- **RAM:** 4 GB
- **Disk Space:** 500 MB free space
- **Display:** 1366 x 768 resolution

### Recommended Requirements
- **Operating System:** Windows 11 (64-bit)
- **Processor:** Intel Core i5 or better
- **RAM:** 8 GB or more
- **Disk Space:** 2 GB free space (for data and backups)
- **Display:** 1920 x 1080 resolution or higher
- **Peripherals:** Barcode scanner, thermal printer (for POS)

### Network Requirements
- **Internet:** Not required (offline-first application)
- **Network:** Optional for multi-user installations

---

## Download

### Latest Version: 1.0.0-beta

**Windows Installer:**
- **File:** `BillSency-Setup-1.0.0-beta.exe`
- **Size:** 75.3 MB
- **Download:** [GitHub Releases](https://github.com/c9infotech/bill-sency-releases/releases/latest)

---

## Installation

**Best for:** Most users, permanent installation

#### Step 1: Download the Installer

Download `BillSency-Setup-1.0.0-beta.exe` from the [releases page](https://github.com/c9infotech/bill-sency-releases/releases).

#### Step 2: Run the Installer

1. **Double-click** the downloaded file
   
2. **User Account Control (UAC) Warning:**
   ```
   "Do you want to allow this app from an unknown publisher 
   to make changes to your device?"
   ```
   - Click **"Yes"**
   - ✅ This warning is expected for beta software without a code signing certificate
   - ✅ The software is safe - this is normal for unsigned applications

#### Step 3: License Agreement

1. Read the End User License Agreement (EULA)
2. Select **"I accept the agreement"**
3. Click **"Next"**

#### Step 4: Choose Destination

1. **Default location:** `C:\Program Files\Bill-Sency`
2. To change, click **"Browse..."** and select a different folder
3. Click **"Next"**

#### Step 5: Select Additional Tasks

Optional tasks:
- ☑️ **Create a desktop icon** (recommended)
- ☑️ **Create a Quick Launch icon**

Click **"Next"**

#### Step 6: Ready to Install

1. Review your choices
2. Click **"Install"**
3. Installation takes about 30 seconds

#### Step 7: Completing Installation

1. ☑️ **Launch Bill-Sency** (checked by default)
2. Click **"Finish"**

The application will start automatically.

---

## First-Time Setup

When you launch Bill-Sency for the first time:

### Step 1: Automatic Configuration

The application automatically configures itself:
- Creates database in `%APPDATA%\BillSency\`
- Applies database migrations
- Sets up default configuration

**No manual configuration needed!**

### Step 2: Login

The login window appears:

- Enter your credentials (provided with installation)
- **Optional:** Check **"Remember me"** to save credentials
- **Important:** Change your password immediately after first login

Click **"Login"**

### Step 3: First Time Setup Window

You'll see the First Time Setup wizard with available apps:

**Demo Apps Available:**
- ✅ **POS System** - Point of Sale with inventory
- ✅ **Core Modules** - Essential system components

**To install an app:**
1. Click **"Install"** next to the app
2. Wait for download and installation (1-2 minutes)
3. Status shows "Installed ✓" when complete

**To skip setup:**
- Click **"Continue"** to start with empty system

### Step 4: Main Window

After setup, you'll see the main window with:
- **Dashboard** (if apps are installed)
- **Developer Studio** - Create custom DocTypes
- **System Settings** - Configure users, roles, etc.

---

## Installing Demo Apps

### From First Time Setup

1. On first launch, click **"Install"** next to desired apps
2. Apps download and install automatically

### From Main Window (After Setup)

1. Click **"File"** → **"App Management"**
2. Click **"Download from Server"**
3. Enter API credentials if prompted
4. Select apps to install
5. Click **"Install"**

### Manual Installation (App Package Files)

If you have app package files:

1. Click **"File"** → **"App Management"**
2. Click **"Import App"**
3. Select the app package file
4. Click **"Install"**

---

## Troubleshooting

### Issue: "Unable to open database file"

**Cause:** Permissions issue or conflicting database locations

**Solution:**
1. Close Bill-Sency completely
2. Delete: `%APPDATA%\BillSency\config.json`
3. Delete: Any `billsency.db` files in Bill-Sency folders
4. Restart Bill-Sency - it will auto-configure

### Issue: Windows SmartScreen Block

**Message:** "Windows protected your PC"

**Solution:**
1. Click **"More info"**
2. Click **"Run anyway"**
3. This is expected for unsigned beta software

### Issue: "Unknown Publisher" Warning

**Message:** UAC shows "Unknown Publisher"

**Solution:**
- Click **"Yes"** to continue
- This is normal for software without a code signing certificate
- The software is safe and from C9 Infotech

### Issue: Login Fails

**Problem:** Can't login with provided credentials

**Solution:**
1. Make sure you're using the correct credentials (case-sensitive)
2. Contact support@c9infotech.com for credential assistance
3. If still fails, delete `%APPDATA%\BillSency\` folder and restart

### Issue: Application Won't Start

**Symptoms:** Nothing happens when launching

**Solutions:**
1. **Check if already running:**
   - Press `Ctrl+Shift+Esc` to open Task Manager
   - Look for `bill-sency.exe` under Processes
   - End task if found, then try again

2. **Run as Administrator:**
   - Right-click `bill-sency.exe`
   - Select **"Run as administrator"**

3. **Verify all components:**
   - The installer includes all required components

### Issue: "Error applying database migrations"

**Cause:** Database corruption or locked file

**Solution:**
1. Close Bill-Sency
2. Navigate to: `%APPDATA%\BillSency\`
3. Rename `billsency.db` to `billsency.db.backup`
4. Restart Bill-Sency (creates fresh database)
5. Import backup if needed

### Issue: Image Upload Errors

**Message:** "Access to path denied"

**Cause:** Permissions issue (should be fixed in this version)

**Solution:**
- Already fixed - images go to `%APPDATA%\BillSency\Uploads\Images\`
- If still occurs, report as bug

---

## Uninstallation

1. Open **"Settings"** → **"Apps"** → **"Apps & features"**
2. Find **"Bill-Sency"**
3. Click **"Uninstall"**
4. Uninstaller will ask:
   ```
   "Do you want to remove database and configuration files?"
   ```
   - **Yes:** Deletes all data in `%APPDATA%\BillSency\` (complete removal)
   - **No:** Keeps your data (can reinstall later)

### Manual Data Removal
   - Delete folder: `%APPDATA%\BillSency\`

---

## Upgrading

### From Beta to Production

When version 1.0.1 or higher is released:

1. **Backup your data first:**
   - Copy folder: `%APPDATA%\BillSency\` to safe location

2. **Download new version**

3. **Install over existing:**
   - Installer will detect old version
   - Your data will be preserved
   - Database will be upgraded automatically

### Backup Before Upgrading

**Important data locations:**
- Database: `%APPDATA%\BillSency\billsency.db`
- Uploads: `%APPDATA%\BillSency\Uploads\`
- Config: `%APPDATA%\BillSency\config.json`

**Backup procedure:**
1. Close Bill-Sency
2. Open File Explorer
3. Paste: `%APPDATA%\BillSency`
4. Copy entire folder to backup location
5. Note the backup date

---

## Post-Installation

### Recommended Steps

1. **Create Additional Users:**
   - Go to **"System"** → **"User Management"**
   - Create users with appropriate roles

2. **Configure Printers:**
   - Go to **"Settings"** → **"Printer Settings"**
   - Add thermal printers for POS

3. **Import Business Data:**
   - Use **"File"** → **"Import"** for products, customers, etc.

4. **Customize Print Formats:**
   - Go to **"System"** → **"Print Format Management"**

5. **Set Up Backups:**
   - Schedule regular database backups
   - Store in safe location (external drive, cloud)

### Security Best Practices

1. **Change Default Password:**
   - Click on username → **"Change Password"**
   - Use a strong password

2. **Create User Accounts:**
   - Don't share administrator account
   - Create separate accounts for each user

3. **Regular Backups:**
   - Back up database daily (if critical)
   - Weekly minimum for small businesses

4. **Update Regularly:**
   - Check for updates monthly
   - Subscribe to release notifications

---

## Support

### Getting Help

- **Documentation:** Check README and docs folder
- **Bug Reports:** [GitHub Issues](https://github.com/c9infotech/bill-sency-releases/issues)
- **Email:** support@c9infotech.com
- **Website:** https://c9infotech.com

### Before Contacting Support

Please have ready:
- Bill-Sency version (check **"Help"** → **"About"**)
- Windows version
- Steps to reproduce the issue
- Screenshots if applicable

---

*Last updated: March 3, 2026*
*Version: 1.0.0-beta*
