AINGE XHUQI — DEBUT WEBSITE (Sakura Noir)
==========================================

WHAT'S INCLUDED
- index.html        The full site (single file: HTML, CSS, and JS all inline)
- img/               12 photos referenced by the site — keep this folder next to index.html

HOW TO RUN LOCALLY
Just double-click index.html, or open it in any browser. No build step,
no dependencies, no server required.

HOW TO DEPLOY
This is a static site, so it works on any static host:
- Netlify / Vercel: drag-and-drop the whole "ainge-debut-site" folder
- GitHub Pages: push this folder to a repo and enable Pages
- Any regular web host: upload index.html and the img/ folder via FTP,
  keeping them in the same directory together

STRUCTURE / HOW TO EDIT
The site is a single-page app: one HTML file with several "pages"
(<div class="page" id="page-home">, id="page-about", id="page-gallery",
id="page-seating", id="page-playlist", id="page-thankyou">). A top nav bar
(class="topnav") calls a JS function goPage('pagename') to show/hide them —
no routing library, no build tools.

Sections to customize before launch:
1. Event date/time  — search for "25 July 2026" and the countdown target
   `new Date('2026-07-25T18:00:00')` (appears once in <script>).
2. Venue/RSVP info   — id="details", the .info-list rows.
3. About Me content  — id="page-about", .favorites and .quote-block.
4. Gallery photos    — id="page-gallery", .masonry — add/remove <div class="gitem">
   blocks; each just needs an <img src="img/yourfile.jpg">.
5. Seating list       — id="page-seating", .tables-grid — replace the
   "Guest Name #" placeholders with real names (11 tables x 10 seats).
6. Playlist           — id="page-playlist", .track rows.
7. Thank-you credits  — id="page-thankyou", .credits-grid.

DESIGN TOKENS (CSS custom properties, top of <style>)
--ink, --ink-2, --charcoal   background shades
--sakura, --sakura-deep      pink accents
--gold                       metallic accent
--paper                      main text color
--muted                      secondary text color
Change these once and the whole palette updates.

FONTS
Cormorant Garamond (display/serif) + Jost (body/labels), loaded from
Google Fonts via <link> in <head>. Swap the href if you want different fonts.

NO BACKEND
The RSVP button and seating search are front-end only (no form submission,
no database). If you want real RSVP capture, you'll need to wire the RSVP
button to a form service (e.g. Formspree, Netlify Forms) or a backend
endpoint — happy to help with that if needed.
