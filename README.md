# Landing Page Maintenance Guide

This guide will help you maintain and customize the Bitvavo VS Coinbase comparison landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

```html
<!-- Original -->
<div class="text-2xl font-bold text-blue-500">Bitvavo</div>

<!-- How to modify -->
<div class="text-2xl font-bold text-blue-500">Your New Text</div>
```

#### Key Tailwind Classes Explained:
- `text-2xl`: Sets font size (can be changed to `text-xl`, `text-3xl`, etc.)
- `text-blue-500`: Sets text color (try `text-green-500` for green)
- `font-bold`: Sets font weight

### Hero Section
To update the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Bitvavo VS Coinbase Review
    <span class="block text-blue-500 mt-2">What You NEED To Know</span>
</h1>
```

#### Responsive Design Classes:
- `md:text-5xl`: Applies at medium screens
- `lg:text-6xl`: Applies at large screens

### Features Section
Each feature card follows this structure:

```html
<div class="bg-gray-900 rounded-2xl p-8 transform hover:scale-105 transition-all duration-300">
    <div class="h-16 w-16 bg-blue-600/20 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-percentage text-2xl text-blue-500"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Low Commission</h3>
    <p class="text-gray-400">Your feature description here</p>
</div>
```

To modify:
1. Change the icon by updating the `fa-percentage` class
2. Update the heading text
3. Modify the description paragraph

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-500 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-blue-500 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="hover:text-blue-500 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="hover:text-blue-500 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace `#section-name` with your new link
3. For external links, use complete URLs: `href="https://example.com"`

### Call-to-Action Links
Update the Bitvavo affiliate link:

```html
<!-- Original -->
<a href="https://bitvavo.com/invite?a=9A12094098" class="inline-block px-8 py-4 bg-blue-600...">

<!-- Replace with your link -->
<a href="your-new-link-here" class="inline-block px-8 py-4 bg-blue-600...">
```

## Linking Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-blue-500 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-500 transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-blue-500 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-blue-500 transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Design**
   - Check for missing `md:` or `lg:` prefixes in Tailwind classes
   - Verify container classes: `container mx-auto px-6`

2. **Icons Not Showing**
   - Ensure Font Awesome CSS is properly linked:
   ```html
   <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
   ```

3. **Smooth Scrolling Not Working**
   - Verify the HTML tag includes:
   ```html
   <html lang="en" class="scroll-smooth">
   ```

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all CSS classes are spelled correctly
3. Ensure all sections have matching IDs for navigation
4. Test all links before deploying changes

Remember to always backup your files before making significant changes!