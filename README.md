# Amber Perez Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Amber Perez landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and brand name:

```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-500 bg-clip-text text-transparent">
    Amber Perez
</a>
```

To update the brand name:
1. Locate this section at the top of the page
2. Replace "Amber Perez" with your desired text
3. The gradient effect is created by these Tailwind classes:
   - `bg-gradient-to-r`: Creates a right-moving gradient
   - `from-purple-600 to-pink-500`: Sets gradient colors
   - `text-transparent bg-clip-text`: Makes text show the gradient

### Hero Section
The main welcome section includes:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-6 bg-gradient-to-r from-purple-600 to-pink-500 bg-clip-text text-transparent">
    Welcome To Amber Perez's Website
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Experience the future of pop music</p>
```

To modify:
1. Change the h1 text to update the main headline
2. Modify the paragraph text for the subtitle
3. The responsive text sizing uses:
   - `text-5xl`: Base size for mobile
   - `md:text-6xl`: Medium screens
   - `lg:text-7xl`: Large screens

### Music Section Cards
Each card follows this structure:

```html
<div class="bg-white rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300 overflow-hidden">
    <div class="aspect-w-16 aspect-h-9 bg-gradient-to-br from-purple-200 to-pink-100"></div>
    <div class="p-6">
        <h3 class="text-xl font-semibold mb-3">Latest Singles</h3>
        <p class="text-gray-600 mb-4">Stream Amber's newest hits and chart-topping songs</p>
        <a href="#" class="text-purple-600 font-semibold hover:text-purple-700">Listen Now →</a>
    </div>
</div>
```

To update cards:
1. Locate each card in the "Hot New Tracks" section
2. Change the h3 title text
3. Update the description paragraph
4. Modify the link text and href attribute
5. Key styling classes:
   - `rounded-2xl`: Rounds corners
   - `shadow-lg`: Adds shadow
   - `hover:shadow-xl`: Enlarges shadow on hover
   - `transition-shadow`: Smooths shadow transition

## Managing Links

### Navigation Menu Links
The main navigation contains these links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#music" class="text-gray-600 hover:text-purple-600 transition-colors duration-300">Music</a>
    <a href="#about" class="text-gray-600 hover:text-purple-600 transition-colors duration-300">About</a>
    <a href="#contact" class="text-gray-600 hover:text-purple-600 transition-colors duration-300">Contact</a>
</div>
```

To update navigation:
1. Find the `href` attributes
2. For internal links (same page sections):
   - Use `#section-id` format
   - Ensure section IDs match (e.g., `id="music"`)
3. For external links:
   - Replace with full URLs (e.g., `href="https://example.com"`)

### Footer Links
Current footer links need proper URLs:

```html
<ul class="space-y-4">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Music</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">About</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Contact</a></li>
</ul>
```

To update footer links:
1. Replace `#` with proper URLs or section IDs
2. Ensure consistency with navigation links
3. Update social media links in the Connect section

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

```html
<!-- Add this to the Quick Links section -->
<ul class="space-y-4">
    <!-- Existing links -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

Steps to implement:
1. Create privacy.html and terms.html files
2. Add the links to the footer's Quick Links section
3. Maintain consistent styling with existing footer links
4. Ensure files are in the same directory as index.html

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Verify no spaces in IDs
   - IDs should be unique

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify media query classes (md:, lg:) are correct
   - Test all screen sizes

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     - `bg-gradient-to-r`
     - `text-transparent`
     - `bg-clip-text`

4. **Social Media Icons Not Loading**
   - Verify SVG paths are complete
   - Check for proper viewBox attributes
   - Ensure proper class names for sizing

Remember to test all changes across different browsers and screen sizes before deploying to production.