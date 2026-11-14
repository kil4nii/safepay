# SafePay MVP

SafePay is an escrow payment platform for businesses of any size, including delivery orders. The payer funds the order upfront. The money is held in escrow at a licensed partner bank and is released to the seller only when delivery is confirmed.

This is a clickable prototype. It has no backend and moves no real money.

## Run it

Open `index.html` in a browser. Everything is in that one file (HTML, CSS and vanilla JavaScript, no build step). The fonts load from Google Fonts; offline, the page falls back to system fonts.

## The four views

1. **Buyer company** (Delta Retail Co., EGP 2,500,000): create and fund an escrow order as one payment or two 50/50 milestones, with a 1% SafePay fee. Approve and release, dispute, or resolve a dispute as released or refunded.
2. **Supplier** (Al-Amal Packaging): upload proof, mark a milestone delivered, and take an early payout from a financing partner for a 1.5% fee.
3. **Delivery checkout** (Nile Crafts shop): the customer prepays EGP 1,530 into escrow. The courier enters the customer's 4-digit handover code to release the money. A wrong code is rejected. A refused parcel is refunded in full.
4. **API & webhooks**: the `POST /v1/escrows` request for the current order and a live list of webhook events.

A side panel always shows where the money is and an event log. Escrow auto-releases 72 hours after delivery if the buyer does nothing.

## Rules in the demo

- SafePay fee: 1% per escrow. Early payout fee: 1.5%.
- SafePay never holds funds and does not lend its own money.
- The total money in the demo never changes. The side panel checks this after every action.
