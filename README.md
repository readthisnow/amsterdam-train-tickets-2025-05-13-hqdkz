# Amsterdam Train Tickets Landing Page - Maintenance Guide

This guide will help you maintain and customize the Amsterdam Train Tickets landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text (ATT)**
```html
<div class="text-2xl font-bold text-blue-600">ATT</div>
```
- Replace "ATT" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Don't Miss Out on Exclusive Amsterdam Train Tickets!
</h1>
```
- Replace the text between the `<h1>` tags
- Maintain responsive sizing:
  - `text-4xl`: Mobile screens
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Lightning-Fast Booking</h3>
    <p class="text-gray-600">Don't waste precious minutes!</p>
</div>
```
To add or modify features:
1. Copy the entire `<div>` block
2. Paste within the `grid` container
3. Update heading and paragraph text
4. Maintain the class structure for consistent styling

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure corresponding sections have matching IDs

2. External links:
   - Replace `href="#"` with full URL
   - Example: `href="https://your-website.com/page"`

### Call-to-Action (CTA) Links
Located in hero and CTA sections:
```html
<a href="https://laptoplifepro.com/traintickets" class="inline-block bg-blue-600...">
```
- Replace the URL with your booking page link
- Maintain the classes for styling and hover effects

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Quick Links section in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
</ul>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Design**
   - Check for missing `md:` or `lg:` prefixes in classes
   - Verify the grid structure remains intact
   - Example: `grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3`

2. **Inconsistent Spacing**
   - Use Tailwind's spacing scale:
     - `p-4`: Padding on all sides
     - `my-4`: Margin top and bottom
     - `mx-auto`: Center horizontally

3. **Color Mismatches**
   - Maintain the color scheme:
     - Primary: `blue-600`
     - Text: `gray-900` (dark) or `gray-600` (lighter)
     - Background: `white`, `gray-50`, or gradients

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check class names for typos
- Ensure all sections have proper closing tags
- Verify all required scripts are loaded:
  ```html
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://unpkg.com/aos@next/dist/aos.js"></script>
  ```

Remember to test all changes across different screen sizes using your browser's developer tools before deploying to production.