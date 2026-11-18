# FreshRoute Prototype — Technical Overview

## 1. Architecture
The application is a static client-side web prototype:
- `index.html` — page structure, navigation, and forms.
- `css/style.css` — visual styling.
- `js/app.js` — navigation, validation, order creation/search/editing, schedule filtering, and persistence.

It uses vanilla JavaScript. The supplied project has no backend API, server-side application, external database, build process, or third-party runtime dependency.

## 2. Runtime
Extract the folder and open `index.html` in a modern browser with JavaScript enabled. It is not configured for cloud deployment or production hosting.

## 3. Order data model
Each order contains:
- `id`: generated reference such as `FR-1042`
- `customer`: customer name
- `contact`: phone number or email
- `orderDate`: order date (`YYYY-MM-DD`)
- `deliveryDate`: delivery date (`YYYY-MM-DD`) or empty
- `instructions`: optional delivery instructions
- `items`: array of item objects containing `name` and `qty`

Quantity is expected to be a positive whole number.

## 4. Persistence and demo data
The local storage key is `freshroute_orders_v1`. On startup, the app attempts to parse the stored value. If no usable array is present, it uses three fictional seed orders (FR-1042, FR-1043, FR-1044) and saves them to local storage. Create/edit actions update the in-memory array and persist it using `localStorage.setItem`.

Storage is scoped to the current browser profile/origin. It is not a central or shared database and does not synchronise across devices.

## 5. Main logic
- **Create:** validates at least one named produce item and positive integer quantities, finds the next unused reference starting at FR-1042, appends the order, and saves.
- **Search:** converts the entered reference to uppercase and performs an exact match against `id`.
- **Unknown reference:** displays a no-match message and does not open an order.
- **Edit:** updates customer, contact, delivery date, instructions, and item lines; retains the existing order ID.
- **Schedule:** filters orders whose `deliveryDate` exactly matches the selected date and renders a table or empty state.
- **Output handling:** user-entered text is escaped in the relevant generated HTML rendering paths.

## 6. Accessibility-related behaviour
The interface uses labelled form controls, semantic buttons, tab/tab-panel roles, and live regions for status messages. Search can be submitted using the keyboard, and the Edit order button is keyboard-focusable. A complete keyboard-only journey must still be executed and recorded in the target browser; source inspection alone does not prove acceptance-test success.

## 7. Security, privacy, and limitations
There is no authentication, authorisation layer, server-side security boundary, secure customer database, backup, audit trail, multi-user concurrency control, retention mechanism, or central access management. Use fictional data only. This prototype is not suitable for real customer or business operations.

## 8. Version
The supplied `VERSION.txt` identifies this refactored file structure as v1.1.
