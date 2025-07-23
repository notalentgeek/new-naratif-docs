---
layout: default
title: Website is Down
nav_order: 1
parent: Emergency Procedures
grand_parent: false
---

# Website is Down
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

{: .warning }
> **CRITICAL**: If the website is completely inaccessible, this is a P1 emergency. Follow these steps immediately.

## Initial Checks (5 minutes)

### 1. Verify the Issue
- [ ] Open [https://newnaratif.com](https://newnaratif.com) in an incognito window
- [ ] Check from mobile data (not WiFi) to rule out local issues
- [ ] Try [https://www.isitdownrightnow.com](https://www.isitdownrightnow.com) to confirm

### 2. Check CloudWays Status
1. Log into [CloudWays Platform](https://platform.cloudways.com)
   - Username: [stored securely]
   - Password: [stored securely]
2. Check server status indicator
3. Look for any warning messages

### 3. Domain Status
- [ ] Check domain expiration at registrar
- [ ] Verify DNS is resolving: `nslookup newnaratif.com`

## Immediate Actions

{: .important }
> Document all actions taken with timestamps in the incident log.

### If Server is Down
1. **Contact CloudWays Support**
   ```
   Support Email: support@cloudways.com
   Live Chat: Available in platform
   Priority: URGENT - Production Down
   ```

2. **Provide Information:**
   - Server ID: [YOUR_SERVER_ID]
   - Application: New Naratif WordPress
   - Issue: Complete site outage
   - Time noticed: [TIMESTAMP]

### If Server is Up but Site is Down

1. **Restart Services via CloudWays**
   - Navigate to Server Management
   - Click "Services" tab
   - Restart Apache/Nginx
   - Restart MySQL
   - Clear Varnish Cache

2. **Check WordPress via SSH**
   ```bash
   ssh [username]@[server-ip]
   cd applications/[app-name]/public_html
   wp core verify-checksums
   ```

## Escalation Path

If not resolved within 30 minutes:

1. **Internal Escalation**
   - Primary: [Developer Name] - [Phone]
   - Secondary: [Manager Name] - [Phone]
   - Tertiary: [CTO/Technical Lead] - [Phone]

2. **External Support**
   - CloudWays Premium Support: [Ticket Number]
   - WordPress Expert: [Contractor Details]

## Post-Incident

Once resolved:
1. Document root cause
2. Update this procedure if needed
3. Schedule post-mortem meeting
4. Notify all stakeholders

---

*Last updated: {{ page.last_modified_date | date: '%B %d, %Y' }}*
