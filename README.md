# Cascadia Living Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize your real estate landing page. Whether you're updating text, fixing links, or adding new pages, we'll walk through each step together.

---

## Table of Contents

1. [Quick Start](#quick-start)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Working with Tailwind CSS Classes](#working-with-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Troubleshooting Guide](#troubleshooting-guide)
8. [Best Practices](#best-practices)

---

## Quick Start

### What You'll Need
- A text editor (we recommend **Visual Studio Code** - it's free!)
- The `index.html` file you received
- Basic understanding of HTML tags (don't worry, we'll explain everything)

### Opening Your File
1. Right-click on your `index.html` file
2. Select "Open with" → "Visual Studio Code" (or your preferred editor)
3. You're ready to make changes!

---

## Understanding the Page Structure

Your landing page is organized into distinct sections. Here's what each section does:

### Header & Navigation
**Location:** Lines 70-110 (the `<header>` tag)

This is the sticky menu at the top that appears on every page. It contains:
- Logo and branding ("Cascadia Living")
- Navigation links (Features, Benefits, Testimonials, About)
- "Get Started" button
- Mobile menu for smaller screens

### Hero Section
**Location:** Lines 112-191

This is the large, eye-catching banner at the very top with:
- Main headline ("Real Estate Agent Snohomish Counties #1")
- Subheading text
- Call-to-action buttons
- Background image
- Statistics boxes

### Features Section
**Location:** Lines 193-309

Three cards explaining what makes your service special:
- Local Market Expertise
- Proven Results
- Top Rated Service

### Benefits Section
**Location:** Lines 311-517

Three larger sections with images showing:
- How to maximize home value
- Local market knowledge
- Proven success and reliability

### Testimonials Section
**Location:** Lines 519-698

Four client review cards with:
- Star ratings
- Customer quotes
- Customer names and locations

### About Section
**Location:** Lines 700-789

Information about Bryce Johnson with:
- Professional photo
- Biography text
- Statistics boxes (500+ Transactions, 15+ Years, etc.)

### Contact Form Section
**Location:** Lines 791-870

A form for visitors to get in touch with:
- Name, email, phone, and message fields
- Form submission handling

### Footer
**Location:** Lines 872-989

The bottom of the page containing:
- Company information
- Quick links
- Services links
- Contact information
- Social media links
- Legal links (Privacy, Terms)

---

## Updating Text Content

### How to Find and Edit Text

The easiest way to update text is to use your editor's **Find & Replace** feature:

1. **Open Find & Replace:**
   - Windows/Linux: Press `Ctrl + H`
   - Mac: Press `Cmd + Option + F`

2. **Type the old text** in the "Find" field
3. **Type the new text** in the "Replace" field
4. **Click "Replace All"** to update everywhere at once

### Common Text Updates

#### Changing the Main Headline

**Current text (Line 133):**
```html
<span class="text-white">Real Estate Agent</span>
<br />
<span class="bg-gradient-to-r from-primary to-accent bg-clip-text text-transparent">Snohomish Counties #1</span>
```

**How to change it:**
1. Find: `Real Estate Agent`
2. Replace with: `Your New Headline`
3. Find: `Snohomish Counties #1`
4. Replace with: `Your New Tagline`

**Example:**
```html
<span class="text-white">Premium Home Sales</span>
<br />
<span class="bg-gradient-to-r from-primary to-accent bg-clip-text text-transparent">Seattle Area Specialists</span>
```

#### Updating the Subheading

**Current text (Line 137):**
```html
<p class="text-xl text-slate-300 leading-relaxed max-w-md">
    Discover why thousands of homeowners trust us to maximize their home value with unparalleled local market expertise and proven results in Snohomish County.
</p>
```

**How to change it:**
- Find the `<p>` tag with `text-xl text-slate-300`
- Replace the text between `>` and `</p>`

**Example:**
```html
<p class="text-xl text-slate-300 leading-relaxed max-w-md">
    Expert real estate services for buyers and sellers across the Pacific Northwest. We deliver results that exceed expectations.
</p>
```

#### Updating Feature Titles and Descriptions

**Location:** Lines 230-309 (three feature cards)

Each feature card has this structure:
```html
<h3 class="text-2xl font-bold text-white mb-4">Local Market Expertise</h3>
<p class="text-slate-300 leading-relaxed mb-6">
    With over 15 years of deep experience...
</p>
```

**To update:**
1. Find the title text you want to change
2. Replace it with your new title
3. Update the description paragraph below it

**Example for Feature 1:**
```html
<h3 class="text-2xl font-bold text-white mb-4">Deep Community Knowledge</h3>
<p class="text-slate-300 leading-relaxed mb-6">
    Our team knows every street, school, and neighborhood. We use this knowledge to help you make the best decision.
</p>
```

#### Updating Testimonials

**Location:** Lines 565-698 (four testimonial cards)

Each testimonial follows this pattern:
```html
<p class="text-lg text-slate-300 leading-relaxed mb-6">
    "Bryce helped us sell our home for $45,000 above asking price!..."
</p>
<div class="border-t border-slate-700 pt-6">
    <p class="font-bold text-white">Sarah & Michael Chen</p>
    <p class="text-slate-400 text-sm">Homeowners, Snohomish</p>
</div>
```

**To update a testimonial:**
1. Find the quote text in quotation marks
2. Replace it with the new testimonial
3. Update the customer name
4. Update the customer description (e.g., "Homeowners, Snohomish")

**Example:**
```html
<p class="text-lg text-slate-300 leading-relaxed mb-6">
    "Working with this team was the best decision we made. They sold our home in just 2 weeks at full asking price!"
</p>
<div class="border-t border-slate-700 pt-6">
    <p class="font-bold text-white">Jennifer & Tom Williams</p>
    <p class="text-slate-400 text-sm">Home Sellers, Mill Creek</p>
</div>
```

#### Updating Contact Information

**Location:** Lines 966-982 (footer contact section)

**Current email:**
```html
<a href="mailto:johnson.bryce@gmail.com" class="text-slate-400 hover:text-primary transition-colors duration-300">johnson.bryce@gmail.com</a>
```

**To change:**
- Find: `johnson.bryce@gmail.com`
- Replace with: `your.email@example.com`
- Make sure to update BOTH the email address in the `href` AND the visible text

**Current phone:**
```html
<span class="text-slate-400">(425) 555-0123</span>
```

**To change:**
- Find: `(425) 555-0123`
- Replace with: `(555) 123-4567`

#### Updating the Company Name

The company name "Cascadia Living" appears in multiple places:

1. **Header logo** (Line 81): `<span class="text-2xl font-bold text-white">Cascadia Living</span>`
2. **Footer** (Line 893): `<span class="text-xl font-bold text-white">Cascadia Living</span>`
3. **Footer copyright** (Line 975): `&copy; 2025 Cascadia Living. All rights reserved.`
4. **Meta tags** (Line 5): In the page description

**To update all at once:**
1. Press `Ctrl + H` (or `Cmd + Option + F` on Mac)
2. Find: `Cascadia Living`
3. Replace with: `Your Company Name`
4. Click "Replace All"

### Editing Statistics Boxes

**Location:** Lines 153-172 (Hero section) and Lines 755-777 (About section)

These boxes display key numbers:

```html
<div class="flex items-center gap-3">
    <div class="w-12 h-12 bg-primary/10 rounded-lg flex items-center justify-center">
        <svg class="w-6 h-6 text-primary" fill="none" stroke="currentColor" viewBox="0 0 24 24" stroke-width="1.5">
            <path stroke-linecap="round" stroke-linejoin="round" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
        </svg>
    </div>
    <div>
        <p class="text-sm text-slate-400">Top Rated</p>
        <p class="font-bold text-white">5/5 Stars</p>
    </div>
</div>
```

**To update the text:**
- Change `Top Rated` to your label (e.g., "Client Rating")
- Change `5/5 Stars` to your statistic (e.g., "4.9/5 Stars")

**Example:**
```html
<div>
    <p class="text-sm text-slate-400">Average Sale Price</p>
    <p class="font-bold text-white">8-12% Above Market</p>
</div>
```

---

## Working with Tailwind CSS Classes

### What Are Tailwind Classes?

Tailwind CSS is a system of pre-made style codes that control how your page looks. Instead of writing complex CSS, you add simple class names to your HTML elements.

**Example:**
```html
<p class="text-white text-lg font-bold">This is styled text</p>
```

Breaking this down:
- `text-white` = Makes text white
- `text-lg` = Makes text large
- `font-bold` = Makes text bold

### Common Tailwind Classes Used on Your Page

#### Text Styling

| Class | What It Does | Example |
|-------|-------------|---------|
| `text-white` | White text | Headlines, main content |
| `text-slate-300` | Light gray text | Descriptions, body text |
| `text-slate-400` | Medium gray text | Secondary text, labels |
| `text-primary` | Purple text | Accent color |
| `text-accent` | Teal/green text | Accent highlights |
| `text-lg` | Large text | Subheadings |
| `text-xl` | Extra large text | Important text |
| `text-2xl` | 2x large text | Section titles |
| `font-bold` | Bold text | Emphasis |
| `font-semibold` | Semi-bold text | Labels |

#### Spacing Classes

| Class | What It Does | Example |
|-------|-------------|---------|
| `p-6` | Padding (space inside) | `p-6`, `p-8`, `p-10` |
| `mb-4` | Margin bottom (space below) | `mb-4`, `mb-6`, `mb-8` |
| `gap-3` | Space between items | `gap-3`, `gap-6`, `gap-8` |
| `py-20` | Padding top & bottom | `py-20`, `py-32` |
| `px-8` | Padding left & right | `px-8`, `px-16` |

#### Background & Border

| Class | What It Does | Example |
|-------|-------------|---------|
| `bg-slate-800` | Dark background | Cards, sections |
| `bg-primary` | Purple background | Buttons |
| `border` | Add border | `border`, `border-2` |
| `border-slate-700` | Dark gray border | Card borders |
| `rounded-lg` | Rounded corners (small) | `rounded-lg` |
| `rounded-2xl` | Rounded corners (large) | `rounded-2xl` |
| `rounded-3xl` | Rounded corners (extra large) | `rounded-3xl` |

#### Responsive Design Classes

These classes make your page look good on phones, tablets, and computers:

| Class | What It Does | Example |
|-------|-------------|---------|
| `md:` prefix | Applies on medium screens (tablets) | `md:text-5xl` |
| `lg:` prefix | Applies on large screens (computers) | `lg:grid-cols-3` |
| `hidden` | Hides element | `hidden md:flex` (hidden on phone, shown on tablet) |

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
    Responsive Heading
</h1>
```

This means:
- On phones: Text size 4xl
- On tablets (md): Text size 5xl
- On computers (lg): Text size 6xl

### Changing Colors

Your page uses a custom color system defined at the top of the file (Lines 18-35):

```css
.text-primary {
    color: #5B4BFF;  /* Purple */
}
.text-accent {
    color: #00E5A8;  /* Teal/Green */
}
```

#### To Change the Purple Color (Primary):

1. Find line 21: `.text-primary { color: #5B4BFF; }`
2. Replace `#5B4BFF` with your color code
3. This updates ALL purple elements at once

**Color code examples:**
- `#FF6B6B` = Red
- `#4ECDC4` = Teal
- `#FFD93D` = Yellow
- `#6C5CE7` = Deep Purple
- `#00B894` = Green

You can find color codes at: [colorpicker.com](https://colorpicker.com)

#### To Change the Teal/Green Color (Accent):

1. Find line 24: `.text-accent { color: #00E5A8; }`
2. Replace `#00E5A8` with your color code

### Changing Spacing

**Example:** Making cards have more padding

**Current:**
```html
<div class="p-8 md:p-10">
```

**To increase padding:**
```html
<div class="p-10 md:p-12">
```

**Padding values:** `p-4`, `p-6`, `p-8`, `p-10`, `p-12` (each step adds more space)

### Changing Text Size

**Current headline:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl">
```

**To make it smaller:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```

**To make it larger:**
```html
<h1 class="text-6xl md:text-7xl lg:text-8xl">
```

### Changing Number of Columns

**Current (3 columns):**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
```

**To change to 2 columns:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
```

**To change to 4 columns:**
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
```

### Maintaining Responsive Design

**Important:** When you modify classes, keep the responsive prefixes:

✅ **Correct:**
```html
<div class="text-2xl md:text-3xl lg:text-4xl">
```
This looks good on all devices.

❌ **Wrong:**
```html
<div class="text-4xl">
```
This is too big on phones.

---

## Fixing and Managing Links

### Understanding Links on Your Page

Links tell visitors where to go when they click. There are two types:

1. **Internal Links** - Go to other pages on your site
2. **External Links** - Go to other websites

### Identifying All Links

Here's every link on your page and where to find it:

#### Navigation Links (Header)

**Location:** Lines 90-96

```html
<a href="#features" class="text-slate-300 hover:text-primary transition-colors duration-300 font-medium">Features</a>
<a href="#benefits" class="text-slate-300 hover:text-primary transition-colors duration-300 font-medium">Benefits</a>
<a href="#testimonials" class="text-slate-300 hover:text-primary transition-colors duration-300 font-medium">Testimonials</a>
<a href="#about" class="text-slate-300 hover:text-primary transition-colors duration-300 font-medium">About</a>
<a href="https://cascadialiving.com" target="_blank" class="btn-primary">Get Started</a>
```

**What these do:**
- `href="#features"` - Jumps to the Features section on the same page
- `href="https://cascadialiving.com"` - Opens a different website
- `target="_blank"` - Opens in a new tab

#### Call-to-Action Buttons

**Location:** Lines 141-149 (Hero section)

```html
<a href="https://cascadialiving.com" target="_blank" class="btn-primary">
    Start Your Journey
    <svg>...</svg>
</a>
<button class="btn-outline">
    <span class="flex items-center justify-center gap-2">
        <i class="fas fa-phone"></i>
        Call Now
    </span>
</button>
```

**Location:** Lines 947-956 (CTA section near bottom)

```html
<a href="https://cascadialiving.com" target="_blank" class="btn-primary">
    Get Started Today
    <svg>...</svg>
</a>
<button class="btn-outline">
    <span class="flex items-center justify-center gap-2">
        <i class="fas fa-envelope"></i>
        Email Me
    </span>
</button>
```

#### Footer Links

**Location:** Lines 903-922 (Quick Links section)

```html
<a href="#features" class="text-slate-400 hover:text-primary transition-colors duration-300">Features</a>
<a href="#benefits" class="text-slate-400 hover:text-primary transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-slate-400 hover:text-primary transition-colors duration-300">Testimonials</a>
<a href="#about" class="text-slate-400 hover:text-primary transition-colors duration-300">About Us</a>
```

**Location:** Lines 925-933 (Services section)

```html
<a href="https://cascadialiving.com" target="_blank" class="text-slate-400 hover:text-primary transition-colors duration-300">Home Buying</a>
<a href="https://cascadialiving.com" target="_blank" class="text-slate-400 hover:text-primary transition-colors duration-300">Home Selling</a>
<a href="https://cascadialiving.com" target="_blank" class="text-slate-400 hover:text-primary transition-colors duration-300">Investment Properties</a>
<a href="https://cascadialiving.com" target="_blank" class="text-slate-400 hover:text-primary transition-colors duration-300">Market Analysis</a>
```

**Location:** Lines 967-982 (Contact section)

```html
<a href="mailto:johnson.bryce@gmail.com" class="text-slate-400 hover:text-primary transition-colors duration-300">johnson.bryce@gmail.com</a>
```

**Location:** Lines 985-990 (Legal links at very bottom)

```html
<a href="privacy.html" class="text-slate-400 hover:text-primary transition-colors duration-300 text-sm">Privacy Policy</a>
<a href="terms.html" class="text-slate-400 hover:text-primary transition-colors duration-300 text-sm">Terms of Service</a>
<a href="blog.html" class="text-slate-400 hover:text-primary transition-colors duration-300 text-sm">Blog</a>
```

### Step-by-Step: Updating External Links

**Example:** Changing the "Get Started" button to point to your website

**Current (Line 100):**
```html
<a href="https://cascadialiving.com" target="_blank" class="btn-primary">Get Started</a>
```

**Steps to change:**

1. **Find the link:**
   - Look for: `href="https://cascadialiving.com"`

2. **Replace the URL:**
   - Change `https://cascadialiving.com` to your URL
   - Example: `https://yourwebsite.com`

3. **Result:**
```html
<a href="https://yourwebsite.com" target="_blank" class="btn-primary">Get Started</a>
```

**Important:** Keep `target="_blank"` - this opens the link in a new tab

### Updating All External Links at Once

**Best way to do this:**

1. Press `Ctrl + H` (or `Cmd + Option + F` on Mac) to open Find & Replace
2. Find: `https://cascadialiving.com`
3. Replace with: `https://yourwebsite.com`
4. Click "Replace All"

This updates every occurrence at once!

### Step-by-Step: Updating Email Link

**Current (Line 967):**
```html
<a href="mailto:johnson.bryce@gmail.com">johnson.bryce@gmail.com</a>
```

**Steps to change:**

1. Find: `mailto:johnson.bryce@gmail.com`
2. Replace with: `mailto:your.email@example.com`
3. Also update the visible text: `johnson.bryce@gmail.com` → `your.email@example.com`

**Result:**
```html
<a href="mailto:your.email@example.com">your.email@example.com</a>
```

### Step-by-Step: Updating Phone Number Link

**Current (Line 970):**
```html
<span class="text-slate-400">(425) 555-0123</span>
```

**To make it clickable:**

Change `<span>` to `<a>` and add `href="tel:"`

**Steps:**

1. Find: `<span class="text-slate-400">(425) 555-0123</span>`
2. Replace with:
```html
<a href="tel:+14255550123" class="text-slate-400 hover:text-primary transition-colors duration-300">(425) 555-0123</a>
```

**Note:** In the `href`, use the format `tel:+1AREACODEPHONENUMBER` (no spaces or dashes)

### Understanding Internal Links (Anchor Links)

Internal links use the `#` symbol to jump to sections on the same page.

**Example:**
```html
<a href="#features">Features</a>
```

This jumps to the section with `id="features"`.

**On your page, these sections have IDs:**
- `id="features"` (Line 193)
- `id="benefits"` (Line 311)
- `id="testimonials"` (Line 519)
- `id="about"` (Line 700)
- `id="contact"` (Line 791)

**These links are already correct** - no changes needed unless you add new sections.

### Fixing Broken Links: Step-by-Step

**If a link doesn't work, follow these steps:**

1. **Identify the broken link**
   - Example: "Get Started" button doesn't work

2. **Find it in the code**
   - Search for the link text: `Get Started`
   - Look at the `href` attribute

3. **Check the URL**
   - Is it spelled correctly?
   - Does it start with `https://`?
   - Is there a typo?

4. **Fix it**
   - Correct the spelling or URL
   - Save the file
   - Test it in your browser

**Example of fixing a typo:**

❌ **Broken:**
```html
<a href="https://cascadialiving.co">Get Started</a>
```
(Missing the "m" in ".com")

✅ **Fixed:**
```html
<a href="https://cascadialiving.com">Get Started</a>
```

---

## Adding Privacy and Terms Pages

### What You Need to Know

Your footer currently has links to three pages:
- `privacy.html` (Privacy Policy)
- `terms.html` (Terms of Service)
- `blog.html` (Blog)

These files don't exist yet, so the links are broken. Let's create them!

### Step 1: Create the Privacy Policy Page

1. **Open your text editor** (Visual Studio Code)

2. **Create a new file:**
   - File → New File (or press `Ctrl + N`)

3. **Copy this template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Cascadia Living Real Estate">
    <title>Privacy Policy - Cascadia Living</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-slate-900 text-white">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-slate-900/95 backdrop-blur-md border-b border-slate-800">
        <nav class="max-w-7xl mx-auto px-8 md:px-16 py-6 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center">
                    <i class="fas fa-home text-white text-lg"></i>
                </div>
                <span class="text-2xl font-bold text-white">Cascadia Living</span>
            </div>
            <a href="index.html" class="text-slate-300 hover:text-blue-500 transition-colors duration-300 font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="py-20 md:py-32">
        <div class="max-w-4xl mx-auto px-8 md:px-16">
            <h1 class="text-4xl md:text-5xl font-bold mb-8">Privacy Policy</h1>
            
            <div class="prose prose-invert max-w-none space-y-8 text-slate-300">
                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Introduction</h2>
                    <p>
                        Cascadia Living ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Information We Collect</h2>
                    <p>
                        We may collect information about you in a variety of ways. The information we may collect on the site includes:
                    </p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Personal identification information (name, email address, phone number)</li>
                        <li>Device information (browser type, IP address)</li>
                        <li>Usage data (pages visited, time spent on site)</li>
                        <li>Information provided through contact forms</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Use of Your Information</h2>
                    <p>
                        Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. Specifically, we may use information collected about you via the site to:
                    </p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Respond to your inquiries and requests</li>
                        <li>Send promotional emails about new listings or services</li>
                        <li>Improve our website and services</li>
                        <li>Protect against fraudulent transactions</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Disclosure of Your Information</h2>
                    <p>
                        We do not sell, trade, or rent your personal identification information to others. We may disclose generic aggregated demographic information not linked to any personal identification information regarding our visitors and users with our business partners, trusted affiliates, and advertisers.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Security of Your Information</h2>
                    <p>
                        We use administrative, technical, and physical security measures to protect your personal information. However, no method of transmission over the Internet or method of electronic storage is 100% secure.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Contact Us</h2>
                    <p>
                        If you have questions or concerns about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-4">
                        Email: <a href="mailto:johnson.bryce@gmail.com" class="text-blue-500 hover:text-blue-400">johnson.bryce@gmail.com</a><br>
                        Phone: <a href="tel:+14255550123" class="text-blue-500 hover:text-blue-400">(425) 555-0123</a>
                    </p>
                </section>

                <section>
                    <p class="text-sm text-slate-400 pt-8">
                        Last updated: January 2025
                    </p>
                </section>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-slate-950 border-t border-slate-800 py-12">
        <div class="max-w-7xl mx-auto px-8 md:px-16 text-center">
            <p class="text-slate-400">
                &copy; 2025 Cascadia Living. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

4. **Save the file:**
   - Press `Ctrl + S` (or `Cmd + S` on Mac)
   - Name it: `privacy.html`
   - Save it in the **same folder** as your `index.html`

### Step 2: Create the Terms of Service Page

1. **Create another new file:**
   - File → New File

2. **Copy this template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Cascadia Living Real Estate">
    <title>Terms of Service - Cascadia Living</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-slate-900 text-white">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-slate-900/95 backdrop-blur-md border-b border-slate-800">
        <nav class="max-w-7xl mx-auto px-8 md:px-16 py-6 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center">
                    <i class="fas fa-home text-white text-lg"></i>
                </div>
                <span class="text-2xl font-bold text-white">Cascadia Living</span>
            </div>
            <a href="index.html" class="text-slate-300 hover:text-blue-500 transition-colors duration-300 font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="py-20 md:py-32">
        <div class="max-w-4xl mx-auto px-8 md:px-16">
            <h1 class="text-4xl md:text-5xl font-bold mb-8">Terms of Service</h1>
            
            <div class="prose prose-invert max-w-none space-y-8 text-slate-300">
                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">1. Agreement to Terms</h2>
                    <p>
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">2. Use License</h2>
                    <p>
                        Permission is granted to temporarily download one copy of the materials (information or software) on Cascadia Living's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 mt-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">3. Disclaimer</h2>
                    <p>
                        The materials on Cascadia Living's website are provided on an 'as is' basis. Cascadia Living makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">4. Limitations</h2>
                    <p>
                        In no event shall Cascadia Living or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Cascadia Living's website.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on Cascadia Living's website could include technical, typographical, or photographic errors. Cascadia Living does not warrant that any of the materials on its website are accurate, complete, or current. Cascadia Living may make changes to the materials contained on its website at any time without notice.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">6. Links</h2>
                    <p>
                        Cascadia Living has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Cascadia Living of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">7. Modifications</h2>
                    <p>
                        Cascadia Living may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-white mb-4">8. Governing Law</h2>
                    <p>
                        These terms and conditions are governed by and construed in accordance with the laws of the State of Washington and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </section>

                <section>
                    <p class="text-sm text-slate-400 pt-8">
                        Last updated: January 2025
                    </p>
                </section>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-slate-950 border-t border-slate-800 py-12">
        <div class="max-w-7xl mx-auto px-8 md:px-16 text-center">
            <p class="text-slate-400">
                &copy; 2025 Cascadia Living. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

3. **Save the file:**
   - Press `Ctrl + S` (or `Cmd + S` on Mac)
   - Name it: `terms.html`
   - Save it in the **same folder** as your `index.html`

### Step 3: Customize the Privacy and Terms Pages

Now that you've created the files, customize them with your own information:

**In both `privacy.html` and `terms.html`:**

1. **Update the company name:**
   - Find: `Cascadia Living`
   - Replace with: Your company name
   - Update in the header and footer

2. **Update the email:**
   - Find: `johnson.bryce@gmail.com`
   - Replace with: Your email

3. **Update the phone number:**
   - Find: `(425) 555-0123`
   - Replace with: Your phone number

4. **Update the content:**
   - Replace the generic text with your specific policies
   - Add any additional sections you need

**Example customization:**

In the "Introduction" section, change:
```html
<p>
    Cascadia Living ("we," "us," "our," or "Company") is committed to protecting your privacy...
</p>
```

To:
```html
<p>
    Your Company Name ("we," "us," "our," or "Company") is committed to protecting your privacy...
</p>
```

### Step 4: Create the Blog Page (Optional)

Your footer also links to a blog page. Here's a simple template:

1. **Create a new file** and name it `blog.html`

2. **Add this content:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Real Estate Blog - Cascadia Living">
    <title>Blog - Cascadia Living</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-slate-900 text-white">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-slate-900/95 backdrop-blur-md border-b border-slate-800">
        <nav class="max-w-7xl mx-auto px-8 md:px-16 py-6 flex items-center justify-between">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 bg-blue-600 rounded-full flex items-center justify-center">
                    <i class="fas fa-home text-white text-lg"></i>
                </div>
                <span class="text-2xl font-bold text-white">Cascadia Living</span>
            </div>
            <a href="index.html" class="text-slate-300 hover:text-blue-500 transition-colors duration-300 font-medium">← Back to Home</a>
        </nav>
    </header>

    <!-- Main Content -->
    <main class="py-20 md:py-32">
        <div class="max-w-4xl mx-auto px-8 md:px-16">
            <h1 class="text-4xl md:text-5xl font-bold mb-8">Real Estate Blog</h1>
            <p class="text-xl text-slate-300 mb-12">
                Stay informed with our latest articles and insights about the real estate market.
            </p>

            <!-- Blog Posts Grid -->
            <div class="space-y-12">
                <!-- Blog Post 1 -->
                <article class="bg-slate-800/50 border border-slate-700 p-8 rounded-2xl hover:bg-slate-800 transition-colors duration-300">
                    <h2 class="text-2xl font-bold text-white mb-3">
                        <a href="#" class="hover:text-blue-500 transition-colors">Tips for Selling Your Home in Today's Market</a>
                    </h2>
                    <p class="text-slate-400 text-sm mb-4">Published on January 15, 2025</p>
                    <p class="text-slate-300 mb-4">
                        In today's competitive real estate market, it's essential to understand the latest strategies for selling your home quickly and at the best price. In this article, we'll share our top tips...
                    </p>
                    <a href="#" class="text-blue-500 hover:text-blue-400 font-semibold">Read More →</a>
                </article>

                <!-- Blog Post 2 -->
                <article class="bg-slate-800/50 border border-slate-700 p-8 rounded-2xl hover:bg-slate-800 transition-colors duration-300">
                    <h2 class="text-2xl font-bold text-white mb-3">
                        <a href="#" class="hover:text-blue-500 transition-colors">First-Time Home Buyer's Guide</a>
                    </h2>
                    <p class="text-slate-400 text-sm mb-4">Published on January 10, 2025</p>
                    <p class="text-slate-300 mb-4">
                        Buying your first home is an exciting but overwhelming experience. This comprehensive guide will walk you through every step of the process, from getting pre-approved to closing day...
                    </p>
                    <a href="#" class="text-blue-500 hover:text-blue-400 font-semibold">Read More →</a>
                </article>

                <!-- Blog Post 3 -->
                <article class="bg-slate-800/50 border border-slate-700 p-8 rounded-2xl hover:bg-slate-800 transition-colors duration-300">
                    <h2 class="text-2xl font-bold text-white mb-3">
                        <a href="#" class="hover:text-blue-500 transition-colors">Understanding Real Estate Market Trends</a>
                    </h2>
                    <p class="text-slate-400 text-sm mb-4">Published on January 5, 2025</p>
                    <p class="text-slate-300 mb-4">
                        Market trends are constantly changing, and it's important to stay informed. Learn how to read market data and make better decisions about your real estate investments...
                    </p>
                    <a href="#" class="text-blue-500 hover:text-blue-400 font-semibold">Read More →</a>
                </article>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-slate-950 border-t border-slate-800 py-12">
        <div class="max-w-7xl mx-auto px-8 md:px-16 text-center">
            <p class="text-slate-400">
                &copy; 2025 Cascadia Living. All rights reserved.
            </p>
        </div>
    </footer>
</body>
</html>
```

3. **Save as:** `blog.html`

### Step 5: Verify Your Links Work

1. **Open your `index.html` file** in a web browser
2. **Scroll to the bottom** (footer section)
3. **Click on:**
   - "Privacy Policy" - Should open `privacy.html`
   - "Terms of Service" - Should open `terms.html`
   - "Blog" - Should open `blog.html`

**If the links don't work:**
- Make sure all three files (`index.html`, `privacy.html`, `terms.html`, `blog.html`) are in the **same folder**
- Check that the filenames are spelled exactly as written (including lowercase letters)

### Step 6: Make Footer Links Consistent

Your footer links are already set up correctly. They point to:
```html
<a href="privacy.html">Privacy Policy</a>
<a href="terms.html">Terms of Service</a>
<a href="blog.html">Blog</a>
```

**If you want to change these links:**

1. Find the footer section (Lines 985-990)
2. Update the `href` values:

```html
<!-- Current -->
<a href="privacy.html">Privacy Policy</a>

<!-- Change to a different URL -->
<a href="https://example.com/privacy">Privacy Policy</a>
```

---

## Troubleshooting Guide

### Problem: Links Not Working

**Symptom:** You click a link and nothing happens, or you get a "404 Not Found" error.

**Solutions:**

1. **Check the file exists:**
   - Make sure `privacy.html`, `terms.html`, and `blog.html` are in the same folder as `index.html`
   - Check the filename spelling (it's case-sensitive on some systems)

2. **Check the link spelling:**
   - Find: `<a href="privacy.html">`
   - Make sure it says `privacy.html` exactly (not `Privacy.html` or `privacy.HTML`)

3. **Test the link:**
   - Right-click the link → "Inspect" (or "Inspect Element")
   - Look at the `href` value
   - Copy and paste it in a new browser tab

### Problem: Text Not Changing After I Edit It

**Symptom:** You changed text in the code, but it doesn't show up on the website.

**Solutions:**

1. **Save the file:**
   - Press `Ctrl + S` (or `Cmd + S` on Mac)
   - Look for a dot or indicator next to the filename in your editor (means unsaved)

2. **Refresh your browser:**
   - Press `Ctrl + R` (or `Cmd + R` on Mac)
   - Or press `Ctrl + F5` to do a "hard refresh" (clears cache)

3. **Close and reopen the file:**
   - Close the browser tab
   - Close the HTML file in your editor
   - Reopen both

### Problem: Styling Looks Wrong

**Symptom:** Text is the wrong color, size, or spacing after you made changes.

**Solutions:**

1. **Check for typos in class names:**
   - `text-white` ✅ (correct)
   - `text-whit` ❌ (missing 'e')
   - `textwhite` ❌ (no hyphen)

2. **Make sure you kept responsive classes:**
   - ✅ `<h1 class="text-4xl md:text-5xl lg:text-6xl">`
   - ❌ `<h1 class="text-4xl">`

3. **Check for missing closing tags:**
   - Every `<div>` needs a `</div>`
   - Every `<p>` needs a `</p>`
   - Every `<a>` needs a `</a>`

### Problem: Button Not Clickable

**Symptom:** You click a button and nothing happens.

**Solutions:**

1. **Check if it's a `<button>` or `<a>` tag:**
   - `<a href="...">` = Link (should work)
   - `<button>` = Button (needs JavaScript)

2. **If it's a button, change it to a link:**
   - Find: `<button class="btn-outline">Call Now</button>`
   - Change to: `<a href="tel:+14255550123" class="btn-outline">Call Now</a>`

3. **Check the href value:**
   - Make sure it's not empty: `href=""`
   - Make sure it has a valid URL: `href="https://example.com"`

### Problem: Mobile Menu Not Working

**Symptom:** The hamburger menu icon appears on phones but doesn't open/close.

**Solutions:**

1. **Check JavaScript is enabled:**
   - This requires JavaScript to work
   - Check your browser settings

2. **Check the HTML structure:**
   - Make sure the mobile menu button and menu are present
   - Look for: `.mobile-menu-button` and `.mobile-menu`

3. **Refresh the page:**
   - Sometimes JavaScript doesn't load properly
   - Try refreshing the browser

### Problem: Images Not Showing

**Symptom:** You see broken image icons instead of pictures.

**Solutions:**

1. **Check the image URL:**
   - Find: `<img src="https://images.unsplash.com/photo-..."`
   - Make sure the URL is complete and correct

2. **Check for typos:**
   - `https://` (correct)
   - `htp://` (missing 's')

3. **Check internet connection:**
   - These images are from external URLs
   - Make sure you're connected to the internet

4. **Use local images instead:**
   - Save an image to your folder
   - Change: `<img src="https://images.unsplash.com/photo-..." alt="Description">`
   - To: `<img src="your-image.jpg" alt="Description">`

### Problem: Form Not Submitting

**Symptom:** You fill out the contact form but it doesn't send.

**Solutions:**

1. **Check the Web3Forms access key:**
   - Find: `<input type="hidden" name="access_key" value="YOUR_WEB3FORMS_ACCESS_KEY">`
   - Replace `YOUR_WEB3FORMS_ACCESS_KEY` with your actual key from Web3Forms

2. **Get a Web3Forms key:**
   - Go to: [web3forms.com](https://web3forms.com)
   - Sign up for free
   - Create a form and copy your access key
   - Paste it in the HTML

3. **Check all required fields are filled:**
   - Name (required)
   - Email (required)
   - Message (required)

### Problem: Colors Don't Match My Brand

**Symptom:** The purple and teal colors don't match your brand colors.

**Solutions:**

1. **Find the color definitions:**
   - Look at Lines 18-35 in the `<style>` section

2. **Update the colors:**
   - Find: `#5B4BFF` (purple)
   - Replace with: Your brand color code
   - Find: `#00E5A8` (teal)
   - Replace with: Your brand color code

3. **Get color codes:**
   - Use: [colorpicker.com](https://colorpicker.com)
   - Or use your brand guidelines

4. **Update everywhere:**
   - Use Find & Replace to update all instances
   - Press `Ctrl + H`

---

## Best Practices

### 1. Always Back Up Before Making Changes

**Why:** If something breaks, you can revert to the original.

**How:**
1. Before making big changes, copy your file
2. Rename it: `index_backup.html`
3. Keep it in the same folder
4. If something goes wrong, you can restore from the backup

### 2. Make One Change at a Time

**Why:** If something breaks, you'll know exactly what caused it.

**Don't do this:**
- Change 10 things, save, then test

**Do this:**
- Change 1 thing
- Save (Ctrl + S)
- Test in browser
- If it works, move to the next change

### 3. Use Consistent Naming

**Why:** It's easier to find and update things later.

**Examples:**
- `privacy.html` not `Privacy Policy.html`
- `contact-form.html` not `contact form.html`
- `about-us.html` not `about-us-page.html`

**Rules:**
- Use lowercase letters
- Use hyphens instead of spaces
- Use descriptive names

### 4. Keep Your Files Organized

**Folder structure:**
```
your-project/
├── index.html
├── privacy.html
├── terms.html
├── blog.html
├── images/
│   ├── logo.png
│   ├── hero-image.jpg
│   └── team.jpg
└── css/
    └── custom.css
```

### 5. Test on Different Devices

**Why:** Your site should look good on phones, tablets, and computers.

**How:**
1. Open your site in a browser
2. Press `F12` to open Developer Tools
3. Click the phone icon to see mobile view
4. Test on different screen sizes

### 6. Use Semantic HTML

**What:** Use the right tags for the right content.

**Examples:**
- Use `<nav>` for navigation
- Use `<header>` for headers
- Use `<footer>` for footers
- Use `<section>` for major sections
- Use `<article>` for blog posts

### 7. Keep Links Updated

**Why:** Broken links hurt user experience and SEO.

**Checklist:**
- [ ] All internal links work (links to your own pages)
- [ ] All external links work (links to other websites)
- [ ] Email links are correct
- [ ] Phone links are formatted correctly

### 8. Test Forms Regularly

**Why:** Forms are critical for getting leads.

**How:**
1. Fill out the contact form
2. Submit it
3. Check that you receive the email
4. Update the access key if needed

### 9. Use Descriptive Alt Text for Images

**Why:** Helps with accessibility and SEO.

**Current:**
```html
<img src="image.jpg" alt="Premium Real Estate">
```

**Better:**
```html
<img src="image.jpg" alt="Modern home exterior with landscaping in Snohomish County">
```

### 10. Keep Your Code Clean

**Why:** Makes it easier to maintain and update.

**Tips:**
- Use proper indentation
- Add comments for complex sections
- Remove unused code
- Keep similar items grouped together

**Example with comments:**
```html
<!-- Hero Section -->
<section class="py-32">
    <h1>Welcome</h1>
    <!-- Main content -->
</section>

<!-- Features Section -->
<section class="py-20">
    <h2>Our Features</h2>
    <!-- Features content -->
</section>
```

### 11. Optimize Images

**Why:** Large images slow down your website.

**Tips:**
- Use external image URLs (like Unsplash) for faster loading
- Or compress local images before uploading
- Use appropriate file formats:
  - `.jpg` for photos
  - `.png` for graphics with transparency
  - `.webp` for modern browsers

### 12. Monitor Your Links Regularly

**Why:** Links can break over time.

**Monthly checklist:**
- [ ] Test all navigation links
- [ ] Test all button links
- [ ] Test email link
- [ ] Test phone link
- [ ] Test footer links
- [ ] Test social media links

---

## Quick Reference: Common Updates

### Updating Your Company Name
```
Find:    Cascadia Living
Replace: Your Company Name
```

### Updating Your Email
```
Find:    johnson.bryce@gmail.com
Replace: your.email@example.com
```

### Updating Your Phone
```
Find:    (425) 555-0123
Replace: (555) 123-4567
```

### Updating Your Website URL
```
Find:    https://cascadialiving.com
Replace: https://yourwebsite.com
```

### Changing the Main Color (Purple)
```
Find:    #5B4BFF
Replace: Your color code
```

### Changing the Accent Color (Teal)
```
Find:    #00E5A8
Replace: Your color code
```

---

## Getting Help

### Resources

- **HTML Help:** [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)
- **CSS/Tailwind Help:** [Tailwind CSS Docs](https://tailwindcss.com/docs)
- **Color Picker:** [colorpicker.com](https://colorpicker.com)
- **Web3Forms:** [web3forms.com](https://web3forms.com)
- **Code Editor:** [Visual Studio Code](https://code.visualstudio.com)

### Common Questions

**Q: Can I add more testimonials?**
A: Yes! Copy one of the testimonial cards (lines 565-598) and paste it below. Update the text and customer name.

**Q: Can I change the number of feature cards?**
A: Yes! The feature section has 3 cards. You can copy/paste to add more or delete to have fewer.

**Q: Can I add a blog post?**
A: Yes! The blog.html file has a template. Copy one of the blog post sections and add your content.

**Q: How do I add my logo?**
A: Replace the home icon with an image:
```html
<!-- Current -->
<i class="fas fa-home text-white text-lg"></i>

<!-- Change to -->
<img src="your-logo.png" alt="Logo" class="h-8 w-8">
```

**Q: Can I add more navigation links?**
A: Yes! Add new links in the header (line 90-96) and mobile menu (line 108-114).

---

## Final Checklist Before Going Live

Before you publish your website, make sure:

- [ ] All text is updated with your information
- [ ] All links work correctly
- [ ] Contact form has a valid Web3Forms access key
- [ ] Email address is correct
- [ ] Phone number is correct
- [ ] Company name is correct everywhere
- [ ] Colors match your brand
- [ ] Images load properly
- [ ] Page looks good on mobile devices
- [ ] Privacy and Terms pages are created and linked
- [ ] Social media links are updated (or removed if not applicable)
- [ ] No broken links in footer
- [ ] All testimonials are accurate or updated
- [ ] About section information is current
- [ ] No placeholder text remains
- [ ] File names are correct and consistent
- [ ] All files are in the same folder

---

## Congratulations!

You now have the knowledge to maintain and customize your Cascadia Living landing page. Remember:

1. **Start small** - Make one change at a time
2. **Test often** - Check your work in the browser frequently
3. **Backup first** - Always keep a backup of your files
4. **Ask for help** - Use the resources provided when stuck
5. **Keep learning** - Web development is always evolving

Good luck with your real estate website! 🎉