# Vision Security Production Readiness Task List

Status: In progress  
Goal: Prepare the static website mockup for production WordPress deployment.

Use this file as the working punch list. Address items in numerical order unless a later item is blocking an earlier one.

## 1. Fix Current Mockup Blockers

- [x] 1.1 Fix broken asset paths on `/services/index.html`.
- [x] 1.2 Fix broken internal links on `/services/index.html`.
- [x] 1.3 Verify `/services/index.html` loads the shared design system at its production URL.
- [x] 1.4 Fix mobile layout overflow on `/contact.html`.
- [x] 1.5 Fix invalid inline CSS on `/contact.html`.
- [x] 1.6 Fix mobile navigation drawer spacing and clipping.
- [x] 1.7 Replace `href="#"` dropdown parent links with accessible buttons or real landing pages.
- [x] 1.8 Remove visible encoding artifacts such as broken middle dots, dashes, and dropdown carets if they remain in source or rendered output.
- [x] 1.9 Verify every internal link across all pages.
- [x] 1.10 Verify every page at mobile, tablet, desktop, and wide desktop widths.

## 2. Replace Placeholder Content

- [ ] 2.1 Replace the Pexels hero video with owned Roaring Fork Valley, Aspen, Vail, or Glenwood Springs footage.
- [ ] 2.2 Add an optimized poster image for the hero video.
- [ ] 2.3 Replace all Unsplash and Pexels stock imagery with approved local, property, install, or team photography.
- [ ] 2.4 Replace demo/fabricated Stories testimonials with real approved customer stories.
- [ ] 2.5 Replace the demo case study on the Property Managers page with a verified client case.
- [ ] 2.6 Replace placeholder team headshots and bios.
- [ ] 2.7 Confirm all stats and claims: `21 years`, `1,300+ accounts`, `100% NICET-certified`, `DSC Top Dealer`, `Alarm.com Beta Partner`, and `AHJ Referred`.
- [ ] 2.8 Get written approval for any customer names, quotes, case studies, photos, or video testimonials.

## 3. Build The WordPress Theme

- [ ] 3.1 Create a custom WordPress theme from the mockup.
- [ ] 3.2 Build reusable header, footer, CTA strip, page header, card grid, testimonial/story, and form components.
- [ ] 3.3 Create the home page template.
- [ ] 3.4 Create the service detail template.
- [ ] 3.5 Create the services hub template.
- [ ] 3.6 Create the persona/audience template.
- [ ] 3.7 Create the industry template.
- [ ] 3.8 Create the market/location template.
- [ ] 3.9 Create the resource template.
- [ ] 3.10 Create the stories/testimonials template.
- [ ] 3.11 Create the legal/basic page template.
- [ ] 3.12 Add ACF or equivalent custom fields for editable page content.
- [ ] 3.13 Convert static navigation into WordPress menus.
- [ ] 3.14 Convert footer columns into editable menus or widget areas.
- [ ] 3.15 Move inline styles and scripts into theme CSS and JS.
- [ ] 3.16 Remove duplicated scripts from individual pages.
- [ ] 3.17 Create a staging environment.

## 4. Integrate Forms And Scale

- [ ] 4.1 Replace all demo form actions that point to `submission-demo.html`.
- [ ] 4.2 Choose Gravity Forms, Fluent Forms, or custom WordPress forms.
- [ ] 4.3 Connect forms to Scale/GoHighLevel webhooks.
- [ ] 4.4 Build the Request Onsite Assessment form.
- [ ] 4.5 Build the Request Compliance Review form.
- [ ] 4.6 Build the Schedule Service form.
- [ ] 4.7 Build the Billing Question form.
- [ ] 4.8 Build the Callback Request form.
- [ ] 4.9 Build the Compliance Calendar Download form.
- [ ] 4.10 Build the Career Application form.
- [ ] 4.11 Build the General Contact form.
- [ ] 4.12 Build the Newsletter Signup form if it remains in scope.
- [ ] 4.13 Add honeypot spam protection.
- [ ] 4.14 Add reCAPTCHA v3 or equivalent.
- [ ] 4.15 Add required SMS consent checkbox with timestamp and IP capture.
- [ ] 4.16 Add marketing consent checkbox where needed.
- [ ] 4.17 Capture UTM parameters on every form.
- [ ] 4.18 Route each form to the correct Scale pipeline and stage.
- [ ] 4.19 Configure email and SMS auto-responses.
- [ ] 4.20 Configure internal alerts.
- [ ] 4.21 Test every form end-to-end from submission to Scale record, autoresponse, and internal alert.

## 5. Complete Compliance And Legal Review

- [ ] 5.1 Complete legal review of the Privacy Policy.
- [ ] 5.2 Complete legal review of the Terms of Use.
- [ ] 5.3 Add cookie or analytics consent if marketing pixels are used.
- [ ] 5.4 Add TCPA-compliant SMS consent language.
- [ ] 5.5 Confirm 10DLC registration for SMS workflows.
- [ ] 5.6 Add physical mailing address to marketing emails.
- [ ] 5.7 Confirm unsubscribe handling for email marketing.
- [ ] 5.8 Add a "Do Not Sell or Share My Personal Information" link if required.
- [ ] 5.9 Confirm careers form resume/file handling policy.
- [ ] 5.10 Confirm video, photo, and testimonial release forms.

## 6. Implement SEO Foundation

- [ ] 6.1 Add canonical tags to every page.
- [ ] 6.2 Add unique Open Graph metadata to every page.
- [ ] 6.3 Add Twitter/X card metadata.
- [ ] 6.4 Add optimized meta descriptions.
- [ ] 6.5 Add `LocalBusiness` and `Organization` schema.
- [ ] 6.6 Add `Service` schema on service pages.
- [ ] 6.7 Add `FAQPage` schema where FAQ content appears.
- [ ] 6.8 Add `BreadcrumbList` schema on nested pages.
- [ ] 6.9 Add `VideoObject` schema for real testimonial videos.
- [ ] 6.10 Add XML sitemap.
- [ ] 6.11 Add HTML sitemap if desired.
- [ ] 6.12 Add `robots.txt`.
- [ ] 6.13 Configure clean WordPress permalinks.
- [ ] 6.14 Create redirect map from current Thryv URLs.
- [ ] 6.15 Implement and test all 301 redirects.
- [ ] 6.16 Connect Google Search Console.
- [ ] 6.17 Connect Bing Webmaster Tools.
- [ ] 6.18 Submit sitemap after launch.

## 7. Optimize Performance

- [ ] 7.1 Convert large PNGs and photos to WebP or AVIF where appropriate.
- [ ] 7.2 Generate responsive image sizes.
- [ ] 7.3 Add lazy loading below the fold.
- [ ] 7.4 Optimize hero video for desktop.
- [ ] 7.5 Optimize hero video for mobile.
- [ ] 7.6 Add mobile fallback video or poster-only mode.
- [ ] 7.7 Self-host or optimize font loading.
- [ ] 7.8 Minify production CSS and JS.
- [ ] 7.9 Remove unused CSS.
- [ ] 7.10 Defer non-critical scripts.
- [ ] 7.11 Test Core Web Vitals.
- [ ] 7.12 Reach Lighthouse Performance score of 90 or higher.
- [ ] 7.13 Reach LCP under 2.5 seconds.
- [ ] 7.14 Reach CLS under 0.1.

## 8. Complete Accessibility Review

- [ ] 8.1 Add skip-to-content link.
- [ ] 8.2 Make dropdown navigation keyboard accessible.
- [ ] 8.3 Ensure the mobile menu handles focus correctly when open.
- [ ] 8.4 Add visible focus states to links, buttons, and form controls.
- [ ] 8.5 Verify color contrast across glass and dark sections.
- [ ] 8.6 Ensure all images have real alt text.
- [ ] 8.7 Ensure decorative images are ignored appropriately.
- [ ] 8.8 Ensure form labels and error messages are accessible.
- [ ] 8.9 Add captions or transcripts for videos.
- [ ] 8.10 Respect `prefers-reduced-motion`.
- [ ] 8.11 Test keyboard-only navigation.
- [ ] 8.12 Run Lighthouse and/or axe accessibility checks.
- [ ] 8.13 Target WCAG 2.1 AA.

## 9. Configure Analytics And Tracking

- [ ] 9.1 Install Google Tag Manager.
- [ ] 9.2 Preserve existing GTM ID if still correct: `GTM-TV2JCMCG`.
- [ ] 9.3 Configure GA4.
- [ ] 9.4 Configure form conversion events.
- [ ] 9.5 Configure phone click tracking.
- [ ] 9.6 Configure CTA click tracking.
- [ ] 9.7 Configure Compliance Calendar download tracking.
- [ ] 9.8 Configure Google Ads and Meta/Facebook pixels only after consent policy is settled.
- [ ] 9.9 Confirm Scale attribution receives source, medium, campaign, landing page, and referrer.
- [ ] 9.10 Test events in GTM Preview and GA4 DebugView.

## 10. Finish Content Production

- [ ] 10.1 Finalize copy for all current pages.
- [ ] 10.2 Remove prototype language from live pages.
- [ ] 10.3 Finalize service page copy.
- [ ] 10.4 Finalize market/location page copy with real local references.
- [ ] 10.5 Finalize persona page copy.
- [ ] 10.6 Finalize About/team content.
- [ ] 10.7 Finalize Careers content and current openings.
- [ ] 10.8 Finalize FAQ content.
- [ ] 10.9 Finalize Compliance Calendar PDF.
- [ ] 10.10 Create or approve all downloadable assets.
- [ ] 10.11 Proofread all pages.
- [ ] 10.12 Confirm brand voice consistency.

## 11. Configure WordPress Administration And Maintenance

- [ ] 11.1 Configure WordPress users and roles.
- [ ] 11.2 Add backup plugin or host-level backups.
- [ ] 11.3 Add security plugin or host-level WAF.
- [ ] 11.4 Add caching layer.
- [ ] 11.5 Add image optimization workflow.
- [ ] 11.6 Add staging-to-production deployment process.
- [ ] 11.7 Disable unnecessary plugins.
- [ ] 11.8 Configure SMTP for WordPress email.
- [ ] 11.9 Configure uptime monitoring.
- [ ] 11.10 Configure broken link monitoring.
- [ ] 11.11 Document how to edit each page type.

## 12. Prepare Hosting And Launch

- [ ] 12.1 Select WordPress host.
- [ ] 12.2 Set up staging domain.
- [ ] 12.3 Set up production environment.
- [ ] 12.4 Install SSL.
- [ ] 12.5 Configure CDN if available.
- [ ] 12.6 Configure DNS migration plan.
- [ ] 12.7 Test current site backup/export.
- [ ] 12.8 Freeze content before launch.
- [ ] 12.9 Run full pre-launch QA.
- [ ] 12.10 Launch during low-traffic window.
- [ ] 12.11 Verify DNS propagation.
- [ ] 12.12 Verify SSL.
- [ ] 12.13 Verify redirects.
- [ ] 12.14 Verify forms.
- [ ] 12.15 Verify tracking.
- [ ] 12.16 Verify sitemap indexing.

## 13. Complete Post-Launch QA

- [ ] 13.1 Check form submissions daily for the first week.
- [ ] 13.2 Check Google Search Console daily for the first week.
- [ ] 13.3 Monitor 404s and redirect misses.
- [ ] 13.4 Monitor Core Web Vitals.
- [ ] 13.5 Monitor page speed after plugins and cache settle.
- [ ] 13.6 Review Scale lead routing.
- [ ] 13.7 Confirm phone tracking works.
- [ ] 13.8 Confirm autoresponders fire within 60 seconds.
- [ ] 13.9 Review the first 30 days of analytics and conversion data.
- [ ] 13.10 Prioritize improvements based on real user behavior.

## Immediate Priority Queue

1. Fix `/services/index.html`.
2. Fix mobile contact layout.
3. Fix mobile nav drawer.
4. Remove demo/fabricated testimonials.
5. Replace form demo actions with production form plan.
6. Replace stock/placeholder imagery.
7. Add SEO, schema, sitemap, robots, and redirect foundation.
8. Convert static mockup into reusable WordPress templates.
9. Run full responsive, accessibility, performance, and form QA.
10. Launch only after Scale, legal, analytics, redirects, and content approvals are complete.
