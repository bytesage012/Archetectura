# ARCHITECTURA — Case Study (Agency)

This project is a portfolio/case-study entry built by the agency to showcase a luxury real-estate client site concept. It demonstrates high-fidelity marketing UI, content sections, and interactive components used when pitching and prototyping client websites.

Overview
- Role: Design + Frontend implementation (prototype). The app is intentionally self-contained as a static case study to illustrate layout, motion, and content hierarchy.
- Goals: Present the company's brand, featured properties, services, team, testimonials and lead capture (visual contact form).
- Outcome: A single-page, responsive marketing experience with accessible navigation, animated testimonial carousel, and reusable UI patterns.

Tech stack
- React (component-driven UI)
- Vite (dev server / build)
- Tailwind CSS (utility-first styling)
- lucide-react (icons)
- External fonts and Unsplash images (used for prototype visuals)

How to run (local)
1. Install dependencies

```bash
npm install
```

2. Start the dev server

```bash
npm run dev
```

3. Build for production

```bash
npm run build
```

Project structure & important files
- `src/App.jsx` — the entire single-page prototype. Contains mock data (`agencyData`) and UI sections: Hero, About, Values, Team, Portfolio, Services, Testimonials, Contact and Footer.
- `index.html`, `vite.config.ts`, `package.json` — standard Vite app files.

App.jsx deep dive (what we implemented)
- Data model: `agencyData` contains structured mock content (company, featuredProperties, services, testimonials, team, values, milestones). This enables swapping content without changing layout.
- Navigation: smooth scroll single-page navigation (`scrollToSection`) with `activeSection` state and a responsive mobile menu (`mobileMenuOpen`).
- Testimonials: auto-rotating carousel using `useEffect` + interval, with controls to pause/play and jump to slides.
- State hooks: `useState` and `useEffect` handle UI state (menu, active section, autoplay), keeping the app purely client-side and framework-agnostic.
- Forms: the contact form is present for visual completeness but is not wired to an API. It should be connected to a serverless function or form service when taking the prototype to production.

Design & implementation notes
- Images and fonts are external (Unsplash, Google Fonts) for rapid prototyping—vendor assets for production.
- The file is intentionally monolithic to keep the prototype self-contained; for production extract components (Nav, Hero, PortfolioCard, TeamCard, Testimonials) into separate files.

Accessibility & performance
- Use semantic HTML and form labels (already present in the markup). Further accessibility improvements: keyboard focus states, aria attributes on carousels, and meaningful alt text for images.
- Performance: lazy-load large images and consider an image CDN or local optimized assets for production.

How to use this as a templated case study
- Replace `agencyData` with real content (or fetch from a CMS).
- Split `App.jsx` into components and add unit tests for interactive logic (carousel, nav behavior).
- Integrate a lead-capture endpoint (serverless function, Netlify forms, or an API).

Contact
- If you'd like, I can split `App.jsx` into components and add a simple mock server endpoint for contact submissions.

