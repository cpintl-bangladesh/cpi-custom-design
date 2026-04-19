# Data Dashboard Theme

**For HIS/M&E dashboards, data visualizations, situation rooms, and real-time monitoring**
*Community Partners International — Bangladesh*

---

## Theme Identity

| Field      | Value                                                      |
| ---------- | ---------------------------------------------------------- |
| Theme Name | CPI Data Dashboard                                          |
| Brand      | Community Partners International                          |
| Context    | NCD Program Monitoring, Coverage Tracking, M&E Reports |

---

## Color Palette (Dark Mode Optimized)

### Background & Surface

| Role            | Name       | Hex         | Usage                        |
| --------------- | ---------- | ----------- | -------------------------- |
| Dashboard BG    | Gunmetal   | `#00272C`  | Main background            |
| Card surface   | Dark Teal  | `#025259`   | Widget cards, panels       |
| Sidebar        | Near Black | `#0F1419`  | Navigation sidebar         |
| Modal/overlay  | Black      | `#000000`  | Modal backgrounds         |

### Text

| Role              | Name        | Hex         | Usage                    |
| ----------------- | ----------- | ----------- | ---------------------- |
| Primary text      | Warm White  | `#F7F9EC` | Headings, key numbers  |
| Secondary text    | Muted       | `#94A3B8` | Labels, meta          |
| Tertiary/hint    | Subtle      | `#64748B`  | Placeholders          |
| Link/interactive | Accent      | `#285CCC`  | Links, buttons        |

### Data Visualization (Program Colors)

| Role                          | Color      | Hex         |
| ---------------------------- | ---------- | ----------- |
| Chart series 1 (Primary)        | Teal       | `#00555A`   |
| Chart series 2                  | Mid Blue   | `#285CCC`   |
| Chart series 3                  | Salmon     | `#FF947A`   |
| Chart series 4                  | Mimosa     | `#FFC94B`   |
| Chart series 5                  | Lavender   | `#D3C5F6`   |
| Chart series 6                  | Xanthous   | `#F7B638`   |

### Status Colors

| Role                          | Color      | Hex         |
| ---------------------------- | ---------- | ----------- |
| Critical/Alert                | Magenta    | `#FF006E`   |
| Warning                     | Sunburst   | `#FFA602`   |
| Good/Success                 | Lemonade   | `#CDF12B`   |
| Neutral/Info                | Mid Blue   | `#285CCC`   |

---

## Typography

| Element           | Font            | Weight | Size    | Color         |
| ----------------- | --------------- | ------ | ------ | ------------- |
| Page title       | Inter           | 700    | 24px   | `#F7F9EC`   |
| Section heading  | Inter           | 600    | 18px   | `#F7F9EC`   |
| Card title      | Inter           | 600    | 16px   | `#F7F9EC`   |
| Stat number     | JetBrains Mono   | 700    | 32-48px| `#F7F9EC`   |
| Stat label      | Inter           | 400    | 13px   | `#94A3B8`    |
| Table cell      | Inter           | 400    | 13px   | `#F7F9EC`   |
| Timestamp      | JetBrains Mono   | 400    | 11px   | `#64748B`    |

---

## Layout Pattern

### Dashboard Container

```
┌─────────────────────────────────────────────────────────────────┐
│ [Sidebar - 240px fixed]  │  [Top bar - 56px fixed]            │
│ ─────────────────    │  ─────────────────────────────────────── │
│                    │                                      │
│  Logo             │  Page title + Filters + User avatar        │
│  ─────────────    │                                      │
│                    │  [Stats row - 100px]                   │
│  Nav items:       │  ┌──────┐┌──────┐┌──────┐┌───────┐    │
│  • Dashboard      │  │ NCD  ││ HCV ││MHPSS ││Total │    │
│  • Patients      │  │ 4560 ││ 890 ││ 234 ││5684  │    │
│  • Reports      │  └──────┘└──────┘└──────┘└───────┘    │
│  • Settings     │                                      │
│                    │  [Charts row - 200px]                    │
│                    │  ┌─────────────────┐┌──────────────┐     │
│                    │  │ Line/Bar chart ││ Pie/Donut   │     │
│                    │  └─────────────────┘└──────────────┘     │
│                    │                                      │
│  [Sync status]    │  [Data table - flexible]                │
│                  │  ───────────────────────────────────────     │
│                  │  ID | Name | Program | Visit | Status      │
│                  │  ───────────────────────────────────────     │
└─────────────────────────────────────────────────────────────────┘
```

### Stat Card Widget

```
┌───────────────────────┐
│  [Icon - top left]    │
│                       │
│  4,523               │  ← JetBrains Mono 36-48px, bold
│  Patients            │  ← Inter 13px, muted
│                       │
│  ████████░░ +12%   │  ← Trend indicator
└───────────────────────┘

Style:
- background: #025259
- border-radius: 8px
- padding: 20px
- border-left: 3px solid [program color]
```

### Chart Container

```
┌───────────────────────────────────┐
│  Monthly Enrollment              │  ← Inter 16px, semi-bold
│  ─────────────────────────────    │
│                                   │
│  [Chart area]                     │
│                                   │
│  [Legend - horizontal]            │
└───────────────────────────────────┘

Style:
- background: #025259
- border-radius: 8px
- padding: 20px
- chart grid: rgba(255,255,255,0.1)
- axis labels: #64748B
```

---

## Responsive Behavior

| Breakpoint | Layout            | Sidebar      |
| ---------- | ---------------- | ------------|
| Desktop >= 1200px | Full 4-column grid | 240px fixed |
| Tablet 768-1199px  | 2-column grid    | Collapsible to icons |
| Mobile < 768px    | Single column   | Hidden, hamburger menu |

---

## Data Table Pattern

```
┌─────────────────────────────────────────────────────────────────┐
│  Patients                                                        │
│  ───────────────────────────���─��───────────────────────────────   │
│  ID       │ Name        │ Program │ Camp │ Last Visit │ Status     │
│  ─────────────────────────────────────────────────────────────   │
│  ZH-001   │ Mohd Rahim │ HCV    │ K1  │ 15 Apr    │ 🟢 Active │
│  ZH-002   │ Fatema    │ CVD/NCD│ K2  │ 12 Apr    │ 🟡 Due    │
│  ZH-003   │ Ahmend    │ MHPSS  │ K1  │ 08 Apr    │ 🔴 Urgent │
└─────────────────────────────────────────────────────────────────┘

Style:
- header: #0F1419 background, Inter 12px bold, uppercase
- row: #025259 background
- alternating row: #00272C background
- hover: rgba(40,92,204,0.2)
- status dot: 8px circle, colored
```

---

## Real-Time Indicators

### Sync Status Badge

```
Online:  ● Green dot + "Synced 2 min ago"
Syncing: ◐ Blue + "Syncing..."
Offline: ○ Purple + "Offline Mode"
Error:   ⚠ Red + "Sync Error"
```

### Live Update Animation

```css
.pulse-indicator {
  animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.5; }
}
```

---

## API Integration Points

When building dashboard components:

1. Fetch data from `/api/v1/dashboard/stats`
2. Program breakdown from `/api/v1/programs`
3. Patient trends from `/api/v1/patients/trends`
4. Use loading skeletons during fetch
5. Cache with 60s TTL for non-critical data

---

## Export Options

| Format | Use Case              | Style                        |
| ------ | ------------------- | ----------------------------|
| PDF    | Donor reports        | Light background, print colors  |
| CSV    | Data analysis      | Raw numbers, no styling        |
| Excel  | M&E analysis      | Formatted with headers       |
| PNG    | Presentations     | 2x resolution for slides   |