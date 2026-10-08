# Technical Defense

Rey Olvera
GIT 515 Advanced Web Coding
Professor Hillerman
Final Production Website Capstone Technical Defense
October 9, 2026
ASU Sun Devils Football Gameday Hub

## What I built

I built the ASU Sun Devils Football Gameday Hub a six-page static site that puts essential ASU football gameday information in one place. The Home page serves as the starting point and includes a Quick Links grid. Gameday Traditions covers fan rituals and the Pat Tillman tribute. Stadium Guide and Policies contains tables for the clear-bag policy and prohibited items. Transportation and Parking includes parking and light-rail tables along with a map. The site also has a Fall Schedule page and an FAQ and Contact page with an accordion and contact form.

The entire site uses semantic HTML and modern CSS. No framework is used, and no core feature depends on JavaScript. The navigation, layout, tables, and form all work through the markup and stylesheet. Every page shares the same header, navigation bar, footer, skip link, and stylesheet, which keeps the site consistent and allows a single change to appear everywhere (MDN Document and website structure).

## Why it fits the audience and task

The audience is ASU students, alumni, local fans, and first-timers heading to Mountain America Stadium in Tempe. What ties them together is one task: find gameday info fast, without digging through several sites. That drove the design.

The structure is flat, so every page is one click from any other. That suits a small reference site more than a deep hierarchy. The things fans scan for most, like bag rules, parking prices, light-rail stops, and kickoff times, sit in data tables with captions and header scope, so they read well for both sighted users and screen readers. I kept the site text-and-layout heavy with small, optimized photos instead of big images, so it stays fast on a phone on a slow gameday connection. There is also a disclaimer pointing fans to official sources before they travel, since this kind of info can go stale during the season (W3C WAI Tables Tutorial).

## Architecture and implementation

The CSS runs in a set order: tokens first, then base styles, layout, components, utilities, states, responsive rules, and a print block. Broader rules come before narrower ones, and nothing uses an ID selector or an important override outside print. Colors, type, spacing, radius, and focus are all custom properties. Each repeated piece, like the nav, cards, buttons, tables, form fields, and the accordion, pulls from its own token block, so a restyle is usually a one-line change.

The card layout uses CSS Grid with a Flexbox fallback. It reflows from one column on a phone to two columns on a tablet and three columns on a desktop. The navigation has four states a closed hamburger, an open hamburger menu, a full row, and a row with shortened labels. The navigation works through a checkbox and media queries without a script. I was especially careful with the no-JavaScript navigation because the assignment says core features cannot depend on JavaScript (MDN CSS Grid Layout).

## Media, typography, accessibility, and discoverability

Every real photo loads through a picture element with a WebP source and a JPEG fallback. Each one has width and height plus a CSS aspect ratio to hold its space, and real alt text. The decorative SVG icons and the trident logo are marked aria-hidden so screen readers skip them. The delivered files are well over ninety percent smaller than the originals, and reserving space for the images and the map kept layout shift low in testing.

The type is Inter for body and Oswald for headings, loaded with a font-display setting and fallback fonts sized to match, so the text does not jump as it loads. For accessibility, the site leans on native landmarks and one h1 per page. The skip link moves focus into the main area, and the focus outline switches to a lighter ring on the maroon header so it stays visible. The data tables have captions and header scope, and on the contact form every field has a real label, with the required state announced rather than carried by a star alone.

For discoverability, each page has its own title and description that match its h1. There is a canonical link, Open Graph and Twitter cards with full image URLs, and FAQPage structured data on the FAQ page that matches the visible questions (MDN Responsive images; W3C WAI Images Tutorial; Google Search Central Intro to Structured Data).

## What I tested

I ran the stylesheet through the W3C CSS Validation Service. The only things it flags are the container queries on the spotlight block and a couple of vendor-prefixed properties, which are valid modern CSS that the validator does not recognize yet, plus its usual notes about custom properties. There are no real errors. I checked the markup on the pages for one main, one h1, labeled landmarks, and a valid head.

I checked the navigation and content links to confirm that every path works and that the map link opens safely in a new tab. I tested one page at narrow, medium, and wide sizes and at 200 percent zoom. The cards reflowed the navigation changed to the hamburger menu, and only the tables scrolled sideways within their wrappers. During keyboard-only tests I confirmed that the skip link, navigation, accordion, and form controls were reachable and had visible focus rings. I also reran an accessibility scan and manually checked the headings, labels, alt text, contrast, and reflow. On the live Home page Lighthouse produced a score of 99 for Performance and 100 for Accessibility, Best Practices, and SEO. The Largest Contentful Paint was 1.0 seconds, and the page had no layout shift. I also checked the metadata and FAQPage structured data, which passed the Schema.org validator without errors (W3C CSS Validation Service; web.dev Lighthouse Performance Audits).

## What I fixed

Most of the real fixes came out of the accessibility work and the release sprint. Earlier I gave the menu toggle a name so screen reader users can operate it, made the main area focusable so the skip link lands there, took out duplicate image tooltips, added opens-in-a-new-tab notes to the new-tab links, and moved the form's required note ahead of the fields with proper required markup. Each one was retested and passed.

During the sprint, I removed an extra inline list style from the FAQ footer so it would use the shared rule. I also changed the font-display setting to optional and updated the related comment on five pages so anyone reading the head can understand the change. The biggest fix involved the Home page hero image. My first Lighthouse run produced a Performance score of about 75 because the hero loaded the full-size photo. I created resized WebP and JPEG versions and updated the hero to use them. This reduced the image from about 8.6 MB to less than half a megabyte and raised the Performance score to 99 (MDN What Went Wrong Troubleshooting HTML and CSS).

## What remains limited

A few items were deliberate calls to hold rather than force in before the deadline. The contact form validates in the browser but cannot submit, since a static host gives me no server to post to; it runs with novalidate and no scripted errors, so hooking it to a form service with inline messages is the clean next step. The schedule stays on labeled placeholder data until the matchups are official, and I held back Event structured data rather than publish markup for games that might change. The map is Google's embed, outside the reach of my own code, so the best I could do was lazy-load it and provide a written address and a direct link as fallbacks. I exercised the site in Chrome, Edge, and Firefox on Windows; a mobile screen-reader pass and a macOS Safari check are the two gaps I did not close. None of these block a clean release, and I am stating them plainly so the boundaries are clear (Google Search Central Intro to Structured Data).

## AI disclosure

AI helped troubleshoot. I verified all content, evidence, sources, accessibility claims, and release claims myself. The final decisions and code are my own.

## References

Google Search Central. Intro to structured data markup. Google. https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data

MDN Web Docs. CSS grid layout. Mozilla. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout

MDN Web Docs. Document and website structure. Mozilla. https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure

MDN Web Docs. Responsive images. Mozilla. https://developer.mozilla.org/en-US/docs/Web/HTML/Guides/Responsive_images

MDN Web Docs. What went wrong? Troubleshooting HTML and CSS. Mozilla. https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Debugging_HTML

Lighthouse performance audits. Google. https://developer.chrome.com/docs/lighthouse/

W3C. CSS Validation Service. World Wide Web Consortium. https://jigsaw.w3.org/css-validator/

W3C WAI. Images tutorial. World Wide Web Consortium. https://www.w3.org/WAI/tutorials/images/

W3C WAI. Tables tutorial. World Wide Web Consortium. https://www.w3.org/WAI/tutorials/tables/
