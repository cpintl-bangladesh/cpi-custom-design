---
name: cpi-custom-design
description: Apply CPI Bangladesh, YPSA and Zarish Health brand guidelines to presentations and documents, including official colors, fonts, and design standards.
metadata:
  version: 1.0.0
  author: CPI Bangladesh / ZarishSphere Platform
  license: Internal Use — CPI Bangladesh Programs
  tags:
    - brand-guidelines
    - theme-factory
    - humanitarian
    - health
    - bangladesh
---
# CPI Custom Design SKILL

This SKILL package is the **Single Source of Truth (SSOT)** for all visual design decisions
across:

* **CPI Bangladesh** — Community Partners International (implementing partner)
* **YPSA** — Young Power in Social Action (co-implementing partner)
* **Zarish Health / ZarishSphere** — Digital health platform for NCD/FDMN programs

---

## 📁 SKILL Structure

```
CPI-custom-design-SKILL/
├── SKILL.md                         ← You are here (AI reads this first)
├── README.md                        ← Human-readable overview
│
├── brand/
│   ├── CPI_BRAND.md                 ← Full CPI brand specification
│   ├── YPSA_BRAND.md                ← Full YPSA brand specification
│   ├── ZARISH_HEALTH_BRAND.md       ← ZarishHealth brand spec
│   └── EXTENDED_COLORS.md          ← Full extended color palette
│
├── themes/
│   ├── CPI_Theme.md                 ← CPI theme (slides, docs, web)
│   ├── YPSA_Theme.md                ← YPSA theme
│   ├── ZarishHealth_Theme.md        ← Zarish Health digital theme
│   ├── Humanitarian_Theme.md        ← Generic humanitarian/NGO theme
│   └── DataDashboard_Theme.md       ← For HIS/EMR dashboards
│
├── design-philosophy/
│   ├── CPI_Philosophy.md            ← CPI visual philosophy
│   ├── YPSA_Philosophy.md           ← YPSA visual philosophy
│   └── HumanitarianDigital.md       ← Digital health visual philosophy
│
├── web-artifacts/
│   ├── CPI_WebTokens.md             ← CSS variables & design tokens
│   ├── YPSA_WebTokens.md
│   ├── ZarishHealth_WebTokens.md
│   └── UIComponents.md              ← Shared component patterns
│
├── canvas/
│   ├── CPI_CanvasRules.md           ← Rules for posters/print
│   └── YPSA_CanvasRules.md
│
└── examples/
    ├── Letterhead_Spec.md
    ├── Report_Cover_Spec.md
    ├── Dashboard_Spec.md
    └── Email_Template_Spec.md
```

---

## 🤖 AI Usage Instructions

When this SKILL is uploaded to an AI assistant:

1. **Read SKILL.md first** (this file) to understand scope.
2. **For brand decisions** → read `brand/CPI_BRAND.md` or `brand/YPSA_BRAND.md`
3. **For slide/doc themes** → read `themes/CPI_Theme.md`
4. **For web/app design** → read `web-artifacts/CPI_WebTokens.md`
5. **For poster/print art** → read `canvas/CPI_CanvasRules.md`
6. **For digital health UI** → read `themes/ZarishHealth_Theme.md` + `web-artifacts/ZarishHealth_WebTokens.md`

**Always apply these non-negotiable rules:**

* Never alter CPI or YPSA logo colors, proportions, or fonts
* Always use Raleway for external CPI materials; Arial for system/email contexts
* YPSA primary color is Dark Navy Blue `#0B0B45` only
* Zarish Health uses a distinct digital-first palette — never mix with CPI brand
* Ensure WCAG AA accessibility contrast on all digital outputs

---

## 🌍 Program Context

 **Organization** : CPI Bangladesh — implementing Community Partners International programs
 **Location** : Cox's Bazar, Bangladesh (Rohingya Refugee Camps)
 **Programs** : NCD/CVD, HCV, MHPSS, Family Planning, MNCH
 **Population served** : FDMN (Forcibly Displaced Myanmar Nationals / Rohingya) + host community
 **Digital platform** : ZarishSphere EMR — offline-first, zero-cost, open-source

This design system must serve: clinical staff, community health workers (CHW), program managers,
donors, and government stakeholders — across print, digital, and low-bandwidth contexts.
