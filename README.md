# Houston Web Landing Page Maintenance Guide

This README provides guidance for maintaining and customizing the Houston Web landing page. It focuses on three key areas: updating text and Tailwind CSS classes, fixing broken links, and linking privacy and terms pages.

## 1. Updating Text and Tailwind CSS Classes

### Header Section

The header contains the logo and navigation menu. To update the logo text:

1. Locate the following line in the HTML:

```html
<a href="#" class="text-2xl font-bold text-blue-600">Houston Web</a>
```

2. Replace "Houston Web" with your desired text.

To modify navigation menu items:

1. Find the `<div class="hidden md:flex space-x-6">` section.
2. Update the text within each `<a>` tag. For example:

```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Our Services</a>
```

### Hero Section

The hero section is the first thing visitors see. To update its content:

1. Locate the following lines:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6">Best Websites In Houston</h1>
<p class="text-xl md:text-2xl mb-8">Custom Websites For Your Business</p>
```

2. Replace the text within these tags with your desired content.

### Features Section

To update feature items:

1. Find the `<section id="features">` block.
2. Within each `<div class="bg-gray-50 p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">`, update the following:
   - The SVG icon (if desired)
   - The `<h3>` tag content for the feature title
   - The `<p>` tag content for the feature description

### Benefits Section

Similar to the features section, update the content within each benefit card:

1. Locate the `<section id="benefits">` block.
2. For each benefit, update the SVG icon, `<h3>` tag, and `<p>` tag content.

### Tailwind CSS Classes

Tailwind CSS uses utility classes to style elements. Here are some common classes used in this landing page:

- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-{weight}`: Sets font weight (e.g., `font-bold`, `font-semibold`)
- `text-{color}`: Sets text color (e.g., `text-blue-600`, `text-gray-600`)
- `bg-{color}`: Sets background color (e.g., `bg-white`, `bg-blue-600`)
- `p-{size}`: Sets padding (e.g., `p-6`)
- `m-{size}`: Sets margin (e.g., `mb-6` for margin-bottom)
- `rounded-{size}`: Applies border radius (e.g., `rounded-lg`)

To modify these classes:

1. Identify the element you want to change.
2. Locate its class attribute.
3. Add, remove, or modify classes as needed.

For example, to change the button color:

```html
<a href="https://sigmaseo.io" class="bg-white text-blue-600 px-8 py-3 rounded-full font-semibold hover:bg-blue-100 transition duration-300 transform hover:scale-105">Get Started</a>
```

Change `bg-white` to `bg-yellow-400` for a yellow background.

Troubleshooting Tip: If your changes don't appear, make sure you're editing the correct class and that your browser cache is cleared.

## 2. Fixing Broken Links

### Navigation Menu Links

The navigation menu contains internal links to page sections. To update these:

1. Locate the `<nav>` section in the header.
2. For each `<a>` tag, ensure the `href` attribute matches the corresponding section `id`. For example:

```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
```

should link to:

```html
<section id="features" class="py-24 bg-white">
```

### Call-to-Action Buttons

There are two CTA buttons linking to "https://sigmaseo.io". To update these:

1. Find the following lines:

```html
<a href="https://sigmaseo.io" class="bg-white text-blue-600 px-8 py-3 rounded-full font-semibold hover:bg-blue-100 transition duration-300 transform hover:scale-105">Get Started</a>
```

and

```html
<a href="https://sigmaseo.io" class="bg-white text-blue-600 px-8 py-3 rounded-full font-semibold hover:bg-blue-100 transition duration-300 transform hover:scale-105">Create Your Website</a>
```

2. Replace "https://sigmaseo.io" with your desired URL.

### Footer Links

The footer contains quick links. To update these:

1. Locate the `<footer>` section at the bottom of the page.
2. Find the "Quick Links" unordered list.
3. Update the `href` attributes of each `<a>` tag. For example:

```html
<li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Home</a></li>
```

Change the `#` to your home page URL or remove it to link to the top of the current page.

Troubleshooting Tip: Use your browser's developer tools to check if links are working correctly. Right-click on a link and select "Inspect" to view its HTML.

## 3. Linking Privacy and Terms Pages

To add links to privacy and terms pages:

1. Locate the footer section at the bottom of the HTML file.
2. Find the "Quick Links" unordered list.
3. Add new list items for Privacy Policy and Terms of Service. Here's an example:

```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Home</a></li>
    <li><a href="#features" class="text-gray-400 hover:text-white transition duration-300">Features</a></li>
    <li><a href="#benefits" class="text-gray-400 hover:text-white transition duration-300">Benefits</a></li>
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
</ul>
```

Make sure to create the `privacy.html` and `terms.html` files in the same directory as your `index.html` file.

Alternatively, you can add these links to the main navigation:

1. Locate the `<div class="hidden md:flex space-x-6">` in the header.
2. Add new `<a>` tags for the privacy and terms pages:

```html
<div class="hidden md:flex space-x-6">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition duration-300">Contact</a>
    <a href="privacy.html" class="text-gray-600 hover:text-blue-600 transition duration-300">Privacy</a>
    <a href="terms.html" class="text-gray-600 hover:text-blue-600 transition duration-300">Terms</a>
</div>
```

Troubleshooting Tip: After adding the links, click on them to ensure they lead to the correct pages. If they don't work, double-check the file names and locations.

Remember to maintain consistent styling with existing links by using the same CSS classes.

By following these instructions, you should be able to effectively maintain and customize your Houston Web landing page. If you encounter any issues or need further assistance, don't hesitate to seek help from a web development professional.