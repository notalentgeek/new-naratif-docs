---
layout: default
title: Backup Verification
parent: Maintenance Tasks
nav_order: 2
grand_parent: false
---

# Backup Verification
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Regular backup verification ensures data can be recovered in emergencies. This guide covers checking backups, testing restoration, and maintaining backup integrity.

{: .warning }
> An untested backup is not a backup! Always verify backups can be restored.

## Backup Schedule

### Automated Backups
- **Daily**: Full site backup at 3 AM
- **Weekly**: Archived to external storage
- **Monthly**: Offsite backup rotation

### Manual Backups
- **Before Updates**: Always create manual backup
- **Before Major Changes**: Content imports, design changes
- **Monthly Test**: Restore verification

## Backup Components

### What Gets Backed Up

1. **Database**
   - All WordPress tables
   - User data
   - Posts and pages
   - Settings and configurations

2. **Files**
   - WordPress core files
   - Themes and plugins
   - Uploads folder (media)
   - Configuration files

3. **Not Included**
   - Server configurations
   - Email accounts
   - External services
   - CDN cached files

## Verification Process

### Daily Checks

{: .note }
> Automated emails should confirm daily backup success

1. **Check Backup Status**
   - Login to CloudWays
   - Navigate to Backups
   - Verify today's backup exists
   - Check backup size (should be consistent)

2. **Review Email Notifications**
   - Check for backup success emails
   - Note any failure notifications
   - Investigate size discrepancies

### Weekly Verification

1. **Download Test File**
   ```
   - Select recent backup
   - Download single file (not full backup)
   - Verify file integrity
   - Check file can be opened
   ```

2. **Check Storage Usage**
   - Monitor backup storage space
   - Ensure adequate space remains
   - Plan for storage expansion

### Monthly Restore Test

{: .important }
> Perform restore tests on staging environment only

1. **Create Test Environment**
   - Use staging site
   - Or create temporary test site
   - Never test on production

2. **Restore Process**
   - Select backup from last week
   - Initiate restore to test site
   - Document time taken
   - Verify complete restoration

## CloudWays Backup Management

### Accessing Backups

1. **Via CloudWays Panel**
   ```
   1. Login to CloudWays
   2. Select Application
   3. Click "Backup and Restore"
   4. View available backups
   ```

2. **Backup Details**
   - Date and time
   - Backup size
   - Backup type (manual/automated)
   - Retention period

### Creating Manual Backups

1. **On-Demand Backup**
   - Click "Take Backup Now"
   - Add descriptive label
   - Select backup frequency
   - Wait for completion

2. **Pre-Update Backup**
   ```
   Label: "Pre-[update type]-backup-YYYY-MM-DD"
   Example: "Pre-plugin-update-backup-2025-01-15"
   ```

### Restore Options

1. **Full Restore**
   - Restores entire application
   - Includes database and files
   - Overwrites current site

2. **Partial Restore**
   - Database only
   - Files only
   - Specific folders

## External Backup Strategy

### Additional Backup Locations

{: .tip }
> Follow 3-2-1 rule: 3 copies, 2 different media, 1 offsite

1. **Local Backup**
   - Download monthly
   - Store on external drive
   - Encrypt sensitive data

2. **Cloud Storage**
   - Google Drive / Dropbox
   - Automated sync
   - Version history enabled

3. **Offsite Physical**
   - Quarterly USB backup
   - Store in different location
   - Rotate old backups

## Testing Procedures

### Quick Verification Test

1. **Database Check**
   - Export current database
   - Compare table count
   - Check recent posts exist
   - Verify user accounts

2. **File Check**
   - Download wp-content folder
   - Verify media files present
   - Check theme files intact
   - Confirm plugin folders

### Full Restore Test

**Quarterly Process:**

1. **Preparation**
   - [ ] Schedule 2-hour window
   - [ ] Notify team of test
   - [ ] Document current state

2. **Execution**
   - [ ] Create test environment
   - [ ] Restore selected backup
   - [ ] Verify all content
   - [ ] Test functionality

3. **Validation**
   - [ ] Homepage loads
   - [ ] Recent posts present
   - [ ] Media displays
   - [ ] Users can login
   - [ ] Forms function

## Troubleshooting

### Backup Failures

**No Daily Backup Created**
1. Check CloudWays status
2. Verify payment status
3. Check storage space
4. Contact support

**Backup Size Unusual**
- Much smaller: Check if content deleted
- Much larger: Look for hack/spam
- Investigate changes
- Run security scan

### Restore Issues

**Restore Fails**
1. Check backup integrity
2. Verify sufficient space
3. Try different backup
4. Contact CloudWays support

**Partial Data After Restore**
1. Check backup completeness
2. Verify restore process completed
3. Review error logs
4. Try manual restoration

## Documentation

### Backup Log Template

```markdown
## Backup Verification Log - [MONTH YEAR]

### Daily Checks
- Week 1: ✓ All backups successful
- Week 2: ✓ All backups successful
- Week 3: ⚠️ Backup delayed on [date]
- Week 4: ✓ All backups successful

### Monthly Restore Test
Date: [DATE]
Backup Tested: [Backup ID/Date]
Test Environment: [Staging/Test site]
Result: [PASS/FAIL]

### Issues Found
- [List any issues]
- [Actions taken]

### Storage Status
- CloudWays: [X]GB used of [Y]GB
- External: [Status]
- Offsite: Last updated [DATE]

### Sign-off
Verified by: [Name]
Date: [Date]
```

## Recovery Procedures

### Emergency Restore

{: .warning }
> Only perform emergency restore after confirming data loss

1. **Assess Damage**
   - Document what's wrong
   - Check if partial fix possible
   - Decide on restore necessity

2. **Communication**
   - Notify all stakeholders
   - Post maintenance notice
   - Estimate downtime

3. **Execute Restore**
   - Select most recent good backup
   - Initiate restore process
   - Monitor progress
   - Test thoroughly

### Post-Restore Tasks

- [ ] Verify all content restored
- [ ] Check user accounts active
- [ ] Test critical functionality
- [ ] Clear all caches
- [ ] Monitor for issues
- [ ] Document incident

---

*Last updated: {{ page.last_modified_date | date: '%B %d, %Y' }}*
