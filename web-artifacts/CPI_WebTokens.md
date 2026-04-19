# CPI Web Design Tokens

**CSS Custom Properties for CPI-branded web properties**
*For use in web-artifacts-builder SKILL*

---

## Brand Colors

```css
:root {
  /* Primary Colors */
  --cpi-purple:    #41273B;
  --cpi-red:       #D91E4D;
  --cpi-black:     #2D2926;
  --cpi-white:     #FFFFFF;
  
  /* Grayscale */
  --cpi-warm-gray: #948794;
  --cpi-light-gray: #D0C4C5;
  --cpi-gray-bg:  #F5F3F4;
  
  /* Secondary */
  --cpi-violet:    #615E9B;
  --cpi-teal:      #4298B5;
}
```

---

## Typography

```css
:root {
  /* Primary Font - External Materials */
  --font-primary: 'Raleway', Arial, sans-serif;
  
  /* System Font - Internal/Email */
  --font-system: Arial, Helvetica, sans-serif;
  
  /* Font Weights */
  --font-light:    300;
  --font-regular:  400;
  --font-medium:   500;
  --font-semibold: 600;
  --font-bold:     700;
}
```

---

## Spacing

```css
:root {
  --space-xs:  4px;
  --space-sm:  8px;
  --space-md:  16px;
  --space-lg:  24px;
  --space-xl:  32px;
  --space-2xl: 48px;
  --space-3xl: 64px;
}
```

---

## Border Radius

```css
:root {
  --radius-sm:  4px;
  --radius-md:  8px;
  --radius-lg:  16px;
  --radius-full: 9999px;
}
```

---

## Shadows

```css
:root {
  --shadow-sm: 0 1px 3px rgba(75, 39, 67, 0.12);
  --shadow-md: 0 4px 12px rgba(75, 39, 67, 0.15);
  --shadow-lg: 0 8px 24px rgba(75, 39, 67, 0.2);
}
```

---

## Breakpoints

```css
:root {
  --bp-sm: 640px;
  --bp-md: 768px;
  --bp-lg: 1024px;
  --bp-xl: 1280px;
}
```

---

## Layout Patterns

### Container

```css
.cpi-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 var(--space-lg);
}
```

### Header

```css
.cpi-header {
  background: var(--cpi-purple);
  padding: var(--space-lg) var(--space-xl);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.cpi-header__logo {
  height: 48px;
}
```

### Hero Section

```css
.cpi-hero {
  background: var(--cpi-purple);
  padding: var(--space-3xl) var(--space-xl);
  color: var(--cpi-white);
}

.cpi-hero__title {
  font-family: var(--font-primary);
  font-weight: var(--font-bold);
  font-size: 2.5rem;
  margin-bottom: var(--space-md);
}

.cpi-hero__subtitle {
  font-family: var(--font-primary);
  font-weight: var(--font-light);
  font-size: 1.25rem;
  color: var(--cpi-light-gray);
}
```

### Stat Block

```css
.cpi-stat {
  text-align: center;
  padding: var(--space-lg);
  background: var(--cpi-gray-bg);
  border-radius: var(--radius-md);
}

.cpi-stat__number {
  font-family: var(--font-primary);
  font-weight: var(--font-bold);
  font-size: 3rem;
  color: var(--cpi-red);
}

.cpi-stat__label {
  font-family: var(--font-primary);
  font-size: 0.875rem;
  color: var(--cpi-warm-gray);
}
```

### Footer

```css
.cpi-footer {
  background: var(--cpi-white);
  border-top: 4px solid var(--cpi-red);
  padding: var(--space-xl);
  text-align: center;
  font-family: var(--font-primary);
  font-size: 0.875rem;
  color: var(--cpi-warm-gray);
}
```

---

## Button Styles

### Primary Button

```css
.btn-cpi-primary {
  background: var(--cpi-red);
  color: var(--cpi-white);
  font-family: var(--font-primary);
  font-weight: var(--font-semibold);
  padding: var(--space-sm) var(--space-lg);
  border: none;
  border-radius: var(--radius-sm);
  cursor: pointer;
  transition: background 0.2s ease;
}

.btn-cpi-primary:hover {
  background: #B8183F;
}
```

### Secondary Button

```css
.btn-cpi-secondary {
  background: transparent;
  color: var(--cpi-purple);
  font-family: var(--font-primary);
  font-weight: var(--font-semibold);
  padding: var(--space-sm) var(--space-lg);
  border: 2px solid var(--cpi-purple);
  border-radius: var(--radius-sm);
  cursor: pointer;
  transition: all 0.2s ease;
}

.btn-cpi-secondary:hover {
  background: var(--cpi-purple);
  color: var(--cpi-white);
}
```

---

## Card Component

```css
.cpi-card {
  background: var(--cpi-white);
  border: 1px solid var(--cpi-light-gray);
  border-radius: var(--radius-md);
  padding: var(--space-lg);
  box-shadow: var(--shadow-sm);
}

.cpi-card__title {
  font-family: var(--font-primary);
  font-weight: var(--font-semibold);
  font-size: 1.25rem;
  color: var(--cpi-purple);
  margin-bottom: var(--space-md);
}

.cpi-card--accent {
  border-left: 4px solid var(--cpi-red);
}
```

---

## Google Fonts Import

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Raleway:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

---

## Tailwind Config Extension

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        cpi: {
          purple: '#41273B',
          red:    '#D91E4D',
          black:  '#2D2926',
          white:  '#FFFFFF',
          warmGray: '#948794',
          lightGray: '#D0C4C5',
          violet: '#615E9B',
          teal:   '#4298B5',
        },
      },
      fontFamily: {
        primary: ['Raleway', 'Arial', 'sans-serif'],
        system:  ['Arial', 'Helvetica', 'sans-serif'],
      },
    },
  },
}
```