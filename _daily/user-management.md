---
layout: default
title: User Management
parent: Daily Operations
nav_order: 3
---

# User Management
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Managing user accounts, roles, and permissions is essential for maintaining site security and proper workflow. This guide covers creating users, assigning roles, and handling common user issues.

## WordPress User Roles

### Role Hierarchy

1. **Administrator**
   - Full site access
   - Can manage all settings
   - Add/remove users
   - Install plugins/themes

2. **Editor**
   - Publish/edit all posts
   - Manage categories
   - Moderate comments
   - Upload media

3. **Author**
   - Publish own posts
   - Upload media
   - Edit own published posts

4. **Contributor**
   - Write posts (can't publish)
   - Edit own pending posts
   - No media upload

5. **Subscriber**
   - Read content
   - Manage profile
   - Comment (if enabled)

### Custom Roles (If Applicable)
- **Staff Writer**: [Custom permissions]
- **Translator**: [Custom permissions]

## Creating New Users

### Step-by-Step Process

1. **Navigate to Users**
   - Go to Users → Add New
   - Or click "+ New" → User

2. **Fill Required Information**
   ```
   Username: firstname.lastname (no spaces)
   Email: user@example.com
   First Name: [User's first name]
   Last Name: [User's last name]
   Website: (optional)
   Password: Generate strong password
   ```

3. **Select Role**
   - Choose appropriate role
   - Start with lower permissions
   - Upgrade as needed

4. **Send Notification**
   - Check "Send User Notification"
   - User receives login details
   - Password reset link included

### Best Practices

{: .important }
> Never share admin credentials. Create individual accounts.

- Use professional usernames
- Require strong passwords
- Assign minimal necessary role
- Document role assignments

## Managing Existing Users

### Viewing Users

1. **Users List**
   - Go to Users → All Users
   - Filter by role
   - Search by name/email

2. **User Information**
   - Click username to edit
   - View posts by user
   - Check last login (if plugin installed)

### Editing Users

1. **Change User Details**
   - Update email
   - Change display name
   - Modify biographical info

2. **Change Role**
   - Select new role from dropdown
   - Consider impact on existing content
   - Notify user of changes

3. **Reset Password**
   - Generate new password
   - Or send reset link
   - Never email passwords directly

### Bulk Actions

1. **Select Multiple Users**
   - Check boxes next to names
   - Use bulk actions dropdown

2. **Available Actions**
   - Delete users
   - Change roles
   - Send password resets

## Common User Tasks

### Password Reset Requests

{: .tip }
> Always verify user identity before resetting passwords

1. **User-Initiated Reset**
   - Direct to login page
   - Click "Lost your password?"
   - Enter username/email

2. **Admin-Initiated Reset**
   - Edit user profile
   - Generate new password
   - Email reset link

### Account Lockouts

**User Can't Login:**
1. Check username/email spelling
2. Verify account exists
3. Check if account is locked (security plugin)
4. Reset password if needed

**Too Many Login Attempts:**
1. Wait for lockout to expire
2. Or manually unlock via security plugin
3. Check for brute force attempts

### Removing Users

{: .warning }
> Always reassign content before deleting users

1. **Delete Process**
   - Go to user profile
   - Delete user link at bottom
   - Choose content attribution:
     - Delete all content
     - Attribute to another user

2. **Alternative: Disable Account**
   - Change role to "No role"
   - Preserves user history
   - Prevents login

## User Security

### Security Best Practices

1. **Password Requirements**
   - Minimum 12 characters
   - Mix of characters
   - No dictionary words
   - Unique per site

2. **Two-Factor Authentication**
   - Enable if plugin available
   - Require for admins
   - Recommend for all users

3. **Regular Audits**
   - Review user list monthly
   - Remove inactive accounts
   - Check for suspicious activity

### Monitoring Activity

1. **Activity Logs**
   - Use activity log plugin
   - Monitor login attempts
   - Track user actions

2. **Suspicious Activity**
   - Multiple failed logins
   - Unusual posting patterns
   - Profile changes

## Member vs User Management

### WordPress Users
- Editorial team
- Content creators
- Site administrators

### Members (Membership Plugin)
- Paying subscribers
- Different system
- Separate documentation

## Troubleshooting

### Email Not Received

1. Check spam folder
2. Verify email address
3. Test email system
4. Send manually if needed

### Permission Issues

**"You don't have permission"**
1. Check user role
2. Verify specific capabilities
3. Clear browser cache
4. Re-login

### Profile Update Errors

1. Check required fields
2. Verify email uniqueness
3. Clear cache
4. Try different browser

## Documentation

### Track User Changes

{: .note }
> Keep record of all user management actions

**Document:**
- New user additions
- Role changes
- Account deletions
- Security incidents

**Template:**
```
Date: [DATE]
Action: [Added/Modified/Deleted]
User: [Username]
Role: [Old Role] → [New Role]
Reason: [Business reason]
Approved by: [Manager name]
```

---

*Last updated: {{ page.last_modified_date | date: '%B %d, %Y' }}*
