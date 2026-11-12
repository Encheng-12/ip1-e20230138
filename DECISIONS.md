# Design Decisions

- 2026-10-25: Use Vue 3 and TypeScript
  for the frontend because they are required
  by the course guideline.

- 2026-10-25: Use NestJS for the backend
  because it is required by the course guideline.

- 2026-10-25: Start with User, Room, and Rental
  as the main data entities.

- 2026-11-12: Domain is Room rental with two roles, Tenant and Landlord,
  so the SPEC stories cover both sides.

- 2026-11-12: Static screens use hard-coded data, because Check 1
  allows no real data yet. Stores and mock data come in Check 2.

- 2026-11-12: One global style.css with CSS variables and no UI library,
  so the styling is simple to explain.

- 2026-11-12: Wireframes are SVG sketches in docs/wireframes/,
  so no design tool is needed.

- 2026-11-12: Vue Router with createWebHistory and a catch-all
  404 route.