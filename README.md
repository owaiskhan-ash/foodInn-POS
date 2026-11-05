# Food Inn POS

Run `npm ci` and `npm run dev`. Run `npm test` for the build and order-flow smoke test.

## Tables and pay-later orders

The Tables view has 12 numbered tables on each of two floors. Selecting a vacant table starts a dine-in draft. Save an order to open its tab, mark the table occupied, and start its timer; customer details are optional. Select an occupied table to view the open order, add or edit items, print its bill or kitchen ticket, and record payment. Recording payment closes the tab and frees its table. Takeaway and delivery orders can also be saved unpaid and settled from Orders.

Orders and occupancy are stored in the browser's local storage, not a shared server. Tabs on the same browser and origin can receive updates, but other devices, browsers, and private sessions do not share data. Clearing browser data deletes it. This is not a multi-terminal production system; a shared, transactional backend and backups are needed for reliable restaurant-wide occupancy. Payment is recorded only; no payment is processed. The default tax rate is unverified and must be checked before billing.
