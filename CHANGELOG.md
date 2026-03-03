# Changelog

All notable changes to Bill-Sency will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Planned
- Cloud sync support
- Mobile companion app
- E-commerce integration
- WhatsApp notifications
- Multi-branch management

---

## [1.0.0-beta] - 2026-03-03

### 🎉 Initial Beta Release

The first public beta release of Bill-Sency, a comprehensive business management system for retail and wholesale businesses.

### Added

#### Core Features
- **Point of Sale System**
  - Touch-friendly POS interface
  - Barcode scanner support
  - Multiple payment methods (Cash, Card, UPI)
  - Real-time stock checking
  - Customer selection and management
  - Thermal printer support (58mm, 80mm)
  - Receipt customization

- **Inventory Management**
  - Real-time stock tracking
  - Automatic stock adjustments
  - Multi-warehouse support
  - Item management with variants
  - Stock reports and analytics
  - Low stock alerts
  - Batch/Serial number tracking

- **User & Role Management**
  - Multi-user support
  - Role-based permissions (Administrator, Manager, User, Guest)
  - Granular permissions per DocType
  - Activity logging
  - Secure authentication with password hashing

- **Reports & Analytics**
  - Sales reports (daily, monthly, custom periods)
  - Stock reports (movement, valuation, balance)
  - Customer analysis
  - Export to Excel, CSV, PDF
  - Custom report builder
  - Dynamic filters

- **Customization**
  - Custom fields for any DocType
  - Workflow automation with hooks
  - Custom print formats
  - Dynamic filter builder
  - Modular architecture

- **System Features**
  - Local database (no server required)
  - Offline-first operation
  - Import/Export business apps and data
  - Database backup and restore
  - Multi-language support framework
  - Configurable settings

#### Technical
- Self-contained Windows application
- Single-file deployment (80 MB standalone)
- Windows installer (75 MB)
- Auto-configuration on first run
- Data stored in `%APPDATA%\BillSency`
- No external dependencies required

### Security
- Local data storage only (no cloud)
- Encrypted password storage (SHA256)
- Role-based access control
- Remember Me feature with Windows DPAPI
- Secure session management

### Known Issues
- ⚠️ Installer shows "Unknown Publisher" warning (no code signing certificate yet)
- ⚠️ Beta version - not recommended for production without testing
- ⚠️ Code is not obfuscated in this beta version
- Some warning messages during uninstall about data cleanup
- Need to manually enter admin password on first login

### Notes
- **Login Credentials:** Provided during installation (contact support if needed)
- **Database Location:** `%APPDATA%\BillSency\billsency.db`
- **Uploads Location:** `%APPDATA%\BillSency\Uploads\Images\`
- **Configuration:** `%APPDATA%\BillSency\config.json`

### Installer Details
- **Installer Size:** 75.3 MB
- **Standalone Size:** 80.4 MB
- **Installation Directory:** `C:\Program Files\Bill-Sency`
- **Includes:** EULA, desktop icon option, start menu shortcuts
- **Requirements:** Windows 10/11 (64-bit), 4 GB RAM minimum

---

## Release Schedule

### Version 1.0.1 (Planned - April 2026)
**Focus: Stability & Security**
- [ ] Code signing certificate
- [ ] Code obfuscation for production
- [ ] Bug fixes from beta feedback
- [ ] Performance improvements
- [ ] Documentation updates

### Version 1.1.0 (Planned - Q2 2026)
**Focus: Enhanced Features**
- [ ] Additional payment integrations
- [ ] Enhanced reporting
- [ ] Backup scheduler
- [ ] Email notifications
- [ ] Advanced search

### Version 2.0.0 (Planned - Q3 2026)
**Focus: Cloud & Mobile**
- [ ] Optional cloud sync
- [ ] Mobile app integration
- [ ] Multi-branch support
- [ ] E-commerce integration
- [ ] API improvements

---

## Version History Summary

| Version | Release Date | Status | Highlights |
|---------|--------------|--------|------------|
| 1.0.0-beta | 2026-03-03 | Beta | Initial public release |
| 1.0.1 | TBD | Planned | Stability & security |
| 1.1.0 | TBD | Planned | Enhanced features |
| 2.0.0 | TBD | Planned | Cloud & mobile |

---

## Upgrade Notes

### Upgrading to v1.0.0-beta
This is the first release. No upgrade path available.

**Fresh Installation Steps:**
1. Download the installer
2. Run BillSency-Setup-1.0.0-beta.exe
3. Follow installation wizard
4. Launch and complete first-time setup

---

## Bug Fixes & Improvements

This section will be updated with each release to document bug fixes and improvements.

### v1.0.0-beta
- Initial release - no previous bugs to fix

---

## Deprecations

No deprecations in this release.

---

## Breaking Changes

No breaking changes - this is the first release.

---

## Contributors

- C9 Infotech Development Team

---

## Support

- **Bug Reports:** [GitHub Issues](https://github.com/c9infotech/bill-sency-releases/issues)
- **Feature Requests:** [GitHub Issues](https://github.com/c9infotech/bill-sency-releases/issues)
- **Email Support:** support@c9infotech.com
- **Website:** https://c9infotech.com

---

*This changelog follows [Keep a Changelog](https://keepachangelog.com/) format.*
