---
layout: default
title: Security Checks
parent: Maintenance Tasks
nav_order: 3
grand_parent: false
---

# Security Checks
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Regular security checks protect the website from threats, unauthorized access, and data breaches. This guide covers routine security monitoring and response procedures.

{: .warning }
> Security is everyone's responsibility. Report suspicious activity immediately.

## Security Check Schedule

### Daily Checks (5 minutes)
- Monitor login attempts
- Check security plugin alerts
- Review 404 errors
- Verify backups completed

### Weekly Checks (30 minutes)
- Review user accounts
- Check file changes
- Scan error logs
- Update security rules

### Monthly Checks (2 hours)
- Full security audit
- Update passwords
- Review permissions
- Test incident response

## Daily Security Monitoring

### 1. Check Security Dashboard

**Via Security Plugin (Wordfence/Sucuri)**
1. Login to WordPress admin
2. Navigate to security plugin
3. Check dashboard for:
   - [ ] Active threats
   - [ ] Blocked attacks
   - [ ] Failed logins
   - [ ] File changes

### 2. Review Login Activity

{: .important }
> Multiple failed logins may indicate attack attempt

**Check for:**
- Unusual login times
- Unknown IP addresses
- Multiple username attempts
- Admin login attempts

**Red Flags:**
- 10+ failed attempts from one IP
- Login attempts at 3 AM
- Unknown usernames tried
- Direct wp-admin access attempts

### 3. Monitor 404 Errors

**Common Attack Patterns:**
- `/wp-config.php` attempts
- `/backup/` directory scans
- Random `.zip` file requests
- Admin file fishing

## Weekly Security Tasks

### 1. User Account Audit

**Review All Users:**
```
Users → All Users
Check for:
- [ ] Unknown accounts
- [ ] Correct role assignments
- [ ] Inactive accounts
- [ ] Strong passwords enabled
```

**Actions:**
- Remove unknown users
- Downgrade unnecessary admins
- Disable inactive accounts
- Force password resets if needed

### 2. File Integrity Check

**Via Security Plugin:**
1. Run file scan
2. Compare to known files
3. Identify changes:
   - Modified core files
   - New unknown files
   - Permission changes

**Manual Check:**
```bash
# Via SSH/FTP
# Check recently modified files
find . -type f -mtime -7
```

### 3. Plugin/Theme Audit

{: .tip }
> Deactivated plugins can still be security risks

- [ ] Remove unused plugins
- [ ] Delete deactivated themes
- [ ] Check for abandoned plugins
- [ ] Verify official sources

## Monthly Security Audit

### 1. Comprehensive Scan

**Full Malware Scan:**
1. Use security plugin scan
2. Include all files
3. Deep scan database
4. Check for:
   - Malicious code
   - Backdoors
   - Spam content
   - Suspicious redirects

### 2. Password Security

**Update Critical Passwords:**
- WordPress admin accounts
- Database passwords
- FTP/SSH credentials
- Email accounts

**Password Requirements:**
- Minimum 16 characters
- Random generation
- Unique per service
- Stored securely

### 3. Permission Review

**File Permissions:**
```
Correct permissions:
- Files: 644
- Folders: 755
- wp-config.php: 640
- .htaccess: 644
```

**Database Permissions:**
- WordPress user: SELECT, INSERT, UPDATE, DELETE
- No CREATE/DROP permissions
- Separate users for different sites

### 4. SSL Certificate

**Check Certificate:**
- Expiration date
- Proper installation
- No mixed content warnings
- HTTPS enforcement

## Security Best Practices

### Login Security

1. **Two-Factor Authentication**
   - Enable for all users
   - Mandatory for admins
   - Use authenticator apps

2. **Login Restrictions**
   - Limit login attempts
   - Hide login errors
   - Change login URL
   - IP whitelist for admins

### File Security

1. **Disable File Editing**
   ```php
   // Add to wp-config.php
   define('DISALLOW_FILE_EDIT', true);
   ```

2. **Protect Sensitive Files**
   ```apache
   # .htaccess rules
   <Files wp-config.php>
   order allow,deny
   deny from all
   </Files>
   ```

### Database Security

1. **Change Table Prefix**
   - Use custom prefix
   - Not default `wp_`

2. **Regular Backups**
   - Before any changes
   - Encrypted storage
   - Test restoration

## Incident Response

### Suspected Hack

{: .warning }
> If you suspect a hack, act immediately but carefully

1. **Don't Panic**
   - Document everything
   - Don't delete evidence
   - Take screenshots

2. **Immediate Actions**
   - [ ] Put site in maintenance mode
   - [ ] Change all passwords
   - [ ] Backup current state
   - [ ] Notify stakeholders

3. **Investigation**
   - Review recent changes
   - Check file modifications
   - Scan for malware
   - Review access logs

### Response Procedures

**Minor Incident (Spam posts)**
1. Delete spam content
2. Check for user compromise
3. Strengthen security
4. Monitor for recurrence

**Major Incident (Site defaced)**
1. Take site offline
2. Restore from clean backup
3. Investigate entry point
4. Patch vulnerabilities
5. Change all credentials
6. Monitor closely

## Security Tools

### Recommended Plugins
- **Wordfence**: Comprehensive security
- **Sucuri**: Malware scanning
- **iThemes Security**: Hardening
- **WP Activity Log**: Audit trail

### External Tools
- **VirusTotal**: File scanning
- **Qualys SSL Test**: SSL verification
- **Have I Been Pwned**: Breach checking
- **Google Safe Browsing**: Blacklist check

## Documentation

### Security Log Template

```markdown
## Security Check Log - [DATE]

### Daily Checks
- [ ] No active threats
- [ ] Failed logins: [number]
- [ ] 404 errors reviewed
- [ ] Backups verified

### Issues Found
1. Issue: [Description]
   Action: [What was done]
   Status: [Resolved/Monitoring]

### Weekly Tasks
- [ ] User audit complete
- [ ] File scan clean
- [ ] Plugins reviewed

### Notes
[Any observations or concerns]

Checked by: [Name]
Time: [Duration]
```

### Incident Report Template

```markdown
## Security Incident Report

Date: [DATE]
Severity: [Low/Medium/High/Critical]

### Description
[What happened]

### Impact
[What was affected]

### Response Actions
1. [Action taken]
2. [Action taken]

### Root Cause
[How it happened]

### Prevention
[Steps to prevent recurrence]

### Follow-up
[Required actions]
```

---

*Last updated: {{ page.last_modified_date | date: '%B %d, %Y' }}*
