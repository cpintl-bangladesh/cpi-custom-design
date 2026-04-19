# Zarish Health / ZarishSphere Brand Specification

**Digital Health Platform — NCD Programming, Rohingya Refugee Health**
*Version 1.0 | CPI Bangladesh Digital Initiative*

---

## 1. BRAND ESSENCE

| Attribute       | Value                                                           |
| --------------- | --------------------------------------------------------------- |
| Platform Name   | Zarish Health / ZarishSphere EMR                                |
| Short Name      | ZARISH                                                          |
| Bengali Meaning | زریش / Zarish — flowering, blossoming (Pashto/Urdu origin) |
| Tagline         | *Health Records. Dignity Preserved.*                          |
| Alt tagline     | *Open Health for All Communities*                             |
| Type            | Open-source, offline-first digital health platform              |
| Programs        | HCV, CVD/NCD, MHPSS, Family Planning, MNCH                      |
| Population      | FDMN (Rohingya) + host community — Cox's Bazar                 |
| GitHub Org      | zarishsphere                                                    |
| Domain          | zarishsphere.com                                                |

---

## 2. DESIGN PHILOSOPHY

Zarish Health is a **digital-first, clinical-grade** platform. Its visual identity must:

* Signal **trust and clinical professionalism** to health workers
* Remain **calm and functional** under stressful field conditions
* Work across **low-spec devices** (offline, low-bandwidth, small screens)
* Respect the **dignity of patients** in its visual language
* Be **fully distinct from CPI and YPSA** corporate identities

The palette draws from **teal, deep ocean, and warm earth** — colors that evoke care,
depth, and the Cox's Bazar coastal environment.

---

## 3. COLOR SYSTEM

### 3.1 Primary Palette — Zarish Health

| Name             | Hex         | RGB            | Usage                                      |
| ---------------- | ----------- | -------------- | ------------------------------------------ |
| Zarish Teal      | `#00555A` | R0 G85 B90     | Primary brand color, headers, key UI       |
| Zarish Ocean     | `#025259` | R2 G82 B89     | Deep variant — nav bars, sidebars         |
| Zarish Gun Metal | `#00272C` | R0 G39 B44     | Dark backgrounds, footer, modal overlays   |
| Zarish White     | `#F7F9EC` | R247 G249 B236 | App background (warm white, not stark)     |
| Zarish Mid Blue  | `#285CCC` | R40 G92 B204   | Interactive elements, links, CTAs          |
| Zarish Velvet    | `#3B2A60` | R59 G42 B96    | MHPSS program color, mental health modules |

### 3.2 Secondary Palette — Program Colors

| Program      | Color Name | Hex         | Usage                         |
| ------------ | ---------- | ----------- | ----------------------------- |
| HCV          | Mimosa     | `#FFC94B` | Hepatitis C program           |
| CVD/NCD      | Salmon     | `#FF947A` | Cardiovascular program        |
| MHPSS        | Lavender   | `#D3C5F6` | Mental health program         |
| Family Plan. | Mid Green  | `#025259` | Family planning module        |
| MNCH         | Xanthous   | `#F7B638` | Maternal & newborn health     |
| Community    | Lemonade   | `#CDF12B` | Community outreach activities |
| Alert/Urgent | Magenta    | `#FF006E` | Urgent flags, critical alerts |
| Warning      | Sunburst   | `#FFA602` | Warnings, pending actions     |

### 3.3 Neutral Scale

| Name           | Hex         | Usage                     |
| -------------- | ----------- | ------------------------- |
| Text Primary   | `#00272C` | All body text             |
| Text Secondary | `#4A5568` | Labels, captions          |
| Border         | `#CBD5E0` | Input borders, dividers   |
| Surface        | `#F7F9EC` | Card and page backgrounds |
| Surface Dark   | `#EDF2F7` | Hover states, zebra rows  |
| Disabled       | `#A0AEC0` | Disabled inputs/buttons   |

---

## 4. TYPOGRAPHY

### 4.1 Primary Stack

| Role           | Font              | Fallback    | Weight    |
| -------------- | ----------------- | ----------- | --------- |
| App headings   | Inter             | Arial       | 600 / 700 |
| UI labels/body | Inter             | Arial       | 400 / 500 |
| Bengali text   | Noto Sans Bengali | Arial       | 400 / 600 |
| Data / numbers | JetBrains Mono    | Courier New | 400       |
| Clinical forms | Source Sans Pro   | Arial       | 400 / 600 |

 **Google Fonts** :

```
https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Noto+Sans+Bengali:wght@400;600&family=JetBrains+Mono:wght@400&display=swap
```

### 4.2 Type Scale (Base 16px)

| Scale | Size | Line Height | Usage                |
| ----- | ---- | ----------- | -------------------- |
| xs    | 12px | 1.5         | Badges, micro labels |
| sm    | 14px | 1.43        | Captions, meta       |
| base  | 16px | 1.5         | Body text            |
| lg    | 18px | 1.56        | Emphasized body      |
| xl    | 20px | 1.4         | Card titles          |
| 2xl   | 24px | 1.33        | Section headings     |
| 3xl   | 30px | 1.2         | Page headings        |
| 4xl   | 36px | 1.1         | Dashboard stats      |

---

## 5. COMPONENT DESIGN LANGUAGE

### 5.1 Core Principles

* **Minimal chrome** : Reduce visual noise in clinical environments
* **High information density** : Show what clinicians need, nothing else
* **Color-coded programs** : Each program has its own color badge
* **Offline indicators** : Always show sync/offline status visibly
* **Multilingual-ready** : All layouts must accommodate Bengali + English side by side

### 5.2 Shape System

* Border radius: `6px` (inputs, cards), `4px` (badges), `12px` (modals)
* Never full-pill buttons for primary actions (clinical context requires clear affordance)
* Use flat shadows: `0 1px 3px rgba(0,39,44,0.1)`

### 5.3 Status Colors

| Status          | Color    | Hex         |
| --------------- | -------- | ----------- |
| Active/Success  | Green    | `#38A169` |
| Warning         | Sunburst | `#FFA602` |
| Critical/Alert  | Magenta  | `#FF006E` |
| Info            | Mid Blue | `#285CCC` |
| Inactive/Closed | Gray     | `#A0AEC0` |
| Offline Mode    | Velvet   | `#3B2A60` |

---

## 6. WEB DESIGN TOKENS

```css
/* ZarishHealth Design Tokens */
:root {
  /* Brand */
  --zh-teal:       #00555A;
  --zh-ocean:      #025259;
  --zh-gunmetal:   #00272C;
  --zh-bg:         #F7F9EC;
  --zh-blue:       #285CCC;
  --zh-velvet:     #3B2A60;

  /* Programs */
  --zh-hcv:        #FFC94B;
  --zh-cvd:        #FF947A;
  --zh-mhpss:      #D3C5F6;
  --zh-fp:         #025259;
  --zh-mnch:       #F7B638;
  --zh-community:  #CDF12B;
  --zh-urgent:     #FF006E;
  --zh-warning:    #FFA602;

  /* Neutrals */
  --zh-text:       #00272C;
  --zh-text-2:     #4A5568;
  --zh-border:     #CBD5E0;
  --zh-surface:    #F7F9EC;
  --zh-surface-2:  #EDF2F7;
  --zh-disabled:   #A0AEC0;

  /* Typography */
  --font-ui:       'Inter', Arial, sans-serif;
  --font-bn:       'Noto Sans Bengali', Arial, sans-serif;
  --font-mono:     'JetBrains Mono', 'Courier New', monospace;

  /* Spacing */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  --space-2xl: 48px;

  /* Radius */
  --radius-sm: 4px;
  --radius-md: 6px;
  --radius-lg: 12px;

  /* Shadows */
  --shadow-sm: 0 1px 3px rgba(0,39,44,0.1);
  --shadow-md: 0 4px 12px rgba(0,39,44,0.15);
  --shadow-lg: 0 8px 24px rgba(0,39,44,0.2);
}
```

---

## 7. SEPARATION FROM CPI/YPSA IDENTITIES

 **CRITICAL RULE** : Zarish Health is an  **independent digital platform identity** .

| Attribute     | Zarish Health         | CPI                | YPSA             |
| ------------- | --------------------- | ------------------ | ---------------- |
| Primary color | Teal `#00555A`      | Purple `#41273B` | Navy `#0B0B45` |
| Accent        | Mid Blue `#285CCC`  | Red `#D91E4D`    | Gold `#f5c518` |
| Font          | Inter                 | Raleway            | Open Sans        |
| Use context   | Digital app only      | All CPI materials  | YPSA materials   |
| Mix with CPI? | NO — separate system | —                 | —               |

CPI/YPSA logos appear in the **footer** or **about/credits** page of Zarish Health
as implementing/funding partners — never as primary brand elements.

---

## 8. LOGO PLACEHOLDER (Until Official Mark Created)

Until a formal Zarish Health logo is designed, use:

```html
<!-- Text-based placeholder -->
<span class="zh-logo-text">
  <span style="color:#00555A; font-weight:700; font-family:Inter;">zarish</span>
  <span style="color:#285CCC; font-weight:700; font-family:Inter;">health</span>
  <span style="display:block; font-size:10px; color:#4A5568; letter-spacing:2px;">EMR PLATFORM</span>
</span>
```

Design brief for final logo:

* Motif: Stylized flowering plant (zarish = blossoming) in teal
* Wordmark: "ZARISH HEALTH" in Inter SemiBold
* Colors: Teal primary, gun metal secondary
* No religious or culturally exclusive symbols
* Works in single color (teal or white) at small sizes
