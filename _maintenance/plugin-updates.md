---
layout: default
title: Plugin Updates
parent: Maintenance Tasks
nav_order: 1
grand_parent: false
---

# Plugin Updates
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Regular plugin updates are critical for security, performance, and compatibility. This guide provides a safe, systematic approach to updating WordPress plugins.

{: .warning }
> Never update plugins directly on production without testing first!

## Update Schedule

### Critical Security Updates
- **When**: Immediately (within 24 hours)
- **What**: Security patches, vulnerability fixes
- **Process**: Fast-track testing

### Regular Updates
- **When**: Weekly (Thursdays 10 AM)
- **What**: Feature updates, bug fixes
- **Process**: Standard testing

### Major Updates
- **When**: Monthly maintenance window
- **What**: Major version changes
- **Process**: Extended testing

## Pre-Update Checklist

### 1. Preparation
- [ ] Check current plugin versions
- [ ] Read update changelogs
- [ ] Verify backup is recent (within 24 hours)
- [ ] Note any custom modifications
- [ ] Check plugin compatibility

### 2. Documentation
- [ ] List plugins to update
- [ ] Note current versions
- [ ] Document expected changes
- [ ] Identify dependencies

### 3. Communication
- [ ] Notify team of maintenance
- [ ] Set "maintenance mode" if needed
- [ ] Prepare rollback plan

## Update Process

### Step 1: Backup Everything

{: .important }
> Always create a full backup before any updates

1. **Via CloudWays**
   ```
   CloudWays → Backups → Create Backup
   Name: Pre-plugin-update-YYYY-MM-DD
   ```

2. **Verify Backup**
   - Check backup completed
   - Note backup location
   - Test restore process (monthly)

### Step 2: Test on Staging

1. **Access Staging Site**
   - URL: `staging.newnaratif.com`
   - Ensure staging matches production

2. **Update Process**
   - Go to Plugins → Installed Plugins
   - Click "Update Available" filter
   - Update one plugin at a time

3. **Test Each Update**
   - Check plugin functionality
   - Test related features
   - Look for conflicts

### Step 3: Update Production

{: .tip }
> Update during low-traffic periods (early morning)

1. **Single Plugin Update**
   - Select one plugin
   - Click "Update"
   - Wait for completion
   - Test immediately

2. **Bulk Updates** (Use Cautiously)
   - Select multiple plugins
   - Bulk Actions → Update
   - Only for minor updates

### Step 4: Post-Update Testing

**Immediate Checks:**
- [ ] Site loads properly
- [ ] Admin dashboard accessible
- [ ] Key functionality works
- [ ] No error messages

**Thorough Testing:**
- [ ] Homepage displays correctly
- [ ] Posts/pages load
- [ ] Forms submit properly
- [ ] Payment processing (if applicable)
- [ ] Member areas accessible

## Plugin-Specific Procedures

### Critical Plugins

**Elementor**
- Always update Elementor Pro first
- Then update base Elementor
- Regenerate CSS after update
- Test all page templates

**WooCommerce**
- Update during maintenance window
- Test checkout process
- Verify payment gateways
- Check member subscriptions

**Security Plugins**
- Update immediately for security patches
- Review new security rules
- Check for false positives
- Verify firewall rules

### Testing Requirements by Plugin Type

**SEO Plugins**: Check meta data, sitemaps
**Cache Plugins**: Clear all caches, test speed
**Form Plugins**: Submit test entries
**Gallery Plugins**: Verify image display
**Social Plugins**: Test sharing functions

## Troubleshooting Updates

### Update Fails

**White Screen of Death**
1. Access via FTP/SSH
2. Rename problem plugin folder
3. Access WordPress admin
4. Reinstall or restore

**Update Stuck**
1. Wait 5 minutes
2. Refresh page
3. Check via FTP if files updated
4. Clear cache and retry

### Compatibility Issues

**Plugin Conflicts**
1. Deactivate all plugins
2. Reactivate one by one
3. Identify conflict pair
4. Seek alternatives or wait for fix

**PHP Errors**
1. Check PHP version compatibility
2. Enable debug mode
3. Review error logs
4. Contact plugin support

## Rollback Procedures

### Quick Rollback

1. **Via Plugin**
   - Use WP Rollback plugin
   - Select previous version
   - Rollback individual plugin

2. **Via Backup**
   - Restore from CloudWays backup
   - Affects entire site
   - Use for multiple failures

### Manual Rollback

1. **Download Previous Version**
   - Get from WordPress.org
   - Or from backup files

2. **Upload via FTP**
   - Delete current plugin folder
   - Upload previous version
   - Reactivate in WordPress

## Best Practices

### Do's
- ✅ Update one plugin at a time
- ✅ Test thoroughly on staging
- ✅ Keep detailed logs
- ✅ Monitor site after updates
- ✅ Maintain update schedule

### Don'ts
- ❌ Update everything at once
- ❌ Skip changelog review
- ❌ Update during peak hours
- ❌ Ignore backup verification
- ❌ Rush major updates

## Update Log Template

```markdown
## Plugin Update Log - [DATE]

### Updated Plugins
1. Plugin Name: v1.0 → v1.1
   - Changes: Bug fixes
   - Tested: ✓
   - Issues: None

2. Plugin Name: v2.0 → v3.0
   - Changes: Major update
   - Tested: ✓
   - Issues: Minor CSS adjustment needed

### Testing Results
- Staging: [PASS/FAIL]
- Production: [PASS/FAIL]
- Rollbacks: [None/List]

### Notes
[Any additional observations]

### Sign-off
Updated by: [Name]
Verified by: [Name]
```

## Monthly Audit

- [ ] Review all installed plugins
- [ ] Check for abandoned plugins
- [ ] Remove unused plugins
- [ ] Update compatibility matrix
- [ ] Plan major updates

---

*Last updated: {{ page.last_modified_date | date: '%B %d, %Y' }}*
