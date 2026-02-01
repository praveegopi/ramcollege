# Holyfaith Group Style Framework - Usage Guide

## Overview

This framework provides a complete, unified CSS system for all Holyfaith Group website pages. It consolidates the best styling patterns from all existing pages into one comprehensive, reusable system.

---

## Quick Start

### Option 1: Link External CSS File

```html
<link rel="stylesheet" href="holyfaith-style-framework.css">
```

### Option 2: Inline CSS (Copy entire CSS)

For standalone pages, copy the entire CSS content from `holyfaith-style-framework.css` into your `<style>` tag.

---

## Required External Resources

Add these to every page's `<head>`:

```html
<!-- Google Fonts: Poppins -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

<!-- Font Awesome Icons -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
```

---

## Color Palette (CSS Variables)

| Variable | Color | Hex | Usage |
|----------|-------|-----|-------|
| `--primary` | Deep Academic Green | `#006a4e` | Main brand color, headings, buttons |
| `--primary-dark` | Dark Green | `#004d38` | Hover states |
| `--accent` | Action Red | `#e31e24` | CTAs, highlights, badges |
| `--accent-dark` | Dark Red | `#c0181d` | Hover states |
| `--text-dark` | Near Black | `#212529` | Primary text |
| `--text-gray` | Gray | `#6c757d` | Secondary text |
| `--light-bg` | Light Gray | `#f8f9fa` | Section backgrounds |
| `--white` | White | `#ffffff` | Backgrounds |
| `--footer-bg` | Dark | `#1a1a1a` | Footer background |

---

## Component Library

### 1. Header & Navigation

#### Full Logo Header (Homepage style)
```html
<header>
    <a href="index.html" class="logo">
        <img src="logo.png" alt="Holyfaith Logo">
        <div class="logo-text">
            HOLYFAITH <span>GROUP</span>
        </div>
    </a>
    
    <div class="mobile-toggle" onclick="toggleMenu()">
        <i class="fas fa-bars"></i>
    </div>
    
    <nav class="nav-links" id="navMenu">
        <a href="index.html">Home</a>
        <a href="about.html">About Us</a>
        <a href="academics.html">Academics</a>
        <a href="admission.html" class="btn-apply-header">Apply Now</a>
    </nav>
</header>
```

#### Back Arrow Header (Inner pages)
```html
<header>
    <a href="index.html" class="back-home-brand">
        <i class="fa-solid fa-arrow-left"></i> Holyfaith Group
    </a>
    <!-- Navigation same as above -->
</header>
```

---

### 2. Hero Sections

#### Video Background Hero (Homepage)
```html
<section class="hero">
    <video autoplay muted loop playsinline class="hero-video">
        <source src="video.mp4" type="video/mp4">
    </video>
    <div class="hero-overlay"></div>
    <div class="hero-content">
        <h1>Main Heading</h1>
        <p>Subtitle text</p>
        <form class="search-program">
            <input type="text" placeholder="Search...">
            <button type="submit">Search</button>
        </form>
    </div>
</section>
```

#### Image Background Hero (Inner pages)
```html
<section class="page-hero">
    <video autoplay muted loop playsinline class="video-bg">
        <source src="video.mp4" type="video/mp4">
    </video>
    <div style="background: rgba(0,0,0,0.6); position: absolute; inset: 0;"></div>
    <div class="hero-content">
        <h1>Page Title</h1>
        <p>Page description</p>
    </div>
</section>
```

---

### 3. Buttons

| Button Class | Style | Usage |
|--------------|-------|-------|
| `.btn-primary` / `.btn-apply` | Red filled | Primary CTAs |
| `.btn-outline` | Green outline | Secondary actions |
| `.btn-pill` | Red pill-shaped | Featured CTAs |
| `.btn-course` | Green outline block | Course links |
| `.btn-submit` | Red full-width | Form submissions |
| `.read-more` | Red text link | Card links |

```html
<!-- Primary Button -->
<a href="#" class="btn-primary">Apply Now</a>

<!-- Outline Button -->
<a href="#" class="btn-outline">Learn More</a>

<!-- Pill Button -->
<a href="#" class="btn-pill">Get Started</a>

<!-- Read More Link -->
<a href="#" class="read-more">View Details <i class="fas fa-arrow-right"></i></a>
```

---

### 4. Cards

#### Standard Card
```html
<div class="card">
    <div class="card-img-wrap">
        <img src="image.jpg" alt="Description">
    </div>
    <div class="card-body">
        <h3>Card Title</h3>
        <p>Card description</p>
        <a href="#" class="read-more">Learn More <i class="fas fa-arrow-right"></i></a>
    </div>
</div>
```

#### Course Card (with badge and specs)
```html
<div class="course-card">
    <div class="img-wrapper">
        <span class="badge">B.Sc / M.Sc</span>
        <img src="image.jpg" alt="Course">
    </div>
    <div class="card-body">
        <h3>Course Title</h3>
        <p>Course description</p>
        <div class="card-specs">
            <div class="spec"><i class="fas fa-calendar-alt"></i> 4 Yrs</div>
            <div class="spec"><i class="fas fa-user-md"></i> Clinicals</div>
            <div class="spec"><i class="fas fa-hospital"></i> 100% Place</div>
        </div>
        <a href="#" class="btn-course">View Details</a>
    </div>
</div>
```

#### Mission Card
```html
<div class="mission-card">
    <i class="fas fa-eye"></i>
    <h3>Our Vision</h3>
    <p>Vision statement here</p>
</div>
```

---

### 5. Grids

```html
<!-- Standard Cards Grid -->
<div class="cards-container">
    <!-- Cards here -->
</div>

<!-- Courses Grid -->
<div class="courses-grid">
    <!-- Course cards here -->
</div>

<!-- Mission Grid -->
<div class="mission-grid">
    <!-- Mission cards here -->
</div>

<!-- Split Layout -->
<div class="story-container">
    <div><!-- Content --></div>
    <div><!-- Image --></div>
</div>
```

---

### 6. Stats/Counters

#### Green Background Stats
```html
<section class="stats-section">
    <div class="stats-grid">
        <div class="stat-item">
            <h2>25+</h2>
            <p>Years Experience</p>
        </div>
        <!-- More stats -->
    </div>
</section>
```

#### White Card Stats
```html
<div class="stats-row">
    <div class="stat-card">
        <span class="stat-num">95%</span>
        Placement Record
    </div>
    <!-- More stat cards -->
</div>
```

---

### 7. Forms

```html
<div class="form-wrapper">
    <h2>Form Title</h2>
    <form>
        <div class="form-group">
            <label>Field Label</label>
            <input type="text" placeholder="Placeholder" required>
        </div>
        
        <div class="form-group">
            <label>Select Option</label>
            <select required>
                <option value="" disabled selected>Choose...</option>
                <option value="1">Option 1</option>
            </select>
        </div>
        
        <div class="form-group">
            <label>Message</label>
            <textarea placeholder="Your message..."></textarea>
        </div>
        
        <button type="submit" class="btn-submit">Submit</button>
    </form>
</div>
```

---

### 8. Process Steps

```html
<div class="process-step">
    <div class="step-num">1</div>
    <div class="step-content">
        <h3>Step Title</h3>
        <p>Step description</p>
    </div>
</div>
```

---

### 9. Side Widget (Fixed)

```html
<div class="side-widget">
    <a href="admission.html" class="widget-item red">
        <i class="fas fa-edit"></i> Admission
    </a>
    <a href="chat.html" class="widget-item">
        <i class="fas fa-comments"></i> Student Chat
    </a>
    <a href="contact.html" class="widget-item">
        <i class="fas fa-phone-alt"></i> Contact Us
    </a>
</div>
```

---

### 10. Footer

```html
<footer>
    <div class="footer-grid">
        <div class="footer-col">
            <h2 style="color:white;">HOLYFAITH</h2>
            <p>Tagline here</p>
            <div class="social-icons">
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
        </div>
        
        <div class="footer-col">
            <h4>Quick Links</h4>
            <ul class="footer-links">
                <li><a href="about.html">About Us</a></li>
                <li><a href="admission.html">Admissions</a></li>
            </ul>
        </div>
        
        <div class="footer-col">
            <h4>Contact Us</h4>
            <ul class="footer-links">
                <li><i class="fas fa-map-marker-alt"></i> Address</li>
                <li><i class="fas fa-phone"></i> Phone</li>
                <li><i class="fas fa-envelope"></i> Email</li>
            </ul>
        </div>
    </div>
    
    <p style="text-align: center; border-top: 1px solid #333; padding-top: 20px;">
        &copy; 2026 Holyfaith Group. All Rights Reserved.
    </p>
</footer>
```

---

## JavaScript Functions

### Mobile Menu Toggle
```javascript
function toggleMenu() {
    const nav = document.getElementById('navMenu');
    nav.classList.toggle('active');
}
```

### Form Success Handler
```javascript
const form = document.getElementById('formId');
const successMsg = document.getElementById('successMsg');

form.addEventListener('submit', function(e) {
    e.preventDefault();
    const formData = new FormData(form);
    
    fetch('https://api.web3forms.com/submit', {
        method: 'POST',
        body: formData
    })
    .then(response => {
        if (response.status === 200) {
            successMsg.style.display = 'block';
            form.reset();
        }
    });
});
```

---

## Responsive Breakpoints

| Breakpoint | Behavior |
|------------|----------|
| > 900px | Full desktop layout |
| < 900px | Mobile layout, hamburger menu, single column grids |
| < 600px | Further adjustments for small screens |

---

## Best Practices

1. **Always include** the Google Fonts and Font Awesome links
2. **Use CSS variables** for colors to maintain consistency
3. **Test on mobile** - all components are mobile-responsive
4. **Keep navigation consistent** across all pages
5. **Use semantic HTML** for better accessibility
6. **Add alt text** to all images
7. **Include the footer** on every page for consistency

---

## File Structure Recommendation

```
/project-root
├── index.html
├── about.html
├── academics.html
├── admission.html
├── placements.html
├── research.html
├── contact.html
├── chat.html
├── holyfaith-style-framework.css  (Shared CSS)
├── logo.png
└── /images (optional folder)
```

---

## Need Help?

Refer to `template-example.html` for a complete working example of all components.
