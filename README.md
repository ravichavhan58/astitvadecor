# Astitva Decoration — Interior Design Website

A responsive React + Vite website with separate routed pages, a shared rotating visual banner below the navigation on every page, a hover-expand social rail, gallery image lightbox, and room-wise decor budget planner.

## Pages
- Home: `/`
- About Us: `/about`
- Services: `/services`
- Gallery: `/gallery`
- Budget: `/budget`
- Contact Us: `/contact`

## Run locally
1. Install Node.js (LTS).
2. Extract this ZIP and open the project folder in VS Code.
3. Run `npm install`.
4. Run `npm run dev` and open the local URL shown in the terminal.
5. Run `npm run build` to create the production build in `dist`.

## Project structure
- `src/components/` — Header, shared page layout, slider, social rail, image lightbox
- `src/context/` — Shared room and budget planner state
- `src/pages/` — Home, About, Services, Gallery, Budget and Contact pages
- `src/data/` — Slider images, gallery samples and room/item catalogue
- `src/assets/` — Local asset folder for your logo and future project photos
- `public/` — PWA manifest and service worker

## Before publishing
- Replace `+91 XXXXX XXXXX` in `src/pages/Contact.jsx` with your actual business number.
- Set your WhatsApp business number in the `send` function in `src/pages/Budget.jsx` and the contact form. Current links use `wa.me/?text=` and open WhatsApp's contact chooser.
- Replace sample Unsplash photos in `src/data/site.js` and page components with your own project photos. Gallery images open in a full-screen lightbox; close with the X, click outside, or press Escape. Arrow keys and on-screen arrows move between images.
- Update business address, social profile URLs, service descriptions and sample catalogue prices.
- Sample catalogue rates are indicative only, not confirmed quotations.

## Notes
- The site is enquiry-led; it has no cart, payment gateway or checkout.
- The budget planner lets customers choose multiple rooms, add room-specific items, adjust quantities, calculate an estimate and send the item list to WhatsApp.
- The PWA service worker caches the app shell and same-origin assets as they are visited. External image URLs may need a first successful visit to be available offline; for reliable offline gallery viewing, add optimized project images to the local `public` folder.
- For production hosting, configure the web server to serve `index.html` for client-side routes (SPA fallback).

## Latest gallery and routing updates
- All route declarations are maintained in `src/routes/AppRoutes.jsx`.
- Gallery has All, Home Decor, Events and Other tabs.
- Click a gallery image to open the full-screen photo viewer; use arrows or keyboard arrow keys to browse and Escape/outside click/X to close.
- Slider photos, page changes, gallery cards and the photo viewer have subtle transitions. Reduced-motion preferences are respected.
- If a remote sample image cannot load, a local branded fallback visual is shown from `public/gallery-fallback.svg`.


## Latest gallery and routing refinements

- Gallery includes All, Home Decor, Events and Other category tabs.
- Each gallery item has a bundled local SVG fallback, so the gallery still displays artwork if a remote photo host is blocked or offline. Replace the sample Unsplash photo URLs in `src/data/site.js` with your own project photographs when ready.
- Open a gallery image to use the full-screen viewer. Navigate with arrows, keyboard arrow keys, or swipe on touch screens; close with the X button, Escape, or outside click.
- All page paths are maintained in `src/routes/routeConfig.jsx` and rendered by `src/routes/AppRoutes.jsx`.
- Page, gallery, hero-slider and image-viewer transitions are animated. Scrollbars are visually hidden while normal scrolling remains enabled.
"# astitvadecor" 
