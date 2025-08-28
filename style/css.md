# CSS Style Guide

This document outlines the CSS conventions and common patterns used in Umidly projects, derived from `base.css`. Adhering to these guidelines ensures consistency and maintainability of our stylesheets.

## 1. CSS Reset

We use a universal reset to normalize default browser styles, ensuring a consistent starting point across all elements.

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

## 2. Colors

Umidly's color palette is defined and used consistently throughout the application. Here are examples of how colors are applied:

```css
/* Body background and text */
body {
    background: #ffffff; /* White */
    color: #202124;      /* Dark Grey */
}

/* Navigation background with blur effect */
nav {
    background: rgba(255, 255, 255, 0.95); /* Transparent White */
    backdrop-filter: blur(10px);
}

/* Link colors and hover states */
.nav-links a {
    color: #5f6368; /* Grey */
}

.nav-links a:hover {
    color: #1a73e8; /* Blue */
    background: rgba(26, 115, 232, 0.08); /* Transparent Blue */
}

/* Gradient for highlights and scroll indicator */
.highlight {
    background: linear-gradient(-45deg, #1a73e8, #4285f4, #00bcd4, #26c6da);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

.scroll-indicator {
    background: linear-gradient(90deg, #4285f4, #1a73e8);
}

/* Borders and backgrounds for components */
.feature-card {
    border: 1px solid #e8eaed; /* Light Grey */
}

.stats-section {
    background: #f8f9fa; /* Very Light Grey */
}

/* Accent color for statistics */
.stat-number {
    color: #1a73e8; /* Blue */
}
```

## 3. Typography

We primarily use the 'Poppins' font. Font sizes, weights, and line heights are carefully chosen for readability and visual hierarchy.

```css
body {
    font-family: 'Poppins', sans-serif;
    line-height: 1.6;
}

/* Hero Title */
.hero-title {
    font-size: clamp(3rem, 7vw, 5.5rem);
    font-weight: 600;
    line-height: 1.1;
    letter-spacing: -0.02em;
}

/* Hero Subtitle */
.hero-subtitle {
    font-size: clamp(1.1rem, 2.2vw, 1.3rem);
    font-weight: 400;
    line-height: 1.7;
}

/* Section Titles */
.section-title {
    font-size: 2.5rem;
    font-weight: 500;
}

/* Navigation Links */
.nav-links a {
    font-weight: 500;
    font-size: 0.9rem;
}

/* Logo Text */
.logo-text {
    font-size: 24px;
    font-weight: 600;
}

/* Statistics Numbers */
.stat-number {
    font-size: 2.5rem;
    font-weight: 900;
}

/* Statistics Labels */
.stat-label {
    font-size: 0.9rem;
    font-weight: 500;
}
```

## 4. Layout (Flexbox)

Flexbox is extensively used for creating flexible and responsive layouts.

```css
/* Navigation container */
.nav-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

/* Navigation links (desktop) */
@media (min-width: 577px) {
    .nav-links {
        display: flex;
        flex-direction: row;
        gap: 1rem;
        align-items: center;
    }
}

/* Features section layout */
.features {
    display: flex;
    justify-content: center;
    gap: 4rem;
    align-items: center;
}

/* Footer links */
.footer-links {
    display: flex;
    gap: 0.5rem;
    align-items: center;
}
```

## 5. Responsive Design

Media queries are used to adapt the layout and styling for different screen sizes, ensuring a mobile-first approach.

```css
/* Mobile-first navigation toggle */
.menu-toggle {
    display: none; /* Hidden on desktop */
    flex-direction: column;
    justify-content: space-between;
    width: 24px;
    height: 18px;
}

@media (max-width: 576px) {
    /* Navigation links become a column on small screens */
    .nav-links {
        display: flex;
        flex-direction: column;
        position: absolute;
        width: 100%;
    }

    /* Features stack vertically on small screens */
    .features {
        flex-direction: column;
        gap: 0.5rem;
    }

    /* Adjust padding for main content on small screens */
    main {
        padding: 6rem 0.5rem 2rem;
    }
}

@media (min-width: 577px) {
    /* Desktop navigation links */
    .nav-links {
        display: flex !important;
        flex-direction: row;
    }

    /* Hide menu toggle on desktop */
    .menu-toggle {
        display: none;
    }
}

@media (max-width: 768px) {
    /* Adjust stats grid for tablets */
    .stats-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 480px) {
    /* Adjust stats grid for very small screens */
    .stats-grid {
        grid-template-columns: 1fr;
    }
}
```

## 6. Effects and Visual Styling

Subtle effects like transitions, shadows, and rounded corners enhance the user experience and visual appeal.

```css
/* Smooth transitions for interactive elements */
.nav-links a {
    transition: color 0.2s ease;
}

.feature-card {
    transition: all 0.2s ease;
}

/* Rounded corners */
.image-placeholder,
.feature-card,
.feature-icon {
    border-radius: 12px;
}

.nav-links a {
    border-radius: 24px;
}

/* Box shadow for depth */
.image-placeholder {
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

/* Animation for gradient text */
@keyframes gradientMove {
    0% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
}

.highlight {
    animation: gradientMove 4s ease-in-out infinite;
}
```