# Ascot Vale Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Ascot Vale Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Modifying Text Content

The landing page is divided into clear sections. Here's how to update text in each area:

#### Header (Company Name)
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">
    Ascot Vale  <!-- Change company name here -->
</a>
```

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900">
    Ascot Vale accounting services  <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    Accounting excellence with a personal touch  <!-- Update subheading here -->
</p>
```

### Understanding Tailwind CSS Classes

Key classes used in this landing page:

1. Text Sizes:
   - `text-4xl`: Large text (Hero headline)
   - `text-xl`: Medium text (Regular paragraphs)
   - `text-2xl`: Slightly larger text (Navigation)

2. Colors:
   - `text-gray-800`: Dark gray text
   - `text-blue-600`: Blue accent color
   - `bg-white`: White background
   - `bg-gray-50`: Light gray background

3. Spacing:
   - `px-6`: Horizontal padding
   - `py-4`: Vertical padding
   - `mb-4`: Bottom margin
   - `mt-12`: Top margin

To modify styling, replace these classes as needed. For example:

```html
<!-- Original -->
<div class="bg-white rounded-xl p-8">

<!-- Modified for different color and padding -->
<div class="bg-gray-50 rounded-xl p-6">
```

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Change the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- Original -->
<a href="#services">Services</a>

<!-- Modified for external link -->
<a href="https://example.com/services">Services</a>
```

### Call-to-Action Buttons
The page contains two main CTA buttons:

```html
<!-- Hero section CTA -->
<a href="https://theaccountants.com" class="inline-block bg-blue-600 text-white px-8 py-4">
    Get Started Today
</a>

<!-- Bottom CTA -->
<a href="https://theaccountants.com" class="inline-block bg-white text-blue-600 px-8 py-4">
    Get Started Now
</a>
```

To update these:
1. Replace `https://theaccountants.com` with your desired URL
2. Update button text as needed

## Adding Privacy and Terms Pages

### Footer Legal Links
Located in the footer section:

```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to privacy and terms pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

### Responsive Design Issues
If elements don't look right on mobile:
- Check for `md:` prefixed classes
- Ensure the viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Broken Links
If links aren't working:
- Verify file paths are correct
- Ensure hash links (`#services`) match section IDs
- Check for typos in URLs
- Test both internal and external links

### Missing Styles
If Tailwind styles aren't applying:
- Confirm the Tailwind CDN is loading:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
- Check for proper class spelling
- Ensure there are no spaces in class names

Remember to:
- Test all changes in multiple browsers
- Verify mobile responsiveness
- Keep backups before making significant changes
- Maintain consistent styling across all pages