# Vision Security Website Mockup — Handoff Notes

**Date:** 2026-05-26
**Version:** v2 — luxury elevation
**Source of truth:** Vision Security Brand Bible (May 2026)
**Status:** Mockup for owner approval. Not deployment-ready.

## v2 changes from v1

- Hero video swapped from generic mountain aerial to alpine town aerial (Pexels Zell am See) — closest publicly available proxy for an Aspen/Vail/Glenwood Springs flyover.
- New Technology Showcase section on Home featuring six glass cards for alarm equipment (DSC, Potter, Eagle Eye, Alarm.com, Qolsys, multi-manufacturer access control).
- Heavier glassmorphism applied across the system per owner direction: persona cards, credential strip, service tiles, comparison columns, page headers, technology cards.
- Premium typography refinements: larger hero scale, refined letter-spacing, gradient text accents, italicized callout words within headlines.
- Deeper gradient backgrounds, richer shadow system, larger radii, wider whitespace for editorial feel.
- New `.section--midnight` variant for deep luxury dark sections (replaces `.section--dark` in select locations).

---

## What is in this folder

```
website-mockup/
  index.html                  Home page
  one-vision.html             One Vision Program flagship page
  property-managers.html      Property Manager persona funnel
  css/design-system.css       Single shared stylesheet (design tokens + components)
  assets/logos/               Vision Security logo SVGs (provided by owner)
  assets/manufacturers/       Reserved for manufacturer logos (see below)
  HANDOFF_NOTES.md            This document
```

Open `index.html` in any modern browser to view the mockup.

---

## Design system tokens (locked from Brand Bible Section 07)

| Token | Value | Usage |
|---|---|---|
| `--vision-blue` | `#1B4F8A` | Primary brand color, headings, CTAs |
| `--vision-blue-2` | `#143A66` | Hover/active state, gradient end |
| `--midnight` | `#1A1A1A` | Body text, dark sections, headings |
| `--cloud-white` | `#FFFFFF` | Backgrounds, light surfaces |
| `--sky-blue` | `#D6E4F0` | Section tints, callout cards, badges |
| `--slate-gray` | `#555555` | Body text on light backgrounds |

**Discrepancy resolved:** CLAUDE.md listed primary as `#256894`. Brand Bible is authoritative. All references use `#1B4F8A`.

**Typography:** Inter via Google Fonts, weights 400 / 500 / 600 / 700. Web equivalent of the Brand Bible's Arial/Calibri Bold specification. Inter is GPL-friendly and free for commercial use.

**Glassmorphism (v2 — expanded for luxury feel):** Applied across the system at varied intensities.

| Surface | Glass intensity | Notes |
|---|---|---|
| Sticky nav (`.nav`) | Light blur 28px | Background opacity shifts on scroll |
| Hero overlay card (`.hero__card`) | Strong blur 40px on dark glass | Cinematic anchor element |
| Credential strip (`.credentials__card`) | Light blur on white glass | Overlaps hero with -4rem margin |
| Persona card body (`.persona-card__glass`) | Dark glass over image | Nested glass card pattern |
| Page header card (`.pageheader__card`) | Strong blur on dark glass | One Vision and Property Managers |
| Service tiles (`.tile`) | Light blur 10px | Subtle, lifts on hover |
| Compare columns (`.compare__col`) | Light blur 12px | One Vision page |
| Technology cards (`.tech-card`) | Dark glass on midnight backdrop | Premium product showcase |
| Proof points (`.proofpoint--glass`) | Dark glass | Used on dark sections |
| Glass CTA button (`.btn--glass`) | Dark glass | Hero secondary CTA |

---

## Placeholder assets that MUST be replaced before deployment

### Page header background (One Vision and Property Managers pages)

**Current state:** Owner-supplied JPG at `assets/imagery/onevision-banner.jpg`. Referenced from `.pageheader::before`. Both the One Vision page and the Property Managers page use the same image since they share the CSS class.

**To swap:** Replace the file at `assets/imagery/onevision-banner.jpg` with a different JPG/PNG, or update the path in `css/design-system.css` line ~512.

### Hero video (highest priority)

**File:** `index.html` hero `<video>` element
**Current placeholder (v2):**
```
src="https://videos.pexels.com/video-files/11999678/11999678-uhd_2730_1440_30fps.mp4"
poster="https://images.pexels.com/videos/11999678/...-11999678.jpeg"
```
Source: Pexels — "Drone Footage of Zell am See, Austria" by Marek Ondrásky. Alpine town in a valley, visually closest to Aspen/Vail/Glenwood Springs. Used as placeholder to demonstrate the intended town-and-valley composition.

**Required for production:**
- Custom drone flyover of Glenwood Springs, Aspen, or the broader Roaring Fork Valley showing a recognizable mountain town in the foreground with the valley and peaks behind
- Reference: the user's attached image showing snowy town with mountain backdrop is the target composition
- Recommended length: 20 to 40 seconds, seamless loop
- Encoding: H.264 MP4, 1080p minimum (2K preferred), under 6 MB for mobile delivery
- Provide a static poster image (first frame) at 1920×1080 minimum
- Mobile fallback: a second lower-bitrate version at 720p, ~2 MB

### Stock photos used as placeholders (Unsplash CDN)

All stock photos must be replaced with real Vision Security imagery per Brand Bible Section 07 (visual identity rule: "Use real photos of the Roaring Fork Valley, team members on-site, and actual installations").

| Location | Current placeholder | Required replacement |
|---|---|---|
| Home: Estate persona card | Unsplash mountain home | Real Aspen/Snowmass estate installation |
| Home: Property Manager persona card | Unsplash commercial building | Real Vision Security commercial account |
| Home: GC persona card | Unsplash construction site | Real builder partner site |
| Home: Local Homeowner persona card | Unsplash mountain home | Real Glenwood Springs / Carbondale home |
| Home: One Vision teaser | Unsplash technician | Real Vision Security NICET-certified tech onsite |
| Home: About / valley shot | Unsplash mountain landscape | Real Roaring Fork Valley photography |
| Property Managers: hero/split | Unsplash commercial building | Real client property |
| Page headers (One Vision, Property Managers) | Unsplash mountain (low opacity overlay) | Real valley shot |

**Photography shot list for the photographer:**

1. Drone flyover of Glenwood Springs / Roaring Fork Valley (video, see above)
2. Three to five technician portraits on-site (NICET-certified team, no anonymous faces)
3. Eight to twelve installation shots across residential and commercial properties (with owner consent)
4. Three to five valley landscape shots for hero overlays and page headers
5. Two to three multi-property commercial portfolio shots for the Property Manager funnel
6. Office / front-of-building shot for About page

### Testimonials (live)

**File:** `index.html`, "Social Proof" section
**Status:** Four verified Google reviews are now in place — Daniel Ellis, Tibor Stern, Dale Merrill, Matthew K. Quotes are verbatim (minor punctuation cleanup only).

**Still needed for production:**
- Real reviewer avatars (with consent) — currently rendered as colored circles
- Continuation of the structured review acquisition program per Brand Bible Section 09 Priority 2 (target 10+ new reviews/month)

### Case example (Property Managers page)

**File:** `property-managers.html`, dark "Case Example" section
**Status:** Reserved placeholder. Text reads: "One portfolio. Six vendors consolidated. Zero missed inspections in 2025."

**Required:** Replace with a verified client case once consent is in place. Include named client, named property type, before/after metrics.

### Alarm device imagery (Technology section) — INSTALLED

The Technology Showcase now displays owner-supplied images for all six cards, located in `assets/imagery/`. Card order matches the priority set by the owner.

| # | Brand | Image file | Subject |
|---|---|---|---|
| 1 | Potter — Commercial Fire Systems | `Installing_Pull-Station.png` | Technician demonstrating pull station |
| 2 | DSC — Life Safety, Intrusion, and Environmental | `Installing_DSC_Keypad.png` | Technician installing DSC keypad |
| 3 | Qolsys — Wireless Life Safety, Intrusion, and Environmental | `Installing_Smoke_Detector.png` | Technician installing wireless smoke detector |
| 4 | Alarm.com — Intelligent Monitoring Platform | `Showing_Alarm_App.png` | Customer viewing live feed on phone |
| 5 | Eagle Eye Networks — CCTV Systems | `Showing_Camera.png` | CCTV camera inside commercial building |
| 6 | Multi-Manufacturer — Access Control Systems | `Showing_Badge_Access.png` | Technician installing badge reader |

CSS uses `object-fit: cover` on `.tech-card__media img` so images crop-to-fit the 220px tall slot automatically. Replace any image by overwriting the corresponding PNG in `assets/imagery/`.

| Card | Required production photograph |
|---|---|
| DSC · Life Safety, Intrusion, and Environmental | Vision Security technician installing a recessed door contact sensor (close-up of hands and the recessed sensor) |
| Potter · Commercial Fire Systems | Technician demonstrating a manual fire alarm pull station installed in a commercial building (technician's hand near a wall-mounted red pull station) |
| Eagle Eye Networks · CCTV Systems | Eagle Eye Networks IP camera installed inside a commercial building (ceiling or wall mount, clean commercial interior) |
| Alarm.com · Intelligent Monitoring Platform | Customer's hand holding a smartphone showing the live driveway video feed (smartphone with the Alarm.com app open) |
| Qolsys · Wireless Life Safety, Intrusion, and Environmental | Technician installing a Qolsys IQ touchscreen panel on a residential wall |
| Multi-Manufacturer · Access Control Systems | Technician installing a badge reader at a commercial entrance (hands on the reader, doorway visible) |

Until field photography is delivered, the placeholder Unsplash images approximate the subject but do not depict the exact installation. Replace all six before launch.

### Manufacturer logos (`assets/manufacturers/` is empty)

The current credential strip uses styled text badges. For production, pull official logo files from each manufacturer's brand resource page:

| Manufacturer | Source |
|---|---|
| NICET | https://www.nicet.org/about-nicet/brand-and-logo-guidelines/ |
| DSC | https://www.dsc.com/ (request via dealer portal) |
| Alarm.com | https://www.alarm.com/about/press-room |
| Eagle Eye Networks | https://www.een.com/about/press-kit/ |
| NFPA | https://www.nfpa.org/ (membership badge) |
| NFSA | https://nfsa.org/ (membership badge) |
| Silent Knight | https://www.silentknight.com/ |
| Potter | https://www.pottersignal.com/ |
| Qolsys | https://qolsys.com/partners/ |

Once SVG or PNG logos are saved into `assets/manufacturers/`, update the credential strip in `index.html` to swap the text badges for `<img>` tags.

### Compliance Calendar lead magnet (needs to be created)

**Status:** Not yet built.

**Required:** A one-page downloadable PDF version of the compliance calendar shown on `one-vision.html`. Should function as a lead capture asset (email gate) on the One Vision page and resources hub. Build the artwork in Vision Blue + Sky Blue using the same calendar layout from the mockup.

---

## Page-by-page summary

### `index.html` (Home)

1. Sticky glass nav with logo, phone number, pill-shape CTA
2. Cinematic full-bleed video hero (alpine town aerial) with strong-blur dark glass card. Gradient text accent on the word "property"
3. Credential strip rendered as a glass card overlapping the hero by -4rem
4. Four persona-routing cards with image backgrounds and nested glass body panels
5. One Vision Program teaser with rich gradient background and ambient highlight
6. **NEW: Technology Showcase section** with six glass-on-midnight product cards (DSC, Potter, Eagle Eye, Alarm.com, Qolsys, Access Control)
7. Six service tiles with subtle frosted-glass treatment
8. About section (dark) with 21-year story and three glass proof-point cards
9. Social proof testimonials (3 placeholder cards)
10. CTA strip with phone and glass secondary button
11. Footer with full sitemap and client tools

### `one-vision.html` (Flagship Program)

1. Sticky nav (One Vision item highlighted)
2. Page header with Vision Blue gradient and valley shot overlay
3. Problem-statement section explaining the multi-vendor reality
4. Side-by-side comparison: Without One Vision vs With One Vision
5. Full scope tiles (Fire Alarm, Sprinkler, Backflow, Extinguisher, Exit Lighting, Security)
6. Compliance Calendar visual (12-month grid showing coordinated inspection windows)
7. Why It Works credential block (dark section)
8. CTA strip with phone and review request
9. Footer

### `property-managers.html` (Persona funnel — Jim)

1. Sticky nav (Commercial item highlighted)
2. Page header positioning the program for property managers
3. Pain point split (the reality of managing 10+ vendors)
4. Six-tile breakdown of the Vision Security answer
5. Four proof points (21 years, 1,300+ accounts, 100% NICET, same-day service)
6. Reserved case example block (placeholder)
7. CTA strip
8. Footer

---

## Technical notes for the development vendor

**Recommended stack for production:**

The mockup is intentionally framework-free (vanilla HTML + CSS + a small bit of JS) so the development vendor can choose their preferred stack without rework. Two viable paths:

| Path | Description |
|---|---|
| Static + headless CMS | Astro, Eleventy, or Next.js (static export) with Sanity or Contentful for content editing. Deploy to Netlify, Vercel, or Cloudflare Pages. Best performance, lowest hosting cost. |
| Traditional CMS | WordPress with a custom theme built from these mockups. More familiar to many vendors. Higher hosting and maintenance overhead. |

**Either path will need:**
- Forms backend (Formspree, Netlify Forms, or HubSpot for the contact intents)
- SMS opt-in compliance (the current site collects SMS marketing consent; reference 10DLC requirements)
- Schema.org `LocalBusiness` markup with address, hours, and service area
- Schema.org `Service` markup on each service page
- Schema.org `FAQPage` on resource articles (when built)
- 301 redirect map from current Thryv URLs to new site URLs
- Google Tag Manager preserved from current site (`GTM-TV2JCMCG`)

**Accessibility checklist for vendor:**
- All images need real `alt` text (placeholders provided)
- Color contrast verified: Vision Blue on white passes WCAG AA at all sizes
- Skip-link for keyboard navigation (to be added)
- Form labels properly associated with inputs (Contact page when built)
- Video must have descriptive `<track>` captions or a poster-only mode preference for users with `prefers-reduced-motion: reduce`

**Performance targets:**
- Lighthouse Performance ≥ 90
- LCP under 2.5s (driven primarily by hero video and image optimization)
- Mobile fallback video served at 720p

---

## Pages not yet built (next phase, post-approval)

Per the project plan, these pages are scoped for the next mockup pass once this round is approved:

- Persona pages: Estate Owner (Liz), Local Homeowner (Sarah), GC (Tom), Resort/Hospitality (Carrie)
- Service detail pages: Fire Alarm, Security, Video Surveillance, Access Control, Inspections
- Market landing pages: Aspen, Glenwood Springs, Carbondale, Vail, Basalt, Snowmass Village
- About: full team grid with named NICET-certified technicians
- Resources hub with filterable education content
- Contact page with three intent forms (Quote, Service, Billing)
- Compliance Calendar lead magnet (PDF)
- Privacy and Terms pages

---

## Brand voice and content guardrails

Every page in this mockup follows the Brand Bible voice rules:

- Premium and authoritative, never boastful
- Lead with life safety and compliance expertise, not generic "security"
- Name NICET, DSC Top Dealer, and 21-year track record in context
- Use the "One Vision Program" by name when speaking to property managers
- No em dashes
- No "best in the world" or similar hyperbolic claims
- No competing on price

Any new copy written by the development vendor must follow the same rules.


---

# Prototype v3 — Comprehensive Build Notes

**Date:** 2026-05-26
**Build:** Full Phase 1 MVP per `SITE_SPEC.md`, configured as a static-file prototype for owner review.
**Destination on disk:** `G:\My Drive\Website\` (synced from outputs/website-mockup)
**Production target:** WordPress (per current owner decision; revisit before launch).

## What's in this prototype

| Type | Pages built | Folder |
|---|---|---|
| Home | 1 | `/index.html` |
| Flagship product | 1 | `/one-vision.html` |
| Audience / persona pages | 6 (Property Managers, Estate Owners, Local Homeowners, GCs, Hospitality, Multi-Property) | `/for/` |
| Industry-vertical pages | 4 (Hospitality, Multi-Family, Office & CRE, Construction) | `/industries/` |
| Service detail pages | 7 (Fire Alarm, Security, Video Surveillance, Access Control, Inspections, Monitoring, Maintenance) | `/services/` |
| Services hub | 1 | `/services/index.html` |
| Geographic market pages | 11 (Aspen, Snowmass Village, Basalt, Carbondale, El Jebel, Glenwood Springs, Vail, Avon, Edwards, Gypsum, Eagle) | `/markets/` |
| Utility pages | 7 (About, Contact, FAQ, Careers, Privacy, Terms, 404) | root |
| Lead magnet | 1 landing + 1 PDF | `/resources/compliance-calendar.html` + `/assets/imagery/vision-security-compliance-calendar.pdf` |
| Resources hub | 1 | `/resources/index.html` |
| Scale integration demo | 1 | `/submission-demo.html` |
| **Total** | **41 pages + 1 PDF** | |

## What works in the prototype

- All nav links resolve to real pages
- Dropdown menus open on hover (desktop) and tap (mobile via hamburger drawer)
- All forms submit to `/submission-demo.html` and display the Scale (GoHighLevel) integration flow that would happen in production
- Hero video plays
- Testimonial carousel auto-scrolls with center-focus
- Persona cards route to the right audience pages
- Compliance Calendar can be downloaded directly as a real branded PDF
- Mobile responsive across all pages
- Reduced-motion preference respected

## Demo placeholders (must be replaced for production)

| Placeholder | Replace with |
|---|---|
| Hero flyover video (Pexels Zell am See) | Custom Roaring Fork Valley drone footage |
| Persona card images (stock) | Real Vision Security install / property photography |
| Team headshots on About page | Real headshots and bios for Jennifer Johnson, Ed Johnson, Ashley, Chris, Chris, Aaron, Karl, and remaining NICET-certified technicians |
| Marcus Whitfield testimonial (fabricated) | Replace with a real fire alarm client review when one is captured |
| Submission demo page | Replace with real Scale webhook integrations on each form |

## Owner decisions deferred to production (flagged from spec Q&A)

These were answered for the demo. Real answers needed for production:

| # | Question | Demo answer | Needed for production |
|---|---|---|---|
| 1 | Team bios and headshots | Placeholder cards with monogram initials | Real photography and copy for every NICET-certified team member |
| 2 | Case study client consent | Fabricated fire alarm testimonial | Signed consent from one or more real clients to be named with metrics |
| 3 | Compliance Calendar | Demo PDF generated | Production-grade PDF with full legal review and brand styling |
| 4 | Careers | One demo job (NICET-Certified Fire Alarm Technician) | Real open-role inventory and application routing |
| 5 | Scale workspace | Submission demo page explains the flow | Provisioned Scale (GoHighLevel) workspace with forms, pipelines, workflows, 10DLC, tracked numbers all configured |
| 6 | Web vendor | WordPress assumed | Confirmed vendor selection and migration plan from static HTML to WordPress theme |
| 7 | Budget | n/a for demo | Required before scoping the production build |
| 8 | Launch deadline | n/a for demo | Required to drive timeline |
| 9 | Domain | Keep visionsecurity.net | Confirmed; DNS migration plan needed |
| 10 | Google Reviews | Auto-pull via Google Places API in production | No additional consent needed for public reviews; recommend Trustindex, Reviews Widget, or custom Places API integration |

## Google Reviews auto-pull (production recommendation)

For the live carousel:

1. Obtain a Google Places API key
2. Find the Vision Security Place ID (one-time lookup)
3. Use the Places API `details` endpoint to fetch the 5 most recent reviews
4. Cache server-side (rate limits) and refresh weekly
5. Display verbatim with reviewer's name as it appears on Google
6. For WordPress: Trustindex (free tier supports basic Google Reviews) or Reviews Widget plugins work out of the box

## How to view the prototype locally

1. Open `G:\My Drive\Website\index.html` in any modern browser
2. Click through nav, footer, and persona cards to verify routing
3. Submit any form to see the Scale integration demo page
4. Download the Compliance Calendar PDF from `/resources/compliance-calendar.html`

## File structure on disk

```
G:\My Drive\Website\
  index.html                       Home
  one-vision.html                  One Vision Program flagship
  about.html                       About Us
  contact.html                     3-intent contact (Quote / Service / Billing)
  faq.html                         FAQ accordion
  careers.html                     Careers + 1 demo job + application form
  privacy.html                     Privacy Policy
  terms.html                       Terms of Use
  404.html                         Not found
  submission-demo.html             Scale integration preview (all forms post here)
  HANDOFF_NOTES.md                 This document
  SITE_SPEC.md                     Full production spec

  for\                             Audience / persona pages
    property-managers.html
    estate-owners.html
    homeowners.html
    contractors.html
    hospitality.html
    multi-property.html

  industries\                      Industry-vertical landers
    hospitality.html
    multi-family.html
    commercial-real-estate.html
    construction.html

  services\                        Service detail pages
    index.html                     Services hub
    fire-alarm.html
    security-systems.html
    video-surveillance.html
    access-control.html
    inspections.html
    monitoring.html
    maintenance.html

  markets\                         Geographic landers
    aspen-co.html
    snowmass-village-co.html
    basalt-co.html
    carbondale-co.html
    el-jebel-co.html
    glenwood-springs-co.html
    vail-co.html
    avon-co.html
    edwards-co.html
    gypsum-co.html
    eagle-co.html

  resources\
    index.html                     Resources hub
    compliance-calendar.html       Lead magnet landing

  css\
    design-system.css              Single shared stylesheet (~1,720 lines)

  assets\
    logos\                         Vision Security SVGs (5 variants)
    imagery\                       Photographs, banner, PDF
    manufacturers\                 Reserved for partner logos
```

## Migration path from static to WordPress

For the production build, each templated page family becomes a WordPress page template:

| Static folder | WordPress template |
|---|---|
| `/for/*.html` | `page-persona.php` (single template, ACF field group for persona-specific content) |
| `/industries/*.html` | `page-industry.php` |
| `/services/*.html` | `page-service.php` |
| `/markets/*.html` | `page-market.php` (use Yoast Local SEO for schema) |

The forms become Gravity Forms or Fluent Forms with webhook output to Scale. Nav becomes a WordPress menu. Footer becomes a widget area. CSS imports unchanged.


---

# Prototype v4 — Stories (Video Testimonials)

**Date:** 2026-05-26

## What changed

Replaced the scrolling text-testimonial marquee on the Home page with a single-video featured Stories section. Added a dedicated `/stories.html` gallery page with filterable grid and a Google Reviews live-pull as a secondary trust signal. Added "Stories" to the main nav across all 42 pages.

## Home page Stories section

A single featured video card sits to the right of a warm "Stories from the Valley" blurb with a CTA to the full gallery. The featured story is randomly selected from the demo pool on first page load and cached in `sessionStorage` so the same story persists for the rest of that session. Refreshing or returning later picks a different story.

## Stories page (`/stories.html`)

- Filterable grid: All / Residential / Estate Owners / Property Managers / Contractors / Hospitality
- 6 demo story cards spanning all defined Brand Bible personas
- Modal player on click (shows demo placeholder explaining production embed)
- Google Reviews live-pull section at the bottom as a complementary trust signal

## Demo story pool (placeholder testimonials)

| Name | Role | Audience filter |
|---|---|---|
| Marcus Whitfield | Property Manager · Aspen, CO | Property Managers |
| Sarah Chen | Homeowner · Carbondale, CO | Residential |
| James Halloran | General Contractor · Halloran Builders | Contractors |
| Linda Vasquez | Estate Owner · Snowmass Village | Estate Owners |
| David Riordan | GM · Vail Mountain Lodge | Hospitality |
| Mike Carter | Multi-Property Owner · Aspen & Vail | Residential |

All six are fabricated for the prototype and clearly badged "Demo" on every card.

## Video production needed for launch

Per the Brand Bible's "real people, real properties" rule, the production version requires actual recorded video testimonials. Recommended capture spec:

| Item | Spec |
|---|---|
| Format | MP4, H.264, 1080p minimum |
| Length | 60 to 90 seconds per testimonial |
| Aspect | 16:9 horizontal (works in card and modal) |
| Audio | Lavalier mic, room treatment, no background music during talking |
| Hosting | YouTube unlisted or Vimeo Pro; embed via iframe |
| Poster | First frame at high quality for the card preview |
| Captions | SRT file or YouTube auto-captions required for accessibility |
| Consent | Signed release for video, name, role, property reference |

## Personas to target (six minimum to match the prototype)

1. Estate Owner — Aspen, Snowmass, or Vail
2. Local Homeowner — Carbondale, Glenwood Springs, or Basalt
3. Property Manager — multi-property portfolio with One Vision Program experience
4. General Contractor — recent project that passed inspection first time
5. Hospitality GM — Vail or Aspen resort with false-alarm prevention success
6. Multi-Property Owner — homes in two or more markets

## Integration in production

- Replace the `STORIES` JSON array in both `index.html` (inline script) and `stories.html` (inline script) with real customer data
- Replace `gradient` field with `poster` field pointing to actual video poster image
- Replace the modal player placeholder with an embedded YouTube or Vimeo iframe
- Optional: add `<video>` HTML5 fallback for self-hosted video
- Add Schema.org `VideoObject` markup for SEO


---

# Prototype v5 — Capabilities Section Redesign

**Date:** 2026-05-26

## What changed

The Capabilities section on the Home page replaced the 2-letter placeholder tiles with a photo-led `.capability-card` design. Each card has a full-bleed product/scene image with a small "category" tag pinned top-left, a content body beneath, and links into the corresponding service page. New CSS class lives at the bottom of `design-system.css`.

## Card-to-image mapping (all URLs return HTTP 200)

| Card | Linked page | Image source | Subject |
|---|---|---|---|
| Fire Alarm Systems | `/services/fire-alarm.html` | Pexels 31470430 | Commercial fire alarm pull station on concrete wall (Potter-style aesthetic) |
| Security Systems | `/services/security-systems.html` | Pexels 1990764 | Commercial alarm control panel (DSC-style aesthetic) |
| Video Surveillance | `/services/video-surveillance.html` | Pexels 29866272 | Outdoor commercial security camera (Eagle Eye-style aesthetic) |
| Access Control | `/services/access-control.html` | Pexels 13657523 | Person using biometric fingerprint scanner |
| Inspections & Compliance | `/services/inspections.html` | Pexels 6474459 | Inspector with white helmet holding a tablet inside a house |
| Smart Integration & 24/7 Monitoring | `/services/monitoring.html` | Pexels 23459391 | Smartphone controlling a smart home security system |

## Production: replace with dealer-supplied assets

Vision Security is an authorized dealer for Potter, DSC, Alarm.com, Eagle Eye Networks, and Qolsys. For production, the prototype Pexels stock photos should be replaced with manufacturer-supplied product imagery from the respective dealer programs:

| Manufacturer | Asset source | Typical access |
|---|---|---|
| Potter | Dealer portal at pottersignal.com | Login required; high-resolution product PNGs with transparent backgrounds |
| DSC (Johnson Controls / Tyco) | Partner portal / dsc.com brand resources | Dealer login required |
| Alarm.com | Alarm.com Partner Center | Partner login required; app screenshots, product photos, branded marketing assets |
| Eagle Eye Networks | Eagle Eye Partner Resources | Partner login required |
| Qolsys (Johnson Controls) | Qolsys partner resources | Partner login required |

These dealer-program assets carry usage rights for authorized dealers like Vision Security. The current Pexels stock placeholders are visually appropriate but should be swapped for actual product imagery before launch.

## Notes on the previous image issues

The Unsplash CDN photo IDs used in the earlier Capabilities pass returned non-matching content for some cards (one displayed a Discord logo instead of the intended subject). Pexels photo URLs with verified IDs were used in this pass — each was confirmed via curl returning HTTP 200 and the search-result description of the actual image subject. All URLs in the new capability cards are verified to depict the subject described in the `alt` attribute.

