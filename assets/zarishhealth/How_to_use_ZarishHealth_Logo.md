# ZarishHealth / ZarishSphere Logo Usage Guide

**Official Logo Assets and Usage Guidelines**
*Version 2.0 | Professional Design System*

---

## Logo Assets

### Primary Logo Files

| File | Description | Use Case |
| ---- | ----------- | -------- |
| `zarish_health_logo_pro.svg` | **Primary vector (professional)** | Web, print, scalable — **USE THIS** |
| `zarish_health_logo_white_pro.svg` | White version | Dark backgrounds |
| `zarish_health_icon.svg` | Circular icon badge | App icons, avatars |
| `zarish_health_logo.svg` | Legacy version | Backward compatibility |
| `zarish_health_logo_white.svg` | Legacy white | Backward compatibility |

---

## Logo Versions

### Professional Primary (Standard)

```
┌─────────────────────────────────────────────────────────────────────┐
│  [Leaf]  zarish   health                        │
│          EMR PLATFORM                            │
└─────────────────────────────────────────────────────────────────────┘

Colors:
- Leaf mark: Teal gradient (#00555A → #025259)
- "zarish": #00555A (Teal)
- "health": #285CCC (Mid Blue)
- "EMR PLATFORM": #00272C (Gun Metal), opacity 0.7
```

### White Reversed (for dark backgrounds)

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                       │
│  [Leaf]  zarish   health                        │
│          EMR PLATFORM                            │
│                                                       │
└─────────────────────────────────────────────────────────────────────┘

Background options:
- Gunmetal (#00272C)
- Dark Teal (#025259)
- Navy (#0B0B45)
- Black (#000000)

Text/Icon: #FFFFFF (White)
```

### Icon Badge (Circular)

```
┌──────────────┐
│   [Leaf]    │
│   ● accent  │
└──────────────┘

Background: Teal gradient (#00555A → #025259)
Leaf: #FFFFFF
Accent dot: #285CCC

Use: App icon, favicon, social, small contexts
```

---

## Color System

### Official ZarishHealth Palette

| Name | Hex | RGB | CMYK | Use |
|------|-----|-----|------|-----|
| Primary Teal | #00555A | 0, 85, 90 | C100 M15 Y10 K65 | Logo, headers, primary UI |
| Ocean | #025259 | 2, 82, 89 | C100 M10 Y15 K67 | Navigation, sidebars |
| Gunmetal | #00272C | 0, 39, 44 | C100 M0 Y0 K100 | Dark backgrounds, footer |
| App Background | #F7F9EC | 247, 249, 236 | C2 M0 Y5 K0 | Page backgrounds |
| Interactive Blue | #285CCC | 40, 92, 204 | C80 M50 Y0 K0 | Links, CTAs, accents |
| Velvet | #3B2A60 | 59, 42, 96 | C80 M80 Y0 K20 | Offline indicator |

### Program Colors (For Badges/Charts)

| Program | Badge Color | Hex | Text Color | Border |
|---------|-----------|-----|-----------|--------|
| HCV | Mimosa (Yellow) | #FFC94B | #7D5A00 | #FFC94B |
| CVD/NCD | Salmon | #FF947A | #8B3A24 | #FF947A |
| MHPSS | Lavender | #3B2A60 | #3B2A60 | #D3C5F6 |
| Family Planning | Mid Green | #025259 | #FFFFFF | #025259 |
| MNCH | Xanthous | #7D5A00 | #7D5A00 | #F7B638 |
| Community | Lemonade | #3A4A00 | #3A4A00 | #CDF12B |

### Status Colors

| Status | Color | Hex | Use |
|--------|-------|-----|-----|
| Success | Green | #38A169 | Active, completed |
| Warning | Sunburst | #FFA602 | Due, pending |
| Danger | Magenta | #FF006E | Urgent, overdue |
| Info | Mid Blue | #285CCC | Information |
| Offline | Velvet | #3B2A60 | Offline mode |

---

## Clear Space

Maintain clear space equal to the **height of the letter "z"** in the logo on all sides.

```
Example: If "z" height = 12px, clear space = 12px minimum

┌──────────────────────┐
│                      │
│   [clear space]      │
│   ┌──────────────┐   │
│   │    Logo     │   │
│   └──────────────┘   │
│   [clear space]      │
│                      │
└──────────────────────┘
```

---

## Minimum Sizes

| Context | Minimum Width | Minimum Height |
|---------|-------------|--------------|
| Print | 25mm | 10mm |
| Web | 160px | 60px |
| App Icon | 32px | 32px |
| Favicon | 16px | 16px |
| Document header | 100px | 40px |

---

## Logo DON'Ts

### Never Do

* ❌ Change logo proportions or distort
* ❌ Alter colors (use specified palette only)
* ❌ Place on busy/patterned backgrounds
* ❌ Add effects (shadows, gradients, outlines)
* ❌ Use below minimum size
* ❌ Rotate the logo
* ❌ Separate "zarish" and "health" text
* ❌ Replace leaf motif with different icon
* ❌ Use on low-contrast backgrounds:
  - Mid gray backgrounds
  - Photographs without overlay

---

## Background Guidelines

### Approved Backgrounds

| Background Color | Logo Version |
| --------------- | ------------|
| White (#FFFFFF) | Primary (teal/blue) |
| Light (#F7F9EC) | Primary |
| Cream (#FFF2BD) | Primary |
| Dark Teal (#025259) | White |
| Gunmetal (#00272C) | White |
| Navy (#0B0B45) | White |
| Black (#000000) | White |

### Backgrounds Requiring Overlay

| Background | Overlay Needed |
| ---------- | --------------|
| Photographs | 40% black or teal overlay |
| Gradients | Test contrast first |
| Dark photos | Full overlay required |

---

## Typography

### Logo Font

| Element | Font | Weight | Size |
|---------|------|--------|------|
| "zarish" | Inter | 700 | 32px (full size) |
| "health" | Inter | 700 | 32px (full size) |
| "EMR PLATFORM" | Inter | 500 | 9px, 2.5px letter-spacing |

### Fallback Font Stack

```css
font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;
```

---

## Co-branding with CPI/YPSA

When ZarishHealth appears with CPI or YPSA:

### Layout Options

**Option 1: Horizontal (equal height)**
```
┌─────────────┐         ┌─────────────┐
│ zarish      │   +    │     CPI    │
│ health     │         │    logo    │
└─────────────┘         └─────────────┘
- Equal height (aligned on baseline)
- 24px minimum gap
```

**Option 2: Vertical stack**
```
┌─────────────┐
│  zarish    │
│  health   │
├─────────────┤
│   CPI     │
│   logo    │
└─────────────┘
```

**Option 3: Footer/credits**
```
┌─────────────────────────────────────┐
│  [Content area]                     │
├─────────────────────────────────────┤
│ zarish health  •  CPI Bangladesh    │
│                    •  YPSA         │
└──────────────────────────────────��──┘
```

---

## Usage by Context

### Documents/Reports

* Primary logo (teal/blue)
* Position: Header (left) or Footer (left)
* For PDF: Use SVG or high-res PNG

### Presentations/Slides

* Primary or white version
* Use `presentation_header.svg` for slide headers
* Use `presentation_footer.svg` for footers

### Web/App

* Primary on light backgrounds
* White on dark/nav backgrounds
* Use `zarish_health_icon.svg` for favicon
* Use SVG when possible

### Email

* Primary version (smaller)
* White version for dark email clients
* 72dpi sufficient

### Social Media

* Use `zarish_social_avatar.svg` for shared images
- LinkedIn
- Facebook
- Twitter

---

## Motif Design Brief

The leaf motif represents "growth in motion" — inspired by:
- **Zarish** (زریš) = flowering, blossoming (Pashto/Urdu)
- **Growth** = patient health improvement
- **Motion** = digital platform, progress

Design principles:
- Minimal, clinical, trustworthy
- No religious/culturally exclusive symbols
- Works in single color at small sizes
- Teal primary (#00555A), blue accent (#285CCC)

---

## File Formats

| Format | Extension | Use | Notes |
|--------|-----------|-----|-------|
| Vector | `.svg` | All purposes | **Preferred** - scalable |
| PNG | `.png` | Email, docs | 300dpi for print |
| JPG | `.jpg` | Presentations | When transparency not needed |
| ICO | `.ico` | Windows favicon | Convert from PNG |

---

## Quick Reference Card

| Element | Value |
|---------|-------|
| Primary color | #00555A (Teal) |
| Secondary color | #285CCC (Blue) |
| Dark BG version | White text (#FFFFFF) |
| Font | Inter (weight 700) |
| Tagline | EMR PLATFORM, letter-spacing 2.5px |
| Clear space | Height of "z" |
| Min print size | 25mm width |
| Min web size | 160px width |

---

## Asset Inventory

```
zarishhealth/
├── zarish_health_logo_pro.svg          ← PRIMARY USE THIS
├── zarish_health_logo_white_pro.svg    ← Dark backgrounds PRIMARY
├── zarish_health_icon.svg            ← Circular badge
├── zarish_favicon.svg              ← 16x16 favicon
├── zarish_social_avatar.svg        ← Social sharing
├── program_badges.svg             ← Program color badges
├── presentation_header.svg         ← Report/slide header
├── presentation_footer.svg         ← Report/slide footer
└── How_to_use_ZarishHealth_Logo.md  ← This guide
```

---

*Version 2.0 — Updated April 2026*
*For questions: Contact ZarishSphere Platform team*