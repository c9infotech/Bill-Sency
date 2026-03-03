# Security Policy

## Supported Versions

| Version | Supported          | End of Support |
| ------- | ------------------ | -------------- |
| 1.0.0-beta   | :white_check_mark: | TBD |
| < 1.0.0      | :x:                | N/A |

**Note:** As this is a beta version, security updates are provided on a best-effort basis.

---

## Reporting a Vulnerability

### How to Report

If you discover a security vulnerability in Bill-Sency, please report it responsibly:

**DO:**
- **Email:** security@c9infotech.com
- **Subject:** `[SECURITY] Brief description`
- **Include:**
  - Detailed description of the vulnerability
  - Steps to reproduce
  - Potential impact
  - Suggested fix (if any)
  - Your contact information

**DON'T:**
- ❌ Open public GitHub issues for security vulnerabilities
- ❌ Discuss vulnerabilities in public forums
- ❌ Exploit the vulnerability maliciously

### Response Timeline

| Stage | Timeline |
|-------|----------|
| **Initial Response** | Within 48 hours |
| **Vulnerability Assessment** | Within 7 days |
| **Fix Development** | Within 30 days (depending on severity) |
| **Patch Release** | As soon as possible |
| **Public Disclosure** | After patch is released |

### Severity Levels

#### Critical
- Remote code execution
- SQL injection vulnerabilities
- Authentication bypass
- Data theft or loss
- **Response:** Immediate patch within 7 days

#### High
- Privilege escalation
- Data exposure
- Denial of service
- **Response:** Patch within 14 days

#### Medium
- Information disclosure
- CSRF vulnerabilities
- **Response:** Patch within 30 days

#### Low
- Minor security improvements
- **Response:** Included in next regular release

---

## Security Features

### Current Implementation

#### Data Security
- **Local Storage:** All data stored locally in `%APPDATA%\BillSency\`
- **No Cloud:** No data sent to external servers by default
- **Database:** Local database with file-level security
- **Encryption:** Passwords hashed with SHA-256
- **Sensitive Files:** Credentials encrypted with Windows DPAPI

#### Authentication
- **Password Hashing:** SHA-256 (not plain text)
- **Remember Me:** Uses Windows Data Protection API (DPAPI)
- **Session Management:** Secure session handling
- **Password Policy:** Configurable (future release)

#### Authorization
- **Role-Based Access Control (RBAC):**
  - Administrator
  - Manager
  - User
  - Guest
- **Granular Permissions:** Per-DocType permissions (Create, Read, Update, Delete, etc.)
- **Activity Logging:** User actions tracked (future enhancement)

#### Code Security
- ⚠️ **Beta Version:** Code is not obfuscated
- ⚠️ **Not Signed:** No code signing certificate yet
- **Single File:** Reduces attack surface
- **Offline First:** No external dependencies

### Planned Security Enhancements

**Version 1.0.1:**
- [ ] Code signing certificate
- [ ] Code obfuscation
- [ ] Enhanced password policies
- [ ] Two-factor authentication (2FA)

**Version 1.1.0:**
- [ ] Audit logging
- [ ] Password expiry
- [ ] IP whitelisting
- [ ] Advanced encryption options

---

## Known Security Limitations

### Beta Version Limitations

1. **Unsigned Application**
   - Installer shows "Unknown Publisher" warning
   - This is expected for beta versions
   - Production version will be signed

2. **No Code Obfuscation**
   - Windows applications can be reverse-engineered
   - Source code can be retrieved with decompiler tools
   - **Exposed in code:**
     - Internal encryption keys
     - Default admin credentials (stored in code)
   - Production version will have obfuscation

3. **Password Storage**
   - Uses SHA-256 hashing (not bcrypt/argon2)
   - Acceptable for business POS, not high-security applications
   - Will be enhanced in future versions

4. **Local File Access**
   - Anyone with filesystem access can access database
   - Database file is not encrypted
   - Relies on Windows file permissions

### Mitigations

**For Users:**
1. **Physical Security:**
   - Secure the computer physically
   - Use Windows login passwords
   - Enable BitLocker drive encryption (optional)

2. **Access Control:**
   - Don't share administrator password
   - Create separate user accounts
   - Use appropriate role assignments

3. **Regular Backups:**
   - Back up to secure location
   - Encrypt backups if sensitive data
   - Test restore procedures

4. **Network Security:**
   - Use firewall
   - Keep Windows updated
   - Use antivirus software

**For Developers:**
- Production deployment should use obfuscation
- Consider changing encryption keys from defaults
- Implement additional security layers as needed

---

## Security Best Practices

### For System Administrators

1. **Installation:**
   - Install in default location (`C:\Program Files\Bill-Sency`)
   - Don't disable UAC
   - Verify installer integrity (checksum - future feature)

2. **Configure role permissions:**
   - Change default passwords immediately
   - Create individual user accounts
   - Assign minimum required permissions

3. **Operations:**
   - Regular security updates
   - Monitor user activity
   - Regular database backups
   - Secure backup storage

4. **Decommissioning:**
   - Delete all data from `%APPDATA%\BillSency\`
   - Securely wipe backups
   - Revoke user access

### For Users

1. **Passwords:**
   - Use strong passwords (12+ characters)
   - Don't share login credentials
   - Change passwords regularly
   - Don't write down passwords

2. **Physical Security:**
   - Lock computer when away
   - Don't leave POS terminal unattended
   - Secure physical access to computers

3. **Data Handling:**
   - Don't email database files
   - Secure USB drives with backups
   - Be cautious with customer data
   - Comply with data protection laws (GDPR, etc.)

4. **Updates:**
   - Install security updates promptly
   - Check for updates monthly
   - Read changelog for security fixes

### For Developers (Self-hosting)

1. **Source Code:**
   - Keep private repository secure
   - Review code for vulnerabilities
   - Use static analysis tools
   - Regular security audits

2. **Dependencies:**
   - Keep NuGet packages updated
   - Review security advisories
   - Use Dependabot (GitHub)

3. **Build Process:**
   - Use code obfuscation for production
   - Sign binaries with certificate
   - Verify build integrity
   - Secure build environment

---

## Compliance

### Data Protection

**GDPR Compliance (EU):**
- Data stored locally (data controller has full control)
- No third-party data sharing
- Data deletion: Uninstall removes all data (if chosen)
- Data portability: Export to CSV/Excel
- Right to erasure: Delete database file

**User Responsibilities:**
- Comply with local data protection laws
- Implement appropriate security measures
- Maintain data backups
- Protect customer information

### Industry Standards

**PCI DSS (if processing cards):**
- ⚠️ Bill-Sency does NOT store credit card information
- For card payments, use certified payment terminals
- Never enter full card numbers in Bill-Sency
- Comply with payment processor requirements

**Local Regulations:**
- Comply with tax reporting requirements
- Maintain audit trails as required
- Secure customer data per local laws

---

## Security Checklist

### Initial Setup
- [ ] Download from official source only
- [ ] Verify installer (future: checksums)
- [ ] Install with elevated privileges
- [ ] Review license agreement
- [ ] Note data locations

### Initial Setup
- [ ] Change default passwords immediately
- [ ] Create individual user accounts
- [ ] Configure role permissions
- [ ] Test user access levels
- [ ] Set up backup schedule

### Ongoing Security
- [ ] Regular backups (daily/weekly)
- [ ] Keep Windows updated
- [ ] Install Bill-Sency updates
- [ ] Monitor for suspicious activity
- [ ] Review user permissions quarterly
- [ ] Test backup restores

### Incident Response
- [ ] Document security incidents
- [ ] Report vulnerabilities responsibly
- [ ] Change passwords if compromised
- [ ] Review access logs
- [ ] Update security measures

---

## Vulnerability Disclosure Policy

### Public Disclosure

After a vulnerability is fixed:

1. **Patch Release:**
   - Security patches released immediately
   - Users notified via GitHub releases
   - Changelog includes security fixes

2. **Public Advisory:**
   - Published 7 days after patch release
   - Includes vulnerability details
   - Credits reporter (if desired)
   - Mitigation steps documented

3. **Timeline Example:**
   - Day 0: Vulnerability reported
   - Day 2: Initial response sent
   - Day 7: Vulnerability assessed
   - Day 14-30: Fix developed and tested
   - Day 31: Patch released
   - Day 38: Public disclosure

### Hall of Fame

Security researchers who responsibly disclose vulnerabilities will be credited here:

*None yet - this is the first release!*

---

## Contact

### Security Team

- **Email:** security@c9infotech.com
- **Response Time:** 48 hours
- **PGP Key:** (Coming soon)

### General Security Questions

- **Support:** support@c9infotech.com
- **Website:** https://c9infotech.com

### Bug Reports (Non-Security)

- **GitHub Issues:** [Report Bug](https://github.com/c9infotech/bill-sency-releases/issues)

---

## Updates to This Policy

This security policy may be updated as the product evolves. Check back regularly for changes.

**Last Updated:** March 3, 2026  
**Version:** 1.0 (Beta)

---

## Acknowledgments

We appreciate the security community's efforts in responsible disclosure and keeping our users safe.

**Thank you to:**
- Security researchers who report vulnerabilities responsibly
- Our beta testers for security feedback
- The open-source security community

---

*For urgent security matters, please email security@c9infotech.com immediately.*
