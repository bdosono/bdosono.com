# Personal Website Documentation (2026 Update)
**Table of Contents**
> 1. [Direction](#direction)
>    - [Purpose](#purpose)
>    - [Theme](#theme)
>    - [Environment](#environment)
> 2. [Design](#design)
>    - [Palette](#palette)
>    - [Typography](#typography)
>    - [Interactions](#interactions)
>    - [Surprises](#surprises)
> 3. [Diligence](#diligence)
>    - [Accessibility](#accessibility)
>    - [Performance](#performance)
>    - [Validation](#validation)
## Direction
### Purpose
- **Objective**: To modernize my one-stop landing page with a dark-mode-first redesign.
- **Outcome**: Website now live at <https://www.bdosono.com/>. This README.md file is an alliterative update to the [2016 version](https://github.com/bdosono/bdosono.com/blob/master/README.md) I initially compiled a decade ago. 
- **Overview**: This site has undergone multiple iterations since grad school. See the visual progression on my [Behance](https://www.behance.net/gallery/38857453/Personal-Website) profile or the [Internet Archive](https://web.archive.org/web/*/https://www.bdosono.com/). This latest revamp trades the minimal light layout for something more atmospheric, and below I document the design decisions and auditing rigor behind it to inspire others to polish their own web presence.
### Theme
- **Celestial Eclipse**: The entire visual identity orbits a single metaphor: a total eclipse. My circular portrait sits inside a golden ring with a layered corona glow that gently pulses, like a ring of light around a dark disc. The near-black background (`#0a0b0c`) is the night sky; a faint radial glow with a cool purple undertone provides the atmosphere.
- **Lux Champagne**: One accent color carries the whole site: champagne gold. Paired with generous negative space, hairline underlines, and a display serif for the name, the effect is closer to a fashion editorial than a portfolio grid. Restraint is the luxury; every gold pixel has to earn its place.
- **Adaptive Light**: Clicking the eclipse (my portrait) toggles a warm paper light mode (`#faf9f6`) with a deeper bronze gold. The preference persists across visits via `localStorage`, and the browser chrome follows along through a dynamic `theme-color` meta tag.
### Environment
- **Architecture**: I aimed for simplicity with a single self-contained `index.html`: CSS and JavaScript embedded, zero frameworks, zero dependencies. The whole page ships in one request.
- **Collaboration**: This revamp was vibe coded with [Claude](https://claude.com/), iterating conversationally through typography auditions, contrast math, and easter egg engineering.
- **Source Hygiene**: I kept a readable, commented `index.source.html` for future edits and deploy the minified `index.html` produced by [html-minifier-terser](https://github.com/terser/html-minifier-terser).
## Design
### Palette
- **Token System**: Every color resolves to a CSS custom property with no hardcoded literals. Two tiers of gold per theme: `--accent` (text-safe: `#e3c27d` on dark, `#8a6420` on light) and `--gold` (a decorative RGB triplet powering all fifteen glow, ring, button, and meteor tints). A consolidation audit deleted three entire light-theme override blocks because the variables now handle theme switching automatically.
- **Contrast Math**: A universal AA-compliant gold is mathematically impossible across both backgrounds (text on near-black needs luminance ≥ 0.19; text on warm paper needs ≤ 0.17), which is precisely why the palette pairs tokens per theme. Dark mode text measures AAA (7.1–16.7:1); light mode measures AA+ (5.1–6.3:1).
- **Undertone**: The ambient glow blends gold with a documented purple undertone (`--glow-cool`): twilight in dark mode, lavender in light.
### Typography
- **Display**: [Rasa](https://fonts.google.com/specimen/Rasa) renders my name with a tall, graceful serif chosen after auditioning Fraunces, Cormorant Garamond, and a shortlist of luxury editorial faces.
- **Body**: [Lato](http://www.latofonts.com/lato-free-fonts/) returns from the previous iteration of the site, keeping continuity with my long-standing brand.
- **Subsetting**: The display font is subset to only the characters my name needs (via the Google Fonts `text=` parameter, then self-hosted as woff2), presenting a dramatic reduction in font payload. The [Typography Handbook](http://typographyhandbook.com/) remains my north star for type on screens.
- **Iconography**: A miniature of the site itself is captured in the favicon eclipse disc, which shows a golden ring, corona glow, and a "BD" monogram set in Lato Bold, converted to vector outlines so no font dependency exists. The `.ico` format keeps it compatible across browsers.
### Interactions
- **Living Background**: The ambient glow drifts toward the cursor with eased lag, so the page feels aware without being busy.
- **Magnetic Links**: The role links (Speaker · Technologist · Advisor · Researcher) lean subtly toward the cursor and reveal hover preview cards describing each destination.
- **Click-to-Copy**: Clicking "Email" copies my address to the clipboard with a gold "Copied ✓" confirmation, announced to assistive technology through an `aria-live` region. The address itself is assembled at runtime to deter scrapers.
### Surprises
- **Golden Shimmer**: Clicking my name sweeps a champagne shine across the letters, implemented with an animated `background-clip: text` gradient, with padding math to keep descenders intact.
- **Shooting Star**: Clicking "fun" delightfully launches a gold meteor arcing across the viewport, each with a randomized origin and trajectory.
- **Konami Storm**: Entering ↑ ↑ ↓ ↓ ← → ← → B A unleashes a shower of 101 meteors over five and a half seconds. Some traditions are worth honoring. 😉
## Diligence
### Accessibility
- **Contrast**: Every text/background pair was verified programmatically against WCAG 2.1 with no eyeballing. The light-mode gold was specifically darkened from its decorative shade to reach AA for small text.
- **Semantics**: One `h1`, a semantic list for roles, a true `<button>` for the theme toggle with `aria-pressed`, visible focus styles throughout, and `aria-label`s announcing which links open in new tabs.
- **Reduced Motion**: `prefers-reduced-motion` disables the cursor glow, magnetic links, glow pulse, shimmer, and meteors entirely. Delight should be opt-out-able.
### Performance
- **Audits**: The site scores a perfect **100/100 on both [Google PageSpeed Insights](https://pagespeed.web.dev/analysis?url=https%3A%2F%2Fwww.bdosono.com%2F) and [Pingdom](https://tools.pingdom.com/)**, which matches the ratings this site earned back in 2016, now with a theme toggle, cursor-reactive lighting, and a meteor storm along for the ride. Getting there meant chasing down every audit flag: render-blocking font requests, forced reflows, unused JavaScript, cache lifetimes, and image sizing.
- **Zero external JavaScript**: Google's ~70 KB gtag.js library is replaced by a hand-rolled [minimal GA4 beacon](https://developers.google.com/analytics/devguides/collection/protocol/ga4) (~25 lines, inline) that sends pageviews directly to the Measurement endpoint, which is the spiritual successor to the minimal snippet approach I used in the Universal Analytics era.
- **Self-hosted fonts**: Both typefaces live on my own server as woff2 files with one-year immutable cache headers, sidestepping the short cache lifetimes Google Fonts assigns to dynamically subset fonts. (History rhymes: I self-hosted fonts a decade ago for compatibility with China and other firewalled regions.)
- **Payload**: The minified page weighs about 14 KB raw and 5 KB gzipped, with styles, scripts, and all three easter eggs included. The entire document costs less than the profile photo.
- **Loading**: The portrait (the Largest Contentful Paint element) is responsive (`srcset` serves 251px or 502px by screen density) and preloaded with `fetchpriority="high"`; explicit dimensions prevent layout shift; animations touch only GPU-composited properties; input listeners are passive and never query layout mid-interaction.
- **Caching & compression**: An `.htaccess` sets year-long immutable caching for images and fonts, short lifetimes for HTML, and gzip compression for text assets.
- **Minification**: [html-minifier-terser](https://github.com/terser/html-minifier-terser) compresses HTML, CSS, and JS in one pass at deploy time, keeping the source copy human-readable.
### Validation
- **Markup**: Both source and minified files pass a strict HTML5 parse with zero errors; the [W3C Markup Validation Service](https://validator.w3.org/) remains a one-click essential.
- **Copyright**: Developed by Bryan Dosono under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).
