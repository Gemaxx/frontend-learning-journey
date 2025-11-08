
```scss

/* ==========================================================
   PURELEARN DESIGN TOKENS — TYPOGRAPHY v3 (rem edition)
   Units: rem (1rem = 10px) via body { font-size: 62.5%; }
   Based on Figma export + fluid clamp() + best practices
   ========================================================== */

/* ----------------------------------------------------------
   ROOT CONFIG
   ---------------------------------------------------------- */
html, body {
  font-size: 62.5%; /* 1rem = 10px */
}

:root {
  --font-family: 'Inter', system-ui, -apple-system, sans-serif;

  /* ==========================================================
     HEADINGS
     ========================================================== */
  --h1-font-size: clamp(3.2rem, 4vw + 1rem, 4.8rem);
  --h1-line-height: 5.6rem;
  --h1-font-weight: 800;
  --h1-tracking: -0.13rem;
  --h1-margin-bottom: 3.2rem;

  --h2-font-size: clamp(2.8rem, 3vw + 0.5rem, 3.6rem);
  --h2-line-height: 4.4rem;
  --h2-font-weight: 700;
  --h2-tracking: -0.07rem;
  --h2-margin-bottom: 2.4rem;

  --h3-font-size: clamp(2.4rem, 2.5vw + 0.5rem, 3rem);
  --h3-line-height: 4rem;
  --h3-font-weight: 600;
  --h3-tracking: -0.035rem;
  --h3-margin-bottom: 2rem;

  --h4-font-size: clamp(1.8rem, 1.5vw + 0.5rem, 2.4rem);
  --h4-line-height: 3.2rem;
  --h4-font-weight: 600;
  --h4-tracking: 0rem;
  --h4-margin-bottom: 1.6rem;

  /* ==========================================================
     BODY TEXT
     ========================================================== */
  --p-font-size: clamp(1.4rem, 0.5vw + 0.25rem, 1.6rem);
  --p-line-height: 2.8rem;
  --p-font-weight: 400;
  --p-tracking: 0rem;
  --p-margin-bottom: 1.6rem;

  --lead-font-size: clamp(1.6rem, 1vw + 0.5rem, 2.4rem);
  --lead-line-height: 2.8rem;
  --lead-font-weight: 400;
  --lead-tracking: -0.015rem;
  --lead-margin-bottom: 2rem;

  --large-font-size: clamp(1.6rem, 1vw + 0.25rem, 2.4rem);
  --large-line-height: 2.8rem;
  --large-font-weight: 600;
  --large-tracking: 0.015rem;
  --large-margin-bottom: 1.2rem;

  --small-font-size: clamp(1.2rem, 0.4vw + 0.25rem, 1.6rem);
  --small-line-height: 2rem;
  --small-font-weight: 400;
  --small-tracking: 0.015rem;
  --small-margin-bottom: 1.2rem;

  --muted-font-size: clamp(1.2rem, 0.4vw + 0.25rem, 1.4rem);
  --muted-line-height: 2rem;
  --muted-font-weight: 400;
  --muted-tracking: 0.015rem;
  --muted-margin-bottom: 1.4rem;

  /* ==========================================================
     UI ELEMENTS
     ========================================================== */
  --btn-font-size: 1.4rem;
  --btn-line-height: 2rem;
  --btn-font-weight: 600;
  --btn-tracking: 0.05rem;
  --btn-margin-bottom: 1.2rem;

  --code-font-size: 1.3rem;
  --code-line-height: 2rem;
  --code-font-weight: 600;
  --code-tracking: 0.02rem;

  --blockquote-font-size: clamp(1.6rem, 1vw + 0.5rem, 1.8rem);
  --blockquote-line-height: 2.8rem;
  --blockquote-font-weight: 400;
  --blockquote-tracking: 0rem;
  --blockquote-margin-bottom: 1.6rem;

  /* ==========================================================
     TABLES & LISTS
     ========================================================== */
  --table-head-font-size: 1.4rem;
  --table-head-line-height: 2.4rem;
  --table-head-font-weight: 600;
  --table-head-tracking: 0.04rem;

  --table-item-font-size: 1.4rem;
  --table-item-line-height: 2.4rem;
  --table-item-font-weight: 400;
  --table-item-tracking: 0.02rem;

  --list-item-font-size: 1.4rem;
  --list-item-line-height: 2.8rem;
  --list-item-font-weight: 400;
  --list-item-tracking: 0.01rem;

  /* ==========================================================
     SEMANTIC ALIASES
     ========================================================== */
  --font-display: var(--h1-font-size);
  --font-body: var(--p-font-size);
  --font-ui: var(--btn-font-size);
  --font-code: var(--code-font-size);
}

/* ==========================================================
   MIXIN: text-style()
   ----------------------------------------------------------
   Use to apply token-based typography easily
   Example: @include text-style('h1');
   ========================================================== */
@mixin text-style($token) {
  font-family: var(--font-family);
  font-size: var(--#{$token}-font-size);
  line-height: var(--#{$token}-line-height);
  font-weight: var(--#{$token}-font-weight);
  letter-spacing: var(--#{$token}-tracking);
}

/* ==========================================================
   NORMALIZATION & BASE STYLES
   ========================================================== */
:where(h1, h2, h3, h4, p) {
  margin: 0;
  color: inherit;
  font-family: var(--font-family);
}

h1 { @include text-style('h1'); margin-bottom: var(--h1-margin-bottom); }
h2 { @include text-style('h2'); margin-bottom: var(--h2-margin-bottom); }
h3 { @include text-style('h3'); margin-bottom: var(--h3-margin-bottom); }
h4 { @include text-style('h4'); margin-bottom: var(--h4-margin-bottom); }

p { @include text-style('p'); margin-bottom: var(--p-margin-bottom); }
.lead { @include text-style('lead'); }
.small { @include text-style('small'); }
.muted { @include text-style('muted'); opacity: 0.8; }

button, .btn {
  @include text-style('btn');
  text-transform: uppercase;
  line-height: var(--btn-line-height);
}

blockquote {
  @include text-style('blockquote');
  font-style: italic;
  border-left: 0.4rem solid currentColor;
  padding-left: 1.6rem;
}

/* ==========================================================
   ACCESSIBILITY: Reduced Motion
   ========================================================== */
@media (prefers-reduced-motion: reduce) {
  * {
    transition-duration: 0.01ms !important;
    animation-duration: 0.01ms !important;
  }
}


```
