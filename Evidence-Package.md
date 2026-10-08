# Evidence Package

Rey Olvera
GIT 515 Advanced Web Coding
Professor Hillerman
Final Production Website Capstone Evidence Package
October 9, 2026
ASU Sun Devils Football Gameday Hub

## Purpose
This document names each required part of the submission and points each rubric area to the evidence that backs it up. The site is the six-page build in this folder, and the planning and build evidence comes from the module work done across the GIT 515 project (MDN Document and website structure).

## Required Parts and Where to Find Them

The site is published on GitHub Pages at https://raolvera.github.io/Olvera-Rey-ProductionWebsiteCapstone/. Each page uses this address in its canonical and social metadata, so those tags point to the live site. The repository contains the six HTML pages, the styles.css stylesheet, and the images folder, and the README explains the file structure. The site uses semantic HTML and modern CSS, and no core feature depends on JavaScript.

The planning evidence is the Module 1 Planning Package: the project brief, content inventory, site map and page requirements, wireframes, behavior notes, and acceptance criteria. The build evidence spans Modules 2 through 6. Module 2 is the CSS Architecture Package, Module 3 is the Responsive Layout Systems Build, Module 4 is the Media and Typography Optimization package, Module 5 is the Accessibility Conformance and Inclusive Quality Build, and Module 6 is the Discoverability and Structured Content Package. Each one was submitted as its own module assignment. The release evidence is the W3C CSS validation result and the FAQPage structured-data check in the Schema.org validator. The Release Checklist Sprint and the Release Plan and Scope were each submitted as their own assignments. The technical defense is in Technical-Defense.md (GitHub Docs About GitHub Pages).

## How Each Requirement Is Met

**Capstone scope, content, and user task fit.** The site matches the six-page scope I approved in the Planning Package, serves one audience and one task, getting ASU football fans their gameday info in one place, and every page has complete content. Evidence: the live site, the Module 1 Planning Package brief and site map, and the page scope section of the README (MDN Document and website structure).

**HTML/CSS architecture and implementation quality.** The pages use semantic landmarks and one h1 each. The stylesheet is built on design tokens in a clear order, with reusable components, a card layout that uses CSS Grid with a Flexbox fallback, a navigation that works with no JavaScript, and a clean file layout. Evidence: the six pages, the styles.css stylesheet, the Module 2 CSS Architecture Package, and the Module 3 Responsive Layout Systems Build with their before-and-after refactor record (MDN CSS grid layout).

**Responsive media, typography, accessibility, and discoverability.** I served the photos as WebP with JPEG fallbacks and set width and height so the layout does not jump while they load. For the fonts I picked fallback faces and sized them to keep the swap from shifting text around. I worked through the accessibility fixes and wrote them down as I went, and I added FAQPage structured data to the metadata. Each of these I built and checked myself. Evidence: the Module 4 Media and Typography Optimization package, the Module 5 Accessibility Conformance and Inclusive Quality Build, the Module 6 Discoverability and Structured Content Package, and the FAQPage check in the Schema.org validator (MDN Responsive images; Google Search Central Intro to Structured Data).

**Release quality and testing evidence.** I validated the CSS, where the only flags are the container queries and a few vendor prefixes the validator does not recognize yet, and I checked the links. I tested the layout narrow, medium, wide, and at 200 percent zoom, did keyboard and accessibility spot checks, and checked it in Chrome, Edge, and Firefox. Lighthouse on the live Home page scored 99 for Performance and 100 for Accessibility, Best Practices, and SEO, with the Largest Contentful Paint at 1.0 seconds and no layout shift. Evidence: the separately submitted Release Checklist Sprint and Release Plan and Scope, and the W3C CSS validation result (W3C CSS Validation Service; Lighthouse Performance Audits).

**Documentation and technical defense.** The evidence package and the defense explain the decisions, the tests, the fixes, the remaining limits, and the release readiness in plain language. Evidence: the Technical Defense, the README, and this document (MDN What Went Wrong Troubleshooting HTML and CSS).

## Known Limitations Carried Into the Final Release

I am recording these boundaries so a reviewer knows exactly where the release stands. The contact form validates fields in the browser but does not submit, because the static host has no server behind it, and it relies on novalidate rather than scripted error messages. The schedule page carries labeled placeholder matchups until the real season is confirmed, which is why it omits Event structured data. The embedded Google Map is third-party content I do not control, so it is lazy-loaded and backed by a written address and a direct link. Testing ran across Chrome, Edge, and Firefox on Windows; a mobile screen-reader pass and a macOS Safari check are still outstanding (Lighthouse Performance Audits).

## AI disclosure

AI helped troubleshoot. I verified all content, evidence, sources, accessibility claims, and release claims myself. The final decisions and code are my own.



## References

GitHub Docs. About GitHub Pages. GitHub. https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages

Google Search Central. Intro to structured data markup. Google. https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data

MDN Web Docs. CSS grid layout. Mozilla. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout

MDN Web Docs. Document and website structure. Mozilla. https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure

MDN Web Docs. Responsive images. Mozilla. https://developer.mozilla.org/en-US/docs/Web/HTML/Guides/Responsive_images

MDN Web Docs. What went wrong? Troubleshooting HTML and CSS. Mozilla. https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Debugging_HTML

Lighthouse performance audits. Google. https://developer.chrome.com/docs/lighthouse/

W3C. CSS Validation Service. World Wide Web Consortium. https://jigsaw.w3.org/css-validator/
