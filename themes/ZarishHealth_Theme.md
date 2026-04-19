# ZarishHealth Digital Theme

**For EMR application, dashboards, web interfaces, and offline-first PWA**
*ZarishSphere Platform — Cox's Bazar*

---

## Theme Identity

| Field      | Value                                                                |
| ---------- | -------------------------------------------------------------------- |
| Theme Name | Zarish Clinical                                                      |
| Version    | 1.0                                                                  |
| Stack      | React 19 + TypeScript + Tailwind CSS + Supabase                      |
| Use cases  | EMR app, patient registration, NCD dashboard, reports, offline forms |

---

## Design Tokens (Complete)

```css
/* ================================================
   ZARISH HEALTH — COMPLETE DESIGN TOKENS
   ================================================ */

:root {
  /* ── Brand Colors ── */
  --zh-teal:         #00555A;
  --zh-ocean:        #025259;
  --zh-gunmetal:     #00272C;
  --zh-bg:           #F7F9EC;
  --zh-blue:         #285CCC;
  --zh-velvet:       #3B2A60;
  --zh-white:        #FFFFFF;

  /* ── Program Badge Colors ── */
  --prog-hcv:        #FFC94B;   /* HCV — Hepatitis C */
  --prog-cvd:        #FF947A;   /* CVD/NCD */
  --prog-mhpss:      #D3C5F6;   /* Mental Health */
  --prog-fp:         #025259;   /* Family Planning */
  --prog-mnch:       #F7B638;   /* Maternal & Newborn */
  --prog-community:  #CDF12B;   /* Community outreach */

  /* ── Status Colors ── */
  --status-success:  #38A169;
  --status-warning:  #FFA602;
  --status-danger:   #FF006E;
  --status-info:     #285CCC;
  --status-neutral:  #718096;
  --status-offline:  #3B2A60;

  /* ── Text Scale ── */
  --text-primary:    #00272C;
  --text-secondary:  #4A5568;
  --text-disabled:   #A0AEC0;
  --text-inverse:    #F7F9EC;

  /* ── Surface Scale ── */
  --surface-0:       #FFFFFF;
  --surface-1:       #F7F9EC;
  --surface-2:       #EDF2F7;
  --surface-3:       #E2E8F0;
  --surface-dark:    #00272C;

  /* ── Border ── */
  --border-light:    #E2E8F0;
  --border-mid:      #CBD5E0;
  --border-dark:     #4A5568;
  --border-brand:    #00555A;

  /* ── Typography ── */
  --font-ui:         'Inter', Arial, sans-serif;
  --font-bn:         'Noto Sans Bengali', Arial, sans-serif;
  --font-mono:       'JetBrains Mono', 'Courier New', monospace;
  --font-clinical:   'Source Sans Pro', Arial, sans-serif;

  /* ── Font Sizes ── */
  --text-xs:   0.75rem;    /* 12px */
  --text-sm:   0.875rem;   /* 14px */
  --text-base: 1rem;       /* 16px */
  --text-lg:   1.125rem;   /* 18px */
  --text-xl:   1.25rem;    /* 20px */
  --text-2xl:  1.5rem;     /* 24px */
  --text-3xl:  1.875rem;   /* 30px */
  --text-4xl:  2.25rem;    /* 36px */

  /* ── Spacing ── */
  --space-1: 4px;
  --space-2: 8px;
  --space-3: 12px;
  --space-4: 16px;
  --space-5: 20px;
  --space-6: 24px;
  --space-8: 32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;

  /* ── Border Radius ── */
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-md: 6px;
  --radius-lg: 12px;
  --radius-xl: 16px;

  /* ── Shadows ── */
  --shadow-xs: 0 1px 2px rgba(0,39,44,0.05);
  --shadow-sm: 0 1px 3px rgba(0,39,44,0.10), 0 1px 2px rgba(0,39,44,0.06);
  --shadow-md: 0 4px 6px rgba(0,39,44,0.07), 0 2px 4px rgba(0,39,44,0.06);
  --shadow-lg: 0 10px 15px rgba(0,39,44,0.10), 0 4px 6px rgba(0,39,44,0.05);
  --shadow-xl: 0 20px 25px rgba(0,39,44,0.10), 0 10px 10px rgba(0,39,44,0.04);

  /* ── Transitions ── */
  --transition-fast: 100ms ease;
  --transition-base: 200ms ease;
  --transition-slow: 300ms ease;

  /* ── Z-index Scale ── */
  --z-base:     0;
  --z-dropdown: 100;
  --z-sticky:   200;
  --z-modal:    300;
  --z-toast:    400;
  --z-tooltip:  500;
}
```

---

## Tailwind CSS Config

```javascript
// tailwind.config.js — ZarishHealth
module.exports = {
  theme: {
    extend: {
      colors: {
        zh: {
          teal:     '#00555A',
          ocean:    '#025259',
          gunmetal: '#00272C',
          bg:       '#F7F9EC',
          blue:     '#285CCC',
          velvet:   '#3B2A60',
        },
        prog: {
          hcv:       '#FFC94B',
          cvd:       '#FF947A',
          mhpss:     '#D3C5F6',
          fp:        '#025259',
          mnch:      '#F7B638',
          community: '#CDF12B',
        },
        status: {
          success: '#38A169',
          warning: '#FFA602',
          danger:  '#FF006E',
          info:    '#285CCC',
          offline: '#3B2A60',
        },
      },
      fontFamily: {
        ui:       ['Inter', 'Arial', 'sans-serif'],
        bn:       ['Noto Sans Bengali', 'Arial', 'sans-serif'],
        mono:     ['JetBrains Mono', 'Courier New', 'monospace'],
        clinical: ['Source Sans Pro', 'Arial', 'sans-serif'],
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

---

## Component Patterns

### Navigation Sidebar

```
Background:   --zh-gunmetal (#00272C)
Active item:  --zh-teal (#00555A)
Hover:        rgba(0,85,90,0.3)
Text:         --text-inverse (#F7F9EC)
Logo area:    --zh-ocean top band
Width:        240px desktop, collapsible to 64px
```

### Top App Bar

```
Background:   --zh-ocean (#025259)
Height:       56px
Logo:         left, 32px height
Offline badge: right, --status-offline color
Sync button:  right, --zh-blue
User avatar:  right, 32px circle
```

### Patient Card

```css
.patient-card {
  background: var(--surface-0);
  border: 1px solid var(--border-light);
  border-left: 4px solid var(--program-color);  /* varies by program */
  border-radius: var(--radius-md);
  padding: var(--space-4);
  box-shadow: var(--shadow-sm);
}
```

### Program Badge

```css
.program-badge {
  display: inline-flex;
  align-items: center;
  padding: 2px 8px;
  border-radius: var(--radius-sm);
  font-size: var(--text-xs);
  font-weight: 600;
  font-family: var(--font-ui);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}
/* HCV badge */
.badge-hcv { background: #FFF3CD; color: #7D5A00; border: 1px solid #FFC94B; }
/* CVD badge */
.badge-cvd { background: #FFF0EB; color: #8B3A24; border: 1px solid #FF947A; }
/* MHPSS badge */
.badge-mhpss { background: #F3EFFE; color: #3B2A60; border: 1px solid #D3C5F6; }
/* MNCH badge */
.badge-mnch { background: #FEF8E7; color: #7D5A00; border: 1px solid #F7B638; }
```

### Clinical Form Fields

```css
.form-label {
  font-family: var(--font-ui);
  font-size: var(--text-sm);
  font-weight: 500;
  color: var(--text-secondary);
  margin-bottom: var(--space-1);
}

.form-input {
  font-family: var(--font-ui);
  font-size: var(--text-base);
  color: var(--text-primary);
  background: var(--surface-0);
  border: 1px solid var(--border-mid);
  border-radius: var(--radius-md);
  padding: var(--space-2) var(--space-3);
  width: 100%;
  transition: border-color var(--transition-fast);
}
.form-input:focus {
  outline: none;
  border-color: var(--zh-teal);
  box-shadow: 0 0 0 3px rgba(0,85,90,0.15);
}
```

### Primary Button

```css
.btn-primary {
  background: var(--zh-teal);
  color: var(--zh-white);
  font-family: var(--font-ui);
  font-weight: 600;
  font-size: var(--text-sm);
  padding: var(--space-2) var(--space-5);
  border-radius: var(--radius-md);
  border: none;
  cursor: pointer;
  transition: background var(--transition-fast);
}
.btn-primary:hover  { background: var(--zh-ocean); }
.btn-primary:active { background: var(--zh-gunmetal); }
```

---

## Dashboard Grid Layout

```
┌─────────────────────────────────────────────┐
│  Sidebar (240px)  │  Main Content           │
│  ─────────────    │  ─────────────────────  │
│  Logo             │  [Top bar — 56px]       │
│  ─────────────    │  ─────────────────────  │
│  Nav items:       │  [Stats row — 4 cards]  │
│  • Dashboard      │  ┌────┐┌────┐┌────┐┌───┤
│  • Patients       │  │ NCD││ HCV││MHPS││TOT│
│  • HCV            │  └────┘└────┘└────┘└───┤
│  • CVD/NCD        │  [Chart section]        │
│  • MHPSS          │  ┌──────────┐┌─────────┤
│  • FP             │  │ Line chart││ Pie     │
│  • MNCH           │  │ (trends) ││ (dist.) │
│  • Reports        │  └──────────┘└─────────┤
│  • Sync           │  [Recent patients]      │
│  ─────────────    │  ─────────────────────  │
│  Offline badge    │  [Paginated table]      │
└─────────────────────────────────────────────┘
```

---

## Offline-First UI Patterns

### Sync Status Indicator

```css
.sync-badge {
  display: flex;
  align-items: center;
  gap: 4px;
  font-size: 12px;
  font-weight: 600;
}
.sync-badge.online  { color: #38A169; }
.sync-badge.offline { color: #3B2A60; background: #EDE9FE; padding: 4px 8px; border-radius: 12px; }
.sync-badge.syncing { color: #285CCC; animation: pulse 1s infinite; }
```

### Offline Banner

```html
<div class="offline-banner" style="
  background: #3B2A60;
  color: #F7F9EC;
  padding: 8px 16px;
  text-align: center;
  font-size: 13px;
  font-family: Inter, sans-serif;
">
  ⚡ Offline Mode — Data saved locally. Will sync when connected.
</div>
```
