# Alexa Cavazos — Portfolio

## Project Overview
Personal portfolio website for Alexa Cavazos, Mechanical Engineering student at Stanford University (Class of 2027). Built with plain HTML, CSS, and JavaScript — no frameworks, no build tools.

## File Structure
```
root/
  index.html                     ← homepage with projects grid
  clock-container-portfolio.html ← ME102 Project 1
  athlete-assist.html            ← ME102 Project 2
  images/                        ← clock container photos
  images2/                       ← athlete assist photos + videos
```

## Fonts
- **Chango** — all headings, section numbers, titles, labels, ticker strips
- **Chiron GoRound TC** — body text (check if loading; may need Google Fonts fallback)
- Load via Google Fonts `<link>` tag in `<head>`

## Color Palette (CSS variables)
```css
--cream:     #F2EDE3   /* page background */
--dark:      #2A2522   /* text, dark sections */
--coral:     #E05A3A   /* primary accent, border, highlights */
--teal:      #3AAEBD   /* secondary accent */
--olive:     #7A8C2E   /* tertiary accent */
--gold:      #D4A017   /* quaternary accent */
--sand:      #C8B89A   /* muted text, subtle elements */
--off-white: #FAF7F2   /* card backgrounds */
```

## Design System
- **Border:** 6px solid #E04E2A on `body` — frames the entire page
- **Border radius:** 16–20px on all cards, modals, and containers
- **Tags/pills:** border-radius 100px
- **Hover:** cards lift with `transform: translateY(-4px)` or `translate(-4px, -4px) + box-shadow`
- **Scroll reveal:** `.reveal` class + IntersectionObserver pattern used on all sections
- **Lightbox:** all images clickable to expand fullscreen, close with ✕, click outside, or Escape
- **Ticker strip:** coral background, Chango font, infinite scroll animation
- **Section headers:** large faded number + title side by side

## Aesthetic
Retro bold. Warm cream + strong coral accent. Chunky display font paired with rounded body font. Feels like a vintage magazine meets engineering portfolio. Consistent across all pages.

## Pages

### index.html — Homepage
- Sticky nav with logo "Alexa Cavazos" + links
- Hero with name in large Chango, outline/filled contrast on second line
- Rotating flower SVG sticker in hero corner
- Coral ticker strip
- About section (dark background)
- Projects grid (12-column, featured card spans 7)
- Skills section (engineering + soft skills with dot ratings + badge pills)
- Contact section (email, LinkedIn, GitHub)
- Footer with coral top border

### clock-container-portfolio.html — ME102 Project 1
- Split hero (dark left with text, right with hero photo)
- Sections: Concept → Design Process → CAD & Tolerances → Final Result → Key Learnings
- Process steps have organic blob-shaped image tops
- CAD cards have image strip at top + specs below
- Engineering drawing with italic disclaimer
- Mosaic photo grid
- Images in `/images/` folder

### athlete-assist.html — ME102 Project 2
- Three-panel hero (photo | dark center text | photo)
- Back link to index.html at top
- Sections: The Mechanism → The Process → Problems & Fixes → Final Build → In Action → Key Learnings
- Fact cards, process cards, problem/fix cards
- Two embedded videos (YouTube iframes or mp4)
- Images in `/images2/` folder

## Key Patterns
```css
/* Section header pattern */
.section-header { display: flex; align-items: baseline; gap: 20px; padding-top: 80px; margin-bottom: 48px; }
.section-num { font-family: 'Chango', system-ui; font-size: 72px; opacity: 0.35; color: var(--sand); }

/* Card pattern */
border-radius: 20px;
overflow: hidden;
background: var(--off-white);
border: 1px solid rgba(42,37,34,0.1);
transition: transform 0.22s ease;

/* Reflection cards — always 3, always these colors */
card 1: background var(--dark), heading color var(--teal)
card 2: background var(--coral), heading color var(--cream)
card 3: background var(--cream), border 2px solid rgba(42,37,34,0.12), heading color var(--dark)
```

## Deployment
GitHub Pages at `https://alexacw7.github.io`
Repo: `alexacw7/alexacw7.github.io`
Push to main branch → auto-deploys within ~60 seconds.

## Owner
Alexa Cavazos · Stanford ME · alexacw7 on GitHub
Partner on Project 2: Daria Hajimiri
