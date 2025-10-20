# Faith Travels — Travel Discovery Web App (Frontend Prototype)

![Status](https://img.shields.io/badge/Status-Prototype-blue)
![React](https://img.shields.io/badge/React-18-61DAFB?logo=react\&logoColor=white\&labelColor=20232a)
![CRA](https://img.shields.io/badge/Bootstrapped%20with-Create%20React%20App-09D3AC?logo=create-react-app\&logoColor=white\&labelColor=20232a)
![Bootstrap 5](https://img.shields.io/badge/Bootstrap-5-7952B3?logo=bootstrap\&logoColor=white)

A responsive, brochure-style travel UI for browsing tours and destinations. This is a **frontend-only prototype** focused on navigation, galleries, and tour cards. There is **no booking/checkout flow** and **no single-tour detail page** (browse-only).

> Live Demo: *https://faith-travels-booking-site.vercel.app/* 

---

## Table of Contents

* [Features](#features)
* [Screenshots](#screenshots)
* [Tech Stack](#tech-stack)
* [Getting Started](#getting-started)
* [Available Scripts](#available-scripts)
* [Project Structure](#project-structure)
* [Architecture Notes](#architecture-notes)
* [Testing](#testing)
* [Performance & Accessibility](#performance--accessibility)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [License](#license)

---

## Features

* **Multi-route navigation**: `HOME`, `ABOUT US`, `TOURS`, `DESTINATION`, `GALLERY`, `CONTACT` with a persistent **Book Now** CTA (leads to contact/intent).
* **Tours grid**: Card layout with **location**, **rating & reviews**, **category badges** (e.g., *Escorted Tour*, *River Cruise*), **“from” price**, and **duration** (days/nights).
* **Media-rich browsing**: Hero/featured **carousels** (`react-slick`) and **lightbox galleries** (`react-image-gallery`, `react-lightbox-gallery`).
* **Date picker (UI only)**: `react-datepicker` wired for selection/validation, not persisted (no backend).
* **Responsive**: Built with **Bootstrap 5 / React-Bootstrap** utilities and components.
* **Quality baseline**: Smoke tests with **Jest + Testing Library**; **Web Vitals** hook included.

---

## Screenshots

> Put images in `docs/` and adjust paths below.

Navbar
<img width="1899" height="906" alt="image" src="https://github.com/user-attachments/assets/d9db0709-4049-4866-881c-bda254184d34" />
![Navbar](docs/screenshot-navbar.png)

Tours Grid (cards, badges, pricing, duration)
<img width="1899" height="903" alt="image" src="https://github.com/user-attachments/assets/879d711d-c719-4964-87fb-e4f94f89240f" />
![Tours Grid](docs/screenshot-tours-grid.png)

---

## Tech Stack

* **React 18**, **React Router v6**
* **Create React App** (`react-scripts`)
* **Bootstrap 5** & **React-Bootstrap**
* **react-slick / slick-carousel**, **react-image-gallery**, **react-lightbox-gallery**
* **react-datepicker** (UI only, no persistence)
* **Jest + @testing-library/react**, **Web Vitals**

> See `package.json` for exact versions.

---

## Getting Started

### Prerequisites

* **Node.js** ≥ 18 LTS recommended
* **npm** (bundled with Node) or **yarn**

### Installation

```bash
# clone
git clone https://github.com/<you>/<repo>.git
cd <repo>

# install deps
npm install
# or
yarn
```

### Run in development

```bash
npm start
# or
yarn start
```

The app opens at [http://localhost:3000](http://localhost:3000).

### Build for production

```bash
npm run build
# or
yarn build
```

---

## Available Scripts

* `npm start` — start dev server (CRA)
* `npm test` — run test runner (Jest + Testing Library)
* `npm run build` — production build to `/build`
* `npm run eject` — eject from CRA (irreversible)

---

## Project Structure

> Adjust to match your repo; this is the recommended layout for readability.

```
travel-app/
├─ public/          # static images, icons
├─ src/
│  ├─ assets/images/
│  ├─ components/
│  │  ├─ Navbar/
│  │  ├─ TourCard/
│  │  ├─ Gallery/
│  │  └─ Carousel/
│  ├─ pages/
│  │  ├─ Home/
│  │  ├─ About/
│  │  ├─ Tours/
│  │  ├─ Destination/
│  │  ├─ Gallery/
│  │  └─ Contact/
│  ├─ utils/          
│  │  ├─ data.js
│  ├─ setupTests.js/
│  ├─ index.css
│  ├─ index.js 
│  ├─ App.test.js 
│  ├─ App.css
│  ├─ App.jsx            
├─ package.json
└─ README.md
```

---

## Architecture Notes

* **Frontend-only**: No backend or IATA/booking API integration.
* **Mock-friendly**: Place JSON in `src/data/` and wire simple services in `src/services/` for seamless future API swaps.
* **Routing**: React Router v6; keep top-level routes minimal and lazy-load heavy pages if needed.
* **UI**: Prefer React-Bootstrap for consistency; custom utilities for spacing/typography where needed.

---

## Testing

* **Scope**: Smoke tests for routes and critical components (e.g., navbar renders, tours list displays, gallery opens).
* **Run**: `npm test`
* **Example ideas**:

  * Navbar contains all top-level links and active state.
  * Tours grid renders N cards from mock data.
  * Clicking a gallery thumbnail opens lightbox.

---

## Performance & Accessibility

* **Web Vitals**: Included; log or send metrics for analysis.
* **Images**: Use lazy-loading, appropriate sizes, and `srcSet`/`sizes` when possible.
* **A11y basics**:

  * Provide `alt` text for images.
  * Ensure keyboard navigation for galleries/lightboxes.
  * Use ARIA labels on carousels and close buttons.

---

## Roadmap

* **Tour detail page**: Rich itinerary, inclusions/exclusions, gallery, map, availability.
* **Booking flow**: Travellers, dates, pricing, review, confirmation.
* **API integration**: Swap mocks for real search/availability/pricing endpoints.
* **State management**: Lift state or add a lightweight store if needed.
* **SEO**: Meta tags, Open Graph, sitemap, structured data (where relevant).
* **Internationalization**: Currency/locale awareness.
* **Deployment**: Vercel/Netlify; consider migrating CRA → **Vite** or **Next.js** for faster builds/code-splitting.

---

## Contributing

### Author

**Faith Travels** — Frontend by *Termille Maduna*.
Find me on [LinkedIn](https://www.linkedin.com/in/termille-maduna/).

---
