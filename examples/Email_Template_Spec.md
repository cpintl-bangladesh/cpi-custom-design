# Email Template Specification

**Ready-to-use email templates for CPI Bangladesh**
*For official correspondence and program communications*

---

## CPI Bangladesh Official Email Header

### Structure

```
┌──────────────────────────────────────────────────────────┐
│ [CPI Red band — full width, 4px height]                  │
├──────────────────────────────────────────────────────────┤
│ [CPI Logo (white) — left, 36px height]                  │
│ [Optional: "Community Partners International"]          │
│                        │ [Program name — right aligned]   │
├──────────────────────────────────────────────────────────┤
│                                                        │
│                    EMAIL CONTENT                          │
│                    (Arial 12pt, #2D2926)              │
│                                                        │
│                                                        │
└──────────────────────────────────────────────────────────┤
│ [CPI Red 1pt rule]                                     │
│ [Footer info — 10pt, #948794]                           │
│  CPI Bangladesh address | phone | email | website      │
└──────────────────────────────────────────────────────────┘
```

### Technical Specs

| Element       | Value                                      |
| ------------- | ------------------------------------------ |
| Width         | 600px (max)                               |
| Margins       | 20px all sides                            |
| Header height | 100px                                     |
| Footer height | 60px                                      |
| Font body     | Arial 12pt                                |
| Color body    | #2D2926                                   |
| Link color   | #D91E4D                                   |

---

## Email Template Variants

### 1. Welcome Email

**For new staff, volunteers, partners**

```
Subject: Welcome to CPI Bangladesh — [Name]

Hi [Name],

Welcome to Community Partners International Bangladesh.

[Optional: Brief program/role introduction]

[3-4 sentences about CPI mission in Bangladesh]

What's next:
• [Action item 1]
• [Action item 2]

Questions? Reply to this email.

Best regards,
[Sender Name]
[Title]
CPI Bangladesh
```

### 2. Program Update Email

**For stakeholders, partners**

```
Subject: [Program Name] Update — [Month Year]

Dear [Name/Team],

[Brief intro paragraph — 2-3 sentences]

Key Highlights:
• [Achievement or update 1]
• [Achievement or update 2]
• [Achievement or update 3]

Looking Ahead:
• [Upcoming activity 1]
• [Upcoming activity 2]

For questions, contact [email]

Warm regards,
[Name]
[Title]
CPI Bangladesh
```

### 3. Meeting Invitation

```
Subject: Meeting Invitation: [Topic] — [Date/Time]

Dear [Name/Team],

You are invited to attend:

[Meeting title]
[Date, Time]
[Location / Virtual link]

Agenda:
1. [Item]
2. [Item]
3. [AOB]

Please confirm attendance by [date].

Best,
[Name]
[Title]
CPI Bangladesh
```

### 4. Field Visit Notification

**For visitor/staff coordination**

```
Subject: Field Visit — [Camp/Location] on [Date]

Dear Team,

[Staff member name] will be visiting [Camp/Facility] on [Date].

Purpose:
• [Reason 1]
• [Reason 2]

Logistics:
• Travel: [Transport details]
• [Meet at] / [Pick up details]
• [Items to prepare]

Please coordinate with [Contact] for logistics.

Thanks,
[Name]
```

---

## Email Signature (Staff)

### Standard Template

```html
<table cellpadding="0" cellspacing="0" style="font-family:Arial,sans-serif;font-size:12px;color:#2D2926;max-width:500px;">
  <tr>
    <td style="padding-bottom:8px;border-bottom:2px solid #D91E4D;">
      <img src="https://cpintl.org/logo.png" height="36" alt="CPI">
    </td>
  </tr>
  <tr>
    <td style="padding-top:8px;">
      <strong style="font-size:14px;color:#41273B;">[Full Name]</strong><br>
      <span style="color:#948794;">[Job Title] | [Program/Unit]</span><br>
      <br>
      <span>Phone: +880 [number]</span><br>
      <span>Email: <a href="mailto:[email]" style="color:#D91E4D;">[email]</a></span><br>
      <span>Web: <a href="https://www.cpintl.org" style="color:#D91E4D;">www.cpintl.org</a></span><br>
      <br>
      <span style="color:#948794;font-size:11px;">
        Community Partners International Bangladesh<br>
        Rabbani Building (4th Floor), Kurushkul Bypass Road<br>
        Cox's Bazar, Bangladesh
      </span>
    </td>
  </tr>
</table>
```

### Signature Rules

* Use Arial 12pt
* Keep to 6 lines max
* Include CPI logo image (hosted)
* Use CPI colors for links
* Phone in Bangladesh format: +880 15XX

---

## HTML Email Best Practices

### Do

* Use table-based layout for Outlook compatibility
* Use inline CSS (no external stylesheets)
* Define all colors explicitly
* Use 600px max width
* Test in multiple email clients
* Include plain-text version

### Don't

* Don't use background images
* Don't use complex CSS (flexbox, grid)
* Don't use custom fonts (Arial fallback)
* Don't use JavaScript
* Don't rely on images (include alt text)
* Don't forget mobile-responsive

---

## Design Tokens for Email

```css
/* Email-specific tokens */
--email-width: 600px;
--email-bg: #FFFFFF;
--email-text: #2D2926;
--email-link: #D91E4D;
--email-accent: #41273B;
--email-muted: #948794;
--email-border: 2px solid #D91E4D;
```

---

## YPSA Email Adaptation

Replace CPI header with YPSA:

```
┌────────────────────────────────────┐
│ [YPSA Navy band full width]       │
│  [YPSA Logo (white)]              │
│  [Program name]                  │
├────────────────────────────────────┤
│                                    │
│       EMAIL CONTENT                │
│       Arial 12pt, #1A1A2E           │
│                                    │
├────────────────────────────────────┤
│ [YPSA Navy 1pt rule]              │
│ [Footer: address | contact]       │
└────────────────────────────────────┘
```

Use Bengali in header when appropriate:
```html
<div style="font-family:'Noto Sans Bengali',Arial,sans-serif;font-size:14px;">
  [Bengali text]
</div>
```