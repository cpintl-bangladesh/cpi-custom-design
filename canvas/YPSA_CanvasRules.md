# YPSA Canvas & Print Design Rules

---

## Core Principle

YPSA visual design is  **bold, minimal, and bilingual** . Navy dominates. White breathes.
Gold accents say "this matters." Bengali always present.

---

## Poster Templates

### YPSA Program Poster (A3)

```
TOP (120mm): YPSA Navy (#0B0B45) background
  YPSA Logo: white, centered, height 60mm
  Bengali program name: Noto Sans Bengali Bold, 24pt, white
  English program name: Open Sans SemiBold, 16pt, rgba(255,255,255,0.8)

MIDDLE (180mm): Photo or illustrated content
  Light navy overlay 20% optional
  Key stat: Open Sans Bold 72pt, #F5C518 (Gold), center-bottom of photo zone

BOTTOM (120mm): White background
  Program details: Open Sans Regular 11pt, #1A1A2E
  YPSA footer band: Navy 30px
    "Young Power in Social Action | ypsa.org.bd" — white 9pt
```

### Bilingual Form Header

```html
<div style="
  background: #0B0B45;
  padding: 16px 24px;
  display: flex;
  align-items: center;
  gap: 16px;
">
  <img src="ypsa-logo-white.png" height="40" alt="YPSA">
  <div>
    <div style="color:white; font-family:'Noto Sans Bengali'; font-size:16px; font-weight:600;">
      [Bengali form title]
    </div>
    <div style="color:rgba(255,255,255,0.75); font-family:'Open Sans'; font-size:13px;">
      [English form title]
    </div>
  </div>
</div>
```

---

## Never Do (YPSA)

* Never use color other than Navy (#0B0B45) for YPSA primary brand elements
* Never omit Bengali text in field-facing materials
* Never stretch or rotate YPSA logo
* Never use YPSA logo on low-contrast backgrounds
