# Landing Page Maintenance Guide

This guide will help you customize and maintain your landing page. Follow these detailed instructions to make changes while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**
```html
<!-- Find this line in the header -->
<div class="text-2xl font-bold">Lorem ipsum</div>
```
- Replace "Lorem ipsum" with your company name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)

2. **Navigation Menu Items**
```html
<a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Home</a>
```
- Update link text between `<a>` tags
- Keep the classes for consistent styling
- These appear in both desktop and mobile menus

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">Transform Your Business Presence</h1>
<p class="text-xl text-gray-600 mb-12">Modern solutions for modern businesses.</p>
```
- Update heading and paragraph text
- Maintain responsive text sizes:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Services Section
Each service card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Web Design</h3>
    <p class="text-gray-600">Modern and minimalist designs...</p>
</div>
```
- Update service titles and descriptions
- Keep the `bg-white` and shadow classes for consistent styling

## Fixing Broken Links

### Navigation Links
Current placeholder links:
```html
<a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Home</a>
```
To update:
1. Replace `#` with proper URLs:
   - Internal pages: `href="about.html"`
   - External pages: `href="https://example.com"`
2. Update both desktop and mobile menu versions

### Call-to-Action Buttons
```html
<a href="#" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">Get Started</a>
```
- Replace `#` with your contact or signup page URL
- Keep all styling classes to maintain button appearance

### Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Home</a></li>
</ul>
```
- Update all footer menu links
- Ensure social media links point to your profiles

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:
```html
<ul class="space-y-2">
    <!-- Add after existing links -->
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
- If layout breaks, check that you haven't removed important Tailwind classes:
  - `md:` prefix for medium screens
  - `lg:` prefix for large screens
  - `container` and `mx-auto` for centering

2. **Missing Styles**
- Ensure the Tailwind CSS link remains in the header:
```html
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
```

3. **Mobile Menu Issues**
- Keep the Alpine.js script tag:
```html
<script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>
```
- Maintain the `x-data` and `x-show` attributes on menu elements

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class references
- Verify all closing tags match opening tags
- Test your page on multiple devices and browsers

Remember to always backup your files before making changes, and test thoroughly after each modification.