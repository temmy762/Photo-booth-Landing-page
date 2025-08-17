Magic Mirror Photobooth — Aruba (Landing Page)
A single‑page, responsive landing site for the Magic Mirror Photobooth service in Aruba. Built with TailwindCSS (via CDN) and lightweight, vanilla JS for simple interactivity.

Live technologies: Tailwind CDN, Remix Icon CDN, Google Fonts.
No build step required. Open 
index.html
 in a browser.
Project Structure
Photo booth Landing page/
├─ index.html
├─ index.html.bak
├─ assets/
│  ├─ logo.svg
│  └─ images/
│     ├─ logo.jpeg
│     ├─ how-it-works/
│     └─ gallery/
└─ js/  (currently unused)
Key file:

index.html
 — all markup, minimal styles, and scripts are inline.
Features
Home hero with CTA
“Events We Cater To” cards
“How It Works” 4‑step section with images
Gallery with filter and Load More
Packages with pricing cards
Client Reviews:
Mobile: swipeable scroll‑snap slider, 1 card per view
Desktop (md+): 3‑column grid
FAQ accordion (semantic details/summary)
Contact form (mailto flow with basic validation)
Accessibility‑minded markup and ARIA labels
SEO:
Title, icons, and Open Graph-friendly structure
JSON‑LD FAQ schema for rich results
Getting Started
Option A: Double‑click 
index.html
 to open in your browser.
Option B: Use a local server for best results (caching/paths):
VS Code “Live Server” extension, or
Python: python -m http.server then open http://localhost:8000
No npm/yarn or build tools are required.

Editing Guide
Branding:
Replace assets/images/logo.jpeg if needed.
Update <title> and meta where appropriate.
Colors and radius:
Tailwind is configured via tailwind.config inline script in 
index.html
.
Gallery:
Add images to assets/images/gallery/photos/ or videos to assets/images/gallery/videos/
Add new items in the #gallery-grid with gallery-item and data-category="photos|videos|weddings|corporate|parties".
Testimonials:
Each card is a .bg-white ... block inside #testimonials-container.
Mobile slider uses scroll‑snap; add new cards as siblings to existing ones.
Packages:
Edit pricing/details inside #packages.
Contact:
The mail recipient is set in the script: const to = 'fotografiamigransenor@gmail.com';
Subject prefill is supported via data-subject on “Book” buttons.
Social links:
Update hrefs under the Contact and Footer sections.
Mobile Reviews Slider (How it works)
Container #testimonials-container:
Mobile: flex overflow-x-auto snap-x snap-mandatory snap-always scroll-smooth no-scrollbar
md+: md:grid md:grid-cols-3 md:gap-8 md:overflow-visible md:snap-none
Slides:
Mobile: flex-none basis-full snap-center to ensure 1 card per view
md+: revert layout with md:basis-auto md:flex-initial md:snap-none
No external slider library is used.

Deployment
GitHub Pages:
Push this repo to GitHub.
Settings → Pages → Source: “Deploy from a branch”.
Select branch main and / (root).
Save. Your site will be available at https://<username>.github.io/<repo>/.
Any static host (Netlify, Vercel, Cloudflare Pages):
Point to the repo. Publish root with 
index.html
 as the entry.
Known Considerations
Readdy.ai placeholder images are used in some sections; replace with production assets.
The contact form uses mailto:; for a full backend submit, integrate a form service or API.
License
Proprietary. All rights reserved by the project owner. Update this if you intend to open‑source.

Credits
Built by SolvaTree (footer credit).
Icons: Remix Icon.
Fonts: Google Fonts (Pacifico).
TailwindCSS via CDN.
Feedback submitted
