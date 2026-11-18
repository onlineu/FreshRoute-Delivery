# FreshRoute Order Management Prototype

A small browser-based coursework prototype for recording produce orders and preparing delivery schedules.

## Requirements
- A modern web browser with JavaScript enabled.
- No package installation, database server, or internet connection is required for normal local use.

## Run the prototype
1. Extract the ZIP file.
2. Open the `FreshRoute_App` folder.
3. Open `index.html` in a modern browser.
4. Use **New Order**, **Manage Orders**, and **Delivery Schedule**.

## Main functions
- Create an order with customer name, contact, order date, optional delivery date/instructions, and one or more produce items with quantities.
- Generate an order reference in the `FR-####` format.
- Search for an existing order by exact order reference.
- View and edit customer/contact details, delivery date, instructions, and produce lines.
- Keep the order reference unchanged when editing.
- Filter orders by delivery date.
- Use keyboard navigation for the exact-reference search and result-opening journey.

## Data and limitations
The app stores records in the current browser's `localStorage` under `freshroute_orders_v1`. On first use it seeds three fictional sample orders (FR-1042, FR-1043 and FR-1044). Records are not shared or synchronised between browsers or devices. Clearing browser storage may remove saved orders.

This is a coursework prototype, not a production system. It has no authentication, shared database, cloud hosting, online payment, stock management, availability checking, substitutions, live tracking, route optimisation, or external integrations. Use fictional data only; do not enter real customer or personal information.

## Project structure
- `index.html` — interface and page structure
- `css/style.css` — visual styling
- `js/app.js` — application behaviour and local storage
- `docs/` — user, technical, and testing documentation

## Documentation
- `docs/USER_GUIDE.md` — how to use the prototype
- `docs/TECHNICAL_OVERVIEW.md` — implementation and data notes
- `docs/TESTING.md` — test cases and a record template

Run the tests in `docs/TESTING.md` on the actual demonstration browser and record the real outcomes. Do not mark tests as passed until they have been executed.
