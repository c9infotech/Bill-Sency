# Support

Looking for help with Bill-Sency? You're in the right place!

---

## 📚 Documentation

Start here for most questions:

### Installation & Setup
- **[Installation Guide](INSTALLATION.md)** - Complete installation instructions
- **[Quick Start](#quick-start)** - Get started in 5 minutes
- **[Troubleshooting](INSTALLATION.md#troubleshooting)** - Common issues and solutions

### User Guides
- **[Full Documentation](README.md)** - Feature overview
- **[Changelog](CHANGELOG.md)** - What's new in each version
- **[Security Policy](SECURITY.md)** - Security information

---

## 🐛 Report Bugs

Found a bug? Help us fix it!

1. **Check [existing issues](https://github.com/c9infotech/bill-sency-releases/issues)** - Someone may have already reported it
2. **Use [Bug Report Template](https://github.com/c9infotech/bill-sency-releases/issues/new?template=bug_report.md)** - Helps us resolve issues faster
3. **Provide details:**
   - Bill-Sency version
   - Windows version
   - Steps to reproduce
   - Screenshots
   - Error messages

---

## 💡 Request Features

Have an idea for a new feature?

1. **Check [feature requests](https://github.com/c9infotech/bill-sency-releases/issues?q=label%3Aenhancement)** - It might already be planned
2. **Use [Feature Request Template](https://github.com/c9infotech/bill-sency-releases/issues/new?template=feature_request.md)**
3. **Explain your use case** - Tell us how it would help your business

---

## 📧 Email Support

### General Support
- **Email:** support@c9infotech.com
- **Response Time:** 1-3 business days
- **For:** Installation help, usage questions, general inquiries

### Security Issues
- **Email:** security@c9infotech.com
- **Response Time:** Within 48 hours
- **For:** Security vulnerabilities (do NOT post publicly)

### Business Inquiries
- **Email:** contact@c9infotech.com
- **For:** Licensing, custom development, partnerships

### Development
- **Email:** dev@c9infotech.com
- **For:** Contributing code, technical discussions

---

## 💬 Community Support

### GitHub Discussions
- Coming soon! Check back for community forums

### Issue Tracker
- Browse [all issues](https://github.com/c9infotech/bill-sency-releases/issues)
- Help others by answering questions
- Vote on feature requests (👍 reactions)

---

## 🚀 Quick Start

### First-Time Users

**1. Download**
- Go to [Releases](https://github.com/c9infotech/bill-sency-releases/releases)
- Download `BillSency-Setup-1.0.0-beta.exe`

**2. Install**
- Run installer
- Click through setup wizard
- Application launches automatically

**3. Login**
- Use credentials provided with installation
- Contact support@c9infotech.com if you need assistance

**4. Setup**
- Complete First Time Setup wizard
- Install demo apps (optional, recommended)
- Start using Bill-Sency!

**Full instructions:** [Installation Guide](INSTALLATION.md)

---

## ❓ Frequently Asked Questions

### Installation

**Q: Why does Windows show "Unknown Publisher"?**  
A: This is expected for beta versions. The production version will be code-signed. Click "More info" → "Run anyway" to proceed. [More details](INSTALLATION.md#windows-smartscreen)

**Q: Can I use Bill-Sency without installing?**  
A: Bill-Sency requires installation to ensure all components are properly configured.

**Q: Where is my data stored?**  
A: `%APPDATA%\BillSency\` which typically resolves to:  
`C:\Users\YourName\AppData\Roaming\BillSency\`

### Login & Setup

**Q: What are the default login credentials?**  
A: Login credentials are provided with your installation. If you didn't receive them or need assistance, please contact support@c9infotech.com

**Q: I forgot my password. How do I reset it?**  
A: Currently, you need to delete the database and start fresh. Password recovery feature is coming in v1.1.0.  
**Delete:** `%APPDATA%\BillSency\billsency.db`

**Q: Can I skip the demo data installation?**  
A: Yes, it's optional. Click "Skip" in the First Time Setup wizard.

### Features

**Q: Can I customize the forms and fields?**  
A: Yes! Bill-Sency allows full customization of forms, fields, and workflows to match your business needs.

**Q: Does it support barcode scanners?**  
A: Not yet. Barcode scanner support is planned for v1.1.0. [Vote for this feature](https://github.com/c9infotech/bill-sency-releases/issues?q=barcode)

**Q: Does it support enterprise databases?**  
A: Yes! Bill-Sency supports both local database and SQL Server for multi-user scenarios. Configure in Database Configuration.

**Q: Can I export/import data?**  
A: Yes! Use the Export feature to create packages containing apps, forms, and data.

### Printing

**Q: How do I set up receipt printing?**  
A: Go to Settings → Print Formats → Configure thermal printer settings.

**Q: Can I customize invoice templates?**  
A: Yes! Bill-Sency includes a built-in print format designer. [Guide](DOCS/Managing_Print_Formats.md)

### Multi-User

**Q: Can multiple people use it at the same time?**  
A: With local database (default): One user at a time per database.  
With SQL Server: Multiple concurrent users supported.

**Q: How do I add more users?**  
A: Login with an admin account → Users → Add User → Assign roles and permissions.

### Updates

**Q: How do I update to a new version?**  
A: Download the new installer and install over the existing version. Your data will be preserved. [Upgrade guide](INSTALLATION.md#upgrading)

**Q: Will I lose my data when upgrading?**  
A: No, your data is separate from the application. However, **always backup before upgrading**:  
Copy: `%APPDATA%\BillSency\billsency.db`

### Errors

**Q: "Unable to open database file" error**  
A: Delete configuration files and let the app auto-configure:
```
%APPDATA%\BillSency\config.json
%APPDATA%\BillSency\credentials.dat
```
Restart the app. [More solutions](INSTALLATION.md#troubleshooting)

**Q: "Access denied" when uploading images**  
A: This should be fixed in v1.0.0-beta. If you still experience it:
1. Ensure folder exists: `%APPDATA%\BillSency\Uploads\Images\`
2. Check folder permissions
3. Run as administrator (not recommended for regular use)

**Q: Application crashes on startup**  
A: Try these steps:
1. Restart your computer
2. Delete `%APPDATA%\BillSency\config.json`
3. Reinstall the application
4. [Report the issue](https://github.com/c9infotech/bill-sency-releases/issues/new?template=bug_report.md)

### Technical

**Q: Is my data secure?**  
A: Yes. Data is stored locally on your computer. Passwords are hashed with SHA-256. No data is sent to external servers. [Security details](SECURITY.md)

**Q: Do I need to install anything else?**  
A: No! Bill-Sency is self-contained and includes all dependencies.

**Q: Can I use it offline?**  
A: Yes! Bill-Sency is fully offline-capable. No internet connection required.

**Q: Can I backup to cloud storage?**  
A: Yes! You can manually copy the database file to Dropbox, OneDrive, Google Drive, etc. Automated cloud backup is planned for v1.2.0.

---

## 🔧 Troubleshooting

### Before Contacting Support

Try these steps first:

1. **Restart the application**
2. **Check [Troubleshooting Guide](INSTALLATION.md#troubleshooting)**
3. **Search [existing issues](https://github.com/c9infotech/bill-sency-releases/issues)**
4. **Update to latest version**
5. **Check Windows Event Viewer** for error details

### Common Solutions

**Application won't start:**
- Delete config: `%APPDATA%\BillSency\config.json`
- Check antivirus isn't blocking it
- Run as administrator (once)

**Database errors:**
- Check file permissions on `%APPDATA%\BillSency\`
- Ensure no other app is using the database
- Try copying database to a different location

**Performance issues:**
- Compact database (Settings → Database → Compact)
- Close other applications
- Check disk space

**Printing issues:**
- Verify printer is online
- Check print format configuration
- Test with Windows Test Page first

---

## 📥 Useful Downloads

- **[Latest Release](https://github.com/c9infotech/bill-sency-releases/releases/latest)** - Installer
- **[All Releases](https://github.com/c9infotech/bill-sency-releases/releases)** - Previous versions
- **[Demo Data](https://github.com/c9infotech/bill-sency-releases/releases)** - Sample data packages

---

## 🎓 Learning Resources

### Video Tutorials
Coming soon! Subscribe to our channel for updates.

### Documentation
- [User Manual](README.md)
- [POS System Guide](DOCS/POS_DocTypes_Guide.md)
- [Reports Guide](DOCS/POS_Reports_Guide.md)
- [Print Formats](DOCS/Managing_Print_Formats.md)

### Sample Files
- Demo apps (included in installer)
- Sample reports
- Print format templates

---

## 🤝 Contributing

Want to help improve Bill-Sency?

- **Report bugs** - Help us squash them
- **Request features** - Tell us what you need
- **Improve documentation** - Fix typos, add examples
- **Help others** - Answer questions in issues
- **Test beta versions** - Provide early feedback

[Contributing Guide](CONTRIBUTING.md)

---

## 📊 System Requirements

**Minimum:**
- Windows 10 (64-bit)
- 4 GB RAM
- 200 MB disk space
- 1280x720 display

**Recommended:**
- Windows 11 (64-bit)
- 8 GB RAM
- 500 MB disk space (more for data)
- 1920x1080 display

[Full requirements](INSTALLATION.md#system-requirements)

---

## 🔗 Quick Links

| Resource | Link |
|----------|------|
| Download | [Releases](https://github.com/c9infotech/bill-sency-releases/releases) |
| Installation | [Guide](INSTALLATION.md) |
| Report Bug | [Template](https://github.com/c9infotech/bill-sency-releases/issues/new?template=bug_report.md) |
| Request Feature | [Template](https://github.com/c9infotech/bill-sency-releases/issues/new?template=feature_request.md) |
| Changelog | [CHANGELOG.md](CHANGELOG.md) |
| Security | [SECURITY.md](SECURITY.md) |
| Website | [c9infotech.com](https://c9infotech.com) |

---

## 📞 Contact Information

### C9 Infotech

- **Website:** https://c9infotech.com
- **Email:** support@c9infotech.com
- **Security:** security@c9infotech.com
- **Business:** contact@c9infotech.com

### Response Times

| Type | Time |
|------|------|
| Security Issues | 48 hours |
| Bug Reports | 2-5 business days |
| Feature Requests | 1-2 weeks |
| General Support | 1-3 business days |

---

## ⚖️ License

Bill-Sency is commercial software. See [LICENSE.txt](LICENSE.txt) for details.

**Beta Version:** Free during beta period. Future pricing TBD.

---

## 🙏 Thank You

Thank you for using Bill-Sency! We're committed to building the best business management solution for small and medium businesses.

**Happy managing!**

---

*Last Updated: March 3, 2026*
