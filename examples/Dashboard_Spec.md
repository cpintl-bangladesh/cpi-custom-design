# Dashboard Specification

**For ZarishHealth NCD Program Dashboards**
*Ready-to-use dashboard templates*

---

## Dashboard Types

### 1. Program Overview Dashboard

**A4 Landscape (297 × 210mm)**

#### Header (25mm)

```
┌─────────────────────────────────────────────────────────────────┐
│ [ZH Gun Metal #00272C background]                          │
│  [zarish health wordmark - left]     │  [Title - center]     │
│  [Period | Facility - right]                           │
└─────────────────────────────────────────────────────────────────┘
```

#### KPI Row (40mm)

4 equal-width cards:

| Metric     | Label                 | Style                    |
| ---------- | -------------------- | ------------------------|
| Total Patients | Patients enrolled | ZH Teal top border      |
| Active     | On active treatment | ZH Blue top border       |
| Due        | Follow-up due       | Yellow warning border   |
| New        | New this month      | Green success border   |

Each card:
- Large number: JetBrains Mono 32pt, bold, ZH Gun Metal
- Label: Inter 12pt, muted
- Card: white background, 6px radius, subtle shadow

#### Charts Section (100mm)

*Left*: Line/area chart - monthly trend
- X-axis: months
- Y-axis: patient count
- Lines: per program (HCV, CVD, MHPSS, etc.)

*Right*: Donut chart - program distribution
- Segments: Program color palette
- Center: Total number

#### Table Section (variable)

Compact patient table:
- Columns: ID | Name | Program | Camp | Last Visit | Status
- Left border: 3px program color
- Alternating row colors
- Status badges: colored dots

---

## 2. Clinical Dashboard

**For clinical staff - focus on action items**

### Priority Sections

1. **Today's Actions** (top)
   - Patients with visits due today
   - Overdue patients
   - Urgent flags

2. **Quick Stats**
   - Active patients by program
   - This week's registrations
   - Pending referrals

3. **Recent Activity**
   - Last 10 patient encounters
   - New registrations today

### Clinical Dashboard Layout

```
┌────────────────────────────────────────────────────────┐
│ [Top bar — user, facility, sync status]              │
├────────────────────────────────────────────────────────┤
│ [Alert Banner — if any urgent items]              │
├────────────────────────────────────────────────────────┤
│ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐  │
│ │ Today's  │ │ Overdue  │ │ Urgent  │ │ New    │  │
│ │ Visits   │ │         │ │         │ │ Today   │  │
│ │   12    │ │    3    │ │    1    │ │    5    │  │
│ └──────────┘ └──────────┘ └──────────┘ └──────────┘  │
├────────────────────────────────────────────────────────┤
│  Overdue Patients                    View All →        │
│  ─���──────────────────────────────────────────────   │
│ [Patient rows with overdue indicator]                 │
├────────────────────────────────────────────────────────┤
│  Recent Activity                                   │
│  ───────────────────────────────────────────────   │
│ [Timeline of recent encounters]                      │
└────────────────────────────────────────────────────────┘
```

---

## 3. M&E Summary Dashboard

**For donors/managers - aggregate metrics**

### Metrics

| Metric                | Definition                    |
| -------------------- | ---------------------------- |
| Total enrolled       | Patients ever enrolled         |
| Active on treatment  | With visit in last 90 days     |
| Treatment coverage  | Active / Target × 100         |
| Retention rate      | Completed f-up / Expected       |
| Lost to follow-up   | No visit in 90+ days        |

### Program Breakdown Table

```
┌───────────────────────────────────────────────────────────┐
│ Program │ Enrolled │ Active │ Coverage │ Retention │ LTFU  │
├───────────────────────────────────────────────────────────┤
│ HCV     │   1,234 │  890   │   72%   │    85%   │  12% │
│ CVD/NCD │   2,456 │ 1,890  │   68%   │    78%   │  15% │
│ MHPSS   │    567  │   423  │   75%   │    82%   │   8% │
│ FP      │   3,890 │ 3,123  │   80%   │    91%   │   5% │
│ MNCH    │   1,234 │   890  │   72%   │    88%   │   7% │
└───────────────────────────────────────────────────────────┘
```

---

## 4. Camp Dashboard

**For camp-level overview**

### Layout

```
┌─────────────────────────────────────────────────┐
│ [Camp name] Dashboard              [Period]    │
│ ────────────────────────────────────────────   │
│  Total Patients: 4,523                       │
├──────────────────────────────────────────────┤
│  ┌────────┐ ┌────────┐ ┌────────┐ ┌────────┐ │
│  │ HCV  │ │ CVD │ │MHPSS│ │ FP   │ │
│  │ 890 │ │1234 │ │ 234 │ │567  │ │
│  └────────┘ └────────┘ └────────┘ └────────┘ │
├──────────────────────────────────────────────┤
│  Coverage by Block                           │
│  [Bar chart by camp/block]                │
├──────────────────────────────────────────────┤
│  Top Facilities (by volume)              │
│  [Facility list with patient counts]      │
└──────────────────────────────────���─��────────────┘
```

---

## Export Options

| Format    | Use Case                    | Notes                    |
| --------- | -------------------------- | ------------------------|
| PDF       | Reporting, presentations  | 2x resolution when text |
| Excel     | Data analysis             | Raw data + headers      |
| CSV       | External analysis        | No formatting          |
| PNG       | Slides                   | 1920×1080 minimum     |