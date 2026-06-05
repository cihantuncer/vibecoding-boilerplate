---
purpose: Web performance and Core Web Vitals directive.
use_when: Work affects page load, images, fonts, layout shift, rendering, hydration, bundle size, INP/LCP/CLS, or perceived responsiveness.
prefer_index: ./INDEX.md
---

# Web Vitals Directive

Protect LCP, CLS, and INP. Avoid layout shifts from late images, fonts, ads, dynamic content, or unstable dimensions. Keep critical content lightweight and defer non-critical work.

Prefer explicit image dimensions, responsive images, font-display choices, stable skeletons, smaller bundles, lazy loading below the fold, and reduced main-thread work. Do not add heavy client code for a visual-only fix.

Validate with a relevant metric, bundle/build output, browser performance check, or before/after reasoning tied to the changed path.
