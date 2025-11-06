# Las Vegas Solar Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your Las Vegas Solar landing page. This document provides step-by-step instructions for users of all technical levels.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Creating and Linking Policy Pages](#creating-and-linking-policy-pages)
7. [Customizing Colors and Branding](#customizing-colors-and-branding)
8. [Mobile Responsiveness](#mobile-responsiveness)
9. [Troubleshooting Common Issues](#troubleshooting-common-issues)

---

## Getting Started

### What You'll Need

- A text editor (we recommend: VS Code, Sublime Text, or even Notepad++)
- Basic understanding of HTML and CSS
- Your `index.html` file open in the text editor
- A web browser to preview changes

### How to Edit This File

1. **Open the file**: Right-click `index.html` → "Open with" → Select your text editor
2. **Make changes**: Follow the instructions in this guide
3. **Save your work**: Press `Ctrl+S` (Windows) or `Cmd+S` (Mac)
4. **Preview changes**: Open `index.html` in your web browser, then refresh the page (`Ctrl+R` or `Cmd+R`)

### File Organization

For best results, organize your project folder like this:

```
your-project-folder/
├── index.html           (Main landing page)
├── privacy.html         (Privacy policy - you'll create this)
├── terms.html           (Terms of service - you'll create this)
├── blog.html            (Blog page - you'll create this)
└── assets/
    └── images/          (Store images here)
```

---

## Understanding the Page Structure

Your landing page is divided into major sections. Here's what each section contains:

### Header Navigation (Lines 109-135)
The sticky navigation bar at the top of the page containing:
- Logo with sun icon
- Navigation menu links
- "Get Started" button
- Mobile hamburger menu

### Hero Section (Lines 137-203)
The large banner at the top featuring:
- Main headline and subheading
- Call-to-action buttons
- Background gradient animations
- Three statistics boxes

### Features Section (Lines 205-284)
Three feature cards describing:
1. Personalized System Design
2. Flexible Financing Options
3. Comprehensive Warranty Coverage

### Benefits Section (Lines 286-387)
Four benefit cards explaining:
1. Guaranteed Performance
2. Protection Against Rising Rates
3. Greener Future Contribution
4. Increased Home Value

### About Us Section (Lines 389-430)
Company information and statistics

### Testimonials Section (Lines 432-516)
Four customer testimonial cards with star ratings

### FAQ Section (Lines 518-648)
Five expandable FAQ questions and answers

### Call-to-Action Section (Lines 650-677)
Full-width banner with background image and CTA button

### Footer (Lines 679-755)
Contact information, quick links, and copyright notice

---

## Updating Text Content

### Hero Section Headline

**Location**: Lines 155-160

**Current Code**:
```html
<h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold mb-6 leading-tight tracking-tight">
    <span class="bg-gradient-to-r from-purple-400 via-blue-400 to-purple-400 bg-clip-text text-transparent">Las Vegas Solar</span>
    <span class="block text-white mt-3">Your Energy Freedom Starts Here</span>
</h1>
```

**How to Change It**:
1. Find the line with `"Your Energy Freedom Starts Here"`
2. Replace the text between the `>` and `</span>` with your new headline
3. Keep the HTML tags (`<span>`, `</span>`) exactly as they are
4. The first line (company name) and second line (tagline) can be edited separately

**Example**:
```html
<h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold mb-6 leading-tight tracking-tight">
    <span class="bg-gradient-to-r from-purple-400 via-blue-400 to-purple-400 bg-clip-text text-transparent">Las Vegas Solar</span>
    <span class="block text-white mt-3">Save Money, Save the Planet</span>
</h1>
```

### Hero Section Subheading

**Location**: Lines 162-166

**Current Code**:
```html
<p class="text-lg sm:text-xl md:text-2xl text-gray-300 mb-8 leading-relaxed max-w-3xl mx-auto">
    Unlock financial independence and sustainable living with customized solar solutions designed specifically for Las Vegas homes. Transform your energy costs into energy savings while contributing to a greener future.
</p>
```

**How to Change It**:
1. Find the paragraph starting with "Unlock financial independence"
2. Replace the text between `>` and `</p>` with your new description
3. Keep the opening `<p>` tag and closing `</p>` tag

**Tips**:
- Keep descriptions clear and concise
- Use persuasive language
- Avoid technical jargon for general audiences

### Feature Card Titles and Descriptions

**Location**: Lines 223-284

Each feature card has a title and description. Here's the structure for the first card:

**Current Code**:
```html
<h3 class="text-2xl font-bold text-white mb-4">Personalized System Design</h3>
<p class="text-gray-400 mb-4 leading-relaxed">
    Our expert engineers conduct comprehensive energy audits...
</p>
```

**How to Change It**:
1. Locate the `<h3>` tag with the feature title
2. Replace the title text (keep the tags)
3. Update the `<p>` tag description below it
4. Modify the bullet points in the `<ul>` list

**Example - Changing Feature 1**:
```html
<h3 class="text-2xl font-bold text-white mb-4">Expert Custom Design</h3>
<p class="text-gray-400 mb-4 leading-relaxed">
    Our certified engineers design systems perfectly matched to your home...
</p>
```

### Testimonial Content

**Location**: Lines 480-515

Each testimonial has a customer name, location, star rating, and quote.

**Current Code for First Testimonial**:
```html
<div class="flex items-center mb-4">
    <div class="w-12 h-12 bg-gradient-to-br from-purple-500 to-blue-500 rounded-full flex items-center justify-center">
        <span class="text-white font-bold">JM</span>
    </div>
    <div class="ml-4">
        <p class="font-bold text-white">James Mitchell</p>
        <p class="text-sm text-gray-400">Las Vegas, NV</p>
    </div>
</div>
```

**How to Change It**:
1. Replace `James Mitchell` with the customer's name
2. Replace `Las Vegas, NV` with their location
3. Update the initials in the circle (e.g., `JM` to `SR`)
4. Modify the testimonial text in the `<p>` tag below

**Example**:
```html
<div class="flex items-center mb-4">
    <div class="w-12 h-12 bg-gradient-to-br from-purple-500 to-blue-500 rounded-full flex items-center justify-center">
        <span class="text-white font-bold">AB</span>
    </div>
    <div class="ml-4">
        <p class="font-bold text-white">Angela Brown</p>
        <p class="text-sm text-gray-400">Henderson, NV</p>
    </div>
</div>
```

### FAQ Questions and Answers

**Location**: Lines 560-648

Each FAQ item contains a question and an answer.

**Current Code Structure**:
```html
<button class="faq-question w-full px-6 py-4 flex items-center justify-between hover:bg-gray-800 transition-colors duration-300">
    <h3 class="text-lg font-semibold text-white text-left">How much can I save with a solar system?</h3>
    <i class="faq-icon fas fa-chevron-down text-purple-400 transition-transform duration-300"></i>
</button>
<div class="faq-answer hidden px-6 py-4 border-t border-gray-700 bg-gray-800 bg-opacity-50">
    <p class="text-gray-300 leading-relaxed mb-4">
        The amount you save depends on several factors...
    </p>
</div>
```

**How to Change It**:
1. Replace the text in the `<h3>` tag with your new question
2. Replace the text in the `<p>` tag with your answer
3. Keep all the class names and HTML structure intact

**Important**: Do NOT remove the `hidden` class from the answer div - this makes it collapse/expand properly.

### Footer Company Description

**Location**: Lines 698-704

**Current Code**:
```html
<p class="text-gray-400 text-sm leading-relaxed">
    Transforming Las Vegas homes with premium solar solutions for energy independence and sustainable living.
</p>
```

**How to Change It**:
```html
<p class="text-gray-400 text-sm leading-relaxed">
    Your new company description goes here. Keep it brief and professional.
</p>
```

### Contact Email

**Location**: Line 737

**Current Code**:
```html
<a href="mailto:x_n2deep_x@yahoo.com" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm flex items-center">
    <i class="fas fa-envelope mr-2"></i>
    x_n2deep_x@yahoo.com
</a>
```

**How to Change It**:
1. Replace `x_n2deep_x@yahoo.com` with your email address (appears twice)
2. Keep the `mailto:` part - it makes the email clickable

**Example**:
```html
<a href="mailto:info@lasvegassolar.com" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm flex items-center">
    <i class="fas fa-envelope mr-2"></i>
    info@lasvegassolar.com
</a>
```

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind Classes

This landing page uses **Tailwind CSS**, a utility-first CSS framework. Instead of writing custom CSS, you add pre-made classes to HTML elements.

**Example**:
```html
<div class="bg-gray-900 text-white p-8 rounded-lg">
    This div has a dark background, white text, padding, and rounded corners
</div>
```

Breaking it down:
- `bg-gray-900` = dark gray background
- `text-white` = white text color
- `p-8` = padding (space inside)
- `rounded-lg` = rounded corners

### Common Tailwind Classes Used in This Page

#### Text Styling

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-white` | White text | `<p class="text-white">` |
| `text-gray-300` | Light gray text | `<p class="text-gray-300">` |
| `text-gray-400` | Medium gray text | `<p class="text-gray-400">` |
| `text-2xl` | Large text size | `<h2 class="text-2xl">` |
| `text-lg` | Medium text size | `<p class="text-lg">` |
| `font-bold` | Bold text | `<h1 class="font-bold">` |
| `font-semibold` | Semi-bold text | `<h3 class="font-semibold">` |

#### Colors

| Class | Color |
|-------|-------|
| `bg-gray-900` | Very dark gray (almost black) |
| `bg-gray-800` | Dark gray |
| `bg-purple-600` | Medium purple |
| `bg-blue-600` | Medium blue |
| `text-purple-400` | Light purple text |
| `text-blue-400` | Light blue text |
| `border-purple-500` | Purple border |

#### Spacing

| Class | What It Does |
|-------|-------------|
| `p-8` | Padding (space inside) = 32px |
| `px-6` | Horizontal padding = 24px |
| `py-4` | Vertical padding = 16px |
| `mb-6` | Margin bottom (space below) = 24px |
| `mt-3` | Margin top (space above) = 12px |
| `ml-4` | Margin left = 16px |

#### Layout

| Class | What It Does |
|-------|-------------|
| `flex` | Makes items line up horizontally |
| `flex-col` | Makes items stack vertically |
| `grid` | Creates a grid layout |
| `grid-cols-1` | 1 column on mobile |
| `md:grid-cols-3` | 3 columns on medium screens and up |
| `gap-8` | Space between grid items = 32px |

#### Responsive Design

Classes change behavior on different screen sizes:

| Prefix | Screen Size |
|--------|------------|
| (none) | Mobile (small screens) |
| `sm:` | 640px and up |
| `md:` | 768px and up |
| `lg:` | 1024px and up |

**Example**:
```html
<h1 class="text-2xl md:text-4xl lg:text-6xl">
    <!-- Text is 2xl on mobile, 4xl on tablets, 6xl on desktops -->
</h1>
```

### How to Change Colors

**Scenario**: You want to change all purple accents to teal.

**Step 1**: Find the color classes
Search for `purple-` in your HTML file. You'll see classes like:
- `from-purple-600` (gradient start)
- `to-purple-500` (gradient end)
- `text-purple-400` (text color)
- `hover:text-purple-400` (hover effect)

**Step 2**: Replace with new colors
Change `purple-600` to `teal-600`, `purple-500` to `teal-500`, etc.

**Before**:
```html
<button class="px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white rounded-lg">
    Start Your Solar Journey
</button>
```

**After**:
```html
<button class="px-8 py-4 bg-gradient-to-r from-teal-600 to-blue-600 text-white rounded-lg">
    Start Your Solar Journey
</button>
```

### How to Change Text Size

**Scenario**: The hero headline is too large on mobile.

**Current Code** (Line 155):
```html
<h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl font-bold mb-6">
```

**What This Means**:
- `text-4xl` = Extra large on mobile
- `sm:text-5xl` = Even larger on small tablets
- `md:text-6xl` = Larger on tablets
- `lg:text-7xl` = Largest on desktops

**To Make It Smaller**:
```html
<h1 class="text-3xl sm:text-4xl md:text-5xl lg:text-6xl font-bold mb-6">
```

### How to Change Spacing (Padding/Margins)

**Scenario**: You want more space inside feature cards.

**Current Code** (Line 223):
```html
<div class="feature-card bg-gray-900 rounded-xl p-8 border border-gray-700 hover:border-purple-500">
```

The `p-8` means 32px of padding on all sides.

**To Increase Padding**:
```html
<div class="feature-card bg-gray-900 rounded-xl p-12 border border-gray-700 hover:border-purple-500">
```

Padding options: `p-4`, `p-6`, `p-8`, `p-10`, `p-12` (smallest to largest)

### How to Change Grid Columns

**Scenario**: You want testimonials to display 2 per row instead of 4.

**Current Code** (Line 473):
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
```

This means:
- 1 column on mobile
- 2 columns on tablets
- 4 columns on desktops

**To Change to 2 Columns on Desktop**:
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-6">
```

### How to Change Border Colors

**Scenario**: You want feature cards to have blue borders instead of gray.

**Current Code** (Line 223):
```html
<div class="feature-card bg-gray-900 rounded-xl p-8 border border-gray-700 hover:border-purple-500">
```

**To Change**:
```html
<div class="feature-card bg-gray-900 rounded-xl p-8 border border-blue-700 hover:border-blue-500">
```

### Tailwind Class Reference for This Page

**Button Styling**:
```html
<!-- Primary button (purple-to-blue gradient) -->
<a class="px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white rounded-lg font-bold">

<!-- Secondary button (outline style) -->
<a class="px-8 py-4 border-2 border-purple-500 text-purple-400 rounded-lg font-bold">
```

**Card Styling**:
```html
<!-- Feature cards -->
<div class="bg-gray-900 rounded-xl p-8 border border-gray-700 hover:border-purple-500">

<!-- Testimonial cards -->
<div class="bg-gray-800 rounded-xl p-6 border border-gray-700">
```

**Icon Containers**:
```html
<!-- Purple-to-blue gradient circle -->
<div class="w-14 h-14 bg-gradient-to-br from-purple-500 to-blue-500 rounded-lg flex items-center justify-center">
```

---

## Fixing and Managing Links

### Understanding Links in This Page

Your landing page has several types of links:

1. **Navigation menu links** - Jump to page sections
2. **CTA buttons** - External link to conversion page
3. **Footer links** - Internal and external links
4. **Social media links** - Placeholder links

### Navigation Menu Links

**Location**: Lines 122-126 (Desktop) and Lines 130-134 (Mobile)

**Current Code**:
```html
<!-- Desktop Menu -->
<a href="#features" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">Features</a>
<a href="#benefits" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">FAQ</a>
```

**How These Work**:
- `href="#features"` jumps to the section with `id="features"`
- The `#` symbol means "jump to this location on the same page"

**What Each Link Does**:
- `#features` → Jumps to Features Section (Line 205)
- `#benefits` → Jumps to Benefits Section (Line 286)
- `#testimonials` → Jumps to Testimonials Section (Line 432)
- `#faq` → Jumps to FAQ Section (Line 518)

**To Add a New Navigation Link**:

1. First, create a section with an ID:
```html
<section id="services" class="py-24 px-4 sm:px-6 lg:px-8">
    <h2>Our Services</h2>
    <!-- Content here -->
</section>
```

2. Then, add a link in the navigation:
```html
<a href="#services" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">Services</a>
```

3. Add it in BOTH places:
   - Desktop menu (after line 125)
   - Mobile menu (after line 133)

### Call-to-Action Buttons

**Locations**: Multiple places on the page

**Current Code Examples**:
```html
<!-- Line 127 -->
<a href="https://americashomecontractors.com/actnow" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-blue-600 text-white rounded-lg font-semibold btn-primary hover:shadow-lg">Get Started</a>

<!-- Line 169 -->
<a href="https://americashomecontractors.com/actnow" class="px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white rounded-lg font-bold text-lg btn-primary hover:shadow-2xl w-full sm:w-auto">
    Start Your Solar Journey
    <i class="fas fa-arrow-right ml-2"></i>
</a>

<!-- Line 661 -->
<a href="https://americashomecontractors.com/actnow" class="inline-block px-10 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white rounded-lg font-bold text-lg btn-primary hover:shadow-2xl mb-4">
    Get Your Free Solar Quote Today
    <i class="fas fa-arrow-right ml-2"></i>
</a>
```

**How to Update CTA Links**:

1. Find all instances of `https://americashomecontractors.com/actnow`
2. Replace with your desired URL

**Quick Find and Replace Method**:
- Press `Ctrl+H` (Windows) or `Cmd+H` (Mac) in your text editor
- Type in the old URL: `https://americashomecontractors.com/actnow`
- Type in the new URL: `https://yourcompany.com/quote`
- Click "Replace All"

**Important CTA Button Locations**:
- Line 127: Header "Get Started" button
- Line 169: Hero section main CTA
- Line 661: Final CTA section button
- Line 734: Footer "Get Started" link

### Footer Links

**Location**: Lines 707-745

**Quick Links Section** (Line 707-714):
```html
<h4 class="text-white font-bold mb-4">Quick Links</h4>
<ul class="space-y-2">
    <li><a href="#features" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Features</a></li>
    <li><a href="#benefits" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Benefits</a></li>
    <li><a href="#testimonials" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Testimonials</a></li>
    <li><a href="#faq" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">FAQ</a></li>
</ul>
```

These links are the same as navigation links (they jump to sections).

**Resources Section** (Line 716-723):
```html
<h4 class="text-white font-bold mb-4">Resources</h4>
<ul class="space-y-2">
    <li><a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Blog</a></li>
    <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Terms of Service</a></li>
    <li><a href="https://americashomecontractors.com/actnow" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Get Started</a></li>
</ul>
```

**How to Update These**:
- `blog.html` - Link to your blog page
- `privacy.html` - Link to your privacy policy (we'll create this next)
- `terms.html` - Link to your terms of service (we'll create this next)
- The last link is the external CTA link

### Social Media Links

**Location**: Lines 740-750

**Current Code**:
```html
<li class="flex space-x-4 pt-2">
    <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
        <i class="fab fa-facebook text-lg"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
        <i class="fab fa-twitter text-lg"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
        <i class="fab fa-instagram text-lg"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
        <i class="fab fa-linkedin text-lg"></i>
    </a>
</li>
```

**How to Update Social Links**:

Replace `href="#"` with your social media URLs:

```html
<li class="flex space-x-4 pt-2">
    <a href="https://facebook.com/yourpage" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
        <i class="fab fa-facebook text-lg"></i>
    </a>
    <a href="https://twitter.com/yourhandle" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
        <i class="fab fa-twitter text-lg"></i>
    </a>
    <a href="https://instagram.com/yourhandle" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
        <i class="fab fa-instagram text-lg"></i>
    </a>
    <a href="https://linkedin.com/company/yourcompany" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">
        <i class="fab fa-linkedin text-lg"></i>
    </a>
</li>
```

### Footer Bottom Links

**Location**: Lines 752-761

**Current Code**:
```html
<div class="flex space-x-6">
    <a href="privacy.html" class="text-gray-500 hover:text-purple-400 transition-colors duration-300 text-sm">Privacy Policy</a>
    <a href="terms.html" class="text-gray-500 hover:text-purple-400 transition-colors duration-300 text-sm">Terms of Service</a>
    <a href="blog.html" class="text-gray-500 hover:text-purple-400 transition-colors duration-300 text-sm">Blog</a>
</div>
```

These are the same pages referenced in the Resources section. Ensure they match.

### Link Verification Checklist

Print this checklist and verify each link works:

```
Navigation Links (should jump to sections):
☐ Features link works
☐ Benefits link works
☐ Testimonials link works
☐ FAQ link works

CTA Buttons:
☐ Header "Get Started" button
☐ Hero "Start Your Solar Journey" button
☐ Final "Get Your Free Solar Quote" button
☐ Footer "Get Started" link

Footer Links:
☐ Blog link works (or shows 404 if page not created yet)
☐ Privacy Policy link works
☐ Terms of Service link works
☐ Social media links open correctly

External Links:
☐ All external URLs are correct
☐ All external links open in new tab (if desired)
```

---

## Creating and Linking Policy Pages

### Why You Need Policy Pages

- **Privacy Policy**: Explains how you collect and use customer data
- **Terms of Service**: Outlines the rules for using your website
- **Legal requirement**: Many jurisdictions require these pages

### Creating a Privacy Policy Page

**Step 1**: Create a new file called `privacy.html`

In your text editor:
1. File → New File
2. Save as `privacy.html` in the same folder as `index.html`

**Step 2**: Add this template code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Las Vegas Solar">
    <meta name="author" content="Las Vegas Solar">
    <title>Privacy Policy - Las Vegas Solar</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-100">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-500 to-blue-500 rounded-lg flex items-center justify-center">
                    <i class="fas fa-sun text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-blue-400 bg-clip-text text-transparent">Las Vegas Solar</a>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#faq" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">FAQ</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-gray-800 bg-opacity-50">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-5xl font-bold text-white mb-4">Privacy Policy</h1>
            <p class="text-gray-400 mb-12">Last updated: January 2025</p>

            <div class="space-y-8 text-gray-300 leading-relaxed">
                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Introduction</h2>
                    <p>
                        Las Vegas Solar ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Information We Collect</h2>
                    <p>We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                    <ul class="list-disc list-inside mt-4 space-y-2">
                        <li><strong>Personal Data:</strong> Name, email address, phone number, mailing address</li>
                        <li><strong>Device Data:</strong> Browser type, IP address, operating system</li>
                        <li><strong>Usage Data:</strong> Pages visited, time spent on pages, links clicked</li>
                        <li><strong>Energy Data:</strong> Current energy usage, utility bills (if provided for solar analysis)</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Use of Your Information</h2>
                    <p>Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the Site to:</p>
                    <ul class="list-disc list-inside mt-4 space-y-2">
                        <li>Generate a personal solar analysis and quote</li>
                        <li>Email you regarding your inquiry or quote</li>
                        <li>Fulfill and manage your purchase or service</li>
                        <li>Send promotional communications (with your consent)</li>
                        <li>Improve our website and services</li>
                        <li>Respond to your inquiries and customer service requests</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Disclosure of Your Information</h2>
                    <p>
                        We may share your information with third parties in the following situations:
                    </p>
                    <ul class="list-disc list-inside mt-4 space-y-2">
                        <li>With service providers who assist us in operating our website and conducting our business</li>
                        <li>When required by law or to protect our legal rights</li>
                        <li>With your consent for specific purposes</li>
                        <li>Financing partners (if you apply for solar financing)</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Security of Your Information</h2>
                    <p>
                        We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet is 100% secure. While we strive to use commercially acceptable means to protect your personal information, we cannot guarantee its absolute security.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Contact Us</h2>
                    <p>
                        If you have questions about this Privacy Policy, please contact us at:
                    </p>
                    <div class="bg-gray-900 rounded p-4 border border-gray-700 mt-4">
                        <p><strong>Email:</strong> x_n2deep_x@yahoo.com</p>
                        <p><strong>Company:</strong> Las Vegas Solar</p>
                    </div>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 border-t border-gray-800 py-16 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-10 h-10 bg-gradient-to-br from-purple-500 to-blue-500 rounded-lg flex items-center justify-center">
                            <i class="fas fa-sun text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold bg-gradient-to-r from-purple-400 to-blue-400 bg-clip-text text-transparent">Las Vegas Solar</span>
                    </div>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Transforming Las Vegas homes with premium solar solutions for energy independence and sustainable living.
                    </p>
                </div>

                <div>
                    <h4 class="text-white font-bold mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="index.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Features</a></li>
                        <li><a href="index.html#testimonials" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Testimonials</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">FAQ</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-bold mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Terms of Service</a></li>
                        <li><a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Blog</a></li>
                        <li><a href="https://americashomecontractors.com/actnow" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Get Started</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-bold mb-4">Get In Touch</h4>
                    <ul class="space-y-3">
                        <li>
                            <a href="mailto:x_n2deep_x@yahoo.com" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm flex items-center">
                                <i class="fas fa-envelope mr-2"></i>
                                x_n2deep_x@yahoo.com
                            </a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="border-t border-gray-800 pt-8">
                <p class="text-gray-500 text-sm text-center">
                    &copy; 2025 Las Vegas Solar. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Creating a Terms of Service Page

**Step 1**: Create a new file called `terms.html`

**Step 2**: Add this template code:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Las Vegas Solar">
    <meta name="author" content="Las Vegas Solar">
    <title>Terms of Service - Las Vegas Solar</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-100">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-500 to-blue-500 rounded-lg flex items-center justify-center">
                    <i class="fas fa-sun text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-blue-400 bg-clip-text text-transparent">Las Vegas Solar</a>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">Home</a>
                <a href="index.html#features" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#faq" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">FAQ</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 px-4 sm:px-6 lg:px-8 bg-gray-800 bg-opacity-50">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-5xl font-bold text-white mb-4">Terms of Service</h1>
            <p class="text-gray-400 mb-12">Last updated: January 2025</p>

            <div class="space-y-8 text-gray-300 leading-relaxed">
                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Agreement to Terms</h2>
                    <p>
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Use License</h2>
                    <p>
                        Permission is granted to temporarily download one copy of the materials (information or software) on Las Vegas Solar's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside mt-4 space-y-2">
                        <li>Modifying or copying the materials</li>
                        <li>Using the materials for any commercial purpose or for any public display</li>
                        <li>Attempting to decompile or reverse engineer any software contained on the website</li>
                        <li>Transferring the materials to another person or "mirroring" the materials on any other server</li>
                        <li>Removing any copyright or other proprietary notations from the materials</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Disclaimer</h2>
                    <p>
                        The materials on Las Vegas Solar's website are provided on an 'as is' basis. Las Vegas Solar makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Limitations</h2>
                    <p>
                        In no event shall Las Vegas Solar or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Las Vegas Solar's website, even if Las Vegas Solar or an authorized representative has been notified orally or in writing of the possibility of such damage.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on Las Vegas Solar's website could include technical, typographical, or photographic errors. Las Vegas Solar does not warrant that any of the materials on its website are accurate, complete, or current. Las Vegas Solar may make changes to the materials contained on its website at any time without notice.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Links</h2>
                    <p>
                        Las Vegas Solar has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Las Vegas Solar of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">7. Modifications</h2>
                    <p>
                        Las Vegas Solar may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">8. Governing Law</h2>
                    <p>
                        These terms and conditions are governed by and construed in accordance with the laws of Nevada, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">9. Contact Us</h2>
                    <p>
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <div class="bg-gray-900 rounded p-4 border border-gray-700 mt-4">
                        <p><strong>Email:</strong> x_n2deep_x@yahoo.com</p>
                        <p><strong>Company:</strong> Las Vegas Solar</p>
                    </div>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 border-t border-gray-800 py-16 px-4 sm:px-6 lg:px-8">
        <div class="max-w-7xl mx-auto">
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-8 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-4">
                        <div class="w-10 h-10 bg-gradient-to-br from-purple-500 to-blue-500 rounded-lg flex items-center justify-center">
                            <i class="fas fa-sun text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold bg-gradient-to-r from-purple-400 to-blue-400 bg-clip-text text-transparent">Las Vegas Solar</span>
                    </div>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Transforming Las Vegas homes with premium solar solutions for energy independence and sustainable living.
                    </p>
                </div>

                <div>
                    <h4 class="text-white font-bold mb-4">Quick Links</h4>
                    <ul class="space-y-2">
                        <li><a href="index.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Home</a></li>
                        <li><a href="index.html#features" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Features</a></li>
                        <li><a href="index.html#testimonials" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Testimonials</a></li>
                        <li><a href="index.html#faq" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">FAQ</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-bold mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Terms of Service</a></li>
                        <li><a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Blog</a></li>
                        <li><a href="https://americashomecontractors.com/actnow" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Get Started</a></li>
                    </ul>
                </div>

                <div>
                    <h4 class="text-white font-bold mb-4">Get In Touch</h4>
                    <ul class="space-y-3">
                        <li>
                            <a href="mailto:x_n2deep_x@yahoo.com" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm flex items-center">
                                <i class="fas fa-envelope mr-2"></i>
                                x_n2deep_x@yahoo.com
                            </a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="border-t border-gray-800 pt-8">
                <p class="text-gray-500 text-sm text-center">
                    &copy; 2025 Las Vegas Solar. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Verifying Policy Page Links

After creating both files:

1. **Test the links from index.html**:
   - Click the "Privacy Policy" link in the footer
   - Click the "Terms of Service" link in the footer
   - Both should open the new pages

2. **Test navigation from policy pages**:
   - Click the "Las Vegas Solar" logo on the policy pages
   - Should return to index.html

3. **Check all links on policy pages**:
   - All footer links should work
   - Navigation links should work

### Customizing Policy Pages

The templates provided are generic. You should customize them with:

1. **Your actual company information**
2. **Your specific data practices**
3. **Your specific terms and conditions**
4. **Your legal requirements** (consult a lawyer if needed)

**Areas to Customize in Privacy Policy**:
- Replace `x_n2deep_x@yahoo.com` with your email
- Add specific information about what data you collect
- Detail how you use customer data
- List any third parties you share data with
- Add any specific privacy practices

**Areas to Customize in Terms of Service**:
- Replace `Nevada` with your state/jurisdiction
- Add specific terms about solar services
- Detail warranty information
- Add cancellation/refund policies
- Include any specific disclaimers

---

## Customizing Colors and Branding

### Understanding the Color Scheme

Your current landing page uses a **purple-to-blue gradient** theme:
- Primary: Purple (`from-purple-600 to-blue-600`)
- Accents: Purple (`purple-400`, `purple-500`)
- Secondary: Blue (`blue-400`, `blue-600`)
- Background: Dark gray (`gray-900`, `gray-800`)

### Complete Color Change Example

**Scenario**: Change from purple-blue to teal-green

**Step 1**: Find all color references

Use Find & Replace (`Ctrl+H` or `Cmd+H`):

| Find | Replace | Count |
|------|---------|-------|
| `from-purple-600` | `from-teal-600` | Multiple |
| `to-blue-600` | `to-green-600` | Multiple |
| `text-purple-400` | `text-teal-400` | Multiple |
| `purple-500` | `teal-500` | Multiple |
| `hover:text-purple-400` | `hover:text-teal-400` | Multiple |
| `border-purple-500` | `border-teal-500` | Multiple |

**Step 2**: Update gradient backgrounds

Example change:
```html
<!-- Before -->
<button class="px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white rounded-lg">

<!-- After -->
<button class="px-8 py-4 bg-gradient-to-r from-teal-600 to-green-600 text-white rounded-lg">
```

### Tailwind Color Options

Common colors available in Tailwind:
- `red`, `orange`, `yellow`, `green`, `teal`, `cyan`, `blue`, `indigo`, `purple`, `pink`

Each color has variations:
- `400` (light)
- `500` (medium)
- `600` (dark)
- `700` (darker)

### Changing the Logo

**Current Logo** (Lines 113-116):
```html
<div class="w-10 h-10 bg-gradient-to-br from-purple-500 to-blue-500 rounded-lg flex items-center justify-center">
    <i class="fas fa-sun text-white text-lg"></i>
</div>
```

**Option 1**: Change the icon
Replace `fa-sun` with another Font Awesome icon:
```html
<!-- Solar/Energy related icons -->
<i class="fas fa-solar-panel"></i>        <!-- Solar panel -->
<i class="fas fa-leaf"></i>              <!-- Environmental -->
<i class="fas fa-bolt"></i>              <!-- Lightning bolt -->
<i class="fas fa-power-off"></i>         <!-- Power -->
<i class="fas fa-lightbulb"></i>         <!-- Light bulb -->
```

**Option 2**: Change the gradient
```html
<div class="w-10 h-10 bg-gradient-to-br from-yellow-500 to-orange-500 rounded-lg flex items-center justify-center">
    <i class="fas fa-sun text-white text-lg"></i>
</div>
```

**Option 3**: Use an image instead
```html
<img src="assets/images/logo.png" alt="Las Vegas Solar" class="w-10 h-10">
```

### Changing Text Colors

**Hero Headline Gradient**:
```html
<!-- Current (purple-blue) -->
<span class="bg-gradient-to-r from-purple-400 via-blue-400 to-purple-400 bg-clip-text text-transparent">

<!-- New (teal-green) -->
<span class="bg-gradient-to-r from-teal-400 via-green-400 to-teal-400 bg-clip-text text-transparent">
```

### Changing Button Styles

**Primary Button** (Current):
```html
<a class="px-8 py-4 bg-gradient-to-r from-purple-600 to-blue-600 text-white rounded-lg font-bold">
```

**To Solid Color**:
```html
<a class="px-8 py-4 bg-purple-600 text-white rounded-lg font-bold hover:bg-purple-700">
```

**To Outline Style**:
```html
<a class="px-8 py-4 border-2 border-purple-600 text-purple-400 rounded-lg font-bold hover:bg-purple-600 hover:text-white">
```

### Brand Color Palette Template

Create a consistent color scheme:

```html
<!-- Save this as a reference -->
<!-- PRIMARY COLORS -->
Primary Gradient: from-[YOUR-COLOR]-600 to-[YOUR-COLOR]-600
Primary Light: [YOUR-COLOR]-400
Primary Dark: [YOUR-COLOR]-700

<!-- ACCENT COLORS -->
Accent Gradient: from-[YOUR-ACCENT]-600 to-[YOUR-ACCENT]-600
Accent Light: [YOUR-ACCENT]-400
Accent Dark: [YOUR-ACCENT]-700

<!-- BACKGROUND COLORS -->
Dark BG: bg-gray-900
Medium BG: bg-gray-800
Light BG: bg-gray-700

<!-- TEXT COLORS -->
Primary Text: text-white
Secondary Text: text-gray-300
Tertiary Text: text-gray-400
```

---

## Mobile Responsiveness

### How Responsive Design Works

Your page automatically adapts to different screen sizes using Tailwind's responsive prefixes:

| Prefix | Screen Size | Device |
|--------|------------|--------|
| (none) | < 640px | Mobile phones |
| `sm:` | 640px+ | Large phones |
| `md:` | 768px+ | Tablets |
| `lg:` | 1024px+ | Laptops |
| `xl:` | 1280px+ | Large monitors |

### Testing Responsive Design

**In Your Browser**:
1. Open `index.html` in Chrome, Firefox, or Safari
2. Press `F12` to open Developer Tools
3. Click the mobile device icon (top-left of DevTools)
4. Select different device sizes to test

**Common Test Sizes**:
- iPhone (375px wide)
- iPad (768px wide)
- Desktop (1024px+ wide)

### Understanding Responsive Classes

**Example 1: Text Size Changes**
```html
<h1 class="text-4xl sm:text-5xl md:text-6xl lg:text-7xl">
```
- Mobile: `text-4xl` (36px)
- Small tablets: `sm:text-5xl` (48px)
- Tablets: `md:text-6xl` (60px)
- Desktops: `lg:text-7xl` (72px)

**Example 2: Grid Layout Changes**
```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
```
- Mobile: 1 column
- Tablets: 2 columns
- Desktops: 4 columns

**Example 3: Hidden/Visible Elements**
```html
<div class="hidden md:flex">
    <!-- This is hidden on mobile, visible on tablets+ -->
</div>
```

### Common Mobile Issues and Fixes

**Issue 1: Text too large on mobile**

Find the text class and reduce the first value:
```html
<!-- Before -->
<h2 class="text-4xl md:text-5xl">

<!-- After (smaller on mobile) -->
<h2 class="text-2xl md:text-5xl">
```

**Issue 2: Images not responsive**

Add width classes:
```html
<!-- Before -->
<img src="image.jpg" alt="Description">

<!-- After -->
<img src="image.jpg" alt="Description" class="w-full h-auto">
```

**Issue 3: Navigation menu overlapping content**

The mobile menu is handled by JavaScript. Ensure it's working:
1. Open the page on mobile
2. Click the hamburger menu icon
3. Menu should slide down
4. Click a link to close it

**Issue 4: Buttons too small on mobile**

Increase padding on mobile:
```html
<!-- Before -->
<a class="px-6 py-2 bg-purple-600">Button</a>

<!-- After -->
<a class="px-4 py-2 sm:px-6 sm:py-3 bg-purple-600">Button</a>
```

### Testing the Mobile Menu

The mobile hamburger menu is in the header (Lines 136-150).

**To test it works**:
1. Open page on mobile or resize browser window to < 768px
2. Click the hamburger icon (three lines)
3. Menu should appear with links
4. Click a link to close menu
5. Click hamburger again to close

**If menu doesn't work**:
1. Check that JavaScript is enabled
2. Verify the mobile menu button HTML hasn't changed
3. Check browser console for errors (`F12` → Console tab)

### Mobile Menu Customization

**Current Mobile Menu** (Lines 138-150):
```html
<div class="mobile-menu hidden absolute top-full left-0 right-0 bg-gray-800 border-t border-gray-700 md:hidden">
    <div class="flex flex-col space-y-4 px-4 py-6">
        <!-- Links here -->
    </div>
</div>
```

**To Add More Links to Mobile Menu**:
1. Add the link to the mobile menu (inside the `<div class="flex flex-col">`)
2. Make sure it matches the desktop menu link

**Example - Adding a "Blog" link**:
```html
<a href="blog.html" class="text-gray-300 hover:text-purple-400 transition-colors duration-300 font-medium">Blog</a>
```

---

## Troubleshooting Common Issues

### Issue: Links Don't Work

**Symptom**: Clicking a link does nothing

**Solution**:
1. Check the `href` attribute has the correct URL
2. Verify the file exists in the same folder
3. Check for typos in the URL
4. Make sure you used `#` for internal links (same page)
5. Make sure you used `https://` for external links

**Example**:
```html
<!-- Wrong -->
<a href="privacy">Privacy</a>

<!-- Correct -->
<a href="privacy.html">Privacy</a>
```

### Issue: Navigation Menu Doesn't Scroll to Section

**Symptom**: Clicking "Features" doesn't jump to features section

**Solution**:
1. Verify the link has `href="#features"`
2. Verify the section has `id="features"`
3. Check spelling matches exactly (case-sensitive)

**Example**:
```html
<!-- Navigation link -->
<a href="#features">Features</a>

<!-- Section must have matching ID -->
<section id="features">
```

### Issue: Colors Look Wrong

**Symptom**: Changed a color class but it didn't change

**Solution**:
1. Make sure you saved the file (`Ctrl+S` or `Cmd+S`)
2. Refresh the browser (`Ctrl+R` or `Cmd+R`)
3. Hard refresh to clear cache (`Ctrl+Shift+R` or `Cmd+Shift+R`)
4. Check that you're editing the right file

### Issue: Mobile Menu Button Doesn't Work

**Symptom**: Hamburger icon doesn't open menu on mobile

**Solution**:
1. Check JavaScript is enabled in browser
2. Open browser console (`F12` → Console tab)
3. Look for error messages
4. Verify the mobile menu HTML structure hasn't changed
5. Check the JavaScript code at the bottom of the file (Lines 757-800)

### Issue: Text Appears Too Small/Large on Mobile

**Symptom**: Content doesn't fit or is hard to read

**Solution**:
1. Test on actual mobile device or use browser dev tools
2. Adjust the `sm:`, `md:`, `lg:` prefixes
3. Reduce text size for mobile, keep larger for desktop

**Example**:
```html
<!-- Too large on mobile -->
<p class="text-2xl md:text-3xl">

<!-- Better -->
<p class="text-base md:text-2xl">
```

### Issue: Images Not Showing

**Symptom**: Image placeholder appears instead of image

**Solution**:
1. Check the image file exists in the correct folder
2. Verify the file path in `src` attribute
3. Check file name spelling and capitalization
4. Try using a full URL instead of relative path

**Example**:
```html
<!-- Relative path (file in same folder) -->
<img src="image.jpg">

<!-- Relative path (file in subfolder) -->
<img src="assets/images/image.jpg">

<!-- Full URL -->
<img src="https://example.com/image.jpg">
```

### Issue: External Links Open in Same Tab

**Symptom**: Clicking external link leaves your site

**Solution**: Add `target="_blank"` to open in new tab

```html
<!-- Opens in same tab -->
<a href="https://example.com">Link</a>

<!-- Opens in new tab -->
<a href="https://example.com" target="_blank">Link</a>
```

### Issue: FAQ Accordion Not Expanding

**Symptom**: Clicking FAQ question doesn't show answer

**Solution**:
1. Check JavaScript is enabled
2. Verify the FAQ HTML structure is correct
3. Check browser console for errors
4. Make sure you didn't accidentally remove the `hidden` class from answers

**Correct Structure**:
```html
<div class="faq-item">
    <button class="faq-question">Question?</button>
    <div class="faq-answer hidden">Answer here</div>
</div>
```

### Issue: Page Loads Slowly

**Symptom**: Takes a long time to display

**Solution**:
1. Check internet connection
2. Optimize images (compress them)
3. Remove unused CSS/JavaScript
4. Check browser cache is working
5. Use a CDN for external resources (already done in this template)

### Issue: Styling Breaks After Changes

**Symptom**: Page looks broken after editing

**Solution**:
1. Don't remove entire class attributes
2. Don't delete opening or closing tags
3. Keep all quotes matched
4. Use Find & Replace carefully

**Common Mistakes**:
```html
<!-- Wrong - removed all classes -->
<div>Text</div>

<!-- Correct - keep classes -->
<div class="text-white">Text</div>

<!-- Wrong - broken tag -->
<div class="text-white>Text</div>

<!-- Correct - matched quotes -->
<div class="text-white">Text</div>
```

### Getting Help with Errors

**To Find Errors**:
1. Open browser Developer Tools (`F12`)
2. Click "Console" tab
3. Look for red error messages
4. Error messages usually indicate what's wrong

**Common Error Types**:
- `Uncaught SyntaxError` - HTML/CSS syntax problem
- `404 Not Found` - File or link doesn't exist
- `Uncaught TypeError` - JavaScript error

---

## Best Practices for Maintenance

### Regular Maintenance Checklist

**Monthly**:
- [ ] Test all links work
- [ ] Check mobile responsiveness
- [ ] Review testimonials (add new ones)
- [ ] Update statistics if changed

**Quarterly**:
- [ ] Review and update pricing/offers
- [ ] Check for broken external links
- [ ] Update FAQ with new questions
- [ ] Review analytics for popular sections

**Annually**:
- [ ] Update copyright year in footer (Line 761)
- [ ] Review and update all content
- [ ] Check for outdated information
- [ ] Consider design refresh

### Version Control

Keep backups of your file:
1. Before making major changes, save a copy
2. Name it with date: `index_backup_2025-01-15.html`
3. Store backups in a safe location

### Documentation

Keep notes about:
- What changes you made
- When you made them
- Why you made them
- Any issues you encountered

**Example Log**:
```
2025-01-15: Updated company email from old@example.com to new@example.com
2025-01-10: Added new testimonial from John Smith
2025-01-05: Changed primary color from purple to teal
```

### Performance Optimization

**To Keep Page Fast**:
1. Minimize image file sizes
2. Use external CSS/JavaScript (already done)
3. Avoid auto-playing videos
4. Keep code clean and organized
5. Test page load speed regularly

**Tools to Check Speed**:
- Google PageSpeed Insights
- GTmetrix
- WebPageTest

---

## Quick Reference Guide

### File Structure
```
your-project/
├── index.html           ← Main landing page
├── privacy.html         ← Privacy policy
├── terms.html           ← Terms of service
├── blog.html            ← Blog (create as needed)
└── assets/
    └── images/          ← Store images here
```

### Key File Locations in index.html

| Section | Lines | Purpose |
|---------|-------|---------|
| Header/Navigation | 109-150 | Main menu and logo |
| Hero Section | 152-203 | Main headline and CTA |
| Features | 205-284 | Three main features |
| Benefits | 286-387 | Four benefits |
| About Us | 389-430 | Company info |
| Testimonials | 432-516 | Customer reviews |
| FAQ | 518-648 | Questions & answers |
| CTA Banner | 650-677 | Final call-to-action |
| Footer | 679-755 | Contact and links |
| JavaScript | 757-800 | Interactive features |

### Common Edit Tasks

**Update company name**:
- Search for "Las Vegas Solar"
- Replace with your company name

**Update email**:
- Search for "x_n2deep_x@yahoo.com"
- Replace with your email

**Update CTA link**:
- Search for "https://americashomecontractors.com/actnow"
- Replace with your conversion URL

**Change colors**:
- Search for "purple-600"
- Replace with your color

**Update phone number**:
- Find the contact section
- Add phone number with `<a href="tel:+1234567890">`

### Useful Keyboard Shortcuts

| Action | Windows | Mac |
|--------|---------|-----|
| Find | Ctrl+F | Cmd+F |
| Find & Replace | Ctrl+H | Cmd+H |
| Save | Ctrl+S | Cmd+S |
| Undo | Ctrl+Z | Cmd+Z |
| Redo | Ctrl+Y | Cmd+Shift+Z |
| Select All | Ctrl+A | Cmd+A |

---

## Conclusion

You now have a comprehensive guide to maintaining and customizing your Las Vegas Solar landing page. Remember:

1. **Always backup** before making major changes
2. **Test thoroughly** after each edit
3. **Keep it simple** - don't overcomplicate things
4. **Stay consistent** with existing styles and formatting
5. **Document changes** for future reference

For additional help:
- Tailwind CSS Docs: https://tailwindcss.com/docs
- Font Awesome Icons: https://fontawesome.com/icons
- HTML/CSS Tutorials: https://www.w3schools.com

Good luck with your solar business website!