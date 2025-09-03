---
layout: default
title: Complete Elementor Guide
nav_order: 1
parent: Daily Operations
---

# New Naratif Elementor Complete Guide
{: .no_toc }

A comprehensive guide to using Elementor for creating beautiful content at New Naratif.
{: .fs-6 .fw-300 }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Getting Started with Elementor

### Introduction to Elementor at New Naratif

Elementor is the primary page builder used at New Naratif for creating visually rich content. It provides a drag-and-drop interface that allows team members to create professional layouts without coding knowledge.

**Current Implementation:**
- Elementor Pro is installed and active
- Integration with BuddyBoss child theme
- Mixed content ecosystem (some posts use Elementor, others use standard WordPress editor)
- Custom conditions implemented for theme builder compatibility

### Accessing Elementor Editor

There are three ways to access Elementor:

1. **From WordPress Admin:**
   - Navigate to Pages or Posts
   - Hover over the item you want to edit
   - Click "Edit with Elementor"

2. **From the WordPress Editor:**
   - Open any page/post in WordPress editor
   - Click the "Edit with Elementor" button at the top

3. **From the Frontend (when logged in):**
   - Visit any Elementor-built page
   - Click "Edit with Elementor" in the admin bar

### Understanding the Interface

The Elementor interface consists of three main areas:

**Left Panel (Widget Panel):**
- Contains all available widgets
- Settings for selected elements
- Page settings and controls
- Navigator for complex layouts

**Center Canvas (Preview Area):**
- Live preview of your page
- Direct editing capabilities
- Responsive preview options
- Interactive design area

**Bottom Bar (Tools Bar):**
- Responsive mode switcher (Desktop/Tablet/Mobile)
- Preview button
- Update/Publish button
- Settings menu
- History (undo/redo)

### Elementor vs WordPress Editor Decision Tree

Use Elementor when:
- Creating landing pages or campaign pages
- Building complex layouts with multiple columns
- Implementing custom designs outside standard templates
- Creating membership or promotional pages
- Developing interactive content with animations

Use WordPress Editor when:
- Publishing standard blog posts or articles
- Creating simple text-based content
- Working with contributors who don't know Elementor
- Optimizing for page speed (simple content)
- Maintaining consistency with existing non-Elementor posts

---

## Elementor Fundamentals

### The Building Block System

Elementor uses a hierarchical structure:

```
Section → Columns → Widgets
```

**Sections:**
- The largest container element
- Can be full-width or boxed
- Contains one or more columns
- Controls background, spacing, and layout

**Creating a Section:**
1. Click the "+" button in the editor
2. Choose your column structure (1-6 columns)
3. Adjust column widths by dragging handles
4. Access section settings via right-click menu

**Columns:**
- Vertical divisions within sections
- Responsive width controls
- Can contain multiple widgets
- Independent padding and margin settings

**Widgets:**
- Individual content elements
- Dragged from left panel into columns
- Each has specific settings and styling options
- Can be duplicated, copied, or saved as global

### Working with Templates

**Using Existing Templates:**
1. Click the folder icon in the editor
2. Browse "My Templates" for saved designs
3. Select and insert into your page
4. Customize as needed

**Creating Custom Templates:**
1. Design your layout
2. Right-click on the section
3. Select "Save as Template"
4. Name it descriptively (e.g., "Article-Header-Standard")
5. Add tags for easy searching

**Template Library Organization:**
- Use naming conventions: `[Type]-[Purpose]-[Version]`
- Examples: `Landing-Membership-v2`, `Article-Header-Standard`
- Tag templates by department or campaign
- Regularly review and clean unused templates

### Navigation and Shortcuts

**Essential Keyboard Shortcuts:**
- `Ctrl/Cmd + Z`: Undo
- `Ctrl/Cmd + Shift + Z`: Redo
- `Ctrl/Cmd + D`: Duplicate element
- `Ctrl/Cmd + C/V`: Copy/Paste element
- `Ctrl/Cmd + Shift + V`: Paste style
- `Delete`: Remove selected element
- `Ctrl/Cmd + S`: Save current work

**Navigator Panel:**
1. Click the navigator icon (bottom left)
2. See hierarchical view of all elements
3. Rename elements for clarity
4. Drag to reorder elements
5. Lock elements to prevent accidental changes

---

## Content Creation Workflows

### Creating New Pages with Elementor

**Step-by-Step Process:**

1. **Create the Page:**
   - Go to Pages → Add New
   - Enter page title
   - Click "Edit with Elementor"

2. **Choose Starting Point:**
   - Start from scratch (blank canvas)
   - Use a template from library
   - Duplicate existing page structure

3. **Build Your Layout:**
   - Add sections and columns
   - Drag widgets into place
   - Configure widget settings
   - Apply styling and spacing

4. **Optimize for Mobile:**
   - Switch to tablet/mobile view
   - Adjust layouts for each breakpoint
   - Test interactive elements
   - Hide unnecessary elements on mobile

5. **Configure Page Settings:**
   - Click gear icon (bottom left)
   - Set page layout (full width/boxed)
   - Configure SEO settings
   - Add featured image if needed

6. **Preview and Publish:**
   - Preview in new tab
   - Test all links and forms
   - Check responsive behavior
   - Click "Publish" when ready

### Creating New Posts with Elementor

**Important Consideration:** Not all posts at New Naratif use Elementor. Evaluate whether your content needs custom design.

**When to Use Elementor for Posts:**
- Feature articles with custom layouts
- Photo essays or visual stories
- Interactive content pieces
- Special reports with data visualization

**Process:**
1. Posts → Add New
2. Add title and configure categories/tags
3. Click "Edit with Elementor"
4. Design your post layout
5. Ensure consistency with site styling
6. Test preview before publishing

### Editing Existing Content

**For Elementor Content:**
1. Locate the page/post
2. Click "Edit with Elementor"
3. Make necessary changes
4. Update to save changes

**Converting Standard Posts to Elementor:**
1. Open post in WordPress editor
2. Copy all content (Ctrl+A, Ctrl+C)
3. Click "Edit with Elementor"
4. Add Text Editor widget
5. Paste content
6. Format and enhance with Elementor features
7. Save as draft and preview thoroughly

---

## Essential Widgets for New Naratif

### Text and Typography

**Text Editor Widget:**
- Primary widget for article content
- Supports rich text formatting
- Can paste from Word/Google Docs
- Maintains SEO-friendly HTML structure

**Best Practices:**
- Use consistent heading hierarchy (H2 → H3 → H4)
- Apply typography settings globally when possible
- Keep paragraphs concise for readability
- Use bullet points for scannable content

**Heading Widget:**
- For standalone headings
- Better performance than Text Editor for simple headings
- Supports dynamic content
- Advanced typography controls

**Typography Settings:**
- Font: Follow New Naratif brand guidelines
- Desktop size: H1 (36px), H2 (28px), H3 (24px), Body (16px)
- Line height: 1.4-1.6 for body text
- Mobile adjustments: Reduce heading sizes by 20-30%

### Media Management

**Image Widget:**
- Supports lazy loading
- Built-in lightbox option
- Caption and alt text fields
- Link options (none, media file, custom URL)

**Image Optimization:**
1. Resize images before uploading (max 1920px width)
2. Use WebP format when possible
3. Compress images (aim for <200KB)
4. Always add alt text for accessibility
5. Use descriptive filenames

**Video Widget:**
- YouTube/Vimeo integration preferred
- Self-hosted video as last resort (bandwidth considerations)
- Autoplay settings (muted only for user experience)
- Custom thumbnail options

**Gallery Widget:**
- Multiple layout options (grid, masonry, carousel)
- Lightbox functionality
- Filterable galleries for categories
- Performance impact: limit to 20 images per gallery

### Interactive Elements

**Button Widget:**
- Consistent styling across site
- Clear call-to-action text
- Hover effects for engagement
- Size variations (small, medium, large)

**Button Best Practices:**
- Primary CTA: "Join Now", "Subscribe", "Donate"
- Secondary: "Learn More", "Read Article"
- Use action verbs
- Maintain visual hierarchy

**Form Integration:**
New Naratif uses forms for:
- Newsletter signups
- Membership applications
- Contact forms
- Event registrations

**Implementation:**
1. Add Form widget
2. Configure fields as needed
3. Set up email notifications
4. Add success message
5. Test thoroughly before publishing

**Social Icons:**
- Link to New Naratif social profiles
- Consistent brand colors
- Strategic placement (header/footer/sidebar)
- Include: Facebook, Twitter, Instagram, LinkedIn

---

## New Naratif-Specific Implementations

### Brand Consistency Guidelines

**Color Palette:**
```css
Primary: #E85A4F    /* New Naratif Red */
Secondary: #1A1A1A  /* Dark Gray */
Accent: #F7B733     /* Yellow */
Text: #333333       /* Body Text */
Background: #FFFFFF /* White */
```

**Typography Standards:**
- Headings: Freight Sans (via Adobe Fonts)
- Body: System fonts for performance
- Consistent weight mappings:
  - Light: 300
  - Regular: 400
  - Medium: 500
  - Bold: 700

**Spacing Conventions:**
- Section padding: 60px top/bottom (desktop), 40px (mobile)
- Column gaps: 20px default
- Widget margins: 20px bottom
- Consistent throughout site

### Common Page Layouts

**Article Page Template:**
```
Header Section
├── Featured Image (full width)
├── Title (H1)
├── Meta information (author, date, category)
└── Social sharing buttons

Content Section
├── Text content (with inline images)
├── Pull quotes
├── Related images/galleries
└── Embedded media

Footer Section
├── Author bio
├── Related articles
├── Comments (if enabled)
└── Newsletter signup
```

**Landing Page Structure:**
```
Hero Section
├── Headline
├── Subheadline
├── CTA button
└── Background image/video

Features Section
├── 3-column layout
├── Icon boxes
└── Brief descriptions

Content Section
├── Detailed information
├── Supporting images
└── Testimonials

CTA Section
├── Strong call-to-action
├── Form or button
└── Urgency messaging
```

**Campaign Page Components:**
- Hero banner with campaign visuals
- Progress indicators (for fundraising)
- Story sections with mixed media
- Donation/action widgets
- Social proof elements
- Share campaign tools

### Social Sharing Integration

**Implementation Steps:**
1. Add Share Buttons widget
2. Configure networks:
   - Facebook (primary)
   - Twitter/X
   - WhatsApp (mobile important)
   - Email
   - Copy link

**Placement Strategy:**
- Floating sidebar (desktop)
- Sticky bottom bar (mobile)
- After content block
- Within hero sections for campaigns

### Membership CTAs

**Standard Membership Blocks:**

**Inline CTA:**
```
[Box with border]
Support Independent Journalism
Join New Naratif as a member and help us 
continue our important work.
[Join Now Button]
```

**Footer Membership Block:**
```
[Full-width section]
Become a Member
- Access all premium content
- Support independent media
- Join our community
[Membership Tiers] [Sign Up Button]
```

{: .important }
> Always use production URLs (newnaratif.com) not development URLs (dev.newnaratif.com)

---

## Advanced Features

### Dynamic Content

Dynamic content pulls information from WordPress automatically.

**Common Use Cases:**
- Post title in hero sections
- Author name and bio
- Publication date
- Category/tag display
- Custom field values

**Implementation:**
1. Select widget (e.g., Heading)
2. Click dynamic tag icon (stack icon)
3. Choose data source:
   - Post Title
   - Post Excerpt
   - Custom Fields
   - Author Info
4. Configure display settings

### Theme Builder

The Theme Builder controls templates for entire post types.

**Current Implementation:**
- Single Post template for articles
- Archive template for category pages
- Custom conditions for Elementor vs non-Elementor posts

**Creating Custom Conditions:**
When you need different templates for different content types:

```php
// Example: Posts built with Elementor
// This is already implemented at New Naratif
add_action('elementor/theme/register_conditions', function($conditions_manager) {
    // Custom condition logic here
});
```

**Managing Templates:**
1. Navigate to Templates → Theme Builder
2. Create new template
3. Set display conditions carefully
4. Test on multiple post types
5. Monitor for conflicts

### Global Widgets

Global widgets maintain consistency across the site.

**Creating Global Widgets:**
1. Design your widget
2. Right-click → Save as Global
3. Name descriptively (e.g., "Global-Newsletter-Signup")
4. Use across multiple pages
5. Edit once, update everywhere

**Use Cases:**
- Newsletter signup forms
- Membership CTAs
- Footer information
- Sidebar widgets
- Author bio boxes

### Custom CSS

For advanced styling beyond Elementor's options:

**Adding Custom CSS:**
1. Select element
2. Advanced tab → Custom CSS
3. Add CSS code
4. Use `selector` as placeholder

**Example:**
```css
selector {
    transition: all 0.3s ease;
    border-radius: 10px;
}

selector:hover {
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0,0,0,0.3);
}
```

---

## Performance Optimization

### Known Performance Issues

**Current Challenges:**
- Homepage loads slowly due to complex Elementor structure
- Editor performance degrades with many elements
- Mobile performance particularly affected
- Multiple font requests slow initial load

### Best Practices for Page Speed

**Content Optimization:**
1. **Limit Sections:** Maximum 10-15 sections per page
2. **Optimize Images:** 
   - Use appropriate formats (WebP preferred)
   - Lazy load below-fold images
   - Compress all images
3. **Minimize Animations:** 
   - Use sparingly
   - Disable on mobile
   - Prefer CSS over JavaScript animations
4. **Widget Selection:**
   - Use basic widgets when possible
   - Avoid nested carousels
   - Limit dynamic content widgets

**Technical Optimizations:**
1. **Enable Elementor Settings:**
   - Improved CSS Loading
   - Optimized DOM Output
   - Lazy Load Background Images

2. **Regular Maintenance:**
   - Clean revision history
   - Remove unused templates
   - Optimize database

3. **Content Delivery:**
   - Use CDN for media files
   - Minimize external requests
   - Combine CSS/JS when possible

### When NOT to Use Elementor

Avoid Elementor for:
- Simple blog posts (use WordPress editor)
- Content that needs frequent updates
- High-traffic pages requiring maximum speed
- Content managed by non-technical users
- Archive pages with many posts

**Performance Comparison:**
- Standard WordPress post: ~1-2 second load
- Simple Elementor page: ~2-3 second load
- Complex Elementor page: ~3-5+ second load

---

## Troubleshooting Guide

### Common Issues and Solutions

**Issue: Elementor Won't Load**

*Symptoms:* Loading screen stuck, white screen, or error messages

*Solutions:*
1. Clear browser cache and cookies
2. Try incognito/private mode
3. Disable browser extensions
4. Increase PHP memory limit
5. Check for plugin conflicts

{: .note }
> For homepage specifically: Be patient - it can take several minutes to load due to complexity

**Issue: Content Not Displaying Correctly**

*Symptoms:* Missing elements, broken layouts, wrong styling

*Solutions:*
1. Regenerate CSS (Elementor → Tools → Regenerate CSS)
2. Clear all caches (server, CDN, browser)
3. Check responsive settings
4. Verify theme compatibility
5. Review custom CSS for conflicts

**Issue: Changes Not Saving**

*Solutions:*
1. Check user permissions
2. Increase PHP max_input_vars
3. Disable security plugins temporarily
4. Save in smaller increments
5. Check server error logs

**Issue: Mobile Display Problems**

*Solutions:*
1. Use responsive preview while editing
2. Check hide/show settings per device
3. Adjust column settings for mobile
4. Test on actual devices
5. Consider mobile-first design approach

### Conflict Resolution

**Plugin Conflicts:**
1. Deactivate all plugins except Elementor
2. Test if issue persists
3. Reactivate plugins one by one
4. Identify conflicting plugin
5. Find alternative or contact support

**Theme Conflicts:**
- New Naratif uses BuddyBoss child theme
- Known compatible with Elementor
- Check child theme customizations
- Verify functions.php modifications

### Emergency Recovery

**If Page Breaks:**
1. Access WordPress admin directly
2. Navigate to page/post list
3. Switch to WordPress editor
4. Save content as draft
5. Restore from revision history
6. Contact technical support if needed

**Revision History:**
1. Edit with Elementor
2. Click History icon (clock symbol)
3. Browse through versions
4. Click "Apply" to restore
5. Save immediately after restoring

---

## Quick Reference

### Essential Keyboard Shortcuts

| Action | Windows/Linux | Mac |
|--------|--------------|-----|
| Undo | Ctrl + Z | Cmd + Z |
| Redo | Ctrl + Shift + Z | Cmd + Shift + Z |
| Save | Ctrl + S | Cmd + S |
| Duplicate | Ctrl + D | Cmd + D |
| Copy | Ctrl + C | Cmd + C |
| Paste | Ctrl + V | Cmd + V |
| Paste Style | Ctrl + Shift + V | Cmd + Shift + V |
| Delete | Delete | Delete |
| Navigator | Ctrl + I | Cmd + I |
| Preview | Ctrl + P | Cmd + P |

### Widget Panel Icons

- 📝 Basic: Text, heading, image, video, button
- 🎨 General: Columns, spacer, divider, Google Maps
- 🔧 Pro: Posts, portfolio, forms, slides
- 🌐 WordPress: WordPress widgets
- ⭐ Global: Saved global widgets

### Responsive Breakpoints

- **Desktop:** 1025px and above
- **Tablet:** 768px to 1024px
- **Mobile:** 767px and below

### CSS Classes for Custom Styling

Common Elementor classes to target:
```css
.elementor-widget-heading     /* All heading widgets */
.elementor-widget-text-editor /* All text editor widgets */
.elementor-widget-image       /* All image widgets */
.elementor-button             /* All buttons */
.elementor-section            /* All sections */
.elementor-column             /* All columns */
```

### Performance Checklist

Before publishing any Elementor page:
- [ ] Images optimized and compressed
- [ ] Responsive settings configured
- [ ] Unnecessary widgets removed
- [ ] Custom CSS minimized
- [ ] Preview tested on all devices
- [ ] Forms tested and working
- [ ] Links verified (no dev URLs)
- [ ] SEO settings configured
- [ ] Performance impact assessed

### Support Resources

**Internal:**
- Technical documentation in Obsidian vault
- Previous troubleshooting logs
- Team knowledge base

**External:**
- [Elementor Documentation](https://elementor.com/help/)
- [WordPress Codex](https://codex.wordpress.org/)
- New Naratif technical support channel

---

*Last updated: {{ site.time | date: '%B %d, %Y' }}*