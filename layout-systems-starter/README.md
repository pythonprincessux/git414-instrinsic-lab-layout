# Layout Systems Starter

Use this small page for Module 3 practice if you do not want to use your capstone yet.

## Files

- `index.html`: sample content with layout patterns.
- `styles.css`: starter CSS with tokens, layers, and layout prompts.

## Practice goal

Build a responsive layout system:

- flexible wrapper
- intrinsic card grid
- content-driven breakpoint
- logical properties
- container query component
- user-preference or feature query

Keep notes about what changed and why.

## Completed Practice
Kiara McRae | GIT 414

### Intrinsic Layout Pattern
The guide cards use repeat(auto-fit, minmax(min(100%, 16rem), 1fr)).
The grid creates as many columns as the container can accommodate on the page,
while allowing a card to shrink below 16rem when its container is
narrower. Cards wrap without separate column-count media queries.

The wrapper uses a logical inline sizing and automatic inline margins
to keep content centered, preserve the side gutters, and stop growing at 72rem.
Section and hero spacing use clamp(2rem, 5vw, 4rem).

### Content-Based Breakpoint
The hero changes from one column to two at 56rem. Below this width,
stacking gives the long heading and Weekend Route card more room.
Above it, the heading and route card can share a row.

In devtools, I checked 880px and 912px on either side of the breakpoint. The hero
was stacked at 880px and displayed beside the route card at 912px.
The card grid adapts independently of this hero breakpoint.

### Browser Checks
I tested the starter locally in Chrome:
- 375px: guide cards displayed in one column.
- 768px: guide cards displayed in two columns.
- 1280px: all four guide cards displayed in one row.
- 880px and 912px: the hero changed arrangements across the breakpoint.
- 200% browser zoom: the visible Weekend Route text and button remained
  inside the card without overlap.

These observations describe the tested views, not a complete
accessibility or cross-browser audit.

### AI Disclosure
For this week's assignment, I used ChatGPT to explain the syntax and 
fluid spacing I applied all of the changes myself and
tested the page in Chrome in devtools. 