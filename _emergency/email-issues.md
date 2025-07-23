---
layout: default
title: Email Delivery Failed
parent: Emergency Procedures
nav_order: 3
grand_parent: false
---

# Email Delivery Failed
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

{: .warning }
> **IMPORTANT**: Email delivery issues affect member communications, password resets, and notifications.

## Quick Diagnosis

### 1. Verify the Issue
- [ ] Check if ANY emails are being sent
- [ ] Test with password reset on test account
- [ ] Check email logs in WordPress admin
- [ ] Verify SMTP settings haven't changed

### 2. Common Email Types Affected
- Member welcome emails
- Password reset emails
- Comment notifications
- Contact form submissions
- Newsletter broadcasts

## Immediate Checks

### Check SMTP Plugin Status

1. **Navigate to Plugin Settings**
   - Go to Settings → WP Mail SMTP (or similar plugin)
   - Verify status shows "Connected"
   - Check authentication is valid

2. **Send Test Email**
   - Use plugin's test email feature
   - Send to your own email
   - Check spam folder

3. **View Email Log**
   - Check email log plugin if installed
   - Look for failed attempts
   - Note any error messages

### Check Server Email Service

1. **CloudWays Email Service**
   ```
   Login to CloudWays → Server → Settings → Mail
   Verify:
   - SMTP is enabled
   - Correct SMTP server
   - Valid credentials
   ```

2. **Email Service Provider**
   - Login to SendGrid/Mailgun/etc.
   - Check account status (not suspended)
   - Verify API key is valid
   - Check sending limits

## Common Issues and Solutions

### Issue: Authentication Failed

**Solution:**
1. Re-enter SMTP credentials
2. Generate new API key if needed
3. Update in WordPress settings
4. Test email again

### Issue: Emails Going to Spam

**Solution:**
1. Check SPF records
2. Verify DKIM is configured
3. Review email content for spam triggers
4. Add "from" email to trusted senders

### Issue: Rate Limit Exceeded

**Solution:**
1. Check sending limits with provider
2. Implement email queue plugin
3. Spread bulk emails over time
4. Upgrade plan if needed

## Manual Email Workarounds

### For Password Resets
1. Manually reset user password in WordPress
2. Users → All Users → Edit user
3. Generate new password
4. Send via personal email or SMS

### For Member Notifications
1. Export affected user emails
2. Use personal email client
3. BCC members (respect privacy)
4. Include apology for technical issues

### For Contact Forms
1. Add notice on website about email issues
2. Provide alternative contact method
3. Check form entries in database
4. Manually forward inquiries

## SMTP Settings Reference

### SendGrid Configuration
```
SMTP Host: smtp.sendgrid.net
SMTP Port: 587
Encryption: TLS
Authentication: Yes
Username: apikey
Password: [Your API Key]
```

### Mailgun Configuration
```
SMTP Host: smtp.mailgun.org
SMTP Port: 587
Encryption: TLS
Username: [Your Username]
Password: [Your Password]
```

## Testing Checklist

After making changes:
- [ ] Send test email from plugin
- [ ] Test password reset
- [ ] Test contact form
- [ ] Check email logs
- [ ] Verify in different email clients
- [ ] Check spam folders

## Escalation

If emails still failing after 30 minutes:

1. **Contact Hosting Support**
   - CloudWays: Open urgent ticket
   - Mention email delivery critical

2. **Contact Email Service**
   - SendGrid/Mailgun support
   - Check service status page

3. **Temporary Alternative**
   - Switch to different SMTP service
   - Use WordPress default mail() as last resort

## Prevention

- Monitor email logs weekly
- Keep API keys secure and updated
- Maintain SPF/DKIM
