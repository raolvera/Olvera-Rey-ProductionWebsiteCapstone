# Release Report

Rey Olvera
GIT 515 Advanced Web Coding
Professor Hillerman
Final Production Website Capstone Release Report
October 9, 2026
ASU Sun Devils Football Gameday Hub

## What this report covers

This is the release record for the Gameday Hub. It walks through the checks I ran before I called the site done, what each check turned up, how I handled the few things it flagged, and the limits I chose to leave in place. The deeper build decisions sit in Technical-Defense.md, and the rubric-by-rubric proof sits in Evidence-Package.md; this report is the testing-and-release layer that pulls from the Module 6 Discoverability and Structured Content Package and the separately submitted Release Checklist Sprint.

## Release state

The site is live on GitHub Pages at https://raolvera.github.io/Olvera-Rey-ProductionWebsiteCapstone/, and every page points its canonical link and social metadata at that address. The build is six semantic HTML pages on one shared stylesheet, with no JavaScript behind any core feature. As of this report it is ready to grade and ready to use (GitHub Docs About GitHub Pages).

## Validation

I ran styles.css through the W3C CSS Validation Service. It comes back with no real errors. What it does flag is the container queries on the spotlight block and a couple of vendor-prefixed properties, which are valid modern CSS the validator has not caught up to yet, plus its standing notes about custom properties. I read through each flag to confirm it was the tool and not my code. I also checked the markup on all six pages for a single main, one h1, labeled landmarks, and a valid head (W3C CSS Validation Service).

## Broken-link and metadata checks

I clicked through every navigation and in-content link on all six pages and confirmed each one lands where it should, including the footer nav and the cross-page links between the Stadium, Transportation, and Schedule pages. The external links, like the photo credits and the map, open in a new tab with a note for screen reader users and safe rel attributes. The FAQPage structured data on faq.html passed the Schema.org validator with no errors or warnings, and it matches the questions a visitor actually sees in the accordion (Google Search Central Intro to Structured Data).

## Responsive and zoom checks

I tested each page narrow, medium, and wide, and again at 200 percent browser zoom. The card and stat grids reflow on their own from one column up to three, the navigation swaps to the hamburger menu below the desktop width, and only the wide data tables scroll sideways inside their own wrappers instead of stretching the page. Nothing overflowed or overlapped at any of those sizes. This builds on the work from the Module 3 Responsive Layout Systems Build (MDN CSS grid layout).

## Accessibility spot checks

I went through the site with the keyboard only and confirmed the skip link, navigation, FAQ accordion, and every form control are reachable in order and show a visible focus ring. I reran an automated accessibility scan and then checked by hand the things a scan misses: heading order, form labels, alt text, color contrast, and reflow at zoom. The required note on the contact form sits ahead of the fields and is announced rather than carried by a red asterisk alone. These checks continue the Module 5 Accessibility Conformance and Inclusive Quality Build.

## Performance diagnostic

I ran Lighthouse against the live Home page. It scored 99 for Performance and 100 for Accessibility, Best Practices, and SEO. Largest Contentful Paint came in at 1.0 seconds and the page recorded no layout shift. The one real performance fix came out of an earlier run that scored about 75 because the hero loaded the full-size photo; I built resized WebP and JPEG versions, which dropped that image from roughly 8.6 MB to under half a megabyte and lifted the score to 99. The media work overall traces back to the Module 4 Media and Typography Optimization package (web.dev Lighthouse performance audits).

## Compatibility notes

I tested the site in Chrome, Edge, and Firefox on Windows and saw consistent layout and behavior across all three. The responsive navigation, the native details and summary accordion, and the grid layouts all held up without a browser-specific workaround. A mobile screen-reader pass and a Safari check on macOS are the two I did not get to; both are listed below as known limitations.

## Known limitations

A few things I chose to document rather than force in before the deadline. The contact form validates in the browser but does not submit, since the static host has no server behind it, so it runs with novalidate and no scripted error messages; wiring it to a form service is the clear next step. The schedule page shows labeled placeholder matchups until the real season is confirmed, which is why it leaves off Event structured data for now. The embedded Google Map is third-party content I cannot tune through my own code, so it is lazy-loaded and backed by a written address and a direct link. None of these block a clean release; I am stating them so the boundaries are clear (Google Search Central Intro to Structured Data).

## Where the rest of the evidence lives

The planning that set this scope is the Module 1 Planning Package, and the build evidence runs across the Module 2 CSS Architecture Package, the Module 3 Responsive Layout Systems Build, the Module 4 Media and Typography Optimization package, the Module 5 Accessibility Conformance and Inclusive Quality Build, and the Module 6 Discoverability and Structured Content Package. Each was submitted as its own module assignment. The Release Checklist Sprint and the Release Plan and Scope were also submitted separately. Evidence-Package.md ties all of it back to the rubric, and Technical-Defense.md explains the reasoning behind the build.

## AI disclosure

AI helped troubleshoot. I verified all content, evidence, sources, accessibility claims, and release claims myself. The final decisions and code are my own.

## References

GitHub Docs. About GitHub Pages. GitHub. https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages

Google Search Central. Intro to structured data markup. Google. https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data

MDN Web Docs. CSS grid layout. Mozilla. https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_grid_layout

Lighthouse performance audits. Google. https://developer.chrome.com/docs/lighthouse/

W3C. CSS Validation Service. World Wide Web Consortium. https://jigsaw.w3.org/css-validator/
