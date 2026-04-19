# Zarish Health Web Design Tokens

**CSS Custom Properties for Zarish Health / ZarishSphere EMR**
*For use in web-artifacts-builder SKILL*

---

## Brand Colors

```css
:root {
  /* Primary */
  --zh-teal:       #00555A;
  --zh-ocean:       #025259;
  --zh-gunmetal:    #00272C;
  --zh-bg:          #F7F9EC;
  --zh-blue:        #285CCC;
  --zh-velvet:      #3B2A60;
  
  /* Program Colors */
  --zh-hcv:         #FFC94B;
  --zh-cvd:         #FF947A;
  --zh-mhpss:       #D3C5F6;
  --zh-fp:          #025259;
  --zh-mnch:        #F7B638;
  --zh-community:    #CDF12B;
  
  /* Status */
  --zh-success:     #38A169;
  --zh-warning:     #FFA602;
  --zh-danger:     #FF006E;
  --zh-info:       #285CCC;
  
  /* Neutrals */
  --zh-text:        #00272C;
  --zh-text-2:      #4A5568;
  --zh-text-3:      #718096;
  --zh-border:      #CBD5E0;
  --zh-surface:     #F7F9EC;
  --zh-surface-2:   #EDF2F7;
  --zh-disabled:    #A0AEC0;
}
```

---

## Typography

```css
:root {
  --font-ui:       'Inter', Arial, sans-serif;
  --font-bn:       'Noto Sans Bengali', Arial, sans-serif;
  --font-mono:     'JetBrains Mono', 'Courier New', monospace;
  
  /* Font Sizes */
  --text-xs:   0.75rem;   /* 12px */
  --text-sm:   0.875rem;  /* 14px */
  --text-base: 1rem;      /* 16px */
  --text-lg:  1.125rem;  /* 18px */
  --text-xl:   1.25rem;   /* 20px */
  --text-2xl:  1.5rem;  /* 24px */
  --text-3xl:  1.875rem; /* 30px */
  --text-4xl:  2.25rem;   /* 36px */
}
```

---

## Spacing

```css
:root {
  --space-1:  4px;
  --space-2:  8px;
  --space-3:  12px;
  --space-4:  16px;
  --space-5:  20px;
  --space-6:  24px;
  --space-8:  32px;
  --space-10: 40px;
  --space-12: 48px;
}
```

---

## Border Radius

```css
:root {
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-md: 6px;
  --radius-lg: 12px;
  --radius-xl: 16px;
}
```

---

## Shadows

```css
:root {
  --shadow-xs: 0 1px 2px rgba(0, 39, 44, 0.05);
  --shadow-sm: 0 1px 3px rgba(0, 39, 44, 0.1);
  --shadow-md: 0 4px 12px rgba(0, 39, 44, 0.15);
  --shadow-lg: 0 8px 24px rgba(0, 39, 44, 0.2);
}
```

---

## Transitions

```css
:root {
  --transition-fast:  100ms ease;
  --transition-base: 200ms ease;
  --transition-slow: 300ms ease;
}
```

---

## Z-Index Scale

```css
:root {
  --z-base:      0;
  --z-dropdown: 100;
  --z-sticky:   200;
  --z-modal:    300;
  --z-toast:    400;
  --z-tooltip:  500;
}
```

---

## Layout Patterns

### App Layout

```css
.zh-app-layout {
  display: flex;
  height: 100vh;
  background: var(--zh-bg);
}

.zh-sidebar {
  width: 240px;
  background: var(--zh-gunmetal);
  color: var(--zh-bg);
  display: flex;
  flex-direction: column;
}

.zh-sidebar--collapsed {
  width: 64px;
}

.zh-main {
  flex: 1;
  overflow: auto;
  display: flex;
  flex-direction: column;
}

.zh-topbar {
  height: 56px;
  background: var(--zh-ocean);
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 var(--space-4);
}
```

### Sidebar Nav Item

```css
.zh-nav-item {
  display: flex;
  align-items: center;
  gap: var(--space-2);
  padding: var(--space-2) var(--space-3);
  color: var(--zh-bg);
  opacity: 0.7;
  transition: all var(--transition-fast);
  cursor: pointer;
}

.zh-nav-item:hover {
  opacity: 1;
  background: rgba(0, 85, 90, 0.3);
}

.zh-nav-item--active {
  opacity: 1;
  background: var(--zh-teal);
  border-left: 3px solid var(--zh-blue);
}
```

### Content Area

```css
.zh-content {
  flex: 1;
  padding: var(--space-4);
  overflow: auto;
}
```

---

## Components

### Patient Card

```css
.zh-patient-card {
  background: var(--zh-surface);
  border: 1px solid var(--zh-border);
  border-left: 4px solid var(--zh-teal);
  border-radius: var(--radius-md);
  padding: var(--space-4);
  margin-bottom: var(--space-2);
  box-shadow: var(--shadow-sm);
}

.zh-patient-card--hcv   { border-left-color: var(--zh-hcv); }
.zh-patient-card--cvd   { border-left-color: var(--zh-cvd); }
.zh-patient-card--mhpss  { border-left-color: var(--zh-mhpss); }
.zh-patient-card--fp    { border-left-color: var(--zh-fp); }
.zh-patient-card--mnch  { border-left-color: var(--zh-mnch); }
```

### Program Badge

```css
.zh-badge {
  display: inline-flex;
  align-items: center;
  padding: 2px 8px;
  border-radius: var(--radius-sm);
  font-size: var(--text-xs);
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.zh-badge--hcv   { background: #FFF3CD; color: #7D5A00; border: 1px solid var(--zh-hcv); }
.zh-badge--cvd   { background: #FFF0EB; color: #8B3A24; border: 1px solid var(--zh-cvd); }
.zh-badge--mhpss { background: #F3EFFE; color: #3B2A60; border: 1px solid var(--zh-mhpss); }
.zh-badge--fp   { background: #E6F4F4; color: #025259; border: 1px solid var(--zh-fp); }
.zh-badge--mnch { background: #FEF8E7; color: #7D5A00; border: 1px solid var(--zh-mnch); }
```

### Form Input

```css
.zh-input {
  width: 100%;
  padding: var(--space-2) var(--space-3);
  background: var(--zh-surface);
  border: 1px solid var(--zh-border);
  border-radius: var(--radius-md);
  font-family: var(--font-ui);
  font-size: var(--text-base);
  color: var(--zh-text);
  transition: border-color var(--transition-fast);
}

.zh-input:focus {
  outline: none;
  border-color: var(--zh-teal);
  box-shadow: 0 0 0 3px rgba(0, 85, 90, 0.15);
}

.zh-input--error {
  border-color: var(--zh-danger);
}
```

### Primary Button

```css
.zh-btn-primary {
  background: var(--zh-teal);
  color: var(--zh-bg);
  font-family: var(--font-ui);
  font-weight: 600;
  font-size: var(--text-sm);
  padding: var(--space-2) var(--space-5);
  border: none;
  border-radius: var(--radius-md);
  cursor: pointer;
  transition: background var(--transition-fast);
}

.zh-btn-primary:hover {
  background: var(--zh-ocean);
}

.zh-btn-primary:active {
  background: var(--zh-gunmetal);
}
```

### Stat Card

```css
.zh-stat-card {
  background: var(--zh-surface);
  border-radius: var(--radius-md);
  padding: var(--space-4);
  box-shadow: var(--shadow-sm);
  border-top: 3px solid var(--zh-teal);
}

.zh-stat-card__number {
  font-family: var(--font-mono);
  font-size: var(--text-3xl);
  font-weight: 700;
  color: var(--zh-text);
}

.zh-stat-card__label {
  font-size: var(--text-sm);
  color: var(--zh-text-2);
  margin-top: var(--space-1);
}
```

### Offline Banner

```css
.zh-offline-banner {
  background: var(--zh-velvet);
  color: var(--zh-bg);
  padding: var(--space-2) var(--space-4);
  text-align: center;
  font-size: var(--text-sm);
  font-weight: 500;
}
```

---

## Google Fonts Import

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Noto+Sans+Bengali:wght@400;600&family=JetBrains+Mono:wght@400;700&display=swap" rel="stylesheet">
```

---

## Tailwind Config Extension

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        zh: {
          teal:      '#00555A',
          ocean:     '#025259',
          gunmetal:  '#00272C',
          bg:        '#F7F9EC',
          blue:      '#285CCC',
          velvet:    '#3B2A60',
        },
        prog: {
          hcv:      '#FFC94B',
          cvd:      '#FF947A',
          mhpss:    '#D3C5F6',
          fp:       '#025259',
          mnch:     '#F7B638',
          community:'#CDF12B',
        },
        status: {
          success:  '#38A169',
          warning:  '#FFA602',
          danger:   '#FF006E',
          info:    '#285CCC',
          offline: '#3B2A60',
        },
      },
      fontFamily: {
        ui:    ['Inter', 'Arial', 'sans-serif'],
        bn:    ['Noto Sans Bengali', 'Arial', 'sans-serif'],
        mono:  ['JetBrains Mono', 'Courier New', 'monospace'],
      },
      borderRadius: {
        xs: '2px',
        sm: '4px',
        md: '6px',
        lg: '12px',
        xl: '16px',
      },
    },
  },
}
```