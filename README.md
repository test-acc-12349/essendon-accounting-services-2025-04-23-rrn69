# Essendon Accounting Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Essendon Accounting landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu:

```html
<header class="fixed w-full bg-gray-900/95 backdrop-blur-sm border-b border-gray-800 z-50">
    <nav class="container mx-auto px-6 py-4">
        <!-- Logo -->
        <a href="/" class="text-2xl font-bold text-white tracking-tight">
            Essendon<span class="text-blue-500">.</span>
        </a>
```

To modify:
1. Change company name: Replace "Essendon" with your company name
2. Adjust logo styling: Modify `text-2xl` for size and `text-blue-500` for accent color

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Essendon accounting services
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Trusted advisors for your financial future
</p>
```

To modify:
1. Update heading: Replace text between `<h1>` tags
2. Change subheading: Modify text in the `<p>` tag
3. Adjust responsive text sizes:
   - `text-4xl`: Mobile size
   - `md:text-5xl`: Tablet size
   - `lg:text-6xl`: Desktop size

### Service Cards
Located in the services section:

```html
<div class="bg-gray-900 p-8 rounded-2xl hover:transform hover:scale-105 transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">Tax Optimization</h3>
    <p class="text-gray-400">Strategic tax planning and optimization...</p>
</div>
```

To modify:
1. Change service title: Update text in `<h3>` tags
2. Modify description: Update text in `<p>` tags
3. Adjust card styling:
   - `bg-gray-900`: Background color
   - `p-8`: Padding
   - `rounded-2xl`: Border radius
   - `hover:scale-105`: Hover animation

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
    <a href="https://theaccountants.com" class="px-6 py-2 bg-blue-600">Get Started</a>
</div>
```

To update:
1. Internal links (starting with #): Ensure they match section IDs
2. External links: Replace `https://theaccountants.com` with your actual URL
3. Add new links: Copy existing link format and modify href/text

### Footer Links
Located at the bottom of the page:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Tax Services</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Cloud Accounting</a></li>
</ul>
```

To update:
1. Replace `href="#"` with actual URLs
2. Maintain consistent styling using `hover:text-white transition-colors duration-300`

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Current footer legal section:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link properly:
1. Create privacy.html and terms.html in your root directory
2. Update href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Example: `href="#services"` needs matching `id="services"` in section tag

2. **Responsive Design Issues**
   - Check media query classes (md: and lg: prefixes)
   - Verify container class is present: `container mx-auto px-6`

3. **Hover Effects Not Working**
   - Ensure transition classes are present: `transition-colors duration-300`
   - Check hover classes begin with `hover:`

4. **Styling Inconsistencies**
   - Copy existing class combinations for similar elements
   - Maintain color scheme using provided color classes (blue-500, gray-900, etc.)

Remember to test all changes across different screen sizes and browsers before deploying to production.