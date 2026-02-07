# Summit Plumbing & Heating

A professional, conversion-focused website template for service businesses -- themed as a plumbing & heating company in Salt Lake City, Utah. Built with Astro and Tailwind CSS 4 for fast load times and easy customization.

![Screenshot placeholder](https://via.placeholder.com/1200x630/080e1c/fb923c?text=Summit+Plumbing+%26+Heating)

> **Live Demo:** [Coming soon](#)

---

## Features

- **4 fully designed pages** -- Home, Services, About, Contact
- **Click-to-call phone links** throughout the site for instant mobile conversions
- **Sticky mobile CTA bar** -- fixed call-now button on mobile devices so visitors can call with one tap from any page
- **Schema.org LocalBusiness structured data** (JSON-LD) for enhanced search engine visibility, including business hours, service area, aggregate rating, and geo coordinates
- **Contact form** powered by [Formspree](https://formspree.io/) -- no backend required
- **Scroll-triggered animations** -- fade-up reveals and staggered children using Intersection Observer (no JS library needed)
- **Responsive mobile navigation** with hamburger menu and animated open/close icons
- **Trust badges section** -- licensed/insured, star rating, years in business, 24/7 emergency
- **Testimonials section** with star ratings and customer attribution
- **Service area callout** listing 10+ served communities
- **Stats section** with animated counters (17+ years, 12 technicians, 4.9 stars, 10k+ jobs)
- **Team photo and Google Maps placeholders** -- ready to swap in real assets
- **Open Graph meta tags** and canonical URLs on every page
- **Custom color system** -- navy/orange palette defined via Tailwind 4 `@theme` block
- **Custom typography** -- DM Serif Display (headings) + Outfit (body) via Google Fonts
- **Subtle texture effects** -- hero crosshatch pattern, noise overlay on footer
- **Static output** -- pre-rendered HTML, zero JavaScript frameworks at runtime
- **100% static deployment** -- works on Vercel, Netlify, Cloudflare Pages, or any static host

## Tech Stack

| Technology | Purpose |
|---|---|
| [Astro 5.x](https://astro.build/) | Static site generator |
| [Tailwind CSS 4](https://tailwindcss.com/) | Utility-first styling via `@tailwindcss/vite` plugin |
| [Schema.org](https://schema.org/) | LocalBusiness + Plumber structured data |
| [Formspree](https://formspree.io/) | Form handling (no backend) |
| [Google Fonts](https://fonts.google.com/) | DM Serif Display + Outfit |
| SVG (Heroicons-style) | Inline icons, no icon library dependency |

## Project Structure

```
/
├── public/
│   ├── favicon.ico
│   └── favicon.svg
├── src/
│   ├── layouts/
│   │   └── BaseLayout.astro      # Shared layout: head, nav, footer, sticky CTA, Schema.org
│   ├── pages/
│   │   ├── index.astro            # Home — hero, trust badges, services overview, testimonials
│   │   ├── services.astro         # Services — 8 service cards, "Why Summit" section, CTA
│   │   ├── about.astro            # About — company story, values, stats, team photo placeholder
│   │   └── contact.astro          # Contact — form, phone, email, hours, map placeholder
│   └── styles/
│       └── global.css             # Tailwind 4 @theme config, animations, component classes
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

## Quick Start

```bash
# Clone the repository
git clone https://github.com/SeekerErebus/service-business-template.git
cd service-business-template

# Install dependencies
npm install

# Start the dev server
npm run dev
```

Open [http://localhost:4321](http://localhost:4321) to view the site.

## Commands

| Command | Action |
|---|---|
| `npm install` | Install dependencies |
| `npm run dev` | Start dev server at `localhost:4321` |
| `npm run build` | Build production site to `./dist/` |
| `npm run preview` | Preview production build locally |

## Customization

### Replace placeholder content

1. **Business info** -- Update the company name, phone number, address, and email in `src/layouts/BaseLayout.astro` (both the visible content and the Schema.org JSON-LD block)
2. **Formspree** -- Replace `YOUR_FORM_ID` in `src/pages/contact.astro` with your actual [Formspree](https://formspree.io/) form ID
3. **Google Maps** -- Uncomment and replace the Maps embed code in `src/pages/contact.astro`
4. **Team photo** -- Replace the placeholder in `src/pages/about.astro` with a real image
5. **Colors** -- Edit the `@theme` block in `src/styles/global.css` to change the navy/orange palette
6. **Fonts** -- Swap the Google Fonts link in `BaseLayout.astro` and update `--font-display` / `--font-sans` in `global.css`
7. **Services** -- Edit the `services` array in `src/pages/services.astro` to match your actual offerings
8. **Testimonials** -- Update the testimonial cards on the home page with real customer reviews

### Deploy

This template outputs static HTML and can be deployed anywhere. Recommended free-tier options:

```bash
# Build for production
npm run build

# Output is in ./dist/ — deploy to any static host
```

- **Vercel**: `npx vercel --prod`
- **Netlify**: drag-and-drop `dist/` folder or connect your repo
- **Cloudflare Pages**: connect your repo and set build command to `npm run build`, output directory to `dist`

## License

MIT License. Use this template for client projects, personal sites, or anything else. No attribution required.
