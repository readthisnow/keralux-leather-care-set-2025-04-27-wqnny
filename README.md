# Keralux Landing Page Maintenance Guide

This guide will help you maintain and customize the Keralux Leather Care Set landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**
```html
<!-- Find this section in the header -->
<a href="/" class="text-2xl font-bold text-gray-900">Keralux</a>
```
- Replace "Keralux" with your desired brand name
- Adjust text size by changing `text-2xl` to `text-3xl` for larger text or `text-xl` for smaller

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 tracking-tight leading-tight mb-8">
    Koop Keralux Leather Care Set Met Korting
</h1>
```
- Replace the text between the `<h1>` tags
- The classes ensure responsive text sizing:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
To add or modify feature cards:

1. Locate the features grid:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
```

2. Copy and paste this template for each new feature:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <svg class="w-12 h-12" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/>
        </svg>
    </div>
    <h3 class="text-xl font-semibold mb-4">Your Feature Title</h3>
    <p class="text-gray-600">Your feature description here.</p>
</div>
```

## Managing Links

### Navigation Menu Links
The navigation menu contains internal page links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Kenmerken</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Change the `href` value to match your section IDs
2. Update the link text between the `<a>` tags
3. Keep the `#` prefix for internal page links

### Call-to-Action Links
Update the purchase links:

```html
<a href="https://amzn.to/3Ykk6ZX" class="inline-flex items-center px-8 py-4 text-lg font-semibold text-white bg-blue-600 rounded-full hover:bg-blue-700 transform hover:scale-105 transition-all duration-300 shadow-lg">
```
- Replace `https://amzn.to/3Ykk6ZX` with your product link
- Test the link after updating to ensure it works correctly

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer links section:

```html
<div>
    <h3 class="text-xl font-semibold mb-4">Links</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Ensure section IDs match the href values
- Section IDs should not contain spaces
- Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues**
- Check that you've maintained the responsive classes:
  - `md:` prefix for medium screens
  - `lg:` prefix for large screens
- Don't remove the `container` class from main sections

3. **Style Conflicts**
- Keep the order of Tailwind classes consistent
- Don't mix custom CSS with Tailwind unless necessary
- Maintain the existing color scheme using Tailwind's color classes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all links work in multiple browsers
- Test the page on different screen sizes using browser dev tools

Remember to always test your changes in multiple browsers and screen sizes before publishing updates to the live site.