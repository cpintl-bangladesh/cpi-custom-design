# YPSA Web Design Tokens

**CSS Custom Properties for YPSA-branded web properties**
*For use in web-artifacts-builder SKILL*

---

## Brand Colors

```css
:root {
  /* Primary */
  --ypsa-navy:     #0B0B45;
  --ypsa-navy-light: #1a1a6e;
  --ypsa-white:     #FFFFFF;
  
  /* Extended */
  --ypsa-sky:      #E8E8F5;
  --ypsa-gold:     #F5C518;
  --ypsa-text:     #1a1a2e;
  --ypsa-gray:     #64748B;
}
```

---

## Typography

```css
:root {
  --font-bengali: 'Noto Sans Bengali', Arial, sans-serif;
  --font-english: 'Open Sans', Arial, sans-serif;
  --font-data:    'Roboto Mono', 'Courier New', monospace;
  
  --font-regular: 400;
  --font-semibold: 600;
  --font-bold:    700;
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
}
```

---

## Border Radius

```css
:root {
  --radius-sm:  4px;
  --radius-md:  6px;
  --radius-lg:  12px;
}
```

---

## Shadows

```css
:root {
  --shadow-sm: 0 2px 4px rgba(11, 11, 69, 0.08);
  --shadow-md: 0 4px 12px rgba(11, 11, 69, 0.12);
  --shadow-lg: 0 8px 24px rgba(11, 11, 69, 0.16);
}
```

---

## Layout Patterns

### Navbar

```css
.ypsa-navbar {
  background: var(--ypsa-navy);
  padding: var(--space-md) var(--space-xl);
  display: flex;
  align-items: center;
  gap: var(--space-lg);
}

.ypsa-navbar__logo {
  height: 48px;
}

.ypsa-navbar__divider {
  height: 32px;
  width: 1px;
  background: rgba(255, 255, 255, 0.2);
}
```

### Bilingual Header

```css
.ypsa-bilingual-title {
  font-family: var(--font-bengali);
  color: var(--ypsa-white);
  font-size: 1.25rem;
  font-weight: 700;
}

.ypsa-bilingual-subtitle {
  font-family: var(--font-english);
  color: rgba(255, 255, 255, 0.8);
  font-size: 0.875rem;
}
```

### Card

```css
.ypsa-card {
  background: var(--ypsa-white);
  border-radius: var(--radius-md);
  box-shadow: var(--shadow-md);
  overflow: hidden;
}

.ypsa-card__header {
  background: var(--ypsa-navy);
  padding: var(--space-md) var(--space-lg);
  color: var(--ypsa-white);
  font-family: var(--font-bengali);
  font-weight: 700;
}

.ypsa-card__body {
  padding: var(--space-lg);
}
```

### Gold Stat Callout

```css
.ypsa-stat-callout {
  background: var(--ypsa-navy);
  padding: var(--space-xl);
  text-align: center;
}

.ypsa-stat-callout__number {
  font-family: var(--font-data);
  font-size: 3rem;
  font-weight: 700;
  color: var(--ypsa-gold);
}

.ypsa-stat-callout__label {
  font-family: var(--font-english);
  font-size: 0.875rem;
  color: rgba(255, 255, 255, 0.8);
  margin-top: var(--space-sm);
}
```

---

## Buttons

### Primary

```css
.btn-ypsa-primary {
  background: var(--ypsa-navy);
  color: var(--ypsa-white);
  font-family: var(--font-english);
  font-weight: var(--font-semibold);
  padding: var(--space-sm) var(--space-lg);
  border: none;
  border-radius: var(--radius-sm);
  cursor: pointer;
}

.btn-ypsa-primary:hover {
  background: var(--ypsa-navy-light);
}
```

### Gold Accent

```css
.btn-ypsa-accent {
  background: var(--ypsa-gold);
  color: var(--ypsa-navy);
  font-family: var(--font-english);
  font-weight: var(--font-bold);
  padding: var(--space-sm) var(--space-lg);
  border: none;
  border-radius: var(--radius-sm);
  cursor: pointer;
}
```

---

## Google Fonts Import

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Bengali:wght@400;600;700&family=Open+Sans:wght@400;600;700&family=Roboto+Mono:wght@400;700&display=swap" rel="stylesheet">
```

---

## Tailwind Config Extension

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        ypsa: {
          navy:     '#0B0B45',
          navyLight: '#1a1a6e',
          white:    '#FFFFFF',
          sky:      '#E8E8F5',
          gold:     '#F5C518',
          text:     '#1a1a2e',
          gray:     '#64748B',
        },
      },
      fontFamily: {
        bengali: ['Noto Sans Bengali', 'Arial', 'sans-serif'],
        english: ['Open Sans', 'Arial', 'sans-serif'],
        mono:    ['Roboto Mono', 'Courier New', 'monospace'],
      },
    },
  },
}
```