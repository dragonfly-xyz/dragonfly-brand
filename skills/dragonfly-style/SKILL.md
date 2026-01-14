---
name: dragonfly-style
description: Apply Dragonfly brand style guidelines to documents, websites, CSS, and digital materials. Use when user asks to style content with Dragonfly branding, create Dragonfly-styled UI, or needs color/typography/logo specs for the Dragonfly crypto investment fund brand.
---

# Dragonfly Brand Style Skill

Apply the Dragonfly brand style guidelines to documents, websites, and digital materials.

## Brand Overview

**Dragonfly** is a leading global crypto investment fund with the tagline "Global From Day One" (早有蜻蜓). The brand essence is the "Cryptonic Ideal" - seeking additional perspectives, subverting accepted assumptions, and pursuing new epiphanies.

## Instructions

When the user asks you to style content with the Dragonfly brand, apply these guidelines:

---

## Color System

### Primary Colors
| Color | Hex | RGB | Usage |
|-------|-----|-----|-------|
| **Black** | `#000000` | 0, 0, 0 | Primary background, dominant color |
| **Grey** | `#F2F2F2` | 242, 242, 242 | Light backgrounds, contrast |
| **Dragon Blood Orange** | `#FA4C14` | 250, 76, 20 | Accent color for emphasis |

### Tertiary Colors (use sparingly)
| Color | Hex | RGB |
|-------|-----|-----|
| **Pink** | `#EC39B6` | 236, 57, 182 |
| **Blue** | `#5014FA` | 80, 20, 250 |

### Color Pairing Rules
- Lead with Black as the dominant color
- Use Dragon Blood Orange and Grey as accents
- Tertiary colors (Pink, Blue) should be used rarely and never dominantly
- Ensure WCAG accessibility: minimum 4.5:1 contrast ratio for text
- Acceptable pairings: Black/White, Black/Orange, Grey/Black, Grey/Orange

---

## Typography

### Primary Typeface: Non Natural Grotesk
A hard-cut geometric sans with harsh right angles and sharp apexes balanced by rounded geometric characters.

**Font Stack (web fallback):**
```css
font-family: 'Non Natural Grotesk', 'Inter', 'Helvetica Neue', Arial, sans-serif;
```

### Secondary Typeface: Mondwest
A pixelated neo-classical serif for alt-headers and stylistic variety. Use sparingly, never in body copy.

**Font Stack (web fallback):**
```css
font-family: 'Mondwest', 'Georgia', serif;
```

### Monospace: Non Natural Mono
For ASCII art, eyebrows, and detail information.

**Font Stack (web fallback):**
```css
font-family: 'Non Natural Mono', 'SF Mono', 'Monaco', 'Consolas', monospace;
```

### Font Files & @font-face Implementation

When building websites, use @font-face declarations to load the brand fonts. The font files are available in woff2 format.

**Required font files:**
- `NONNaturalGrotesk-Regular.woff2` (weight: 400)
- `NONNaturalGrotesk-Bold.woff2` (weight: 700)
- `NONNaturalMono-Light.woff2` (weight: 300)

**@font-face CSS declarations:**
```css
/* Non Natural Grotesk - Primary Font */
@font-face {
  font-family: 'Non Natural Grotesk';
  src: url('fonts/NONNaturalGrotesk-Regular.woff2') format('woff2');
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}
@font-face {
  font-family: 'Non Natural Grotesk';
  src: url('fonts/NONNaturalGrotesk-Bold.woff2') format('woff2');
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

/* Non Natural Mono - Monospace Font */
@font-face {
  font-family: 'Non Natural Mono';
  src: url('fonts/NONNaturalMono-Light.woff2') format('woff2');
  font-weight: 300;
  font-style: normal;
  font-display: swap;
}
```

**Important:** Place font files in a `fonts/` directory relative to your CSS. Remove any Google Fonts imports when using the brand fonts.

### Type Scale

| Style | Font | Weight | Size | Line Height | Letter Spacing |
|-------|------|--------|------|-------------|----------------|
| **H1** | Non Natural Grotesk | 700 | 95px | 90% | -2px |
| **H1 Alt** | Mondwest | 400 | 110px | 80% | -3px |
| **H2** | Non Natural Grotesk | 700 | 50px | 90% | -1px |
| **P Large Bold** | Non Natural Grotesk | 700 | 28px | 120% | 0 |
| **P Large Regular** | Non Natural Grotesk | 400 | 28px | 120% | 0 |
| **P Large Alt** | Mondwest | 400 | 32px | 90% | -0.01em |
| **P Style Bold** | Non Natural Grotesk | 700 | 16px | 110% | 0 |
| **P Style Regular** | Non Natural Grotesk | 400 | 16px | 110% | 0 |
| **P Style Alt** | Mondwest | 400 | 18px | 110% | 0 |
| **P Small** | Non Natural Mono | 400 | 12px | 130% | 0 |
| **P XSmall** | Non Natural Mono | 400 | 9px | 120% | 0.01em |

---

## Logo System

### Logomark
The abstracted dragonfly symbol based on unicode `>|<` characters.
- Use at smaller sizes and in tight spaces
- Clearspace: equal to the size of the greater-than sign on all sides

### Wordmark
Custom wordmark: **DRAGONFLY**
- Clearspace: equal to the size of the "N" on all sides

### Logo SVG Files

Use the official SVG files for web implementation. Available variants:

**Logomark (Icon):**
- `Dragonfly_Logo-Light.svg` - Light/white version (for dark backgrounds)
- `Dragonfly_Logo-Dark.svg` - Dark/black version (for light backgrounds)
- `Dragonfly_Logo-ASCII-Light.svg` - ASCII style, light version
- `Dragonfly_Logo-ASCII-Dark.svg` - ASCII style, dark version

**Wordmark:**
- `Dragonfly_Logo-Wordmark-Light.svg` - Light/white version (for dark backgrounds)
- `Dragonfly_Logo-Wordmark-Dark.svg` - Dark/black version (for light backgrounds)

**Full Logo (Logomark + Wordmark):**
- `Dragonfly_Logo-Full-Light.svg` - Combined logo, light version
- `Dragonfly_Logo-Full-Dark.svg` - Combined logo, dark version

### Logo HTML Implementation

```html
<!-- Header logo example (dark background) -->
<div class="logo">
  <img src="images/logomark.svg" alt="Dragonfly" class="logomark">
  <img src="images/wordmark.svg" alt="Dragonfly" class="wordmark">
</div>
```

```css
/* Logo sizing */
.logo {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logomark {
  height: 24px;  /* Adjust as needed */
  width: auto;
}

.wordmark {
  height: 16px;  /* Adjust as needed */
  width: auto;
}
```

### Logo Treatments
1. **Standard** - Solid white or black
2. **ASCII** - Using high-contrast characters (`###`, `##`)
3. **Outlined** - Thin outlines (be mindful of legibility when scaling)
4. **Glass** - For digital only, minimum 80px
5. **Clipped Photo** - High-contrast black/white images

### Logo Don'ts
- Do not squish or stretch
- Do not add shadows
- Do not use non-brand colors
- Do not tilt or rotate
- Do not alter spacing
- Do not use low-quality versions
- Do not recreate or modify

---

## Visual Elements

### ASCII Art
The primary visual motif. Use for:
- Background textures
- Spot illustrations
- Image post-processing
- Data visualization textures

Example ASCII logomark:
```
        ##
  ###   ##     ###
    ### ##   ###
      ### ## ###
      ### ## ###
    ### ##   ###
  ###   ##     ###
        ##
```

### 3D Elements
- Use abstract, metaphorical representations (not literal)
- Apply in backgrounds for visual interest
- Themes: chains, ribbons, glass materials
- Can be post-processed with ASCII effect

### Spot Illustrations
- Thin line weights
- Geometric/isometric style
- Subtle blurs for depth
- Themes: cubes, spheres, nodes/networks, wireframes

### Data Visualization
- Uncluttered, straightforward layouts
- Use text/ASCII as texture in charts
- Monospace type for labels
- Dotted/dashed separators

---

## Website Grid System

### Desktop (12 columns)
- Margin: 24px
- Gutter: 24px
- Column width: Flexible

### Mobile (4 columns)
- Margin: 16px
- Gutter: 16px
- Column width: Flexible

---

## CSS Variables Template

```css
:root {
  /* Colors */
  --dfly-black: #000000;
  --dfly-grey: #F2F2F2;
  --dfly-orange: #FA4C14;
  --dfly-pink: #EC39B6;
  --dfly-blue: #5014FA;

  /* Typography */
  --font-primary: 'Non Natural Grotesk', 'Inter', sans-serif;
  --font-secondary: 'Mondwest', 'Georgia', serif;
  --font-mono: 'Non Natural Mono', 'SF Mono', monospace;

  /* Spacing */
  --spacing-xs: 8px;
  --spacing-sm: 16px;
  --spacing-md: 24px;
  --spacing-lg: 48px;
  --spacing-xl: 96px;

  /* Grid */
  --grid-margin-desktop: 24px;
  --grid-gutter-desktop: 24px;
  --grid-margin-mobile: 16px;
  --grid-gutter-mobile: 16px;
}
```

---

## Tailwind CSS Theme Extension

```javascript
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        'dfly-black': '#000000',
        'dfly-grey': '#F2F2F2',
        'dfly-orange': '#FA4C14',
        'dfly-pink': '#EC39B6',
        'dfly-blue': '#5014FA',
      },
      fontFamily: {
        'primary': ['Non Natural Grotesk', 'Inter', 'sans-serif'],
        'secondary': ['Mondwest', 'Georgia', 'serif'],
        'mono': ['Non Natural Mono', 'SF Mono', 'monospace'],
      },
      fontSize: {
        'h1': ['95px', { lineHeight: '0.9', letterSpacing: '-2px' }],
        'h1-alt': ['110px', { lineHeight: '0.8', letterSpacing: '-3px' }],
        'h2': ['50px', { lineHeight: '0.9', letterSpacing: '-1px' }],
        'p-lg': ['28px', { lineHeight: '1.2' }],
        'p-lg-alt': ['32px', { lineHeight: '0.9', letterSpacing: '-0.01em' }],
        'p': ['16px', { lineHeight: '1.1' }],
        'p-alt': ['18px', { lineHeight: '1.1' }],
        'p-sm': ['12px', { lineHeight: '1.3' }],
        'p-xs': ['9px', { lineHeight: '1.2', letterSpacing: '0.01em' }],
      },
    },
  },
}
```

---

## Brand Voice & Tone

- **Confident and dramatic** - Lead with bold statements
- **Technical but accessible** - Deep crypto expertise presented clearly
- **Global perspective** - Bridge between East and West
- **Forward-thinking** - Always seeking new epiphanies
- **Professional objectivity** - Facts over hype

---

## Application Examples

### Dark Mode (Primary)
- Background: Black (`#000000`)
- Text: White or Grey (`#F2F2F2`)
- Accents: Dragon Blood Orange (`#FA4C14`)
- ASCII textures at 10-20% opacity in backgrounds

### Light Mode (Secondary)
- Background: Grey (`#F2F2F2`)
- Text: Black (`#000000`)
- Accents: Dragon Blood Orange (`#FA4C14`)
- Section dividers: Dotted lines

### UI Components
- Buttons: Orange background with black text, or outlined with orange border
- Links: Orange text, underline on hover
- Tags/Labels: Monospace font, uppercase, small size
- Borders: Thin (1px), dotted or solid
- Cards: Black background with subtle grey borders

---

## Quick Reference

**Always:**
- Use Black as the dominant color
- Apply ASCII aesthetic where appropriate
- Maintain generous whitespace
- Use uppercase for labels and eyebrows
- Keep layouts clean and uncluttered

**Never:**
- Use gradients (not part of brand)
- Use rounded corners excessively
- Mix too many colors
- Use decorative/script fonts
- Overuse tertiary colors (Pink/Blue)

---

## Bundled Assets

This skill includes brand assets in the `assets/` directory that can be copied to projects:

### Font Files (`assets/fonts/`)
```
NONNaturalGrotesk-Regular.woff2
NONNaturalGrotesk-Bold.woff2
NONNaturalMono-Light.woff2
```

### Logo SVG Files (`assets/logos/`)
```
Dragonfly_Logo-Light.svg          # Logomark - white (for dark bg)
Dragonfly_Logo-Dark.svg           # Logomark - black (for light bg)
Dragonfly_Logo-ASCII-Light.svg    # ASCII logomark - white
Dragonfly_Logo-ASCII-Dark.svg     # ASCII logomark - black
Dragonfly_Logo-Wordmark-Light.svg # Wordmark - white (for dark bg)
Dragonfly_Logo-Wordmark-Dark.svg  # Wordmark - black (for light bg)
Dragonfly_Logo-Full-Light.svg     # Full logo - white (for dark bg)
Dragonfly_Logo-Full-Dark.svg      # Full logo - black (for light bg)
```

### Usage

When creating a Dragonfly-branded project:

1. Copy font files to `project/fonts/`
2. Copy appropriate logo SVGs to `project/images/`
3. Add @font-face declarations (see Typography section)
4. Reference logos via `<img>` tags (see Logo System section)

Asset location: `~/.claude/skills/dragonfly-style/assets/`
