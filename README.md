# Photography Is Us - Landing Page Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing the Photography Is Us landing page. This guide is designed for developers of all skill levels, with detailed instructions for the most common customization tasks.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Managing Links](#fixing-and-managing-links)
5. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
6. [Common Customization Tasks](#common-customization-tasks)
7. [Troubleshooting](#troubleshooting)
8. [Best Practices](#best-practices)

---

## Getting Started

### Prerequisites

- A text editor (VS Code, Sublime Text, or Notepad++)
- Basic understanding of HTML tags
- A web browser for testing changes
- FTP access or a way to upload files to your web server

### File Structure

Your project should have the following structure:

```
project-folder/
├── index.html          (Main landing page)
├── privacy.html        (Privacy policy page - to be created)
├── terms.html          (Terms of service page - to be created)
└── assets/
    └── images/         (Optional: for local images)
```

### How to Open and Edit the File

1. **Locate the file**: Find `index.html` on your computer
2. **Open with a text editor**: Right-click the file → "Open with" → Select your text editor
3. **Make changes**: Find the section you want to modify using this guide
4. **Save**: Press `Ctrl+S` (Windows) or `Cmd+S` (Mac)
5. **View in browser**: Open the file in your web browser to see the changes

---

## Updating Text Content

This section shows you exactly where to find and change the text on your landing page. Each section is identified with line numbers and context.

### Header/Navigation Section

**Location**: Lines 67-93 (Desktop Navigation)

The header contains your site name and navigation menu. Here's what each part does:

#### Site Name/Logo

**Current code:**
```html
<h1 class="text-2xl font-bold text-gray-900">
    <i class="fas fa-camera mr-2 text-gray-800"></i>Photography Is Us
</h1>
```

**To change the site name:**
1. Find the text `Photography Is Us` (around line 71)
2. Replace it with your company name
3. Example: `<i class="fas fa-camera mr-2 text-gray-800"></i>My Photo Studio`

**To change the logo icon:**
- Visit [Font Awesome Icons](https://fontawesome.com/icons) (free icons)
- Find an icon you like (e.g., `fa-image`, `fa-lens`)
- Replace `fa-camera` with your chosen icon
- Example: `<i class="fas fa-image mr-2 text-gray-800"></i>`

#### Navigation Menu Items

**Current code (Desktop - Line 76):**
```html
<nav class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">Contact</a>
</nav>
```

**To add or change menu items:**
1. Replace the menu text (e.g., "Features" → "Our Products")
2. Change the `href` to match your section ID (more on this in the Links section)
3. Example:
```html
<a href="#products" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">Our Products</a>
```

**Important**: The text between the `>` and `</a>` tags is what users see. The `href` tells the browser where to go when clicked.

#### Mobile Navigation Menu

**Current code (Lines 111-125):**
```html
<nav id="mobile-menu" class="mobile-menu-closed md:hidden overflow-hidden smooth-transition">
    <div class="px-2 pt-2 pb-3 space-y-1">
        <a href="#features" class="block px-3 py-2 rounded-md text-gray-700 hover:bg-gray-100 font-medium">Features</a>
        <a href="#benefits" class="block px-3 py-2 rounded-md text-gray-700 hover:bg-gray-100 font-medium">Benefits</a>
        <a href="#faq" class="block px-3 py-2 rounded-md text-gray-700 hover:bg-gray-100 font-medium">FAQ</a>
        <a href="#contact" class="block px-3 py-2 rounded-md text-gray-700 hover:bg-gray-100 font-medium">Contact</a>
        <a href="https://led.com" target="_blank" rel="noopener noreferrer" class="block px-3 py-2 rounded-md bg-gray-900 text-white font-semibold text-center mt-2">Shop Now</a>
    </div>
</nav>
```

**Important**: Update the mobile menu with the same changes you made to the desktop menu. This ensures consistency across all devices.

---

### Announcement Bar

**Location**: Lines 129-136

This is the dark bar at the very top with shipping information.

**Current code:**
```html
<div class="announcement-bar">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <p class="text-center text-sm font-medium">
            <i class="fas fa-truck mr-2"></i>
            Fast Worldwide Shipping (5 days delivery) | Free Delivery on Orders Over $100
        </p>
    </div>
</div>
```

**To change the announcement text:**
1. Find the text: `Fast Worldwide Shipping (5 days delivery) | Free Delivery on Orders Over $100`
2. Replace with your message
3. Example: `Free Shipping on All Orders | Limited Time Offer`

**To change the icon:**
- Replace `fa-truck` with another icon from Font Awesome
- Examples: `fa-star`, `fa-gift`, `fa-bell`

---

### Hero Section

**Location**: Lines 138-180

This is the large banner section with the background image and main call-to-action.

#### Main Headline

**Current code (Line 152):**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Photography Is Us
</h1>
```

**To change the headline:**
1. Replace `Photography Is Us` with your headline
2. Example: `Professional Photography Equipment`

**Understanding the text size classes:**
- `text-4xl` = size on mobile phones
- `md:text-5xl` = size on tablets
- `lg:text-6xl` = size on desktop

#### Subheading

**Current code (Line 156):**
```html
<p class="text-xl md:text-2xl lg:text-3xl text-gray-100 mb-8 font-light leading-relaxed">
    Best Photography Kit
</p>
```

**To change:**
1. Replace `Best Photography Kit` with your subheading
2. Example: `Professional Grade Equipment for Every Photographer`

#### Hero Description

**Current code (Lines 159-161):**
```html
<p class="text-lg md:text-xl text-gray-200 mb-12 max-w-2xl mx-auto leading-relaxed">
    Professional photography equipment for every level. From LED lighting to tripods and pro gear.
</p>
```

**To change:**
1. Replace the descriptive text
2. Keep it concise (2-3 sentences)
3. Example: `Discover premium photography equipment trusted by professionals worldwide. Fast shipping, lifetime support, and satisfaction guaranteed.`

#### Hero Button Text

**Current code (Lines 164-171):**
```html
<a href="https://led.com" target="_blank" rel="noopener noreferrer"
   class="inline-block bg-white text-gray-900 px-8 md:px-10 py-3 md:py-4 rounded-lg font-bold text-lg smooth-transition btn-hover hover:bg-gray-100 shadow-lg"
   aria-label="Shop the best photography kit">
    Explore Collection
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**To change button text:**
1. Replace `Explore Collection` with your button text
2. Example: `Shop Now` or `Get Started`

**To change button link:**
1. Replace `https://led.com` with your target URL
2. This is covered in detail in the [Fixing and Managing Links](#fixing-and-managing-links) section

---

### Features Section

**Location**: Lines 182-245

This section showcases three key features with icons and descriptions.

#### Section Title and Description

**Current code (Lines 185-192):**
```html
<div class="text-center mb-12 md:mb-16">
    <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
        Our Premium Features
    </h2>
    <p class="text-lg text-gray-600 max-w-2xl mx-auto leading-relaxed">
        Discover what makes our photography kit the choice of professionals
    </p>
</div>
```

**To change:**
1. Replace `Our Premium Features` with your section title
2. Replace the description text below it
3. Example title: `Why Choose Our Equipment`
4. Example description: `Industry-leading technology combined with affordable pricing`

#### Individual Feature Cards

Each feature has three parts: Icon, Title, and Description.

**Feature 1 - LED Lighting (Lines 198-220):**

```html
<div class="card-hover p-8 md:p-10 bg-white rounded-xl border border-gray-200 smooth-transition">
    <div class="mb-6">
        <div class="inline-flex items-center justify-center w-16 h-16 bg-gray-100 rounded-lg">
            <i class="fas fa-lightbulb feature-icon text-gray-900"></i>
        </div>
    </div>
    <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-4">LED Lighting</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Professional-grade LED lighting systems for perfect illumination. Adjustable color temperature and intensity for any shooting condition.
    </p>
    <ul class="space-y-2 text-gray-600">
        <li class="flex items-center"><i class="fas fa-check text-gray-900 mr-3"></i>5000K-6500K color temperature</li>
        <li class="flex items-center"><i class="fas fa-check text-gray-900 mr-3"></i>Dimmable controls</li>
        <li class="flex items-center"><i class="fas fa-check text-gray-900 mr-3"></i>Low heat emission</li>
    </ul>
</div>
```

**To customize Feature 1:**

1. **Change the icon**: Replace `fa-lightbulb` with another Font Awesome icon
   - Example: `fa-sun` for lighting, `fa-star` for premium

2. **Change the title**: Replace `LED Lighting`
   - Example: `Professional Lighting Systems`

3. **Change the description**: Replace the main paragraph text
   - Keep it 1-2 sentences

4. **Change the bullet points**: Replace the list items
   - Example: `<li class="flex items-center"><i class="fas fa-check text-gray-900 mr-3"></i>Your feature here</li>`

**Feature 2 - Premium Tripods (Lines 222-244):**

Follow the same process as Feature 1. The structure is identical.

**Feature 3 - Pro Equipment (Lines 246-268):**

Follow the same process as Feature 1. The structure is identical.

**Quick Reference - Icon Examples:**
- Lighting: `fa-lightbulb`, `fa-sun`, `fa-bolt`
- Support: `fa-headset`, `fa-phone`, `fa-envelope`
- Quality: `fa-star`, `fa-medal`, `fa-award`
- Speed: `fa-rocket`, `fa-bolt`, `fa-gauge`
- Find more at [Font Awesome Icons](https://fontawesome.com/icons)

---

### Benefits Section

**Location**: Lines 270-430

This section has three large benefit cards with images and detailed descriptions.

#### Section Title

**Current code (Lines 273-280):**
```html
<div class="text-center mb-12 md:mb-16">
    <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
        Why Choose Us
    </h2>
    <p class="text-lg text-gray-600 max-w-2xl mx-auto leading-relaxed">
        Experience the difference with our commitment to quality and service
    </p>
</div>
```

**To change:**
1. Replace `Why Choose Us` with your title
2. Replace the description paragraph

#### Benefit 1 - Free Delivery (Lines 283-320)

**Current code:**
```html
<h3 class="text-3xl md:text-4xl font-bold text-gray-900 mb-6">Free Delivery</h3>
<p class="text-lg text-gray-600 mb-6 leading-relaxed">
    Enjoy complimentary shipping on all orders. We believe quality photography equipment should be accessible to everyone, which is why we offer free delivery to your doorstep.
</p>
<ul class="space-y-4 mb-8">
    <li class="flex items-start">
        <i class="fas fa-check text-gray-900 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-600">No minimum order requirement</span>
    </li>
    <li class="flex items-start">
        <i class="fas fa-check text-gray-900 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-600">Worldwide delivery available</span>
    </li>
    <li class="flex items-start">
        <i class="fas fa-check text-gray-900 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-600">Secure packaging guaranteed</span>
    </li>
</ul>
```

**To change the title:**
1. Replace `Free Delivery` with your benefit title
2. Example: `Free Shipping Worldwide`

**To change the description:**
1. Replace the paragraph text
2. Keep it 2-3 sentences explaining the benefit

**To change the bullet points:**
1. Each bullet point is a `<li>` element
2. Replace the text inside `<span class="text-gray-600">...</span>`
3. To add more bullets, copy an entire `<li>` block and paste it below
4. To remove bullets, delete the entire `<li>` block

**To change the button:**
1. Find the "Learn More" button link (around line 318)
2. Update the `href="https://led.com"` to your target URL
3. Change the button text if desired

#### Benefit 2 - Fast Shipping (Lines 322-360)

Follow the same process as Benefit 1. The structure is identical.

#### Benefit 3 - High Quality Products (Lines 362-400)

Follow the same process as Benefit 1. The structure is identical.

---

### FAQ Section

**Location**: Lines 465-600

This section contains expandable questions and answers.

#### Section Title

**Current code (Lines 468-475):**
```html
<div class="text-center mb-12 md:mb-16">
    <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
        Frequently Asked Questions
    </h2>
    <p class="text-lg text-gray-600 leading-relaxed">
        Find answers to common questions about our products and services
    </p>
</div>
```

**To change:**
1. Replace `Frequently Asked Questions` with your title
2. Replace the description

#### Individual FAQ Items

**Current code for FAQ Item 1 (Lines 481-495):**

```html
<div class="accordion-item">
    <button class="accordion-header w-full px-6 md:px-8 py-5 md:py-6 flex items-center justify-between hover:bg-gray-50 smooth-transition"
            aria-expanded="false"
            aria-controls="faq-1">
        <span class="text-lg font-semibold text-gray-900 text-left">What is included in the Photography Kit?</span>
        <i class="fas fa-chevron-down accordion-icon text-gray-600"></i>
    </button>
    <div id="faq-1" class="accordion-content">
        <div class="px-6 md:px-8 py-4 md:py-5 bg-gray-50 text-gray-600 leading-relaxed">
            <p>Our complete Photography Kit includes professional LED lighting systems, premium tripods with ball heads, 5-in-1 reflector kits, diffusers, and various professional accessories. Each item is carefully selected for quality and durability to meet professional standards.</p>
        </div>
    </div>
</div>
```

**To change a FAQ question:**
1. Replace the text in the `<span>` tag (the question)
2. Example: `What payment methods do you accept?`

**To change a FAQ answer:**
1. Replace the text in the `<p>` tag inside the accordion-content
2. Example: `We accept all major credit cards, PayPal, and bank transfers.`

**Important**: Keep the `id="faq-1"`, `aria-controls="faq-1"` values consistent. If you change them, make sure they match.

**To add a new FAQ item:**
1. Copy the entire accordion-item block (lines 481-495)
2. Paste it after the last FAQ item
3. Change `faq-1` to `faq-7` (or next number)
4. Update the question and answer text
5. Example:
```html
<div class="accordion-item">
    <button class="accordion-header w-full px-6 md:px-8 py-5 md:py-6 flex items-center justify-between hover:bg-gray-50 smooth-transition"
            aria-expanded="false"
            aria-controls="faq-7">
        <span class="text-lg font-semibold text-gray-900 text-left">Your new question here?</span>
        <i class="fas fa-chevron-down accordion-icon text-gray-600"></i>
    </button>
    <div id="faq-7" class="accordion-content">
        <div class="px-6 md:px-8 py-4 md:py-5 bg-gray-50 text-gray-600 leading-relaxed">
            <p>Your answer here.</p>
        </div>
    </div>
</div>
```

---

### Testimonials Section

**Location**: Lines 625-720

This section displays customer reviews with star ratings.

#### Section Title

**Current code (Lines 628-635):**
```html
<div class="text-center mb-12 md:mb-16">
    <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
        What Our Customers Say
    </h2>
    <p class="text-lg text-gray-600 max-w-2xl mx-auto leading-relaxed">
        Join thousands of satisfied photographers worldwide
    </p>
</div>
```

**To change:**
1. Replace `What Our Customers Say` with your title
2. Replace the description

#### Individual Testimonials

**Current code for Testimonial 1 (Lines 641-664):**

```html
<div class="testimonial-card card-hover">
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
            <i class="fas fa-star star-rating"></i>
        </div>
    </div>
    <p class="text-gray-700 mb-6 leading-relaxed">
        "The LED lighting system completely transformed my studio setup. The color accuracy is incredible, and the customer service was exceptional. Highly recommended!"
    </p>
    <div class="flex items-center">
        <div class="w-12 h-12 bg-gray-300 rounded-full mr-4"></div>
        <div>
            <p class="font-semibold text-gray-900">Sarah Johnson</p>
            <p class="text-sm text-gray-600">Professional Photographer</p>
        </div>
    </div>
</div>
```

**To change the testimonial text:**
1. Replace the quoted text in the `<p>` tag
2. Example: `"Best purchase I've made for my photography business. Highly recommended!"`

**To change the customer name:**
1. Replace `Sarah Johnson` with the actual customer name
2. Example: `John Smith`

**To change the customer title:**
1. Replace `Professional Photographer` with their title
2. Example: `Wedding Photographer` or `Content Creator`

**To change the star rating:**
1. If you want 4 stars instead of 5, remove one `<i class="fas fa-star star-rating"></i>` line
2. To add half stars, use `<i class="fas fa-star-half-alt star-rating"></i>`

**To add a new testimonial:**
1. Copy the entire testimonial-card block
2. Paste it before the closing `</div>` of the grid
3. Update all the text

---

### Newsletter Section

**Location**: Lines 759-773

This is the email subscription form.

#### Section Title and Description

**Current code (Lines 762-767):**
```html
<h2 class="text-3xl md:text-4xl font-bold text-white mb-4 tracking-tight">
    Stay Updated
</h2>
<p class="text-lg text-gray-300 mb-8 leading-relaxed">
    Subscribe to our newsletter for exclusive deals, photography tips, and new product launches.
</p>
```

**To change:**
1. Replace `Stay Updated` with your title
2. Replace the description text

#### Button Text

**Current code (Line 774):**
```html
<input type="email" placeholder="Enter your email" required class="flex-1 px-6 py-3 rounded-lg text-gray-900 placeholder-gray-600 focus:outline-none focus:ring-2 focus:ring-white" aria-label="Email address">
<button type="submit" class="bg-white text-gray-900 px-8 py-3 rounded-lg font-semibold smooth-transition btn-hover hover:bg-gray-100" aria-label="Subscribe to newsletter">
    Subscribe
</button>
```

**To change placeholder text:**
1. Replace `Enter your email` with your text
2. Example: `Your email address`

**To change button text:**
1. Replace `Subscribe` with your button text
2. Example: `Sign Up` or `Get Updates`

---

### Footer Section

**Location**: Lines 775-850

The footer contains company info, links, and contact details.

#### Company Name and Description

**Current code (Lines 783-790):**
```html
<div>
    <h4 class="text-lg font-bold text-white mb-6">Photography Is Us</h4>
    <p class="text-sm leading-relaxed mb-6">
        Your trusted source for professional photography equipment and accessories.
    </p>
```

**To change:**
1. Replace `Photography Is Us` with your company name
2. Replace the description

#### Quick Links Section

**Current code (Lines 799-808):**
```html
<div>
    <h4 class="text-lg font-bold text-white mb-6">Quick Links</h4>
    <ul class="space-y-3">
        <li><a href="#features" class="text-gray-400 hover:text-white smooth-transition">Features</a></li>
        <li><a href="#benefits" class="text-gray-400 hover:text-white smooth-transition">Benefits</a></li>
        <li><a href="#faq" class="text-gray-400 hover:text-white smooth-transition">FAQ</a></li>
        <li><a href="https://led.com" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-white smooth-transition">Shop</a></li>
    </ul>
</div>
```

**To change link text:**
1. Replace the text between `>` and `</a>` tags
2. Example: `<a href="#features" class="...">Our Features</a>`

**To add new links:**
1. Copy a `<li>` line
2. Paste it below
3. Change the `href` and link text
4. Example:
```html
<li><a href="#blog" class="text-gray-400 hover:text-white smooth-transition">Blog</a></li>
```

#### Contact Information

**Current code (Lines 825-836):**
```html
<div>
    <h4 class="text-lg font-bold text-white mb-6">Contact</h4>
    <ul class="space-y-3">
        <li class="flex items-start">
            <i class="fas fa-envelope mr-3 mt-1 flex-shrink-0"></i>
            <a href="mailto:admin@led.com" class="text-gray-400 hover:text-white smooth-transition">admin@led.com</a>
        </li>
        <li class="flex items-start">
            <i class="fas fa-phone mr-3 mt-1 flex-shrink-0"></i>
            <span class="text-gray-400">+1 (800) LED-PHOTO</span>
        </li>
        <li class="flex items-start">
            <i class="fas fa-map-marker-alt mr-3 mt-1 flex-shrink-0"></i>
            <span class="text-gray-400">Worldwide Shipping Available</span>
        </li>
    </ul>
</div>
```

**To change email:**
1. Replace `admin@led.com` in both places:
   - In the `href="mailto:admin@led.com"`
   - In the link text
2. Example:
```html
<a href="mailto:contact@mysite.com" class="text-gray-400 hover:text-white smooth-transition">contact@mysite.com</a>
```

**To change phone number:**
1. Replace `+1 (800) LED-PHOTO`
2. Example: `+1 (555) 123-4567`

**To change address:**
1. Replace `Worldwide Shipping Available`
2. Example: `123 Main St, New York, NY 10001`

#### Copyright and Legal Links

**Current code (Lines 845-855):**
```html
<div class="border-t border-gray-800 pt-8">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <p class="text-sm text-gray-400">
            &copy; 2024 Photography Is Us. All rights reserved.
        </p>
        <div class="flex flex-col sm:flex-row sm:justify-end gap-6">
            <a href="#" class="text-sm text-gray-400 hover:text-white smooth-transition">Privacy Policy</a>
            <a href="#" class="text-sm text-gray-400 hover:text-white smooth-transition">Terms of Service</a>
            <a href="#" class="text-sm text-gray-400 hover:text-white smooth-transition">Cookie Policy</a>
        </div>
    </div>
</div>
```

**To change copyright year:**
1. Replace `2024` with current year
2. Example: `&copy; 2025 Photography Is Us. All rights reserved.`

**To change company name in copyright:**
1. Replace `Photography Is Us` with your company name

**To update policy links:**
1. See the [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages) section for detailed instructions

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a utility-first CSS framework that uses pre-defined classes to style elements. This section explains how to modify colors, spacing, sizes, and responsive behavior.

### Understanding Tailwind Classes

Every Tailwind class does one specific thing. Classes are combined to create the full style. For example:

```html
<h1 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Photography Is Us
</h1>
```

**Breaking it down:**
- `text-3xl` = Font size (3xl on mobile)
- `md:text-4xl` = Font size (4xl on tablets)
- `lg:text-5xl` = Font size (5xl on desktop)
- `font-bold` = Font weight (bold)
- `text-gray-900` = Text color (dark gray)
- `mb-4` = Margin bottom (spacing below element)
- `tracking-tight` = Letter spacing (tight)

### Common Tailwind Classes Used in This Landing Page

#### Text Size Classes

| Class | Size | Usage |
|-------|------|-------|
| `text-sm` | Small | Captions, small text |
| `text-base` | Normal | Body text |
| `text-lg` | Large | Larger body text |
| `text-xl` | Extra Large | Subheadings |
| `text-2xl` | 2XL | Section titles |
| `text-3xl` | 3XL | Main titles |
| `text-4xl` | 4XL | Large titles |
| `text-5xl` | 5XL | Hero titles |
| `text-6xl` | 6XL | Very large titles |

**Example - Making text larger:**
```html
<!-- Before -->
<h2 class="text-2xl md:text-3xl font-bold">Section Title</h2>

<!-- After (larger) -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold">Section Title</h2>
```

#### Text Color Classes

| Class | Color | Usage |
|-------|-------|-------|
| `text-white` | White | Light backgrounds |
| `text-gray-900` | Dark Gray | Main text |
| `text-gray-700` | Medium Gray | Secondary text |
| `text-gray-600` | Light Gray | Tertiary text |
| `text-gray-400` | Lighter Gray | Disabled or footer text |

**Example - Changing text color:**
```html
<!-- Before -->
<p class="text-gray-600">Secondary text</p>

<!-- After (darker) -->
<p class="text-gray-900">Secondary text</p>
```

#### Background Color Classes

| Class | Color | Usage |
|-------|-------|-------|
| `bg-white` | White | Light backgrounds |
| `bg-gray-50` | Very Light Gray | Alternate sections |
| `bg-gray-100` | Light Gray | Cards, boxes |
| `bg-gray-900` | Dark Gray | Dark sections |
| `bg-yellow-400` | Yellow | Accents, stars |

**Example - Changing background color:**
```html
<!-- Before -->
<div class="bg-gray-50 rounded-lg p-8">Content</div>

<!-- After (white background) -->
<div class="bg-white rounded-lg p-8">Content</div>
```

#### Padding and Margin Classes

Padding is space inside an element. Margin is space outside.

| Class | Space | Usage |
|-------|-------|-------|
| `p-4` | Padding all sides | Standard padding |
| `px-6` | Padding left & right | Horizontal padding |
| `py-3` | Padding top & bottom | Vertical padding |
| `m-4` | Margin all sides | Standard margin |
| `mb-6` | Margin bottom | Space below |
| `mt-4` | Margin top | Space above |

**Example - Increasing padding:**
```html
<!-- Before -->
<div class="p-4">Content</div>

<!-- After (more padding) -->
<div class="p-8">Content</div>
```

**Example - Responsive padding:**
```html
<!-- Before -->
<div class="p-4 md:p-8">Content</div>

<!-- After (more padding on desktop) -->
<div class="p-4 md:p-12 lg:p-16">Content</div>
```

#### Border and Rounding Classes

| Class | Effect | Usage |
|-------|--------|-------|
| `rounded-lg` | Slightly rounded corners | Buttons, cards |
| `rounded-xl` | More rounded corners | Cards, containers |
| `border` | Thin border | Cards, separators |
| `border-gray-200` | Border color | Light border |

**Example - Changing corner roundness:**
```html
<!-- Before -->
<div class="rounded-lg border border-gray-200">Card</div>

<!-- After (more rounded) -->
<div class="rounded-xl border border-gray-200">Card</div>
```

#### Display and Layout Classes

| Class | Effect | Usage |
|-------|--------|-------|
| `flex` | Flexbox layout | Align items |
| `grid` | Grid layout | Multi-column layouts |
| `hidden` | Hide element | Hidden by default |
| `md:flex` | Show on tablets+ | Responsive display |
| `md:hidden` | Hide on tablets+ | Mobile-only content |

**Example - Responsive display:**
```html
<!-- This is hidden on mobile, shown on tablets and up -->
<nav class="hidden md:flex items-center space-x-8">
    <!-- Navigation items -->
</nav>
```

#### Responsive Design Prefixes

Tailwind uses prefixes to apply styles at different screen sizes:

| Prefix | Screen Size | Usage |
|--------|-------------|-------|
| None | Mobile (< 768px) | Default |
| `sm:` | Small (≥ 640px) | Large phones |
| `md:` | Medium (≥ 768px) | Tablets |
| `lg:` | Large (≥ 1024px) | Desktop |
| `xl:` | Extra Large (≥ 1280px) | Large desktop |

**Example - Responsive text size:**
```html
<!-- Mobile: text-2xl, Tablet: text-3xl, Desktop: text-4xl -->
<h2 class="text-2xl md:text-3xl lg:text-4xl font-bold">Section Title</h2>
```

### Step-by-Step: Changing Colors

**Task: Change the main heading color from dark gray to a different color**

**Original code (Line 152):**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Photography Is Us
</h1>
```

**Step 1**: Identify the color class
- The color class is `text-white` (white text)

**Step 2**: Find a replacement color
- Available colors: `text-gray-900`, `text-gray-700`, `text-yellow-400`, etc.

**Step 3**: Replace the class
```html
<!-- Before -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">

<!-- After (yellow text) -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-yellow-400 mb-6 leading-tight tracking-tight">
```

**Step 4**: Save and test in browser

### Step-by-Step: Changing Spacing

**Task: Increase padding in feature cards**

**Original code (Line 198):**
```html
<div class="card-hover p-8 md:p-10 bg-white rounded-xl border border-gray-200 smooth-transition">
```

**Step 1**: Identify the padding classes
- `p-8` = padding on mobile
- `md:p-10` = padding on tablets and up

**Step 2**: Choose larger padding
- Larger options: `p-10`, `p-12`, `md:p-12`, `md:p-16`

**Step 3**: Replace the classes
```html
<!-- Before -->
<div class="card-hover p-8 md:p-10 bg-white rounded-xl border border-gray-200 smooth-transition">

<!-- After (more padding) -->
<div class="card-hover p-10 md:p-12 bg-white rounded-xl border border-gray-200 smooth-transition">
```

**Step 4**: Save and test

### Step-by-Step: Changing Button Styles

**Task: Change button background color and add more padding**

**Original code (Line 88):**
```html
<a href="https://led.com" target="_blank" rel="noopener noreferrer"
   class="hidden md:inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold smooth-transition btn-hover hover:bg-gray-800"
   aria-label="Shop now button">
    Shop Now
</a>
```

**Step 1**: Identify the classes to change
- `bg-gray-900` = background color (dark gray)
- `px-6 py-2` = padding
- `hover:bg-gray-800` = hover state color

**Step 2**: Choose new values
- New background: `bg-blue-600`
- New padding: `px-8 py-3`
- New hover: `hover:bg-blue-700`

**Step 3**: Replace the classes
```html
<!-- Before -->
<a href="https://led.com" target="_blank" rel="noopener noreferrer"
   class="hidden md:inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold smooth-transition btn-hover hover:bg-gray-800"
   aria-label="Shop now button">
    Shop Now
</a>

<!-- After -->
<a href="https://led.com" target="_blank" rel="noopener noreferrer"
   class="hidden md:inline-block bg-blue-600 text-white px-8 py-3 rounded-lg font-semibold smooth-transition btn-hover hover:bg-blue-700"
   aria-label="Shop now button">
    Shop Now
</a>
```

### Custom CSS Modifications

For changes beyond Tailwind's built-in classes, modify the `<style>` section (Lines 18-63).

**Example - Changing hover effect speed:**

**Original code (Line 24):**
```css
.smooth-transition {
    transition: all 0.3s ease-in-out;
}
```

**To make transitions faster:**
```css
.smooth-transition {
    transition: all 0.2s ease-in-out;
}
```

**To make transitions slower:**
```css
.smooth-transition {
    transition: all 0.5s ease-in-out;
}
```

**Example - Changing button hover scale:**

**Original code (Lines 26-28):**
```css
.btn-hover:hover {
    transform: scale(1.05);
}
```

**To make buttons grow more on hover:**
```css
.btn-hover:hover {
    transform: scale(1.10);
}
```

---

## Fixing and Managing Links

This section covers all the links in your landing page and how to update them correctly.

### Understanding Links in HTML

A link is created with an anchor tag: `<a href="URL">Link Text</a>`

- `href="URL"` = Where the link goes
- `Link Text` = What users see and click on
- `target="_blank"` = Opens in new tab
- `rel="noopener noreferrer"` = Security feature for external links

### Types of Links on This Page

#### 1. Internal Links (Jump to Sections)

These links jump to different sections on the same page using `#` and section IDs.

**Current internal links:**
- `href="#features"` → Jumps to Features section
- `href="#benefits"` → Jumps to Benefits section
- `href="#faq"` → Jumps to FAQ section
- `href="#contact"` → Jumps to Contact section (Note: This section doesn't exist yet)

**Locations of internal links:**
- Navigation menu (Line 76-79)
- Mobile menu (Line 116-119)
- Footer Quick Links (Line 802-805)

**How internal links work:**

1. A section has an `id` attribute:
```html
<section id="features" class="py-16 md:py-24 bg-white">
```

2. A link points to that `id` with `#`:
```html
<a href="#features">Features</a>
```

3. When clicked, the page scrolls to that section

**To verify internal links are working:**

1. Check that the section ID exists:
   - Search for `id="features"` (should find it)
   - Search for `id="benefits"` (should find it)
   - Search for `id="faq"` (should find it)

2. Check that links point to the correct ID:
   - Search for `href="#features"` (should match the ID)

3. If a link doesn't work:
   - The ID might be misspelled
   - The ID might not exist
   - The link might point to wrong ID

**Example - Fixing a broken internal link:**

**Scenario**: The "FAQ" link in the navigation doesn't work.

**Step 1**: Find the link
```html
<a href="#faq" class="...">FAQ</a>
```

**Step 2**: Check if the section ID exists
- Search the page for `id="faq"`
- If found, the ID exists
- If not found, the ID doesn't exist

**Step 3**: If ID doesn't exist, add it
```html
<!-- Find the FAQ section (around line 465) -->
<section id="faq" class="py-16 md:py-24 bg-gray-50">
    <!-- FAQ content -->
</section>
```

**Step 4**: If ID exists but link is wrong, fix the link
```html
<!-- Before (wrong) -->
<a href="#faqs">FAQ</a>

<!-- After (correct) -->
<a href="#faq">FAQ</a>
```

#### 2. External Links (Links to Other Websites)

These links go to external websites and usually open in a new tab.

**Current external links:**
- `https://led.com` → Main shopping link (appears multiple times)

**Locations of external links:**
- Shop Now button in header (Line 88)
- Mobile menu Shop Now (Line 123)
- Hero section Explore Collection button (Line 167)
- Benefits section Learn More buttons (Lines 318, 356, 394)
- CTA section button (Line 442)
- FAQ support email (Line 600)
- Footer Quick Links (Line 805)
- Footer Contact email (Line 829)

**How to update external links:**

**Step 1**: Identify which link you need to change
- All "Shop Now" buttons → Change to your store URL
- All "Learn More" buttons → Can link to specific product pages
- Email links → Change to your email address

**Step 2**: Replace the URL

**Example - Changing the main shop link:**

**Original code (Line 88):**
```html
<a href="https://led.com" target="_blank" rel="noopener noreferrer"
   class="hidden md:inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold smooth-transition btn-hover hover:bg-gray-800"
   aria-label="Shop now button">
    Shop Now
</a>
```

**To change to your store:**
```html
<a href="https://mystore.com" target="_blank" rel="noopener noreferrer"
   class="hidden md:inline-block bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold smooth-transition btn-hover hover:bg-gray-800"
   aria-label="Shop now button">
    Shop Now
</a>
```

**Important**: Replace ALL instances of `https://led.com` with your actual URL.

**To find all instances:**
1. Press `Ctrl+F` (Windows) or `Cmd+F` (Mac) in your text editor
2. Search for `https://led.com`
3. Replace each one with your store URL
4. Or use "Replace All" feature

### Email Links

Email links use `mailto:` instead of `http://`

**Current email links:**
- `mailto:admin@led.com` (Footer contact)

**How to update email links:**

**Original code (Line 829):**
```html
<a href="mailto:admin@led.com" class="text-gray-400 hover:text-white smooth-transition">admin@led.com</a>
```

**To change email:**
```html
<a href="mailto:contact@mycompany.com" class="text-gray-400 hover:text-white smooth-transition">contact@mycompany.com</a>
```

**Important**: Update both the `href` and the link text to match.

### Social Media Links

**Current code (Lines 793-800):**
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white smooth-transition" aria-label="Facebook">
        <i class="fab fa-facebook text-xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition" aria-label="Instagram">
        <i class="fab fa-instagram text-xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition" aria-label="Twitter">
        <i class="fab fa-twitter text-xl"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-white smooth-transition" aria-label="LinkedIn">
        <i class="fab fa-linkedin text-xl"></i>
    </a>
</div>
```

**To add your social media links:**

**Step 1**: Find your social media URLs
- Facebook: `https://facebook.com/yourpage`
- Instagram: `https://instagram.com/yourprofile`
- Twitter: `https://twitter.com/yourhandle`
- LinkedIn: `https://linkedin.com/company/yourcompany`

**Step 2**: Replace the `#` with your URL

**Example:**
```html
<!-- Before -->
<a href="#" class="text-gray-400 hover:text-white smooth-transition" aria-label="Facebook">
    <i class="fab fa-facebook text-xl"></i>
</a>

<!-- After -->
<a href="https://facebook.com/myphotocompany" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-white smooth-transition" aria-label="Facebook">
    <i class="fab fa-facebook text-xl"></i>
</a>
```

**Note**: Added `target="_blank" rel="noopener noreferrer"` to open in new tab safely.

### Creating a Contact Section

The navigation links to `#contact` but there's no contact section on the page yet. Here's how to add one:

**Step 1**: Add the section before the FAQ section (around line 465)

```html
<!-- Contact Section -->
<section id="contact" class="py-16 md:py-24 bg-white">
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <h2 class="text-3xl md:text-4xl lg:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
            Get In Touch
        </h2>
        <p class="text-lg text-gray-600 mb-12 leading-relaxed">
            Have questions? We'd love to hear from you.
        </p>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-12">
            <!-- Email -->
            <div class="bg-gray-50 rounded-lg p-8">
                <i class="fas fa-envelope text-3xl text-gray-900 mb-4"></i>
                <h3 class="text-xl font-bold text-gray-900 mb-2">Email</h3>
                <a href="mailto:admin@led.com" class="text-gray-600 hover:text-gray-900">admin@led.com</a>
            </div>
            
            <!-- Phone -->
            <div class="bg-gray-50 rounded-lg p-8">
                <i class="fas fa-phone text-3xl text-gray-900 mb-4"></i>
                <h3 class="text-xl font-bold text-gray-900 mb-2">Phone</h3>
                <p class="text-gray-600">+1 (800) LED-PHOTO</p>
            </div>
            
            <!-- Location -->
            <div class="bg-gray-50 rounded-lg p-8">
                <i class="fas fa-map-marker-alt text-3xl text-gray-900 mb-4"></i>
                <h3 class="text-xl font-bold text-gray-900 mb-2">Address</h3>
                <p class="text-gray-600">Worldwide Shipping</p>
            </div>
        </div>
    </div>
</section>
```

**Step 2**: Save and test the link

Now the "Contact" link in the navigation will work!

### Link Checklist

Use this checklist to verify all links are correct:

- [ ] All "Shop Now" buttons link to your store
- [ ] All internal section links work (`#features`, `#benefits`, `#faq`)
- [ ] Contact link works (either to contact section or email)
- [ ] Email links use correct email address
- [ ] Social media links point to your profiles
- [ ] Footer policy links work (see next section)
- [ ] All external links open in new tab (`target="_blank"`)
- [ ] All external links have security attribute (`rel="noopener noreferrer"`)

---

## Adding Privacy and Terms Pages

This section shows you how to create separate pages for Privacy Policy and Terms of Service, and link them from your main page.

### Step 1: Create the Privacy Policy Page

**Step 1a**: Create a new file

1. Open your text editor
2. Click "File" → "New File"
3. Save it as `privacy.html` in the same folder as `index.html`

**Step 1b**: Add the basic HTML structure

Copy and paste this code into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Photography Is Us">
    <meta name="author" content="Photography Is Us">
    <title>Privacy Policy - Photography Is Us</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Poppins', sans-serif;
        }
        
        .smooth-transition {
            transition: all 0.3s ease-in-out;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-1000 bg-white border-b border-gray-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <!-- Logo -->
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl font-bold text-gray-900">
                        <i class="fas fa-camera mr-2 text-gray-800"></i>Photography Is Us
                    </a>
                </div>

                <!-- Navigation -->
                <nav class="hidden md:flex items-center space-x-8">
                    <a href="index.html#features" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">Features</a>
                    <a href="index.html#benefits" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">Benefits</a>
                    <a href="index.html#faq" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">FAQ</a>
                    <a href="index.html" class="bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold smooth-transition hover:bg-gray-800">Home</a>
                </nav>

                <!-- Mobile Menu Button -->
                <button class="md:hidden text-gray-900 focus:outline-none">
                    <i class="fas fa-bars text-2xl"></i>
                </button>
            </div>
        </div>
    </header>

    <!-- Privacy Policy Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            <p class="text-gray-600 mb-8">Last updated: January 2024</p>

            <div class="prose max-w-none text-gray-700 space-y-8">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p class="leading-relaxed">
                        Photography Is Us ("we," "us," "our," or "Company") operates the website. This page informs you of our policies regarding the collection, use, and disclosure of personal data when you use our Service and the choices you have associated with that data.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information Collection and Use</h2>
                    <p class="leading-relaxed mb-4">
                        We collect several different types of information for various purposes to provide and improve our Service to you.
                    </p>
                    <h3 class="text-xl font-semibold text-gray-900 mb-3">Types of Data Collected:</h3>
                    <ul class="list-disc list-inside space-y-2 leading-relaxed">
                        <li><strong>Personal Data:</strong> While using our Service, we may ask you to provide us with certain personally identifiable information that can be used to contact or identify you ("Personal Data"). This may include, but is not limited to:
                            <ul class="list-circle list-inside ml-4 mt-2 space-y-1">
                                <li>Email address</li>
                                <li>First name and last name</li>
                                <li>Phone number</li>
                                <li>Address, State, Province, ZIP/Postal code, City</li>
                                <li>Cookies and Usage Data</li>
                            </ul>
                        </li>
                        <li><strong>Usage Data:</strong> We may also collect information on how the Service is accessed and used ("Usage Data"). This may include information such as your computer's Internet Protocol address, browser type, browser version, the pages you visit, the time and date of your visit, and other diagnostic data.</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Use of Data</h2>
                    <p class="leading-relaxed mb-4">
                        Photography Is Us uses the collected data for various purposes:
                    </p>
                    <ul class="list-disc list-inside space-y-2 leading-relaxed">
                        <li>To provide and maintain our Service</li>
                        <li>To notify you about changes to our Service</li>
                        <li>To allow you to participate in interactive features of our Service when you choose to do so</li>
                        <li>To provide customer support</li>
                        <li>To gather analysis or valuable information so that we can improve our Service</li>
                        <li>To monitor the usage of our Service</li>
                        <li>To detect, prevent and address technical issues</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Security of Data</h2>
                    <p class="leading-relaxed">
                        The security of your data is important to us but remember that no method of transmission over the Internet or method of electronic storage is 100% secure. While we strive to use commercially acceptable means to protect your Personal Data, we cannot guarantee its absolute security.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Contact Us</h2>
                    <p class="leading-relaxed">
                        If you have any questions about this Privacy Policy, please contact us at:
                    </p>
                    <div class="mt-4 p-4 bg-gray-50 rounded-lg">
                        <p class="font-semibold text-gray-900">Photography Is Us</p>
                        <p class="text-gray-600">Email: <a href="mailto:admin@led.com" class="text-blue-600 hover:underline">admin@led.com</a></p>
                        <p class="text-gray-600">Phone: +1 (800) LED-PHOTO</p>
                    </div>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12 md:py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-12">
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Photography Is Us</h4>
                    <p class="text-sm leading-relaxed">Your trusted source for professional photography equipment and accessories.</p>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Quick Links</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html" class="text-gray-400 hover:text-white smooth-transition">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-white smooth-transition">Features</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-white smooth-transition">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Support</h4>
                    <ul class="space-y-3">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-white smooth-transition">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-white smooth-transition">Terms of Service</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Contact</h4>
                    <ul class="space-y-3">
                        <li class="flex items-start">
                            <i class="fas fa-envelope mr-3 mt-1 flex-shrink-0"></i>
                            <a href="mailto:admin@led.com" class="text-gray-400 hover:text-white smooth-transition">admin@led.com</a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="border-t border-gray-800 pt-8">
                <p class="text-sm text-gray-400">
                    &copy; 2024 Photography Is Us. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**Step 2a**: Create a new file

1. Open your text editor
2. Click "File" → "New File"
3. Save it as `terms.html` in the same folder as `index.html`

**Step 2b**: Add the basic HTML structure

Copy and paste this code into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Photography Is Us">
    <meta name="author" content="Photography Is Us">
    <title>Terms of Service - Photography Is Us</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap');
        
        * {
            font-family: 'Poppins', sans-serif;
        }
        
        .smooth-transition {
            transition: all 0.3s ease-in-out;
        }
    </style>
</head>
<body class="bg-white">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-1000 bg-white border-b border-gray-200">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-16">
                <!-- Logo -->
                <div class="flex-shrink-0">
                    <a href="index.html" class="text-2xl font-bold text-gray-900">
                        <i class="fas fa-camera mr-2 text-gray-800"></i>Photography Is Us
                    </a>
                </div>

                <!-- Navigation -->
                <nav class="hidden md:flex items-center space-x-8">
                    <a href="index.html#features" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">Features</a>
                    <a href="index.html#benefits" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">Benefits</a>
                    <a href="index.html#faq" class="text-gray-700 hover:text-gray-900 font-medium smooth-transition">FAQ</a>
                    <a href="index.html" class="bg-gray-900 text-white px-6 py-2 rounded-lg font-semibold smooth-transition hover:bg-gray-800">Home</a>
                </nav