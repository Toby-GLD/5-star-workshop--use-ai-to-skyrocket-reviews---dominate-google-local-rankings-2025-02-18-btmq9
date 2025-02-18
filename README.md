# RocketReviews.ai Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the RocketReviews.ai landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Located at the top of the page -->
<div class="text-2xl font-bold">
    RocketReviews.ai  <!-- Company name -->
</div>
```
To change the company name, simply modify the text between these div tags.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    5-Star Workshop: Use AI to Skyrocket Reviews & Dominate Google Local Rankings
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    How to Get More Reviews & Rank Higher on Google Using AI
</p>
```
Update the main headline and subheading by changing the text within these elements.

### Tailwind CSS Class Modifications

#### Understanding Responsive Classes
In this landing page, responsive classes follow this pattern:
- Default (mobile): `text-4xl`
- Medium screens (md): `md:text-5xl`
- Large screens (lg): `lg:text-6xl`

Example:
```html
<!-- Original -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">

<!-- To make text smaller -->
<h1 class="text-3xl md:text-4xl lg:text-5xl">
```

#### Common Tailwind Classes Used
- Text colors: `text-gray-600`, `text-white`
- Background colors: `bg-white`, `bg-gray-50`
- Padding: `px-6` (horizontal), `py-4` (vertical)
- Margin: `mb-8` (margin-bottom), `mt-12` (margin-top)
- Hover effects: `hover:shadow-lg`, `hover:scale-105`

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

To update these:
1. Locate the `href` attribute
2. Replace the `#section-name` with your desired link
3. For external links, use complete URLs: `href="https://example.com"`

### Button Links
Workshop registration buttons need proper links:
```html
<!-- Hero section button -->
<button class="bg-gradient-to-r from-blue-600 to-indigo-600">
    Reserve Your Spot Now
</button>
```

To make buttons clickable:
1. Wrap the button in an anchor tag:
```html
<a href="https://your-registration-page.com">
    <button class="bg-gradient-to-r from-blue-600 to-indigo-600">
        Reserve Your Spot Now
    </button>
</a>
```

## 3. Linking Privacy and Terms Pages

### Footer Link Updates
Locate the footer links section:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To add proper policy links:
1. Create your privacy.html and terms.html pages
2. Update the href attributes:
```html
<ul class="space-y-2">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Social Media Links
Update social media links in the footer:
```html
<div class="flex space-x-4">
    <a href="https://twitter.com/yourusername" class="hover:text-white">
        <!-- Twitter icon -->
    </a>
    <a href="https://linkedin.com/company/yourcompany" class="hover:text-white">
        <!-- LinkedIn icon -->
    </a>
</div>
```

## Troubleshooting Tips

1. **Broken Layouts**
   - Check for missing closing tags
   - Verify Tailwind classes are spelled correctly
   - Ensure responsive classes follow the correct order (default → md → lg)

2. **Link Issues**
   - Test all links after updating
   - Use relative paths for internal pages (`privacy.html`)
   - Use full URLs for external links (`https://example.com`)

3. **Style Problems**
   - Keep the existing class structure for consistency
   - Test on different screen sizes using browser dev tools
   - Don't remove `transition` classes when updating hover effects

## Need Help?

If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify Tailwind CSS is loading properly
3. Ensure all HTML tags are properly closed
4. Compare your changes against the original code
5. Test responsiveness at different screen sizes

Remember to always backup your code before making significant changes!