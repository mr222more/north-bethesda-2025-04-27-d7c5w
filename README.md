# Custom Euro Glass Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Custom Euro Glass landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<a href="/" class="text-2xl font-bold text-gray-900">Custom Euro Glass</a>
```
- Replace "Custom Euro Glass" with your desired company name
- The `text-2xl` class controls size (options: text-xl, text-3xl, text-4xl)

2. Navigation Menu Items:
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```
- Replace "Features" with new menu item text
- Keep the `hover:text-gray-900` class for consistent hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">North Bethesda</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Custom shower glass for luxury bathrooms</p>
```
- Update heading and subheading text as needed
- The responsive classes (`md:text-5xl lg:text-6xl`) ensure proper sizing on different devices
- Don't remove these responsive classes to maintain mobile compatibility

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Tempered Safety Glass</h3>
    <p class="text-gray-600">Resists cracks and breaks...</p>
</div>
```
To add new features:
1. Copy the entire `<div>` block
2. Paste within the `grid` container
3. Update heading and description text
4. Maintain the class structure for consistent styling

## Managing Links

### External Links
Current external links point to customeuroglass.com:
```html
<a href="http://www.customeuroglass.com" class="bg-blue-600 text-white px-6 py-2 rounded-full">Contact Us</a>
```
To update:
1. Replace `http://www.customeuroglass.com` with your desired URL
2. Always include `http://` or `https://`
3. Test the link after updating

### Internal Links
Navigation menu internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
These correspond to section IDs:
```html
<section id="features">
<section id="benefits">
<section id="faq">
```
To modify:
1. Update both the `href` and corresponding `id` attributes
2. Keep the `#` symbol for internal links
3. Ensure IDs are unique and match exactly

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the Quick Links section:
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling:
```html
<main class="pt-32 pb-24">
    <div class="container mx-auto px-6">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Policy content here -->
    </div>
</main>
```

## Troubleshooting

### Common Issues

1. Broken Styles
- Verify the Tailwind CDN link is present:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
- Check for typos in class names
- Classes are case-sensitive

2. Navigation Links Not Working
- Ensure section IDs match href attributes exactly
- IDs cannot contain spaces
- Check for missing `#` in href attributes

3. Responsive Issues
- Don't remove `md:` or `lg:` prefixes from classes
- Test on multiple screen sizes
- Use browser developer tools to check mobile view

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all changes in a development environment first
- Keep a backup of the original file before making changes

Remember to test all changes across different devices and browsers before publishing to your live site.