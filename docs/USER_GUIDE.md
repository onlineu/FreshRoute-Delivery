# FreshRoute Prototype — User Guide

## 1. Purpose
FreshRoute is a browser-based prototype for staff order administration. It demonstrates creating a produce order, finding/updating an existing order, and viewing orders scheduled for a selected delivery date. It uses fictional demonstration records and is not connected to a live business system.

## 2. Start the application
1. Extract the ZIP archive.
2. Open the `FreshRoute_App` folder.
3. Open `index.html` in a modern browser with JavaScript enabled.
4. The **New Order** screen opens first.

No installation or server setup is required.

## 3. Create a new order
1. Select **New Order**.
2. Enter the customer's name and a contact number or email.
3. Check the order date and optionally select a delivery date.
4. Optionally enter delivery instructions.
5. Enter at least one produce item and a whole-number quantity of 1 or more.
6. Select **+ Add another item** for additional produce lines.
7. Select **Save order**.

A success message appears and the app assigns the next available reference in the `FR-####` format. The order is saved in the current browser's local storage. Fields marked with an asterisk are required. Invalid or incomplete produce lines are rejected. Use **Clear form** to reset the form. The × control removes an additional produce row; at least one row must remain.

## 4. Find and view an order
1. Select **Manage Orders**.
2. Enter the complete reference, including `FR-` (for example, `FR-1042`).
3. Select **Search order** or submit using the keyboard.
4. If found, the order details appear.
5. If not found, the app displays a message such as: `No order found for FR-9999. Check the reference and try again.`

Search is by exact reference. Customer surname and partial-reference search are not supported.

## 5. Edit an order
1. Find the order using its exact reference.
2. Select **Edit order**.
3. Update customer name, contact, delivery date, instructions, or produce lines.
4. Enter produce lines one per line using `item,quantity` format, e.g.:
   ```text
   Apples,5
   Carrots,3
   ```
5. Select **Save changes**.

The updated order is displayed and its original reference remains unchanged. Each produce line must contain an item name and a whole-number quantity of at least 1. Select **Cancel** to leave the edit screen without saving.

## 6. View the delivery schedule
1. Select **Delivery Schedule**.
2. Choose a delivery date.
3. Select **Show orders** or change the date.
4. Matching orders appear with reference, customer, contact, items, quantities, and instructions.
5. If no orders match, an empty-schedule message appears.

Only orders whose delivery date exactly matches the selected date are shown.

## 7. Keyboard use
Use Tab to move between controls. In **Manage Orders**, focus the reference field, enter the full reference, and press Enter to submit. When an order is found, Tab to **Edit order** and press Enter. Execute and record the complete keyboard-only acceptance test in `TESTING.md` on the target browser before claiming it passes.

## 8. Data handling
Use fictional customer details only. Records are stored in the current browser profile, are not shared with other users/devices, and may be removed if browser/site storage is cleared. Do not use this prototype for real customer orders or operational delivery work.
