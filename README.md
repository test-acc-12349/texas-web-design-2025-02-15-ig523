# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make common updates safely.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

```html
<!-- Logo Text -->
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>

<!-- Navigation Menu Items -->
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Additional menu items -->
</div>
```

To modify:
1. Change logo text by replacing "TWD"
2. Update menu items by editing text between `<a>` tags
3. Maintain the existing classes to preserve styling

### Hero Section
The main banner section contains your primary headline:

```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-4">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-white/90 mb-8">Best Websites In Texas</p>
```

Styling tips:
- `text-4xl`: Controls text size on mobile
- `md:text-6xl`: Controls text size on desktop
- `mb-4`: Adds margin bottom spacing
- Don't remove `data-aos` attributes as they control animations

### Features and Benefits Sections
To update feature cards:

```html
<div class="bg-white p-8 rounded-2xl shadow-lg">
    <h3 class="text-xl font-bold mb-4">Low Cost</h3>
    <p class="text-gray-600">Affordable web solutions...</p>
</div>
```

Important classes:
- `p-8`: Adds padding
- `rounded-2xl`: Creates rounded corners
- `shadow-lg`: Adds shadow effect
- `text-gray-600`: Sets text color

## Managing Links

### Navigation Links
Current navigation links include:
- Features (`#features`)
- Benefits (`#benefits`)
- FAQ (`#faq`)
- Contact (`mailto:admin@twd.com`)

To update:
1. Locate the header `<nav>` section
2. Find `<a>` tags within the navigation
3. Update `href` attributes:
   ```html
   <!-- Example: Updating email -->
   <a href="mailto:your.new.email@domain.com">Contact</a>
   
   <!-- Example: External link -->
   <a href="https://your-website.com">Get Started</a>
   ```

### Call-to-Action Buttons
Update CTA button links:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-white text-blue-600 rounded-full">
    Start Your Project
</a>
```

Replace `https://twd.com` with your desired URL.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add new links:

```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
    <div>
        <h3 class="text-xl font-bold mb-4">Links</h3>
        <ul class="space-y-2">
            <!-- Add these new items -->
            <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
            <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Step 2: Create Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Add your policy content in the main section

## Troubleshooting

Common issues and solutions:

1. **Broken Links**
   - Check for typos in `href` attributes
   - Ensure file names match exactly
   - Verify file locations in your directory

2. **Styling Issues**
   - Don't remove `class` attributes
   - Keep responsive classes (those starting with `md:`)
   - Maintain the `container mx-auto px-6` pattern for sections

3. **Animation Problems**
   - Verify AOS script is loaded
   - Check `data-aos` attributes remain intact
   - Ensure proper class names for transitions

4. **Mobile Display Issues**
   - Keep the `hidden md:flex` classes in navigation
   - Maintain responsive text classes (e.g., `text-4xl md:text-6xl`)
   - Test all changes on mobile devices

Remember to:
- Back up files before making changes
- Test all links after updates
- Verify mobile responsiveness
- Keep the original class structure intact
- Maintain consistent spacing and padding

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [AOS Animation Library](https://michalsnik.github.io/aos/)