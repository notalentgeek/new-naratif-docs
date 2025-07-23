---
layout: default
title: Managing Media
parent: Daily Operations
nav_order: 2
---

# Managing Media
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Overview

Proper media management is crucial for site performance and organization. This guide covers uploading, organizing, and optimizing media files in WordPress.

## Media Guidelines

### Accepted File Types
- **Images**: JPG, PNG, GIF, WebP, SVG (with caution)
- **Documents**: PDF, DOC, DOCX
- **Video**: MP4, MOV (use embed for YouTube/Vimeo)
- **Audio**: MP3, WAV

### Size Limits
- **Images**: Maximum 2MB (optimize larger files)
- **Documents**: Maximum 10MB
- **Server limit**: 64MB (but avoid large files)

### Image Dimensions
- **Featured images**: 1200x630px minimum
- **In-content images**: 1200px wide maximum
- **Thumbnails**: Will be auto-generated

## Uploading Media

### Method 1: Media Library

1. **Access Media Library**
   - Go to Media → Library
   - Click "Add New"

2. **Upload Files**
   - Drag and drop files
   - Or click "Select Files"
   - Wait for upload to complete

3. **Add Media Details**
   - Title: Descriptive name
   - Alt Text: Describe image for accessibility
   - Caption: If needed for context
   - Description: Additional details

### Method 2: Within Posts/Pages

1. **Add Media Block**
   - Click "+" in editor
   - Choose Image/Video/Audio block
   - Upload or select from library

2. **Direct Upload**
   - Drag image directly into editor
   - Automatically creates image block

## Organizing Media

### Using Folders (If Plugin Installed)

1. **Create Folders**
   - In Media Library, create folder structure
   - Organize by: Year/Month, Content Type, or Campaign

2. **Move Existing Media**
   - Select files
   - Drag to appropriate folder
   - Bulk organize old media

### Naming Conventions

{: .important }
> Use consistent naming for easy searching

**Recommended Format:**
- `yyyy-mm-dd-description-type.jpg`
- Example: `2025-01-15-climate-protest-featured.jpg`

**Avoid:**
- Spaces (use hyphens)
- Special characters
- Generic names (IMG_1234.jpg)

## Image Optimization

### Before Upload

1. **Resize Images**
   - Use tools: Photoshop, GIMP, Canva
   - Maximum width: 1200px for content
   - Keep aspect ratio

2. **Compress Images**
   - TinyPNG.com
   - ImageOptim (Mac)
   - Squoosh.app

3. **Choose Right Format**
   - JPG: Photos
   - PNG: Graphics with transparency
   - WebP: Modern browsers (best compression)

### After Upload

1. **WordPress Auto-Optimization**
   - Multiple sizes created automatically
   - Serves appropriate size based on context

2. **Additional Optimization**
   - Use image optimization plugins
   - Run bulk optimization monthly

## Media Management Tasks

### Daily Tasks

- [ ] Check recently uploaded media for proper naming
- [ ] Add missing alt text to new images
- [ ] Delete unused uploaded files
- [ ] Verify featured images for new posts

### Weekly Tasks

- [ ] Review media library for duplicates
- [ ] Organize new media into folders
- [ ] Check for broken image links
- [ ] Optimize any large files

### Monthly Tasks

- [ ] Run bulk image optimization
- [ ] Audit media library size
- [ ] Delete truly unused media
- [ ] Backup media library

## Finding and Reusing Media

### Search Techniques

1. **By Date**
   - Use date filter in Media Library
   - Find recent uploads easily

2. **By Type**
   - Filter by Images, Audio, Video
   - Narrow down search results

3. **By Keyword**
   - Search by filename
   - Search by alt text
   - Use consistent naming

### Reusing Images

{: .tip }
> Always check image rights before reusing

1. **From Media Library**
   - Click "Add Media" in post
   - Search or browse
   - Select and insert

2. **Copy Media URL**
   - Click on image in library
   - Copy URL from details
   - Use for external sharing

## Troubleshooting

### Upload Errors

**"File type not permitted"**
- Check file extension
- Ensure not corrupted
- Contact admin for special types

**"File exceeds size limit"**
- Compress image
- Resize dimensions
- Use external hosting for large files

### Display Issues

**Broken Images**
- Check if file exists
- Regenerate thumbnails
- Clear cache

**Slow Loading**
- Optimize image size
- Use lazy loading
- Consider CDN

## Best Practices

### Accessibility
- Always add alt text
- Describe image content
- Use captions for complex images

### SEO
- Use descriptive filenames
- Include keywords naturally
- Optimize file size for speed

### Legal
- Verify image rights
- Credit photographers
- Keep license documentation

### Performance
- Optimize before upload
- Use appropriate dimensions
- Regular library cleanup

## Advanced Tips

### Bulk Actions

1. **Select Multiple Files**
   - Shift-click for range
   - Ctrl/Cmd-click for individual

2. **Bulk Delete**
   - Select files
   - Choose "Delete Permanently"
   - Confirm action

### Hotlinking Prevention

- Use security plugins
- Add .htaccess rules
- Monitor bandwidth usage

---

*Last updated: {{ page.last_modified_date | date: '%B %d, %Y' }}*
