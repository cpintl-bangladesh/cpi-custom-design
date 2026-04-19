# YPSA Theme

**Young Power in Social Action — Visual Theme**
*For documents, reports, and co-branded materials*

---

## Theme Identity

| Field      | Value                                               |
| ---------- | --------------------------------------------------- |
| Theme Name | YPSA Classic                                        |
| Use cases  | YPSA reports, program documents, co-branded outputs |

---

## Color Palette

| Role           | Name      | Hex         |
| -------------- | --------- | ----------- |
| Primary        | YPSA Navy | `#0B0B45` |
| Background     | White     | `#FFFFFF` |
| Light Surface  | Sky       | `#E8E8F5` |
| Accent         | Gold      | `#F5C518` |
| Body Text      | Dark Navy | `#1A1A2E` |
| Secondary Text | Mid Gray  | `#64748B` |

---

## Typography

| Element        | Font              | Weight | Size | Color     |
| -------------- | ----------------- | ------ | ---- | --------- |
| Document title | Noto Sans Bengali | 700    | 28pt | YPSA Navy |
| Section head   | Open Sans         | 700    | 18pt | YPSA Navy |
| Subheading     | Open Sans         | 600    | 14pt | YPSA Navy |
| Body (Bangla)  | Noto Sans Bengali | 400    | 11pt | Dark Navy |
| Body (English) | Open Sans         | 400    | 11pt | Dark Navy |
| Caption        | Open Sans         | 400    | 9pt  | Mid Gray  |
| Stat number    | Open Sans         | 700    | 36pt | YPSA Navy |
| Stat label     | Open Sans         | 400    | 10pt | Mid Gray  |

---

## Document Layout

### Page Setup

* Size: A4 (210 × 297 mm)
* Margins: 2cm top/bottom, 2.5cm left/right
* Header height: 40mm
* Footer height: 15mm

### Header

```
[YPSA Navy band — full width, 40mm]
  [YPSA Logo — white, left aligned, height 28mm]
  [Document title — white, right aligned, Open Sans Bold 14pt]
```

### Footer

```
[Thin YPSA Navy rule — 1.5pt]
[YPSA full name (Bengali + English) — center, 8pt]
[Page number — right, 8pt]
```

### Color Accents

* Section dividers: YPSA Navy 2pt rule
* Pull quotes: Left border 4px YPSA Navy, Sky Blue background
* Data callout boxes: YPSA Navy background, white text
* Key statistics: Gold (#F5C518) number on Navy background

---

## CSS Tokens (Web/HTML)

```css
:root {
  --ypsa-navy:   #0B0B45;
  --ypsa-light:  #1a1a6e;
  --ypsa-sky:    #E8E8F5;
  --ypsa-gold:   #F5C518;
  --ypsa-text:   #1A1A2E;
  --ypsa-gray:   #64748B;
  --ypsa-white:  #FFFFFF;

  --font-bn:     'Noto Sans Bengali', Arial, sans-serif;
  --font-en:     'Open Sans', Arial, sans-serif;
}
```

---

## Slide Theme (Presentations)

### Master Colors

```
Slide background:  #FFFFFF
Title text:        #0B0B45
Body text:         #1A1A2E
Accent 1:          #F5C518 (Gold)
Accent 2:          #E8E8F5 (Sky)
Accent 3:          #64748B (Gray)
Header bar:        #0B0B45
Footer rule:       #0B0B45
```

### Title Slide Layout

```
[Full YPSA Navy top half]
  [YPSA Logo — white, centered]
  [Bengali title line]
  [English title line — smaller]
[White bottom half]
  [Subtitle / program name]
  [Date | Location]
```
