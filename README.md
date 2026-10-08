# ASU Sun Devils Football Gameday Hub

Rey Olvera
GIT 515 Advanced Web Coding
Professor Hillerman
Final Production Website Capstone
October 9, 2026

## About the ASU Gameday Hub

The Gameday Hub is a small, fast website that puts ASU Sun Devils football gameday info in one place: clear-bag rules, stadium policies, parking, Valley Metro light rail, traditions, the fall schedule, and a short FAQ with a contact form. It is made for ASU students, alumni, local fans, and first-time visitors going to Mountain America Stadium in Tempe, so they do not have to hunt across several sites for the basics. The site is semantic HTML and modern CSS only. There is no framework and no JavaScript behind any core feature, which keeps it light and easy to maintain (MDN Document and website structure).

## Published site

The live site is available at https://raolvera.github.io/Olvera-Rey-ProductionWebsiteCapstone/, and the source is available at https://github.com/raolvera/Olvera-Rey-ProductionWebsiteCapstone. Each page uses the live address in its canonical tag, Open Graph URL, and social image paths, so these references point to the published site (GitHub Docs About GitHub Pages).

## Page scope

The site contains six pages, and each one answers a specific gameday question. Home (index.html) is the starting point and includes a hero, a Quick Links grid, and a Gameday at a Glance stat list. Gameday Traditions (traditions.html) covers Forks Up, the Tillman Tunnel run-out, the fight song, tailgating tips, and the Pat Tillman tribute. Stadium Guide and Policies (stadium.html) explains the clear-bag policy, prohibited items, and gate times. Transportation and Parking (transportation.html) includes parking and light-rail tables, an embedded Google Map, and a text address backup. Fall Schedule (schedule.html) contains the season matchup table with clearly labeled placeholder data. FAQ and Contact (faq.html) includes an accordion, FAQPage structured data, and a contact form. All six pages share the same header, navigation bar, footer, skip link, and stylesheet, so changes to these shared parts appear throughout the site (MDN Document and website structure).

## File organization

The six HTML pages are index.html (Home), traditions.html (Gameday Traditions and the Pat Tillman tribute), stadium.html (Stadium Guide and Policies), transportation.html (Transportation and Parking, with the map), schedule.html (Fall Schedule), and faq.html (FAQ and Contact, with the form and FAQPage structured data). The styles.css file is the shared stylesheet, holding the tokens, components, states, responsive rules, and print block. The images folder holds each photo at several widths in both WebP and JPEG, plus logo.svg, favicon.svg, and footerLogo.png, with the original photos kept next to the smaller versions so the source is clear. The written documents are this README, Release-Report.md, Technical-Defense.md, and Evidence-Package.md.

The planning and build work from Modules 1 through 6 was submitted as its own module assignment and is described in Evidence-Package.md: the Module 1 Planning Package, the Module 2 CSS Architecture Package, the Module 3 Responsive Layout Systems Build, the Module 4 Media and Typography Optimization, the Module 5 Accessibility Conformance and Inclusive Quality Build, and the Module 6 Discoverability and Structured Content Package.

## Release state

The final build has been tested and validated. The W3C CSS Validation Service reports only the container queries and a few vendor prefixes, which are valid modern CSS features that the validator does not yet recognize. The FAQPage structured data passed the Schema.org validator with no errors or warnings. On the live Home page, Lighthouse scored 99 for Performance and 100 for Accessibility, Best Practices, and SEO. The smaller fixes and retests completed during the release sprint are listed in the Release Checklist Sprint, which was submitted as its own assignment.

## Known limitations

A few things are worth knowing before you use the site. The contact form validates in the browser but will not send, since a static site has no server to receive it; wiring it to a form service is the obvious next step. It runs with novalidate and no scripted error messages. The schedule shows placeholder matchups, clearly marked, until the real season is set, so that page skips Event structured data for now. The map is an embedded Google frame I can't tune from my own code, so it loads lazily and ships with a text address and a direct map link as fallbacks. Browser testing covered Chrome, Edge, and Firefox on Windows; a mobile screen-reader pass and a Safari check are still to come.

## Evidence package

The planning, build, and release evidence from Modules 1 through 6 is summed up in Evidence-Package.md, which points to its supporting work. Technical-Defense.md explains the choices, the testing, the fixes, and what is still limited in one place (MDN What went wrong Troubleshooting HTML and CSS).

## AI disclosure

AI helped troubleshoot. I verified all content, evidence, sources, accessibility claims, and release claims myself. The final decisions and code are my own.


## References

GitHub Docs. About GitHub Pages. GitHub. https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages

Google Search Central. Intro to structured data markup. Google. https://developers.google.com/search/docs/appearance/structured-data/intro-structured-data

MDN Web Docs. Client-side form validation. Mozilla. https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation

MDN Web Docs. Document and website structure. Mozilla. https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure

MDN Web Docs. Publishing your website. Mozilla. https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/Publishing_your_website

MDN Web Docs. What went wrong? Troubleshooting HTML and CSS. Mozilla. https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Debugging_HTML

W3C. CSS Validation Service. World Wide Web Consortium. https://jigsaw.w3.org/css-validator/
