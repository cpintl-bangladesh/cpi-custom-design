# YPSA Brand Identity Specification

**Young Power in Social Action**
*Version 1.0 | Cox's Bazar Partner Organization*

---

## 1. BRAND ESSENCE

| Attribute            | Value                                                     |
| -------------------- | --------------------------------------------------------- |
| Full Name            | Young Power in Social Action                              |
| Short Name           | YPSA                                                      |
| Bengali Name         | ইপসা (Ipsha)                                          |
| Tagline              | *Empowering Communities for Sustainable Change*         |
| Type                 | National NGO — Bangladesh                                |
| Role in CPI Programs | Implementing / co-implementing partner                    |
| Context              | Health, WASH, Livelihood, Protection — Rohingya response |

---

## 2. COLOR SYSTEM

### 2.1 Primary Colors

| Name           | Hex         | RGB            | CMYK           | HSV           | Usage                              |
| -------------- | ----------- | -------------- | -------------- | ------------- | ---------------------------------- |
| Dark Navy Blue | `#0B0B45` | R11 G11 B69    | C84 M84 Y0 K73 | 240° 84% 27% | Logo background, all brand primary |
| Pure White     | `#FFFFFF` | R255 G255 B255 | C0 M0 Y0 K0    | —            | Logo icon, text on navy            |

### 2.2 Logo Color Rules

* **Primary Logo** : White logo/icon on Navy Blue background (square/rectangle)
* **Reversed** : Navy Blue on White background (for print letterhead)
* **Never use** any other color combination for the logo
* The circular logo badge always uses Navy Blue as background

### 2.3 Extended Brand Colors (Digital Use)

These may be used in YPSA-branded digital interfaces:

| Name         | Hex         | Usage                          |
| ------------ | ----------- | ------------------------------ |
| Navy Blue    | `#0B0B45` | Primary (always)               |
| Light Navy   | `#1a1a6e` | Hover states, gradients        |
| Sky          | `#e8e8f5` | Light background, card fills   |
| Accent Gold  | `#f5c518` | Highlights, key stats          |
| Neutral Text | `#1a1a2e` | Body text on light backgrounds |
| White        | `#FFFFFF` | Reversed text, backgrounds     |

---

## 3. LOGO SPECIFICATIONS

### 3.1 Logo Description

The YPSA logo is a **circular badge** design:

* Outer ring: Navy Blue background with white toothed/sun-ray border
* Inner circle: Three connected human silhouettes (white) holding hands — representing community solidarity
* Top arc: Bengali text "ইপসা" (YPSA in Bengali)
* Bottom arc: "YPSA" (Latin script)
* Outer border: Two concentric rings with decorative teeth

### 3.2 Aspect Ratio

**0.80 : 1** (width : height) — always maintain this ratio

### 3.3 Logo DON'Ts (Never Do)

* Never leave out either element (image mark or text)
* Never stretch or distort the logo
* Never alter any colors
* Never use another typeface within the logo
* Never display at an angle (always horizontal/upright)
* Never use on a background that creates insufficient contrast

### 3.4 Minimum Clear Space

Maintain clear space equal to at least 10% of the logo width on all sides.

### 3.5 Logo Variants Available

| Variant                 | Background     | Use Case                     |
| ----------------------- | -------------- | ---------------------------- |
| White mark on Navy      | Navy (#0B0B45) | Default — most uses         |
| Navy mark on White      | White          | Letterhead, formal documents |
| Navy mark on Light Gray | Light gray     | Subdued print contexts       |

---

## 4. TYPOGRAPHY

YPSA does not specify a proprietary typeface. Recommended system:

| Role         | Primary Font      | Fallback      |
| ------------ | ----------------- | ------------- |
| Headlines    | Noto Sans Bengali | Arial Bold    |
| Subheadings  | Open Sans         | Arial         |
| Body         | Noto Sans Bengali | Arial Regular |
| English text | Open Sans         | Arial         |
| Data/Numbers | Roboto Mono       | Courier New   |

 **Google Fonts** :

```
https://fonts.googleapis.com/css2?family=Noto+Sans+Bengali:wght@400;600;700&family=Open+Sans:wght@400;600;700&display=swap
```

---

## 5. DESIGN PRINCIPLES

### 5.1 Visual Identity Characteristics

* **Simple and bold** : Heavy use of Navy Blue creates strong brand recognition
* **Community-centered** : The three figures in the logo reflect collective strength
* **Bilingual identity** : Bengali and English always co-present
* **Trust and solidity** : Deep navy communicates stability and reliability

### 5.2 Layout Principles

* Navy Blue header bars anchor documents
* White body areas for readability
* Accent gold for key data points and callouts
* Generous whitespace — never crowded layouts
* Bengali text should always match English counterpart in weight/size

---

## 6. DIGITAL / WEB DESIGN TOKENS

```css
/* YPSA Design Tokens — Web */
:root {
  --ypsa-navy:       #0B0B45;
  --ypsa-navy-light: #1a1a6e;
  --ypsa-sky:        #e8e8f5;
  --ypsa-gold:       #f5c518;
  --ypsa-text:       #1a1a2e;
  --ypsa-white:      #FFFFFF;

  --font-bengali:    'Noto Sans Bengali', Arial, sans-serif;
  --font-english:    'Open Sans', Arial, sans-serif;
  --font-data:       'Roboto Mono', 'Courier New', monospace;

  --ypsa-radius:     6px;
  --ypsa-shadow:     0 2px 8px rgba(11, 11, 69, 0.15);
}
```

---

## 7. CO-BRANDING WITH CPI

When YPSA and CPI appear together:

| Element             | Rule                                          |
| ------------------- | --------------------------------------------- |
| Logo order          | CPI left, YPSA right (or as agreed per MOU)   |
| Logo sizing         | Equal height (aligned on horizontal baseline) |
| Divider             | Thin vertical line `#D0C4C5`between logos   |
| Background          | White always for logo bars                    |
| Spacing             | Minimum 24px between logos                    |
| Background for both | Never colored background on co-brand bar      |

 **Co-brand CSS pattern** :

```css
.partner-logo-bar {
  background: #FFFFFF;
  display: flex;
  align-items: center;
  gap: 24px;
  padding: 16px 24px;
  border-bottom: 2px solid #D91E4D; /* CPI Red rule */
}
```

---

## 8. ACCESSIBILITY

| Combination                  | Contrast | Status |
| ---------------------------- | -------- | ------ |
| White on YPSA Navy (#0B0B45) | 17.8:1   | ✅ AAA |
| YPSA Navy on White           | 17.8:1   | ✅ AAA |
| Gold (#f5c518) on Navy       | 8.2:1    | ✅ AAA |
| Navy on Sky (#e8e8f5)        | 14.5:1   | ✅ AAA |

---

## 9. PRINT SPECIFICATIONS

| Item           | Color Mode | Notes                         |
| -------------- | ---------- | ----------------------------- |
| Logo (print)   | CMYK       | C84 M84 Y0 K73 for navy       |
| Letterhead     | CMYK       | White paper, navy header band |
| Report cover   | CMYK       | Full navy header, white body  |
| Digital/web    | RGB/HEX    | #0B0B45 exact                 |
| Screen display | sRGB       | Use #0B0B45                   |
