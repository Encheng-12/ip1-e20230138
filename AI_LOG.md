## 2026-10-25 - Initial project planning

Tool: ChatGPT

Asked: Help plan a room rental management system.

Kept: The initial user roles and proposed entity structure.

Rejected: None yet.

Checked by: I reviewed the proposed requirements
and will confirm the project scope with my teacher.

## 2026-11-12 - SPEC draft for Room rental

Tool: Claude

Asked: Draft user stories with acceptance criteria for a room rental app
with two roles (Tenant, Landlord), based on the project guideline.

Kept: 8 user stories and their acceptance criteria in docs/SPEC.md.

Rejected: TODO: write what you changed or removed.

Checked by: I read every story and compared the count and roles
with the Check 1 checklist (6-10 stories, at least 2 roles).

## 2026-11-12 - Static Vue screens and dashboard theme

Tool: Claude

Asked: Build the first static screens (login, my room, invoices,
report issue, landlord dashboard) and style them like a reference
landlord dashboard (navy sidebar, white cards, status pills).

Kept: The page structure, hard-coded demo data, and the colour
variables in style.css.

Rejected: The cashflow chart and net worth panel from the reference,
because they are not in my SPEC. TODO: add anything else you changed.

Checked by: I ran npm run dev and clicked through each screen,
and checked a narrow browser window.

## 2026-11-12 - Wireframes and Vue Router

Tool: Claude

Asked: Create simple wireframes for the main screens, and set up
Vue Router with a param route (/rooms/:id) and a 404 page.

Kept: Five SVG wireframes in docs/wireframes/, the routes list,
RouterLink sidebar, and useRoute for the :id param.

Rejected: TODO.

Checked by: I opened /rooms/B-204 and a wrong URL (/abc) by hand
to check the param route and the 404 page.