# CPI Canvas & Print Design Rules

**For posters, fact sheets, banners, social media, and printed materials**

---

## CPI Visual Philosophy in Practice

Reference: `design-philosophy/CPI_Philosophy.md` — "Dignified Presence"

### Canvas Design Principles (CPI)

1. **Community at center** — photography dominates over decoration
2. **Generous whitespace** — let content breathe
3. **Restrained palette** — maximum 3 colors per design (from CPI brand)
4. **CPI Red as life force** — use for the single most important element
5. **Typography scales with importance** — do not use more than 3 type sizes
6. **Logo is small** — it signs the work, it does not dominate it
7. **Never decorative for its own sake** — every shape must serve a communication purpose

---

## Poster Design Templates

### Template 1: Impact Poster (A3 / A2)

```
CANVAS: A3 — 297mm × 420mm, portrait

TOP ZONE (100mm):
  Background: CPI Red (#D91E4D) or CPI Purple (#41273B)
  CPI Logo: White version, top-left, 40mm wide, 15mm from edges
  Headline text: Raleway Bold, 32-40pt, white
  CPI leaf watermark: right side, 46% opacity grey

MIDDLE ZONE (220mm):
  Full-bleed photograph
  CPI Red color overlay: 40% opacity (optional)
  Key statistic overlay: Raleway Bold 72pt, white, bottom-left of photo zone

BOTTOM ZONE (100mm):
  Background: White
  Supporting text: Raleway Regular 11pt, CPI Black
  CPI Red horizontal rule: 2pt, full width
  Contact/website: Raleway Regular 9pt, CPI Warm Gray, bottom
```

### Template 2: Fact Sheet (A4 one-pager)

```
CANVAS: A4 — 210mm × 297mm, portrait
Margins: 15mm all sides

HEADER (50mm):
  CPI Purple background
  CPI Logo: white, top-left
  Program name: Raleway Light 12pt, white, below logo
  Title: Raleway Bold 24pt, white
  Subtitle: Raleway Light 16pt, CPI Light Gray

BODY:
  2-column grid (85mm each, 10mm gutter)
  Section headings: Raleway SemiBold 14pt, CPI Red
  Body: Raleway Regular 10pt, CPI Black
  Key stats: Box with CPI Purple background, white Raleway Bold 36pt number
  Bullet points: CPI Red square marker (not default bullet)

FOOTER:
  CPI Red 1.5pt rule
  CPI logo small + website + contact: Raleway Regular 8pt, CPI Warm Gray
```

### Template 3: Social Media Card (1080×1080px)

```
CANVAS: 1080 × 1080px square

Background: CPI Purple (#41273B)

Elements:
  Top: CPI logo white, left, 120px wide
  Center: Large statistic or quote (Raleway Bold 80-100pt, white/CPI Red)
  Sub-text: Raleway Regular 28pt, CPI Light Gray
  Bottom strip: CPI Red 60px band
    - "Empower communities. Transform lives." white Raleway Medium 20pt
    - cpintl.org | white Raleway Regular 18pt
  Right watermark: CPI leaf, 15% opacity, grey on multiply
```

### Template 4: Co-branded Banner (CPI + YPSA)

```
CANVAS: 1200 × 300px horizontal

Left half: CPI Purple background
  CPI Logo: white, centered

Divider: Thin white line 1px, vertical center

Right half: YPSA Navy (#0B0B45) background
  YPSA Logo: white, centered

Bottom band: White 40px
  "Community Partners International & Young Power in Social Action"
  Raleway/Open Sans Regular 10pt, CPI Black, centered
```

---

## Required File Formats for Delivery

| Output Type         | Format     | Resolution | Color Mode |
| ------------------- | ---------- | ---------- | ---------- |
| Print poster        | PDF (CMYK) | 300dpi     | CMYK       |
| Digital web graphic | PNG        | 72-150dpi  | RGB/sRGB   |
| Social media        | PNG or JPG | 72dpi      | sRGB       |
| Editable template   | SVG or AI  | Vector     | RGB        |
| Email header        | PNG        | 150dpi     | sRGB       |

---

## Camp-Context Design Adaptations

When creating materials for **Rohingya camp contexts** (field-level distribution):

1. **Use pictograms** over text-heavy content where possible
2. **Bangla script prominently** — equal or larger than English
3. **Avoid blue as primary** (associated with UNHCR, may confuse program identity)
4. **High contrast** — materials may be photocopied in black & white
5. **Large touch / reading areas** — assume low literacy + poor lighting
6. **Minimal color printing version** always as fallback (2-color version)
7. **Culturally appropriate imagery** — modest dress, no religious iconography
8. **Include CPI Bangladesh contact** — not US/Myanmar addresses

---

## Python Script Template (for programmatic poster generation)

```python
# Requires: Pillow, reportlab
from reportlab.lib.pagesizes import A4
from reportlab.lib.colors import HexColor
from reportlab.pdfgen import canvas

# CPI Brand Colors
CPI_PURPLE = HexColor('#41273B')
CPI_RED    = HexColor('#D91E4D')
CPI_GRAY   = HexColor('#948794')
CPI_WHITE  = HexColor('#FFFFFF')
CPI_BLACK  = HexColor('#2D2926')

def create_cpi_fact_sheet(output_path, title, stats, body_text):
    c = canvas.Canvas(output_path, pagesize=A4)
    w, h = A4

    # Header band
    c.setFillColor(CPI_PURPLE)
    c.rect(0, h - 120, w, 120, fill=1, stroke=0)

    # Title
    c.setFillColor(CPI_WHITE)
    c.setFont("Helvetica-Bold", 24)
    c.drawString(40, h - 70, title)

    # Red rule
    c.setStrokeColor(CPI_RED)
    c.setLineWidth(2)
    c.line(0, h - 125, w, h - 125)

    # Body text area
    c.setFillColor(CPI_BLACK)
    c.setFont("Helvetica", 10)
    y = h - 160
    for line in body_text.split('\n'):
        c.drawString(40, y, line)
        y -= 15
        if y < 60:
            break

    # Footer
    c.setStrokeColor(CPI_RED)
    c.setLineWidth(1)
    c.line(0, 50, w, 50)
    c.setFont("Helvetica", 8)
    c.setFillColor(CPI_GRAY)
    c.drawCentredString(w/2, 35, "www.cpintl.org | info@cpintl.org | Cox's Bazar, Bangladesh")

    c.save()
```
