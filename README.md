# DSJ Tax Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the DSJ Tax landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<div class="text-2xl font-bold text-blue-500">DSJ Tax</div>
```
- To change the company name: Replace "DSJ Tax" with your text
- To modify logo size: Adjust `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)
- To change logo color: Replace `text-blue-500` with another color (e.g., `text-red-500`)

### Hero Section
The main banner section contains your primary headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    DSJ Tax Multiservices Trusted Tax Prep & Debt Collection South Florida
</h1>
```
- To update headline: Replace the text between the `<h1>` tags
- Text sizes are responsive:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

### Feature Cards
Each feature card follows this structure:

```html
<div class="bg-gray-900 p-8 rounded-2xl hover:transform hover:scale-105 transition-all duration-300">
    <i class="fas fa-shield-alt text-4xl text-blue-500 mb-4"></i>
    <h3 class="text-2xl font-bold mb-4">Trust</h3>
    <p class="text-gray-400">Your financial matters...</p>
</div>
```
- To change icons: Replace `fa-shield-alt` with any [Font Awesome](https://fontawesome.com/icons) icon name
- To modify card background: Update `bg-gray-900` to any Tailwind color class
- To adjust spacing: Modify `p-8` (padding) or `mb-4` (margin) values

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="hover:text-blue-500 transition-colors duration-300">Services</a>
    <a href="#benefits" class="hover:text-blue-500 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="hover:text-blue-500 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="hover:text-blue-500 transition-colors duration-300">Contact</a>
</div>
```
To update links:
1. Locate the `href` attribute
2. For internal sections: Use `#section-id`
3. For external links: Use full URL (e.g., `https://example.com`)

### Call-to-Action Buttons
```html
<a href="https://form.jotform.com/250476421727054" class="bg-blue-600 text-white px-8 py-4 rounded-full">
    Start Your Tax Journey
</a>
```
- Update the `href` with your form or landing page URL
- Modify button text between the `<a>` tags
- Adjust styling using Tailwind classes:
  - Background color: `bg-blue-600`
  - Text color: `text-white`
  - Padding: `px-8 py-4`
  - Border radius: `rounded-full`

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer section:
```html
<div>
    <h4 class="text-xl font-bold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-blue-500 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-500">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-blue-500">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Section IDs should not contain spaces
   - Example: `href="#contact"` links to `id="contact"`

2. **Responsive Design Issues**
   - Check mobile responsiveness using browser dev tools
   - Verify media query classes (e.g., `md:`, `lg:`) are correct
   - Test different screen sizes

3. **Icon Not Displaying**
   - Verify Font Awesome CDN is loaded
   - Check icon class names against Font Awesome documentation
   - Ensure proper icon prefix (`fas`, `fab`, etc.)

4. **Styling Inconsistencies**
   - Maintain color scheme using Tailwind color classes
   - Keep consistent spacing using Tailwind spacing utilities
   - Follow existing pattern for hover effects

### Need Help?
- Review [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check [Font Awesome](https://fontawesome.com/icons) for icon references
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different devices and browsers before deploying to production.