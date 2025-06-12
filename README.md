# Texas Pros Garage Doors Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Pros Garage Doors landing page. This documentation assumes basic familiarity with HTML but includes beginner-friendly explanations.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold text-blue-600">Texas Pros</a>
```
- To change company name: Replace "Texas Pros" with your text
- To modify text size: Change `text-2xl` to `text-lg`, `text-3xl`, etc.
- To change color: Replace `text-blue-600` with other colors like `text-red-600`

### Hero Section
Located below the header, contains main headline and call-to-action buttons:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Texas Pros Garage Doors SA
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    We provide top-notch garage doors services in San Antonio
</p>
```
- Update text between opening and closing tags
- Responsive text sizes use format: `text-[size] md:text-[larger] lg:text-[largest]`
- Maintain spacing classes (`mb-6`, `mb-8`) for consistent layout

### Services Cards
Each service card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <!-- Icon container -->
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Garage Doors</h3>
    <p class="text-gray-600">Premium quality garage doors for your home or business</p>
</div>
```
- Update service titles in `<h3>` tags
- Modify descriptions in `<p>` tags
- Keep consistent spacing and styling classes

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Internal links (same page sections):
   - Keep `#` followed by section ID
   - Example: `href="#services"` links to `<section id="services">`

2. External links:
   - Replace `href="https://texasprosgaragedoors.com/"` with your website URL
   - Always include `https://` for external links

### Call-to-Action Buttons
Located in hero section and CTA section:
```html
<a href="https://texasprosgaragedoors.com/" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">
    Get Started
</a>
```
- Update `href` attribute with your desired URL
- Maintain button styling classes for consistent appearance

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html in same directory as index.html
2. Update links in footer:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in IDs
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Maintain responsive classes (e.g., `md:`, `lg:` prefixes)
   - Test on different screen sizes
   - Don't remove `container` and `mx-auto` classes

3. **Styling Inconsistencies**
   - Keep consistent color classes (e.g., `text-blue-600`)
   - Maintain spacing classes (`mb-4`, `py-24`, etc.)
   - Don't remove transition classes for hover effects

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)