# ZarishHealth Web Design Tokens & Components

**React + TypeScript + Tailwind CSS patterns**
*For use with web-artifacts-builder SKILL*

---

## Setup Instructions for AI

When building ZarishHealth web artifacts:

1. Import tokens from `ZarishHealth_WebTokens.md`
2. Use Inter font from Google Fonts
3. Noto Sans Bengali for any Bengali text
4. Apply `zh-` prefix to all custom classes
5. Never use excessive gradients, purple glass effects, or Inter + rounded-everything combos
6. Clinical feel > trendy feel

---

## HTML/CSS Boilerplate

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ZarishHealth</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Noto+Sans+Bengali:wght@400;600&family=JetBrains+Mono&display=swap" rel="stylesheet">
  <style>
    /* Paste ZarishHealth tokens here */
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: var(--font-ui); background: var(--zh-bg); color: var(--text-primary); }
  </style>
</head>
```

---

## React Component Library (Key Patterns)

### PatientCard Component

```tsx
interface Patient {
  id: string;
  name: string;
  namebn?: string;
  program: 'hcv' | 'cvd' | 'mhpss' | 'fp' | 'mnch';
  status: 'active' | 'inactive' | 'referred';
  nextVisit?: string;
}

const programColors = {
  hcv:   { bg: '#FFF3CD', text: '#7D5A00', border: '#FFC94B', label: 'HCV' },
  cvd:   { bg: '#FFF0EB', text: '#8B3A24', border: '#FF947A', label: 'CVD/NCD' },
  mhpss: { bg: '#F3EFFE', text: '#3B2A60', border: '#D3C5F6', label: 'MHPSS' },
  fp:    { bg: '#E6F4F4', text: '#025259', border: '#025259', label: 'FP' },
  mnch:  { bg: '#FEF8E7', text: '#7D5A00', border: '#F7B638', label: 'MNCH' },
};

function PatientCard({ patient }: { patient: Patient }) {
  const prog = programColors[patient.program];
  return (
    <div style={{
      background: '#fff',
      borderLeft: `4px solid ${prog.border}`,
      borderRadius: '6px',
      padding: '16px',
      boxShadow: '0 1px 3px rgba(0,39,44,0.1)',
      marginBottom: '8px',
    }}>
      <div style={{ display: 'flex', justifyContent: 'space-between', alignItems: 'flex-start' }}>
        <div>
          <div style={{ fontWeight: 600, fontSize: '16px', color: '#00272C' }}>{patient.name}</div>
          {patient.namebn && (
            <div style={{ fontFamily: "'Noto Sans Bengali'", fontSize: '14px', color: '#4A5568' }}>
              {patient.namebn}
            </div>
          )}
          <div style={{ fontSize: '12px', color: '#718096', marginTop: '4px' }}>ID: {patient.id}</div>
        </div>
        <span style={{
          background: prog.bg, color: prog.text,
          border: `1px solid ${prog.border}`,
          padding: '2px 8px', borderRadius: '4px',
          fontSize: '11px', fontWeight: 700,
          textTransform: 'uppercase', letterSpacing: '0.5px'
        }}>
          {prog.label}
        </span>
      </div>
      {patient.nextVisit && (
        <div style={{ marginTop: '8px', fontSize: '13px', color: '#285CCC' }}>
          📅 Next: {patient.nextVisit}
        </div>
      )}
    </div>
  );
}
```

### StatCard Component

```tsx
function StatCard({ value, label, program, trend }: {
  value: string | number;
  label: string;
  program?: keyof typeof programColors;
  trend?: 'up' | 'down' | 'stable';
}) {
  const trendIcon = trend === 'up' ? '↑' : trend === 'down' ? '↓' : '→';
  const trendColor = trend === 'up' ? '#38A169' : trend === 'down' ? '#FF006E' : '#718096';
  return (
    <div style={{
      background: '#fff',
      borderRadius: '6px',
      padding: '20px',
      boxShadow: '0 1px 3px rgba(0,39,44,0.1)',
      borderTop: program ? `3px solid ${programColors[program].border}` : '3px solid #00555A',
    }}>
      <div style={{ fontSize: '36px', fontWeight: 700, color: '#00272C', fontFamily: 'JetBrains Mono' }}>
        {value}
        {trend && <span style={{ fontSize: '16px', color: trendColor, marginLeft: '8px' }}>{trendIcon}</span>}
      </div>
      <div style={{ fontSize: '13px', color: '#4A5568', marginTop: '4px' }}>{label}</div>
    </div>
  );
}
```

### OfflineBanner Component

```tsx
function OfflineBanner({ isOnline }: { isOnline: boolean }) {
  if (isOnline) return null;
  return (
    <div style={{
      background: '#3B2A60',
      color: '#F7F9EC',
      padding: '8px 16px',
      textAlign: 'center',
      fontSize: '13px',
      fontFamily: 'Inter, sans-serif',
      fontWeight: 500,
    }}>
      ⚡ Offline Mode — Data saved locally. Will sync when connected.
    </div>
  );
}
```

### AppLayout Component

```tsx
function AppLayout({ children, sidebarOpen }: { children: React.ReactNode; sidebarOpen: boolean }) {
  return (
    <div style={{ display: 'flex', height: '100vh', background: '#F7F9EC' }}>
      {/* Sidebar */}
      <aside style={{
        width: sidebarOpen ? '240px' : '64px',
        background: '#00272C',
        color: '#F7F9EC',
        transition: 'width 200ms ease',
        flexShrink: 0,
        display: 'flex',
        flexDirection: 'column',
      }}>
        <div style={{ padding: '16px', borderBottom: '1px solid rgba(247,249,236,0.1)' }}>
          {sidebarOpen ? (
            <span style={{ fontWeight: 700, color: '#F7F9EC' }}>
              <span style={{ color: '#00B4C4' }}>zarish</span>health
            </span>
          ) : (
            <span style={{ color: '#00B4C4', fontWeight: 700 }}>Z</span>
          )}
        </div>
        {/* Nav items here */}
      </aside>
      {/* Main */}
      <main style={{ flex: 1, overflow: 'auto' }}>
        {children}
      </main>
    </div>
  );
}
```

---

## CPI Web Component Patterns

### CPI Report Header

```html
<header style="
  background: #41273B;
  padding: 24px 40px;
  display: flex;
  align-items: center;
  justify-content: space-between;
">
  <!-- CPI Logo (white version) -->
  <img src="cpi-logo-white.png" alt="CPI" height="40">
  <div style="color: #D0C4C5; font-family: Raleway, sans-serif; font-size: 14px; text-align: right;">
    <div style="color: white; font-weight: 600;">NCD Program Report</div>
    <div>Cox's Bazar, Bangladesh | Q1 2026</div>
  </div>
</header>
<!-- Red rule -->
<div style="height: 4px; background: #D91E4D;"></div>
```

### CPI Stat Block

```html
<div style="
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 16px;
  padding: 32px 40px;
  background: #F5F3F4;
">
  <div style="text-align: center;">
    <div style="font-size: 48px; font-weight: 700; color: #D91E4D; font-family: Raleway, sans-serif;">4,523</div>
    <div style="font-size: 14px; color: #948794; font-family: Raleway, sans-serif;">Patients Served</div>
  </div>
  <!-- repeat for other stats -->
</div>
```

---

## YPSA Web Component Patterns

### YPSA Nav Bar

```html
<nav style="
  background: #0B0B45;
  padding: 16px 32px;
  display: flex;
  align-items: center;
  gap: 24px;
">
  <img src="ypsa-logo-white.png" alt="YPSA" height="48">
  <div style="height: 32px; width: 1px; background: rgba(255,255,255,0.2);"></div>
  <span style="
    font-family: 'Noto Sans Bengali', sans-serif;
    color: rgba(255,255,255,0.9);
    font-size: 16px;
  ">ইপসা স্বাস্থ্য কার্যক্রম</span>
</nav>
```

---

## Accessibility Checklist

Before shipping any web artifact:

* [ ] All text meets 4.5:1 contrast ratio (AA)
* [ ] Interactive elements min 44×44px touch target
* [ ] Form labels associated with inputs (`for`/`id` pairing)
* [ ] Bengali text uses `lang="bn"` attribute
* [ ] Images have meaningful `alt` text
* [ ] Tab order logical (left-to-right, top-to-bottom)
* [ ] Offline state clearly communicated
* [ ] Error states use both color AND text (not color alone)
* [ ] Focus ring visible on all interactive elements (`outline: 2px solid #00555A`)
