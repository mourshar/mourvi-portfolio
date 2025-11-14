# Portfolio Redesign Progress Document

## Project Overview

Created an alternate portfolio version in `/Users/mourvi/portfolio/alt/` based on the design reference from https://www.wallofportfolios.in/portfolios/anurag-goyal/

## Project Goals

- Create a modern, side-by-side layout portfolio
- Integrate company logos prominently
- Make the design mobile responsive
- Use clean system fonts matching the original portfolio
- Create a one-page hero section that fits viewport without scrolling
- Showcase work at Meta, Disney, Sesame Workshop, IBM Research, Byju's, and BigFatPhoenix Interactive

## File Structure

```
/Users/mourvi/portfolio/alt/
├── index.html          # Main homepage with side-by-side hero/about layout
├── styles.css          # Complete styling for alternate portfolio
└── PROGRESS.md         # This document

/Users/mourvi/portfolio/
├── fairside-stories.html      # Updated with simplified content structure
├── meta.html                  # New page for Meta AI Characters work
├── projects.html              # Updated with Meta project, removed Disney Smart Beginnings & Afterschool STEM
├── first8studios.html         # Renamed to "WGBH: Early Math with Gracie and Friends"
├── learn-to-read.html         # Updated with images
├── sesame-board-games.html    # Updated with images
└── images/
    ├── cover/                 # Profile photo
    ├── Meta/                  # Meta project images
    ├── Fairside Stories/      # Fairside project images
    ├── early math with gracie and friends/  # Early math game images
    ├── Learn to Read/         # Literacy program images
    ├── sesame street board games and floor games/  # Board game images
    └── logos/                 # Company logos (Meta, Disney, Sesame, IBM, Byju's, Harvard)
```

## Key Design Decisions

### Layout
- **Side-by-side hero/about**: Left column (400px) contains hero content and company logos, right column contains about text
- **Sticky left column**: Hero section stays visible while scrolling on desktop (position: sticky; top: 100px)
- **One-page hero**: Hero section fits in viewport with `min-height: calc(100vh - 80px)`
- **Scrollable about section**: Right column has max-height and overflow-y: auto

### Typography
- **System fonts**: `-apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica Neue', Arial, sans-serif`
- **Base font size**: 16px
- **Profile title size**: 1.35rem ("Creative and Content Strategist")
- **Font smoothing**: Applied for better rendering

### Visual Elements
- **Profile photo**: 160px circular image with shadow
- **Company logos**: 140px max-height, displayed in grid (3 columns desktop, 2 tablet, 1 mobile)
- **Logo styling**: Full color (no greyscale), minimal spacing between logos
- **Brand names in bold**: Only Meta, Disney, Sesame Workshop, IBM Research, BigFatPhoenix Interactive

### Responsive Design
Breakpoints:
- 1200px: Adjust container width
- 1024px: Switch to single column, remove sticky positioning
- 768px: Adjust logo grid to 2 columns
- 480px: Single column logos, smaller typography

## Content Changes

### Alt Portfolio (index.html)

**Hero Section:**
- Title: "Creative and Content Strategist"
- Tagline: "Building scalable content systems and stories that power AI products, games, and learning experiences"
- Profile photo: `/images/cover/26230184-10102295368335862-144264102828286482-n.jpg`

**Company Logos (in order):**
Row 1: Meta, Sesame Workshop, IBM Research
Row 2: Byju's, Harvard University

**About Section:**
- 4 paragraphs covering 15 years of experience
- Work at Meta (AI character products)
- Previous work at Disney, Sesame Workshop, IBM Research, BigFatPhoenix Interactive
- Recognition and impact highlights

**Navigation:**
- Work (links to #work)
- About (links to #about)
- Contact (links to #contact)
- LinkedIn (external link to https://www.linkedin.com/in/mourvi/)

**Selected Work Section:**
Featured projects with thumbnails and descriptions:
1. Meta AI Characters (Featured project)
2. Fairside Stories
3. IBM Watson & Sesame Street
4. Disney Imagicademy
5. Disney Byju's Early Learn
6. Sesame Street: Radiophone
7. Learn to Read, Read to Learn

**Contact Section:**
- Heading: "Collaborate with me"
- Email: mourvi@gmail.com

### Main Portfolio Updates

#### Removed Sections:
- Disney Smart Beginnings
- Afterschool STEM (Sesame Schoolhouse)

#### Added Sections:
- Meta AI Characters (new page: meta.html)

#### Updated Pages:

**fairside-stories.html:**
- Simplified structure with 4 main sections
- My Role: 5 focused bullet points (Studio Founder, Systems Design, Creative Lead, Co-Design Pioneer, Partnerships)
- Why It's Unique: 3 key differentiators
- Recognition & Press: Consolidated paragraph
- Sidebar intact with Impact metrics and awards

**first8studios.html:**
- Renamed to "WGBH: Early Math with Gracie and Friends"
- Fixed image paths to `/images/early math with gracie and friends/`

**projects.html:**
- Meta AI Characters added as first project
- Updated thumbnails for all projects
- Removed deleted projects

## Technical Implementation

### CSS Grid Layout
```css
.hero-about-container {
    display: grid;
    grid-template-columns: 400px 1fr;
    gap: 4rem;
    align-items: start;
}
```

### Sticky Positioning
```css
.hero-left {
    position: sticky;
    top: 100px;
}
```

### Viewport Height Calculation
```css
.hero-about-section {
    min-height: calc(100vh - 80px);
    display: flex;
    align-items: center;
}
```

### Logo Grid
```css
.logos-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0.4rem;
    padding: 0.4rem;
}

.logo-item img {
    max-height: 140px;
}
```

### Mobile Responsive
```css
@media (max-width: 1024px) {
    .hero-about-container {
        grid-template-columns: 1fr;
        gap: 2rem;
    }

    .hero-left {
        position: static;
    }
}
```

## Iterations and Refinements

### Phase 1: Initial Creation
- Created alt folder structure
- Built side-by-side layout
- Integrated company logos
- Added all content sections

### Phase 2: Content Refinement
- Removed "15 years" experience badge
- Removed achievements metrics (100→1,000, $1.3M funding, etc.)
- Updated about section text (shorter version)
- Changed title from "Experience Designer & Product Innovator" to "Creative and Content Strategist"
- Removed "Experience Includes" heading, then added back just "Experience"

### Phase 3: Visual Adjustments
- Increased logo size from 50px → 80px → 200px → 140px (final)
- Removed greyscale filter from logos
- Reduced spacing between logos dramatically
- Increased profile photo from 120px → 160px
- Increased title font size to 1.35rem

### Phase 4: Typography
- Initially tried Inconsolata monospace font
- Switched to system fonts matching original portfolio
- Increased base font size from 14px to 16px
- Added font smoothing

### Phase 5: Navigation & Contact
- Added LinkedIn link to navigation
- Changed contact heading to "Collaborate with me"
- Added email link (mourvi@gmail.com)
- Removed descriptive contact text

### Phase 6: Mobile Responsiveness
- Removed name under photo (kept only in header)
- Removed "San Francisco Bay Area" location
- Made hero section fit viewport without scrolling
- Enhanced mobile breakpoints and layouts

### Phase 7: Bold Text Refinement
- First iteration: Made all achievements, products, brands bold
- Final iteration: Only brand names bold (Meta, Disney, Sesame Workshop, IBM Research, BigFatPhoenix Interactive)

## Issues Resolved

### Issue 1: First8Studios Images Not Showing
- **Problem**: Images looking in wrong folder path
- **Solution**: Updated paths to `/images/early math with gracie and friends/`

### Issue 2: Logo Identification
- **Problem**: Confusion about which logo file was Harvard vs Disney
- **Solution**: Identified 6c895... as Harvard University logo and reordered accordingly

### Issue 3: Logo Size Not Changing
- **Problem**: Increasing max-height didn't visually increase logos
- **Solution**: Reduced spacing (gap, padding) while increasing max-height to 140px

### Issue 4: Font Reference
- **Problem**: Couldn't extract fonts from external website
- **Solution**: Used system font stack from original portfolio instead

## Current State

### Completed Features:
✅ Alt portfolio with side-by-side layout
✅ Mobile responsive design
✅ Company logos prominently displayed
✅ One-page hero section
✅ System fonts applied
✅ All content updated per user specifications
✅ Fairside Stories page simplified
✅ Meta project page created
✅ Navigation with LinkedIn link
✅ Contact section with email

### Design Specifications:
- Profile photo: 160px
- Title font size: 1.35rem
- Logo max-height: 140px
- Left column width: 400px
- Hero section: calc(100vh - 80px)
- Base font: 16px system fonts
- Navigation height: 80px

### Color Scheme:
- Hero background: Linear gradient (135deg, #f8f9fa 0%, #e9ecef 100%)
- Primary text: #333
- Secondary text: #666
- Links: #0066cc (hover: #0052a3)
- Logos background: White with subtle shadow

### Logo Order:
Row 1: Meta, Sesame Workshop, IBM Research
Row 2: Byju's, Harvard University

## Next Steps (If Needed)

Potential future enhancements:
- Update other project pages to match Fairside Stories simplified structure
- Add more interactive elements or animations
- Optimize images for web performance
- Add dark mode toggle
- Implement analytics tracking
- Add more projects to Selected Work section

## Notes for Future Development

- Logo files are in `/Users/mourvi/portfolio/images/logos/`
- Main portfolio files are in `/Users/mourvi/portfolio/`
- Alt portfolio uses relative paths to access images: `../images/`
- All links to project pages use relative paths: `../meta.html`, `../fairside-stories.html`, etc.
- System uses standard HTML5 and CSS3, no frameworks or dependencies
- Mobile-first responsive design approach
- Semantic HTML structure for accessibility

## User Preferences

- Clean, minimal design
- No emojis
- System fonts (no custom web fonts)
- Brand names in bold only
- Professional tone
- One-page hero section
- Company logos in full color
- Mobile responsive required
- Email contact preferred over forms

---

**Last Updated**: Session ending on conversation about Fairside Stories content update
**Portfolio Location**: `/Users/mourvi/portfolio/alt/`
**Status**: Production ready
