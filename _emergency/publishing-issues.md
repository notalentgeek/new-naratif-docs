---
layout: default
title: Cannot Publish Content
parent: Emergency Procedures
nav_order: 2
grand_parent: false
---

# Cannot Publish Content
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

{: .warning }
> **URGENT**: If content cannot be published for time-sensitive materials, follow these steps immediately.

## Quick Diagnostics

### 1. User Permissions Check
- [ ] Verify user is logged in with correct account
- [ ] Check user role (should be Editor/Administrator)
- [ ] Try logging out and back in

### 2. Browser Issues
- [ ] Clear browser cache
- [ ] Try different browser
- [ ] Disable browser extensions
- [ ] Check JavaScript console for errors (F12)

### 3. WordPress Admin Check
1. Navigate to Users → Your Profile
2. Verify your role and capabilities
3. Check if account is active

## Common Publishing Issues

### Issue: "Publishing Failed" Error

{: .note }
> This is often due to REST API issues or plugin conflicts.

**Solution Steps:**
1. Go to Settings → Permalinks
2. Click "Save Changes" (without changing anything)
3. Try publishing again

If that fails:
1. Deactivate all plugins except essential ones
2. Try publishing
3. Reactivate plugins one by one to identify conflict

### Issue: Stuck in "Updating" or "Publishing"

**Solution Steps:**
1. Wait 60 seconds
2. Refresh the page
3. Check if post actually published (Posts → All Posts)
4. If not published, copy content to clipboard
5. Create new post and paste content

### Issue: Block Editor Not Loading

**Solution Steps:**
1. Add `?classic-editor` to the URL
2. Or switch to Classic Editor temporarily:
   - Go to Posts → All Posts
   - Hover over post title
   - Click "Edit (Classic Editor)"

## Alternative Publishing Methods

### Method 1: Quick Draft
1. Dashboard → Quick Draft
2. Add title and content
3. Save Draft
4. Edit and publish from Posts list

### Method 2: Email Publishing
If configured:
1. Send email to [configured-publishing-email]
2. Subject becomes title
3. Body becomes content
4. Check Posts → All Posts for draft

### Method 3: WordPress Mobile App
1. Download WordPress app
2. Add site: newnaratif.com
3. Login with credentials
4. Create and publish from app

## Plugin-Specific Issues

### Elementor Not Loading
1. Elementor → Tools → Regenerate CSS
2. Elementor → Tools → Sync Library
3. Clear Elementor cache

### Yoast SEO Blocking
1. Temporarily ignore SEO warnings
2. Publish first, optimize later
3. Or disable Yoast temporarily

## Escalation

If unable to publish after 15 minutes:

1. **Contact Developer**
   - [Developer Name]: [Phone/Email]
   - Provide error messages and screenshots

2. **Emergency Workaround**
   - Send content to team member who can publish
   - Post on social media with "full article coming soon"
   - Use backup publishing platform if available

## Prevention

- Keep browser updated
- Regular cache clearing
- Don't work on posts for too long without saving
- Use draft autosave feature
- Keep local backup of important content

---

*Last updated: {{ page.last_modified_date | date: '%B %d, %Y' }}*
